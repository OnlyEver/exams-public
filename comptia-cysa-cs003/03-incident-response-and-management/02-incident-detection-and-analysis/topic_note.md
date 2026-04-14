A [seismologist](https://en.wikipedia.org/wiki/Seismology) does not see the [tectonic plates](https://en.wikipedia.org/wiki/Plate_tectonics) grinding beneath the [earth's crust](https://en.wikipedia.org/wiki/Earth%27s_crust); they see the tremors. They look at scattered data points across an array of distributed sensors that, when pieced together, reveal the shape of an invisible, catastrophic force. As a security operations analyst, your reality is fundamentally the same. You rarely physically watch an adversary compromise a [domain controller](https://en.wikipedia.org/wiki/Domain_controller) in real time. Instead, you observe the digital tremors—the [dropped packets](https://en.wikipedia.org/wiki/Packet_loss), the mismatched [protocols](https://en.wikipedia.org/wiki/Communication_protocol), the subtle alterations in user behavior. The art of incident detection and analysis is the art of reading these scattered tremors perfectly to reconstruct the earthquake before the building falls.

![A seismogram recording distinct waveforms of ground motion. Just as seismologists read these waves to understand an earthquake, security analysts read digital telemetry to detect cyber intrusions.](https://wikipedia.org/wiki/Special:Redirect/file/Seismogram.gif)

## The Nature of an Incident and the NIST Framework

Before we can detect an incident, we must rigorously define what an incident actually is. The [National Institute of Standards and Technology](https://en.wikipedia.org/wiki/National_Institute_of_Standards_and_Technology) provides the canonical framework for this. 

> **NIST SP 800-61 Revision 2** defines an incident as a violation or imminent threat of violation of [computer security](https://en.wikipedia.org/wiki/Computer_security) policies, [acceptable use policies](https://en.wikipedia.org/wiki/Acceptable_use_policy), or standard security practices. 

Notice the phrase "imminent threat." An incident is not just a breached [database](https://en.wikipedia.org/wiki/Database); a localized [ransomware](https://en.wikipedia.org/wiki/Ransomware) infection spreading toward your core servers is an incident because the violation of policy is imminent. 

Handling these events requires a structured methodology. **Detection and Analysis is the second phase of the NIST [incident response](https://en.wikipedia.org/wiki/Computer_security_incident_management) lifecycle** (following Preparation). It is arguably the most complex phase because it requires differentiating the signal of an attack from the immense background noise of normal network operations.

Within this phase, we look for two distinct temporal signals: precursors and indicators.
*   **A precursor is a sign that an attacker may launch an incident in the future.** Think of this as the reconnaissance phase: a [web application](https://en.wikipedia.org/wiki/Web_application) [vulnerability scanner](https://en.wikipedia.org/wiki/Vulnerability_scanner) probing your external IP range, or a threat actor boasting about targeting your organization on a [dark web](https://en.wikipedia.org/wiki/Dark_web) forum.
*   **An indicator is a sign that an incident may have occurred or may currently be occurring on a network.** If an [antivirus](https://en.wikipedia.org/wiki/Antivirus_software) alert triggers, or a system suddenly crashes, you are looking at an indicator.

## The Taxonomy of Evidence: Indicators of Compromise

When an indicator is verified as malicious, it becomes a crucial piece of [forensic data](https://en.wikipedia.org/wiki/Computer_forensics). **[Indicators of Compromise](https://en.wikipedia.org/wiki/Indicator_of_compromise) (IoCs) are forensic artifacts that provide evidence of a potential security breach.** They are the breadcrumbs the adversary leaves behind. We generally categorize these into three tiers of fidelity.

### 1. Deterministic Indicators
At the foundation, we have undeniable mathematical proofs. **[Cryptographic file hashes](https://en.wikipedia.org/wiki/Cryptographic_hash_function) matching known [malware signatures](https://en.wikipedia.org/wiki/Signature-based_detection) serve as deterministic Indicators of Compromise.** If you pull an [SHA-256](https://en.wikipedia.org/wiki/SHA-2) hash off an endpoint and it perfectly matches a known [Emotet](https://en.wikipedia.org/wiki/Emotet) [payload](https://en.wikipedia.org/wiki/Payload_%28computing%29), there is no ambiguity. The file is malicious. 

![An illustration of the avalanche effect in cryptographic hashing. Even a minute change to a file's contents produces a completely different hash output, allowing analysts to rely on exact hash matches as deterministic indicators of compromise.](https://wikipedia.org/wiki/Special:Redirect/file/Cryptographic_Hash_Function.svg)

### 2. Network-Based Indicators
Attackers must communicate with their infrastructure, which inevitably leaves network artifacts. For example, **unusual outbound network traffic to unexpected geographic locations acts as a network-based Indicator of Compromise.** If a human resources workstation in Ohio suddenly initiates a massive outbound transfer to an [IP block](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing) in North Korea at 3:00 AM, the network is speaking to you. 

Furthermore, attackers often try to hide this communication by blending in. You must look closely at [application layers](https://en.wikipedia.org/wiki/Application_layer). **A mismatched application protocol running on a non-standard port indicates potential [command and control](https://en.wikipedia.org/wiki/Command_and_control_%28malware%29) communication.** If you see [SSH](https://en.wikipedia.org/wiki/Secure_Shell) traffic traversing [port 80](https://en.wikipedia.org/wiki/List_of_TCP_and_UDP_port_numbers) (usually reserved for unencrypted [HTTP](https://en.wikipedia.org/wiki/HTTP)), the adversary is attempting to bypass perimeter port restrictions by disguising their [remote access tool](https://en.wikipedia.org/wiki/Remote_access_trojan).

### 3. Behavioral Indicators
Adversaries can change file hashes easily, and they can route traffic through local [VPNs](https://en.wikipedia.org/wiki/Virtual_private_network), but changing their fundamental behavior is much harder. **Behavioral Indicators of Compromise include abnormal user login times and unexpected [privilege escalation](https://en.wikipedia.org/wiki/Privilege_escalation) events.** A service account designed to run a local backup script suddenly attempting to add itself to the Domain Admins group is a behavioral IoC.

![A conceptual diagram of privilege escalation. Behavioral indicators frequently involve detecting unauthorized attempts by a process or user to bypass normal elevation gates to gain administrative or root access.](https://wikipedia.org/wiki/Special:Redirect/file/Privilege_Escalation_Diagram.svg)

### Standardizing the Threat Lexicon
To ensure security teams globally can share these findings, we use standardized languages and frameworks:
*   **The OpenIOC framework is an extensible [XML](https://en.wikipedia.org/wiki/XML)-based format used for describing Indicators of Compromise.** It allows security tools to consume and search for these artifacts systematically.
*   **[STIX (Structured Threat Information eXpression)](https://en.wikipedia.org/wiki/STIX) is a standardized language used for conveying data about [cybersecurity threats](https://en.wikipedia.org/wiki/Threat_%28computer%29) and Indicators of Compromise.** STIX is often paired with TAXII (the transport mechanism) to automate [threat intelligence](https://en.wikipedia.org/wiki/Cyber_threat_intelligence) sharing.
*   To understand the *meaning* behind these IoCs, we map them to behavior. **The [MITRE ATT&CK](https://en.wikipedia.org/wiki/MITRE_ATT%26CK) framework is a globally accessible knowledge base of adversary tactics and techniques based on real-world observations.** If you find an IoC, MITRE ATT&CK tells you *why* the adversary used it and what they will likely do next.

## Telemetry and Instrumentation: Gathering the Tremors

To analyze log data during an incident, you must first collect it. The modern network generates terabytes of [telemetry](https://en.wikipedia.org/wiki/Telemetry) daily. 

At the center of your operations is the SIEM. **A [Security Information and Event Management](https://en.wikipedia.org/wiki/Security_information_and_event_management) (SIEM) system centralizes log data from multiple sources for correlation and analysis.** The SIEM is your central brain. But a brain needs nerve endings. 

![A typical Security Information and Event Management (SIEM) architecture, demonstrating how logs from diverse network devices, servers, and endpoints are centralized for correlation and analysis.](https://wikipedia.org/wiki/Special:Redirect/file/Basic_SIEM_Infrastructure.png)

To gain visibility at the host level, organizations deploy specialized software. **[Endpoint Detection and Response](https://en.wikipedia.org/wiki/Endpoint_detection_and_response) (EDR) agents provide continuous monitoring and logging of endpoint system activities for incident detection.** EDR acts as a flight data recorder for your endpoints, capturing process executions, [registry](https://en.wikipedia.org/wiki/Windows_Registry) modifications, and file creations.

### Decoding Operating System Logs

When diving into endpoints, you must be fluent in the native logging languages of the [operating systems](https://en.wikipedia.org/wiki/Operating_system). 

For Windows environments, the [Windows Security Event Log](https://en.wikipedia.org/wiki/Event_Viewer) is your primary source of truth. Memorizing key Event IDs is non-negotiable for rapid triage.

| Windows Event ID | Significance in Incident Analysis |
| :--- | :--- |
| **4624** | **Indicates a successful account logon.** Crucial for tracking [lateral movement](https://en.wikipedia.org/wiki/Lateral_movement_%28cybersecurity%29). |
| **4625** | **Indicates a failed account logon attempt.** A high volume of these often reveals [brute-force](https://en.wikipedia.org/wiki/Brute-force_attack) or password-spraying attacks. |
| **4720** | **Indicates the creation of a new user account.** Attackers frequently create dormant accounts to maintain persistence. |
| **1102** | **Indicates the security audit log has been cleared.** This is a massive red flag. |

Regarding Event ID 1102: **Attackers deploy log clearing techniques to hide their tracks and disrupt subsequent incident analysis efforts.** If you see an 1102 event triggered by a user account, treat it as a high-severity incident until proven otherwise.

In [Linux](https://en.wikipedia.org/wiki/Linux) environments, authorization data is stored in [plain text](https://en.wikipedia.org/wiki/Plaintext), but the location varies by distribution architecture:

| Linux Distribution | Authentication Log Path | Description |
| :--- | :--- | :--- |
| [Debian-based](https://en.wikipedia.org/wiki/Debian) (e.g., [Ubuntu](https://en.wikipedia.org/wiki/Ubuntu)) | `/var/log/auth.log` | **The Linux `/var/log/auth.log` file stores system authorization information and user login attempts on Debian-based systems.** |
| [Red Hat-based](https://en.wikipedia.org/wiki/Red_Hat_Enterprise_Linux) (e.g., RHEL, [CentOS](https://en.wikipedia.org/wiki/CentOS)) | `/var/log/secure` | **The Linux `/var/log/secure` file stores authentication and authorization events on Red Hat-based systems.** |

## The Network Vantage Point

Endpoint logs tell you what happened on a machine, but network logs tell you how the attacker got there and what they stole.

Understanding the difference between network telemetry types is like understanding the difference between a phone bill and a wiretap.
*   **Network flow data ([NetFlow](https://en.wikipedia.org/wiki/NetFlow)) provides [metadata](https://en.wikipedia.org/wiki/Metadata) about network connections rather than the full packet [payload](https://en.wikipedia.org/wiki/Payload_%28computing%29).** It tells you Source IP, Destination IP, ports, protocols, and the volume of data transferred. It is lightweight, making it excellent for spotting large data exfiltration over long periods.
*   **Full [packet capture](https://en.wikipedia.org/wiki/Packet_analyzer) (PCAP) contains the complete payload and headers of network traffic for deep forensic analysis.** PCAP allows you to literally reconstruct the file the attacker downloaded or read the plain-text commands they sent. However, it requires massive storage overhead.

Beyond PCAP and NetFlow, specialized appliances provide context:
*   **[Firewall](https://en.wikipedia.org/wiki/Firewall_%28computing%29) logs identify accepted and dropped network connections at the network perimeter or internal network segments.** They are your first check to see if an external attack breached the perimeter or was halted at the gate.
*   **[Proxy](https://en.wikipedia.org/wiki/Proxy_server) logs contain details of outbound web requests including requested [URLs](https://en.wikipedia.org/wiki/URL), [user agent strings](https://en.wikipedia.org/wiki/User_agent), and [HTTP status codes](https://en.wikipedia.org/wiki/List_of_HTTP_status_codes).** If [malware](https://en.wikipedia.org/wiki/Malware) is beaconing out to `evil-domain.com`, your proxy logs will capture the exact [URI](https://en.wikipedia.org/wiki/Uniform_Resource_Identifier) structure and the user agent the malware is masquerading as.
*   **[DNS sinkholing](https://en.wikipedia.org/wiki/DNS_sinkhole) logs reveal internal hosts attempting to resolve known malicious domains.** By routing known bad domains to a black hole (sinkhole), you not only prevent the connection but generate a clean, high-fidelity alert identifying the infected internal machine.

![By acting as an intermediary between internal users and the internet, a proxy server logs exact outbound requests, URLs, and user agents, revealing when internal malware attempts to communicate with external command and control infrastructure.](https://wikipedia.org/wiki/Special:Redirect/file/Proxy_concept_en.svg)

### The Encryption Blindspot
There is a profound challenge in modern network analysis. The widespread adoption of [HTTPS](https://en.wikipedia.org/wiki/HTTPS) and [TLS](https://en.wikipedia.org/wiki/Transport_Layer_Security) is excellent for consumer privacy, but terrible for defenders. **Encrypted network traffic prevents traditional [deep packet inspection](https://en.wikipedia.org/wiki/Deep_packet_inspection) without the deployment of TLS/[SSL](https://en.wikipedia.org/wiki/Transport_Layer_Security) decryption proxies.** If the traffic is encrypted, your PCAP will just look like mathematical noise. You must rely entirely on NetFlow metadata, endpoint logs, or SSL interception to deduce malicious activity.

## Analytical Techniques: Making Sense of the Noise

Having the logs is not enough; you must manipulate them to reveal the narrative of the attack. 

> **CRITICAL ARCHITECTURAL REQUIREMENT:** 
> **Clock synchronization across all network devices via [Network Time Protocol](https://en.wikipedia.org/wiki/Network_Time_Protocol) (NTP) is strictly required to ensure accurate temporal correlation of logs.** 
> If your firewall thinks it is 10:04 AM and your domain controller thinks it is 10:07 AM, piecing together an attacker's rapid lateral movement becomes a maddening, mathematically impossible jigsaw puzzle.

![The hierarchical structure of the Network Time Protocol (NTP). Synchronizing clocks across all network strata is strictly required for accurately correlating log timestamps during incident analysis.](https://wikipedia.org/wiki/Special:Redirect/file/Network_Time_Protocol_servers_and_clients.svg)

With synchronized logs, we apply specific analytical techniques:

1.  **Log Correlation:** 
    This is the core function of a SIEM. **Log correlation links multiple distinct log events to identify a broader attack sequence.** A failed login (Windows Event 4625), followed immediately by an [IDS](https://en.wikipedia.org/wiki/Intrusion_detection_system) alert for a [buffer overflow](https://en.wikipedia.org/wiki/Buffer_overflow), followed by a successful login (Windows Event 4624) from the same IP, creates a correlated alert: *Successful Brute Force Compromise*.
2.  **Data Enrichment:**
    Raw logs are often just IP addresses and timestamps. **Data enrichment adds contextual information to raw log events by appending details like geographic location or threat intelligence scores.** Converting an IP address into "Pyongyang, North Korea" immediately changes how an analyst treats the alert.
3.  **Baseline Comparison:**
    You cannot detect anomalies if you do not know what is normal. **Baseline comparison involves measuring current system behavior against a known-good historical state to detect anomalies.** If a server normally peaks at 50MB of outbound traffic a day, a sudden spike to 5GB is an anomaly detected via baselining.
4.  **Trend Analysis:**
    Some attacks are "low and slow." **Trend analysis examines historical log data over time to identify slow-developing attacks or gradual changes in system behavior.** A threat actor exfiltrating 10MB of data per day over six months might evade sudden baseline spikes, but trend analysis will catch the sustained shift.
5.  **Heuristic Analysis:**
    Signatures only catch known malware. **[Heuristic analysis](https://en.wikipedia.org/wiki/Heuristic_analysis) uses rules and algorithms to detect previously unknown threats based on suspicious characteristics.** If a brand-new, never-before-seen [executable](https://en.wikipedia.org/wiki/Executable) injects code into `explorer.exe` and attempts to delete [shadow volume copies](https://en.wikipedia.org/wiki/Shadow_Copy), heuristics flag it as ransomware based purely on its behavior, regardless of its file hash.
6.  **The Super Timeline:**
    During a deep incident response investigation, analysts must construct the ultimate forensic artifact. **A super timeline aggregates log data from file systems, [memory](https://en.wikipedia.org/wiki/Computer_memory), and network devices into a chronological sequence of events.** It merges registry modifications, PCAP timestamps, and Event IDs into one master script, allowing the responder to replay the attacker's every move, second by second.

## Friction in the Machine: Analyst Challenges and Proactive Defense

The systems we build to detect threats are imperfect, and navigating their flaws is a daily reality for the SOC analyst.

*   **[False positives](https://en.wikipedia.org/wiki/False_positive_paradox) occur when an alerting system incorrectly identifies benign network activity as malicious.** A developer testing a new API might trigger a [SQL injection](https://en.wikipedia.org/wiki/SQL_injection) alert. 
*   **False negatives occur when an alerting system completely fails to identify actual malicious activity.** This is the worst-case scenario—an attacker slips past the defenses undetected.

The sheer volume of telemetry creates a psychological toll. **A high volume of inaccurate security alerts can lead to [alert fatigue](https://en.wikipedia.org/wiki/Alarm_fatigue) for [Security Operations Center](https://en.wikipedia.org/wiki/Security_operations_center) analysts.** When an analyst sees 500 false positives a day, human nature dictates they might glance over the 501st alert—which happens to be the true positive, the actual breach. Tuning the SIEM to reduce false positives without creating false negatives is an ongoing, delicate balancing act.

Furthermore, we are bound by physics and law. We cannot keep telemetry forever. **Log retention policies dictate how long security event data must be stored for compliance auditing and historical incident analysis.** If an attacker has been in your network for 200 days, but your retention policy only stores logs for 90 days, the beginning of the attack is permanently erased from history.

### The Shift to Proactive Defense: Threat Hunting
Because false negatives happen and sophisticated adversaries evade automated SIEM alerts, the best security teams do not wait for the alarm to ring. 

**[Threat hunting](https://en.wikipedia.org/wiki/Cyber_threat_hunting) is a proactive approach to finding undetected threats in a network by iteratively analyzing security data and logs.** A threat hunter assumes the perimeter has already been breached. They form a hypothesis—for example, *"Adversaries are using [PowerShell](https://en.wikipedia.org/wiki/PowerShell) to bypass our EDR"*—and then manually sift through the telemetry, looking for the subtle tremors that the automated systems missed. 

![A threat hunter using PowerShell to navigate the Windows registry. Because advanced adversaries frequently use built-in tools like PowerShell to bypass security agents, proactive hunting involves manually querying the system for anomalous behavior.](https://wikipedia.org/wiki/Special:Redirect/file/PowerShell_registry_provider.png)

By mastering incident detection and analysis, you stop being a passive recipient of alerts. You become the active investigator, using baselines, heuristics, and correlated telemetry to illuminate the dark corners of your network where adversaries attempt to hide.