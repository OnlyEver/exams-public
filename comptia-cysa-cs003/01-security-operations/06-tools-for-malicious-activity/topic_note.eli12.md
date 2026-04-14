Imagine someone sneaks in and steals the prize from the school office. You didn’t see them do it, but you have to figure out how they got in using only the muddy footprints they left behind. In computer security, hackers leave digital footprints. We use special tools to spot these footprints. Some tools act like magnifying glasses, while others act like giant bulletin boards. By putting all these clues together, a security defender can see exactly how the bad guy tried to sneak in!

![An early 20th-century demonstration of physical security against a bank robbery. In cybersecurity, defenders must similarly reconstruct "invisible" thefts using the digital artifacts left behind on networks and endpoints.](https://wikipedia.org/wiki/Special:Redirect/file/Bundesarchiv_Bild_102-12762%2C_Bank%C3%BCberfall.jpg)

## The Physics of the Network: [[Packet Capture | Packet capture]] Tools

When a hacker tries to sneak around your network to steal data, they have to follow the rules of computers. They have to send little chunks of data called packets. Catching these packets is like catching the hacker red-handed!

Normally, your computer's internet card only pays attention to messages that are sent directly to it. But to play detective, you need to hear everything. Wireshark requires a network interface card to be placed in promiscuous mode to capture all traffic on a local network segment. Think of "promiscuous mode" like listening to every single conversation in the school cafeteria, instead of just the person talking directly to you.

![A standard Network Interface Card (NIC). Placing a NIC into promiscuous mode bypasses its default filtering, allowing it to read every network frame on the wire for full packet capture.](https://wikipedia.org/wiki/Special:Redirect/file/An_Intel_82574L_Gigabit_Ethernet_NIC%2C_PCI_Express_x1_card.jpg)

### [[Wireshark | Wireshark]]: The Analyst's Microscope

When you want to look at exactly what is traveling over your network, there is a famous tool you can use. Wireshark is a graphical network protocol analyzer used to capture and inspect network traffic in real time. It has menus and buttons you can click on, kind of like a video game interface! When you save the data you caught, the default packet capture file format used by modern versions of Wireshark is pcapng.

![The Wireshark graphical user interface, which allows analysts to inspect captured network traffic, apply display filters, and analyze packet payloads in granular detail.](https://wikipedia.org/wiki/Special:Redirect/file/Wireshark_3.6_screenshot.png)

If you capture everything, you will get way too much information. It’s like trying to drink from a fire hose! To make sense of it, you use filters. Wireshark display filters evaluate captured packets against specific criteria to show only matching traffic without altering the underlying capture file. This means if you clear the filter, all your original data is still safe and sound.

Here are two handy filters:
*   The Wireshark display filter 'ip.addr == 192.168.1.1' displays all packets with a source or destination IP address of 192.168.1.1. (This is like searching for only letters sent to or from your house).
*   The Wireshark display filter 'tcp.port == 80' filters captured traffic to show only packets using TCP port 80. (This is like filtering your messages to only show regular web traffic).

Sometimes, looking at individual packets is like reading a book one letter at a time. It’s super slow! The Wireshark 'Follow TCP Stream' feature reconstructs and displays the complete payload of a specific TCP session in a human-readable format. It puts all the letters together so you can read the whole conversation at once.

### [[CLI | Command-line interface]] Packet Analysis: [[tcpdump | tcpdump]] and [[TShark | TShark]]

Sometimes, you have to work on computers that don't have a screen for pointing and clicking. You only get a black box where you type commands.

![A standard Linux command-line interface. SOC analysts rely heavily on CLI environments to execute lightweight analysis tools like tcpdump on remote or headless servers.](https://wikipedia.org/wiki/Special:Redirect/file/Linux_command-line._Bash._GNOME_Terminal._screenshot.png)

In this typing screen, you use a special tool. tcpdump is a command-line packet analyzer used to capture and display packets transmitted over a network. Instead of clicking menus, you type rules. Berkeley Packet Filter (BPF) syntax is used by tools like tcpdump to define capture filters that limit the packets recorded by the tool. Think of BPF as a secret code that tells the tool exactly what kind of traffic is allowed in.

Here are the special commands (called flags) you add to tcpdump:
*   The tcpdump '-i' flag specifies the network interface on which the tool should listen for network traffic. (This tells it which "ear" to listen with).
*   The tcpdump '-n' flag prevents the resolution of IP addresses to hostnames to speed up packet output. (This stops it from wasting time looking up computer names).
*   The tcpdump '-w' flag writes captured network packets to a specified file instead of displaying the packets on the screen. (This saves your game for later).
*   The tcpdump '-r' flag reads and displays packets from a previously saved packet capture file. (This loads your saved game).
*   The tcpdump '-X' flag displays packet contents in both hexadecimal and ASCII formats. (This shows the data in computer numbers and human letters so you can spot hidden words).

If you really want the super-power of Wireshark but only have a typing screen, you use another tool. TShark is a terminal-oriented version of Wireshark used for capturing and displaying packet data via the command line.

## High-Altitude [[Telemetry | Telemetry]]: [[Network Flow | Traffic flow (computer networking)]] and [[Metadata | Metadata]]

Saving every single thing sent over a huge network takes up too much space. Sometimes, you just want the summary—like the final score of a sports game, rather than watching every single play.

*   NetFlow data provides summarized network traffic statistics rather than full packet payloads. It’s like a phone bill that shows who you called and for how long, but it doesn't show what you actually talked about.
*   Another great tool is Zeek. Zeek is a passive, open-source network traffic analyzer used to generate connection logs and detect suspicious network patterns.
*   Instead of saving the whole conversation, Zeek extracts application-layer metadata from network traffic and stores the metadata in tab-separated log files. (Metadata is just "data about data," like knowing a pizza has pepperoni without opening the box).

![A conceptual diagram of NetFlow architecture, illustrating how network traffic flow statistics are aggregated by standalone probes and exported to a centralized collector for review.](https://wikipedia.org/wiki/Special:Redirect/file/NewNetFlowApproach.png)

## The [[Endpoint | Host (network)]] Reality: [[EPP | Endpoint security]], [[EDR | Endpoint detection and response]], and [[HIDS | Host-based intrusion detection system]]

The network shows us the paths hackers take, but endpoints (like your laptop or phone) show us what they actually touched.

First, you want to stop bad guys from getting in at all. Endpoint Protection Platforms (EPP) primarily focus on preventing malware infections and securing endpoints before an attack executes. EPP is like the sturdy lock on your front door.

But if a hacker has the key and gets past the lock, you need security cameras inside! Endpoint Detection and Response (EDR) solutions monitor endpoint activity in real time to detect and respond to advanced threats. Even better, EDR tools provide continuous recording of endpoint telemetry to facilitate post-incident forensic investigations. That means it records everything like a video camera, so you can rewind and see what happened after a break-in.

To keep an eye on a single computer, we use another tool. Host-based Intrusion Detection Systems (HIDS) analyze operating system logs and file modifications on a single host to detect malicious activity. This checks if someone messed with important files on just one specific computer.

### Peering into [[Windows | Microsoft Windows]]: [[Microsoft Sysmon | Sysinternals]]

If you use a Windows computer, there is an awesome tool to watch everything that happens. Microsoft Sysmon is a Windows system service that logs detailed system activity to the Windows event log. It keeps a diary of everything the computer does!

Security guards love to check two specific events in this diary:
*   Sysmon Event ID 1 records the creation of a new process on a Windows system. Think of a "process" like opening a new app or video game.
*   Sysmon Event ID 3 records network connections initiated or received by a Windows system. This tells you if an app is secretly trying to talk to the internet.

## The Grand Synthesis: [[SIEM | Security information and event management]] and [[Log Management | Log management]]

We have all these clues now! But having a million clues spread everywhere is confusing. We need to put them all in one giant puzzle.

Security Information and Event Management (SIEM) systems aggregate log data from multiple sources to identify potential security incidents. A SIEM is like a giant command center that collects everyone's diaries to spot the bad guy.

How do the diaries get to the command center? Syslog is a standard protocol used for sending system log or event messages to a centralized logging server. It's like a mail truck that delivers the logs. By default, the Syslog protocol uses UDP port 514 by default for transmitting log messages.

![A high-level architectural diagram of a Security Information and Event Management (SIEM) infrastructure, showing how it centralizes, standardizes, and correlates log data from diverse network and endpoint sources.](https://wikipedia.org/wiki/Special:Redirect/file/Basic_SIEM_Infrastructure.png)

### The Mechanics of SIEM [[Correlation | Event correlation]]

Because different computers speak different languages, the SIEM has to translate them. Log normalization standardizes log data from diverse sources into a uniform format to facilitate efficient searching and correlation. Imagine if one friend calls it "soda" and another calls it "pop"—normalization changes them all to "drink" so they match!

Once they match, the SIEM does its magic. Log correlation is the process of linking related log events from different systems to detect complex attack patterns. If the front door opens, and then a window breaks, correlation puts those two events together to shout "Burglary!"

For this to work, the clocks on all your computers must be exactly the same. Let's do a quick math calculation to see how much a computer clock can drift over time. If a computer's clock is too fast and gains 2 minutes every week, how far off will it be after 4 weeks?

1. First, find out how many minutes are gained each week: 2
2. Next, count the total number of weeks: 4
3. Multiply the minutes per week by the number of weeks: 2 * 4 = 8

The computer clock will be 8 minutes wrong! If that happens, the SIEM wouldn't know which event happened first. Because of this, time synchronization using Network Time Protocol (NTP) across all logging devices is strictly required for accurate log correlation.

![A hierarchical network topology diagram showing Network Time Protocol (NTP) synchronization. Perfect temporal alignment is mathematically required for a SIEM to accurately correlate log events.](https://wikipedia.org/wiki/Special:Redirect/file/Network_Time_Protocol_servers_and_clients.svg)

### Managing the Evidence

Hackers are sneaky. They might try to erase their tracks by changing your logs. We stop them with cool math! Log hashing verifies the integrity of log files by detecting unauthorized modifications to the stored log data. A hash is like a digital fingerprint. If someone changes even one letter in the log, the fingerprint changes completely, and we catch them!

![An illustration of a cryptographic hash function in action. Even a microscopic change to an input file completely alters the resulting hash digest, immediately exposing unauthorized log tampering.](https://wikipedia.org/wiki/Special:Redirect/file/Cryptographic_Hash_Function.svg)

There are even rules for how to do this perfectly. NIST SP 800-92 defines log management infrastructure as comprising log generation, log analysis and storage, and log monitoring. That just means you have to create the logs, save and study them carefully, and then always have someone watching them to keep the network safe.

When you know how to use all these tools, you are like a superhero protecting the digital world!