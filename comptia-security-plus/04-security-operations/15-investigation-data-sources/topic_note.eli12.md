When a sneaky hacker breaks into a computer network, they leave clues behind, just like footprints in muddy grass or empty pizza boxes in a kitchen. Every time they connect to a network, open a file, or type a web address, the computer saves a tiny record of what happened. A security analyst’s job is like being a digital detective. They don't just guess who did it; they collect all these tiny clues to prove exactly what happened. By reading the secret diaries kept by firewalls, computers, and the network itself, we can build a perfect timeline of how the bad guy got in.

If you want to be a great security detective someday, you need to know where to look for clues. You have to know what different logs can tell you, what they can't tell you, and how to put the puzzle pieces together.

## The Foundation of Measurement: Time and Translation

Imagine trying to figure out who ate the last slice of pizza at a party, but everyone’s watch is set to a different time. The stories wouldn't make any sense! 

To fix this problem on computers, **Network Time Protocol (NTP)** synchronizes the system clocks of devices across an enterprise network. Synchronizing device clocks via Network Time Protocol is mandatory for constructing accurate chronological attack timelines from diverse logs. If your firewall says someone broke in at 10:04, and your server says a bad file opened at 10:02, it makes no sense unless both clocks are exactly the same. 

Here is how you use math to figure out the real time if a clock is broken:
1. Check the time the broken computer says the event happened: 10:05.
2. Figure out how many minutes the computer's clock is running fast: 3 minutes.
3. Subtract the fast minutes from the computer's time: 10:05 - 3 = 10:02. 
Now both clocks match!

Once all the clocks are fixed, we have another problem: computers speak different languages. A Windows computer writes clues one way, and an Apple or Linux computer writes them another way. 

To fix this, we use **Security Information and Event Management (SIEM)** systems. Think of a SIEM as a giant, smart filing cabinet. Security Information and Event Management systems aggregate logs from multiple data sources into a central repository. But just putting them in a pile isn't enough. Security Information and Event Management systems parse log fields to normalize diverse log structures into a standard format. This means it translates all the different computer languages into one easy language, so you can search for a bad guy's IP address and find every clue at the same time!

## Interrogating the Network Perimeter

The network is the roads and bridges connecting computers. Unlike a computer, which a hacker can trick, the network never lies. It just watches the cars drive by.

### Firewall Telemetry
The first line of defense is the firewall, which acts like a bouncer at a club. **Firewall logs** record the source and destination IP addresses of traffic crossing a network boundary. When you read this log, you are looking to see who was allowed in and who was kicked out. Firewall logs indicate whether a specific network connection was explicitly permitted or denied by an access control list (which is basically a VIP guest list). 

Why do we care about the people who got kicked out? Analyzing denied traffic in firewall logs helps identify external scanning attempts against a network. If a hacker is walking around your house jiggling every single doorknob to see if one is unlocked, your firewall log will show a giant spike of denied connections. This gives you an early warning that someone is snooping!

### DNS and Web Proxies
Just like you, hackers use domain names (like www.google.com) to find things. But computers only understand IP numbers, so they use a phone book called DNS. **DNS logs** contain records of domain name resolution queries made by systems on a network. Security analysts review DNS logs to detect internal endpoints attempting to resolve known malicious command and control domains. This is like catching a computer asking for the address of the villain's secret volcano base!

Once the computer gets the address, it often asks a "web proxy" to go fetch the website for it. **Web proxy logs** contain records of external web requests including the specific Uniform Resource Locators (URLs, or web links) accessed by internal users. 

> **The Encryption Blindspot:**
> Today, almost all internet traffic is locked inside secret codes using HTTPS. Because the web link is locked up, normal tools can't see exactly which file the hacker is trying to download. To get this visibility back, web proxy logs require **TLS inspection** to record the full Uniform Resource Locator paths of encrypted HTTPS traffic. This means the proxy carefully unlocks the secret code, writes down the exact web link, and locks it back up before sending it along.

## Network Flow vs. Packet Captures

When collecting clues, detectives have to balance how much detail they want with how much storage space they have. We handle this by using two different tools: Network Flow and Packet Captures.

### Network Flow (NetFlow)
Think of **network flow data** like a family phone bill. It shows who called whom, and for how long, but it doesn't have a recording of what you said. Network flow data records metadata about network connections rather than the actual data payload. Network flow metadata includes the source IP address, destination IP address, protocol used, and total bytes transferred. 

Because it doesn't save the heavy payload (the actual conversation), network flow data requires significantly less storage capacity than full packet captures. 

Here is how we calculate the saved space:
1. Start with the size of a giant, full data recording: 1,000 Megabytes.
2. Look at the fraction of space that network flow data uses: 1/100 of the size.
3. Divide the big size by 100: 1,000 / 100 = 10 Megabytes.
Saving all that computer space is a great deal, kind of like keeping an extra \$10 in your pocket!

Even without the payload, security analysts use network flow data to identify abnormal data exfiltration volumes over time. "Exfiltration" is a fancy word for sneaking data out. If a computer normally sends out 5 Megabytes a day, but suddenly sends out 400 Gigabytes in the middle of the night, you know a hacker is stealing a massive amount of files!

### Packet Captures (PCAP)
Sometimes you don't just want the phone bill; you want to listen to the whole phone call. A **packet capture** contains the raw network data payloads and network headers transmitted over a network segment. Packet captures are typically saved in the **PCAP** file format.

Because you have everything that was sent, security analysts use packet captures to extract malware files transmitted over unencrypted network protocols. If a bad guy downloads a virus over an unlocked connection, the actual virus file is sitting right there in your PCAP file for you to study!

| Tool | Purpose | Interface |
| :--- | :--- | :--- |
| **Wireshark** | Wireshark is a graphical protocol analyzer used to inspect network packet captures. It lets you click around with your mouse and puts everything into neat, color-coded windows. | Graphical User Interface (GUI) |
| **Tcpdump** | Tcpdump is a command-line utility used to capture raw network packets. It is super fast and lightweight, but you have to type text commands to use it instead of clicking with a mouse. | Command-Line Interface (CLI) |

## The Endpoints: Where Code Meets Hardware

The network shows you how the hacker traveled, but endpoint logs (the logs on laptops, phones, and servers) show you what they did when they arrived. 

### Windows Auditing and Authentication
If you are looking at a Windows computer, the main diary is the Event Log. Windows operating systems store security-related events in the Windows Security Event Log. It gives every action a special ID number. 

Two ID numbers are super important for figuring out who is logging in:
*   **Windows Event ID 4624** signifies a successful user logon event.
*   **Windows Event ID 4625** signifies a failed user logon attempt.

If a hacker is trying to guess a password, they will make a lot of noise. Correlating multiple failed logon events in endpoint logs can indicate an active brute-force password attack. A "brute-force" attack is when a hacker acts like a burglar trying 1,000 different keys on a chest until it pops open. If you see fifty 4625s (failures) and then one 4624 (success), the hacker just guessed the password!

### Linux Logging Paths
Linux computers don't have an Event Log like Windows. Instead, they write their diaries in simple text files hidden in special folders. Linux operating systems typically store centralized system logging data in the `/var/log/syslog` or `/var/log/messages` files. 

If you want to see if someone logged into a Linux computer without permission, you check a different file. Linux authentication events are recorded in the `/var/log/auth.log` or `/var/log/secure` files. Every time someone types a password, right or wrong, it goes into these files permanently.

### Endpoint Detection and Response (EDR)
Sometimes hackers are so sneaky they can hide from normal Windows and Linux diaries. To catch them, we use an advanced tool called EDR. Endpoint Detection and Response logs provide deep visibility into host-level activities like registry modifications and injected threads. This is like giving the computer an X-ray. It lets the detective see if a hacker changed deep, hidden settings (registry modifications) or tried to stuff evil code into a good program (injected threads). 

## Synthesizing Telemetry Across Domains

The best digital detectives know how to combine clues from everywhere to tell one big story. 

Imagine your firewall catches a computer inside your house talking to a bad guy's computer in another country. The firewall tells you the connection happened, but it doesn't know *which* video game or app on your computer started the chat. 

By jumping over to the computer's diary, correlating endpoint process creation logs with network flow data helps trace a malicious executable to a specific outbound network connection. You can prove that at exactly 2:00 PM, a bad file opened on the laptop, and at exactly 2:01 PM, that exact file reached out through the network! You connected the footprints right from the front door to the kitchen.

### Beyond the Traditional Perimeter
Finally, we have to remember that today, lots of computers live invisibly on the internet in the "cloud." 
*   **Cloud infrastructure logs** track API calls made to cloud service management planes. An API call is just a behind-the-scenes command. If a hacker steals a password for the cloud, they don't log into a normal screen; they send secret API commands to build fake servers or steal data.
*   **Web Application Firewall (WAF)** logs record HTTP-specific attack signatures such as cross-site scripting attempts. "Cross-site scripting" is when a hacker tries to sneak evil code into a website's typing box. A normal firewall wouldn't see it, but a WAF is a special shield that catches these exact website tricks.

By learning how to read all these different logs—from the network phone bills to the deep X-rays of a computer—you will have the superhero vision needed to catch any hacker and keep networks safe!