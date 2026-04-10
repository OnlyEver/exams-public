When a digital environment is compromised, the adversary leaves behind a fractured, scattered record of their movements. Every [packet](https://en.wikipedia.org/wiki/Network_packet) crossing a boundary, every [process execution](https://en.wikipedia.org/wiki/Process_%28computing%29) on a [CPU](https://en.wikipedia.org/wiki/Central_processing_unit), and every queried [domain name](https://en.wikipedia.org/wiki/Domain_name) generates a tiny mathematical fragment of data. The security analyst’s job is not merely to collect these fragments, but to fuse them into a precise, unified reality. We do not guess; we measure. By interrogating [firewall](https://en.wikipedia.org/wiki/Firewall_%28computing%29) logs, host [operating systems](https://en.wikipedia.org/wiki/Operating_system), and raw [network telemetry](https://en.wikipedia.org/wiki/Telemetry), we reconstruct the anatomy of a [breach](https://en.wikipedia.org/wiki/Data_breach) with absolute fidelity. 

To pass the [CompTIA Security+](https://en.wikipedia.org/wiki/CompTIA) exam and, more importantly, to operate effectively in a modern [Security Operations Center](https://en.wikipedia.org/wiki/Security_operations_center) (SOC), you must understand how to read these distinct data sources. You must know what each log can tell you, what it cannot tell you, and how to combine them to piece together an attack timeline.

## The Foundation of Measurement: Time and Translation

Imagine trying to reconstruct a multi-car collision at an intersection where every witness’s watch is set to a different [time zone](https://en.wikipedia.org/wiki/Time_zone). The testimonies would contradict each other, and [causality](https://en.wikipedia.org/wiki/Causality) would be impossible to prove. 

In a network, **[Network Time Protocol](https://en.wikipedia.org/wiki/Network_Time_Protocol) (NTP)** synchronizes the [system clocks](https://en.wikipedia.org/wiki/System_time) of devices across an enterprise network. Synchronizing device clocks via Network Time Protocol is mandatory for constructing accurate chronological attack timelines from diverse logs. If your firewall records a connection at 10:04:22 and your server records an execution at 10:02:15, you cannot prove the connection caused the execution unless both devices share an identical, synchronized time standard.

![NTP synchronizes device clocks across a hierarchical network, establishing a unified chronological timeline essential for correlating diverse security logs.](https://wikipedia.org/wiki/Special:Redirect/file/Network_Time_Protocol_servers_and_clients.svg)

Once time is synchronized, we face a second problem: language. A [Windows server](https://en.wikipedia.org/wiki/Windows_Server) formats its logs as complex [XML](https://en.wikipedia.org/wiki/XML) events, a [Linux](https://en.wikipedia.org/wiki/Linux) firewall uses plain text [Syslog](https://en.wikipedia.org/wiki/Syslog), and a [proxy](https://en.wikipedia.org/wiki/Proxy_server) uses [comma-separated values](https://en.wikipedia.org/wiki/Comma-separated_values). 

**[Security Information and Event Management](https://en.wikipedia.org/wiki/Security_information_and_event_management) (SIEM)** systems solve this. SIEMs aggregate logs from multiple data sources into a central repository. However, aggregation is just the first step. To make the data searchable, SIEM systems parse log fields to normalize diverse log structures into a standard format. This normalization allows an analyst to run a single query for a specific [IP address](https://en.wikipedia.org/wiki/IP_address) and instantly retrieve matching firewall blocks, Windows logons, and proxy requests, regardless of their original native formatting.

![A basic SIEM infrastructure aggregates, normalizes, and correlates log data from diverse network and endpoint sources into a single centralized database.](https://wikipedia.org/wiki/Special:Redirect/file/Basic_SIEM_Infrastructure.png)

## Interrogating the Network Perimeter

The network never lies. Unlike a compromised endpoint system, which can be manipulated by [malware](https://en.wikipedia.org/wiki/Malware) to hide running processes, network infrastructure passively observes the physics of the data moving across it. 

### Firewall Telemetry
The traditional first line of defense is the [network perimeter](https://en.wikipedia.org/wiki/Network_security). **[Firewall logs](https://en.wikipedia.org/wiki/Firewall_%28computing%29)** record the source and destination IP addresses of traffic crossing a network boundary. When you look at a firewall log, you are primarily looking for access control decisions. Firewall logs indicate whether a specific network connection was explicitly permitted or denied by an [access control list](https://en.wikipedia.org/wiki/Access-control_list) (ACL). 

Why do we care about blocked traffic? Analyzing denied traffic in firewall logs helps identify external scanning attempts against a network. If an adversary is systematically probing your external IP range on [port 3389](https://en.wikipedia.org/wiki/Remote_Desktop_Protocol) (RDP) and [port 22](https://en.wikipedia.org/wiki/Secure_Shell) (SSH), your firewall logs will show a massive spike in denied connection attempts from a single source IP, giving you an early warning of targeted [reconnaissance](https://en.wikipedia.org/wiki/Reconnaissance).

![Network firewalls filter traffic between security zones, generating logs that document explicitly permitted or denied connection attempts.](https://wikipedia.org/wiki/Special:Redirect/file/Firewall.png)

### DNS and Web Proxies
Adversaries, like legitimate users, rely on domain names to navigate. **[DNS](https://en.wikipedia.org/wiki/Domain_Name_System) logs** contain records of domain name resolution queries made by systems on a network. When an employee clicks a [phishing](https://en.wikipedia.org/wiki/Phishing) link, their machine must first ask the [DNS server](https://en.wikipedia.org/wiki/Name_server) where that domain lives. Security analysts review DNS logs to detect internal endpoints attempting to resolve known malicious [command and control](https://en.wikipedia.org/wiki/Command_and_control_%28malware%29) (C2) domains.

![DNS resolution involves multiple steps to translate a domain name into an IP address; DNS logs capture these queries to identify connections to malicious infrastructure.](https://wikipedia.org/wiki/Special:Redirect/file/DNS_Architecture.svg)

Once the name is resolved, the actual [HTTP](https://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol)/[HTTPS](https://en.wikipedia.org/wiki/HTTPS) connection is often routed through a proxy. **[Web proxy](https://en.wikipedia.org/wiki/Proxy_server) logs** contain records of external web requests including the specific [Uniform Resource Locators](https://en.wikipedia.org/wiki/URL) (URLs) accessed by internal users. 

![A proxy server acts as an intermediary for web traffic, allowing analysts to log specific external URLs requested by internal users.](https://wikipedia.org/wiki/Special:Redirect/file/Proxy_concept_en.svg)

> **The Encryption Blindspot:**
> Today, almost all web traffic is encrypted via HTTPS. Because the URL path is encrypted inside the HTTP [payload](https://en.wikipedia.org/wiki/Payload_%28computing%29), standard network monitoring can only see the destination IP and the domain name, not the specific file being requested. To regain this visibility, web proxy logs require **[TLS inspection](https://en.wikipedia.org/wiki/Transport_Layer_Security)** to record the full [Uniform Resource Locator](https://en.wikipedia.org/wiki/URL) paths of encrypted HTTPS traffic. By decrypting, logging, and re-encrypting the traffic, the proxy reveals exactly which malicious file path the user attempted to download.

## Network Flow vs. Packet Captures

When analyzing network data, analysts must constantly balance the *depth* of the data against the *cost* of storing it. We navigate this tradeoff using Network Flow and Packet Captures.

### Network Flow (NetFlow)
Think of **[network flow](https://en.wikipedia.org/wiki/Traffic_flow_%28computer_networking%29) data** as an itemized phone bill. It records [metadata](https://en.wikipedia.org/wiki/Metadata) about network connections rather than the actual data payload. Network flow metadata includes the source IP address, destination IP address, [protocol](https://en.wikipedia.org/wiki/Communication_protocol) used, and total [bytes](https://en.wikipedia.org/wiki/Byte) transferred. 

Because it discards the actual contents of the communication, network flow data requires significantly less [storage capacity](https://en.wikipedia.org/wiki/Computer_data_storage) than full packet captures. You can store months of [NetFlow](https://en.wikipedia.org/wiki/NetFlow) data on the same [hard drive](https://en.wikipedia.org/wiki/Hard_disk_drive) that would fill up in hours if you recorded full packets. Security analysts use network flow data to identify abnormal [data exfiltration](https://en.wikipedia.org/wiki/Data_exfiltration) volumes over time. If a [database server](https://en.wikipedia.org/wiki/Database_server) that normally sends 50 [Megabytes](https://en.wikipedia.org/wiki/Megabyte) of data to the internet suddenly transfers 400 [Gigabytes](https://en.wikipedia.org/wiki/Gigabyte) at 2:00 AM, the payload itself doesn't matter—the metadata alone proves a massive exfiltration event is occurring.

### Packet Captures (PCAP)
When you need the absolute ground truth of an interaction, you capture the packets. A **[packet capture](https://en.wikipedia.org/wiki/Packet_analyzer)** contains the raw network data payloads and network headers transmitted over a [network segment](https://en.wikipedia.org/wiki/Network_segment). Packet captures are typically saved in the **[PCAP](https://en.wikipedia.org/wiki/pcap)** file format.

Because you have the entire payload, security analysts use packet captures to extract malware files transmitted over unencrypted network protocols. If an attacker downloads an [executable](https://en.wikipedia.org/wiki/Executable) over [plaintext](https://en.wikipedia.org/wiki/Plaintext) HTTP, the actual [binary code](https://en.wikipedia.org/wiki/Binary_code) of the malware is sitting inside your PCAP file, ready to be carved out and [reverse-engineered](https://en.wikipedia.org/wiki/Reverse_engineering).

| Tool | Purpose | Interface |
| :--- | :--- | :--- |
| **[Wireshark](https://en.wikipedia.org/wiki/Wireshark)** | A graphical [protocol analyzer](https://en.wikipedia.org/wiki/Packet_analyzer) used to inspect network packet captures. It reconstructs [TCP](https://en.wikipedia.org/wiki/Transmission_Control_Protocol) streams and decodes hundreds of protocols for deep visual analysis. | [Graphical User Interface](https://en.wikipedia.org/wiki/Graphical_user_interface) (GUI) |
| **[Tcpdump](https://en.wikipedia.org/wiki/tcpdump)** | A command-line utility used to capture raw network packets directly from a [network interface](https://en.wikipedia.org/wiki/Network_interface_controller), ideal for lightweight, [headless server](https://en.wikipedia.org/wiki/Headless_computer) operations. | [Command-Line Interface](https://en.wikipedia.org/wiki/Command-line_interface) (CLI) |

![Wireshark provides a graphical interface for analyzing PCAP files, allowing analysts to visually inspect individual network packets, reconstruct TCP streams, and examine raw data payloads.](https://wikipedia.org/wiki/Special:Redirect/file/Wireshark_3.6_screenshot.png)

## The Endpoints: Where Code Meets Hardware

Network data tells you *how* the attacker arrived; endpoint logs tell you *what* they did once they got there. 

### Windows Auditing and Authentication
In a [Microsoft](https://en.wikipedia.org/wiki/Microsoft)-dominated enterprise, the **[Windows Security Event Log](https://en.wikipedia.org/wiki/Event_Viewer)** is your primary source of truth. Windows operating systems store security-related events in the Windows Security Event Log, assigning a unique numerical "Event ID" to different types of actions. 

Two Event IDs are paramount for authentication investigations:
*   **Windows Event ID 4624** signifies a successful user [logon](https://en.wikipedia.org/wiki/Logging_in) event.
*   **Windows Event ID 4625** signifies a failed user logon attempt.

If an attacker is trying to guess an [administrator's](https://en.wikipedia.org/wiki/System_administrator) password, they will generate noise. Correlating multiple failed logon events (Event ID 4625) in endpoint logs can indicate an active [brute-force password attack](https://en.wikipedia.org/wiki/Brute-force_attack). If you see fifty 4625s followed immediately by a single 4624 for the same [user account](https://en.wikipedia.org/wiki/User_%28computing%29), the attacker has successfully guessed the [password](https://en.wikipedia.org/wiki/Password).

### Linux Logging Paths
Linux architectures do not use an event-viewer database; they rely on plain text files organized in specific [directories](https://en.wikipedia.org/wiki/Directory_%28computing%29). Linux operating systems typically store centralized system logging data in the `/var/log/syslog` or `/var/log/messages` files, depending on the specific [distribution](https://en.wikipedia.org/wiki/Linux_distribution) ([Ubuntu](https://en.wikipedia.org/wiki/Ubuntu)/[Debian](https://en.wikipedia.org/wiki/Debian) vs. [Red Hat](https://en.wikipedia.org/wiki/Red_Hat_Enterprise_Linux)/[CentOS](https://en.wikipedia.org/wiki/CentOS)). 

When investigating unauthorized access on a Linux server, you look at a specialized file: Linux authentication events are recorded in the `/var/log/auth.log` or `/var/log/secure` files. Every [SSH](https://en.wikipedia.org/wiki/Secure_Shell) login, [sudo](https://en.wikipedia.org/wiki/sudo) [privilege escalation](https://en.wikipedia.org/wiki/Privilege_escalation), and failed password attempt is permanently etched into these text files.

### Endpoint Detection and Response (EDR)
Standard [OS](https://en.wikipedia.org/wiki/Operating_system) logs are helpful, but modern adversaries frequently attempt to evade them by executing malware solely in [memory](https://en.wikipedia.org/wiki/Computer_memory) or hijacking legitimate system processes. 

To counter this, **[Endpoint Detection and Response](https://en.wikipedia.org/wiki/Endpoint_detection_and_response) (EDR)** platforms deploy lightweight [agents](https://en.wikipedia.org/wiki/Software_agent) to the operating system [kernel](https://en.wikipedia.org/wiki/Kernel_%28operating_system%29). EDR logs provide deep visibility into host-level activities like [registry](https://en.wikipedia.org/wiki/Windows_Registry) modifications and [injected threads](https://en.wikipedia.org/wiki/Code_injection). Instead of just seeing that a user logged in, an analyst reviewing EDR telemetry can see that [Microsoft Word](https://en.wikipedia.org/wiki/Microsoft_Word) opened, spawned a suspicious [PowerShell](https://en.wikipedia.org/wiki/PowerShell) sub-process, and injected malicious code into an innocent-looking system file.

![By operating at the kernel level, EDR agents can monitor deep system behaviors—such as memory manipulation and process injection—that bypass standard application logs.](https://wikipedia.org/wiki/Special:Redirect/file/Kernel_Layout.svg)

## Synthesizing Telemetry Across Domains

The hallmark of a senior security analyst is the ability to fuse disparate data sources. No single log tells the whole story. 

Imagine you detect an unauthorized outbound connection from an internal [workstation](https://en.wikipedia.org/wiki/Workstation) to a known [Russian](https://en.wikipedia.org/wiki/Russia) IP address in your firewall logs. The firewall tells you the connection occurred, but it cannot tell you *which* software on the workstation made the connection. 

By pivoting to the endpoint, correlating endpoint process creation logs with network flow data helps trace a malicious executable to a specific outbound network connection. You can prove mathematically that at exactly 14:02:11, the EDR system recorded the creation of `malware.exe`, and at exactly 14:02:12, the network flow recorded that specific local [port](https://en.wikipedia.org/wiki/Port_%28computer_networking%29) opening a connection to the foreign IP. 

### Beyond the Traditional Perimeter
Finally, we must recognize that the modern perimeter has dissolved into the [cloud](https://en.wikipedia.org/wiki/Cloud_computing) and [web applications](https://en.wikipedia.org/wiki/Web_application).
*   **[Cloud infrastructure](https://en.wikipedia.org/wiki/Cloud_computing) logs** track [API](https://en.wikipedia.org/wiki/API) calls made to cloud service [management planes](https://en.wikipedia.org/wiki/Management_plane). If an attacker steals an [AWS](https://en.wikipedia.org/wiki/Amazon_Web_Services) or [Azure](https://en.wikipedia.org/wiki/Microsoft_Azure) credential, they won't log into a traditional [desktop](https://en.wikipedia.org/wiki/Desktop_computer); they will issue API commands to spin up rogue [cryptomining](https://en.wikipedia.org/wiki/Cryptojacking) servers or modify [Identity and Access Management](https://en.wikipedia.org/wiki/Identity_management) (IAM) policies. 
*   **[Web Application Firewall](https://en.wikipedia.org/wiki/Web_application_firewall) (WAF)** logs record HTTP-specific attack signatures such as [cross-site scripting](https://en.wikipedia.org/wiki/Cross-site_scripting) (XSS) attempts or [SQL injections](https://en.wikipedia.org/wiki/SQL_injection). While a standard network firewall only sees traffic on [port 443](https://en.wikipedia.org/wiki/HTTPS), a WAF parses the actual web requests, blocking and logging the specific malicious scripts an attacker is trying to feed into your [web forms](https://en.wikipedia.org/wiki/Form_%28HTML%29).

By mastering these diverse data sources—from the raw packets of the network to the deeply nested API calls of the cloud—you equip yourself with the observational power to reconstruct any digital event, expose any adversary, and secure the modern [enterprise](https://en.wikipedia.org/wiki/Enterprise_architecture).