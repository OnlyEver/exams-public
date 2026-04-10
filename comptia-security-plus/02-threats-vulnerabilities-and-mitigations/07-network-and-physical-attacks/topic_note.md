Whether constructed of steel tumblers or [cryptographic algorithms](https://en.wikipedia.org/wiki/Cryptography), an [access control system](https://en.wikipedia.org/wiki/Access_control) is fundamentally a boundary where a system must decide whether to grant trust. If we examine how these boundaries fail in the real world, we see that attackers rarely play by the rules the system's designer imagined. They do not merely attempt to guess the correct mathematical key; they might smash the mechanism holding the lock, perfectly mimic the signal of an authorized user from a distance, or simply flood the hallway with so much noise that legitimate users cannot reach the door at all. For the [network administrator](https://en.wikipedia.org/wiki/Network_administrator) or [security professional](https://en.wikipedia.org/wiki/Information_security), understanding these attacks requires zooming out from the idealized protocols and looking at the raw, physical reality of how devices communicate, fail, and authenticate. 

To defend an infrastructure, we must understand how attackers manipulate the physical environment, exhaust network resources, subvert the internet’s routing maps, and echo our own credentials back at us.

## The Physical Perimeter: Breaking Doors and Stealing Signals

Before a [packet](https://en.wikipedia.org/wiki/Network_packet) ever reaches a [router](https://en.wikipedia.org/wiki/Router_%28computing%29), your network relies on the physical integrity of your facilities. We often spend millions on [firewalls](https://en.wikipedia.org/wiki/Firewall_%28computing%29) and [intrusion prevention systems](https://en.wikipedia.org/wiki/Intrusion_detection_system), only to leave the [physical access points](https://en.wikipedia.org/wiki/Physical_security) vulnerable to highly tangible exploits.

### The Brute Force Reality
In the digital realm, we think of [brute force](https://en.wikipedia.org/wiki/Brute-force_attack) as a computationally intensive password-guessing game. In the physical realm, it is much more literal. **Physical brute force attacks involve using destructive force to bypass physical access controls.** This might mean using a [crowbar](https://en.wikipedia.org/wiki/Crowbar_%28tool%29) on a server room door or drilling out the core of a server rack lock. No cryptographic algorithm can withstand a severed cable or a stolen [hard drive](https://en.wikipedia.org/wiki/Hard_disk_drive). 

Even when destructive force isn't used, physical access control mechanisms can be mathematically exhausted. Consider the [electronic lock](https://en.wikipedia.org/wiki/Electronic_lock) on your [data center](https://en.wikipedia.org/wiki/Data_center). **A physical brute force attack on an electronic keypad involves testing all possible numerical combinations to gain unauthorized entry.** If a keypad has four digits and no lockout mechanism after failed attempts, an attacker standing at the door simply acts as a slow, mechanical [script](https://en.wikipedia.org/wiki/Scripting_language), systematically testing from `0000` to `9999` until the door clicks open.

![An electronic keypad lock representing a physical access boundary. Without a lockout mechanism after failed attempts, an attacker can sequentially test every numerical combination to gain entry.](https://wikipedia.org/wiki/Special:Redirect/file/Digicode.JPG)

### The Invisible Pickpocket: RFID Cloning
Most modern enterprises use [radio frequency identification](https://en.wikipedia.org/wiki/Radio-frequency_identification) (RFID) badges rather than keys or keypads. When an employee taps their badge to a reader, they are transmitting an identifier. But [radio waves](https://en.wikipedia.org/wiki/Radio_wave) do not stop at the plastic casing of a card reader—they bleed into the physical environment.

If a system uses unencrypted legacy RFID technology, it is highly susceptible to cloning. **[RFID cloning](https://en.wikipedia.org/wiki/Radio-frequency_identification%23Security_and_privacy) involves capturing the radio frequency signal from a legitimate access badge and copying the badge data to a blank card.** 

> **The Mechanics of the Skim:** 
> Attackers use **concealed RFID readers to surreptitiously capture access badge signals from targeted employees in public spaces**. Imagine an employee sitting at a coffee shop next to your office building. An attacker sits at the adjacent table with a concealed reader in a backpack. **An RFID skimmer can read an unencrypted access card from a distance of up to three feet.** The employee never knows their badge just "shouted" its ID to a malicious device. 

To stop this, we must shift the paradigm of how the badge proves its identity. **Encrypted [smart cards](https://en.wikipedia.org/wiki/Smart_card) prevent RFID cloning by requiring dynamic [cryptographic handshakes](https://en.wikipedia.org/wiki/Challenge%E2%80%93response_authentication) instead of transmitting static identifiers.** Rather than the card continually shouting a static string of numbers (which a cloner can simply record and parrot back), the door reader issues a unique mathematical challenge. The card processes this challenge using a secret internal key and returns a unique answer. Because the answer changes every single time, a cloned recording of yesterday's handshake is completely useless today.

![A smart card held to the light, revealing the embedded copper antenna coil and integrated microchip. Unlike basic RFID badges, these chips perform dynamic cryptographic handshakes to prevent signal cloning.](https://wikipedia.org/wiki/Special:Redirect/file/Australia_Bank_Paypass_Card.png)

## Asymmetric Warfare on the Wire: DoS and DDoS Attacks

Moving from the [physical layer](https://en.wikipedia.org/wiki/Physical_layer) to the [network layer](https://en.wikipedia.org/wiki/Network_layer), we encounter a different philosophy of attack. Sometimes, an attacker doesn't want to steal your data; they simply want to stop you from doing business. 

**A [Denial of Service (DoS) attack](https://en.wikipedia.org/wiki/Denial-of-service_attack) attempts to make a machine or network resource unavailable to legitimate users.** When an attacker realizes that their single computer cannot generate enough traffic to take down an enterprise firewall, they distribute the workload. **A [Distributed Denial of Service (DDoS) attack](https://en.wikipedia.org/wiki/Denial-of-service_attack%23Distributed_attack) uses multiple [compromised devices](https://en.wikipedia.org/wiki/Zombie_%28computer_science%29) to overwhelm a single target system with excessive network traffic.**

**The [Mirai botnet](https://en.wikipedia.org/wiki/Mirai_%28malware%29) historically launched massive Distributed Denial of Service attacks by compromising millions of [Internet of Things](https://en.wikipedia.org/wiki/Internet_of_things) (IoT) devices.** By infecting poorly secured webcams, baby monitors, and home routers, attackers built an army of millions of devices, turning mundane household electronics into a synchronized [cyber weapon](https://en.wikipedia.org/wiki/Cyberweapon).

![Diagram illustrating a Distributed Denial of Service (DDoS) attack, where a malicious actor commands a distributed network of compromised devices to simultaneously flood a target server with traffic.](https://wikipedia.org/wiki/Special:Redirect/file/Stachledraht_DDos_Attack.svg)

### Exhausting the Network: Volumetric and Protocol Attacks
DDoS attacks generally fall into different categories based on *what* resource they are trying to exhaust.

1. **Bandwidth Exhaustion:** **Volumetric Distributed Denial of Service attacks aim to completely consume all available network bandwidth of a target organization.** If your corporate internet pipe can handle 10 [Gigabits per second](https://en.wikipedia.org/wiki/Gigabit_per_second), the attacker simply sends 20 Gigabits per second of junk data. The [internet service provider's](https://en.wikipedia.org/wiki/Internet_service_provider) circuits saturate, and legitimate traffic is dropped before it ever reaches your firewall.
2. **State Exhaustion:** Other attacks target the processing memory of your [networking equipment](https://en.wikipedia.org/wiki/Networking_hardware). **A [SYN flood](https://en.wikipedia.org/wiki/SYN_flood) is a network layer attack that exhausts server resources by rapidly initiating incomplete [Transmission Control Protocol](https://en.wikipedia.org/wiki/Transmission_Control_Protocol) (TCP) connections.** 

> **Analogy of a SYN Flood:** 
> Imagine a restaurant where customers call in to reserve a table. A customer calls (sending a `SYN` packet), and the host writes their name in the ledger and reserves a table (the server replies with a `SYN-ACK` and holds memory open). In a SYN flood, the attacker makes thousands of calls per second but hangs up before confirming. The host fills the entire ledger with half-open reservations, leaving no tables available for legitimate, paying customers.

![Mechanism of a SYN flood. The attacker repeatedly sends synchronization requests (SYN) but intentionally ignores the server's acknowledgments (SYN-ACK), creating half-open connections that quickly exhaust the server's available memory.](https://wikipedia.org/wiki/Special:Redirect/file/Tcp_synflood.png)

### Weaponizing Trust: Amplification Attacks
Why generate your own attack traffic when you can trick legitimate internet infrastructure into doing it for you? 

**An [amplification attack](https://en.wikipedia.org/wiki/Denial-of-service_attack%23Amplification) exploits vulnerable third-party servers to multiply the size of the malicious network traffic sent to a victim.** The attacker sends a small request to a vulnerable server, but [spoofs (fakes) their return IP address](https://en.wikipedia.org/wiki/IP_spoofing) so it looks like the request came from the *victim*. The server then sends a massive reply to the victim. 

The scale of these attacks can be staggering. **Attackers historically exploited the [Memcached](https://en.wikipedia.org/wiki/Memcached) protocol to achieve a Distributed Denial of Service amplification factor of over 50,000 times.** An attacker with just 1 [Megabit](https://en.wikipedia.org/wiki/Megabit) of bandwidth could generate 50 Gigabits of crushing attack traffic, effectively weaponizing the internet's own servers against the target.

## Subverting the Map: DNS Attacks

To direct traffic on a network, computers rely on the [Domain Name System](https://en.wikipedia.org/wiki/Domain_Name_System) (DNS) to translate human-readable names (like `bank.com`) into [IP addresses](https://en.wikipedia.org/wiki/IP_address). If an attacker can manipulate this translation, they control reality for the user. 

**[DNS spoofing](https://en.wikipedia.org/wiki/DNS_spoofing) involves maliciously altering Domain Name System records to redirect users from a legitimate website to an attacker-controlled website.** The user types the correct [URL](https://en.wikipedia.org/wiki/URL), their browser shows a green padlock, but they are secretly interacting with a malicious server designed to steal their credentials.

![The standard process of a DNS resolver translating a domain name into an IP address by iteratively querying authoritative servers. Attackers target this resolution chain to seamlessly redirect users to malicious infrastructure.](https://wikipedia.org/wiki/Special:Redirect/file/Example_of_an_iterative_DNS_resolver.svg)

How does the attacker alter these records? There are two primary methods, operating at different levels of the infrastructure:

| Attack Type | Mechanism of Action | Scope of Impact |
| :--- | :--- | :--- |
| **[DNS Cache Poisoning](https://en.wikipedia.org/wiki/DNS_spoofing)** | **DNS cache poisoning introduces corrupt domain name resolution data into the cache of a Domain Name System resolver.** An attacker tricks a local DNS server (like your ISP's resolver) into saving a fake IP address. | Affects only the users relying on that specific poisoned resolver until the cache expires. |
| **[Domain Hijacking](https://en.wikipedia.org/wiki/Domain_hijacking)** | **Domain hijacking occurs when an attacker gains unauthorized administrative control over a target [domain name registration](https://en.wikipedia.org/wiki/Domain_name_registrar) account.** The attacker logs into the [registrar](https://en.wikipedia.org/wiki/Domain_name_registrar) (e.g., [GoDaddy](https://en.wikipedia.org/wiki/GoDaddy), [Route53](https://en.wikipedia.org/wiki/Amazon_Route_53)) and changes the official authoritative records. | Global impact. The entire internet is handed the attacker's fake routing instructions. |

DNS is not only a target; it can also be a weapon. Returning to the concept of amplification, **[DNS amplification](https://en.wikipedia.org/wiki/Denial-of-service_attack%23Amplification) is a Distributed Denial of Service technique exploiting [open DNS resolvers](https://en.wikipedia.org/wiki/Domain_Name_System%23DNS_resolvers) to send oversized response packets to a spoofed victim IP address.** Because a small DNS query (e.g., "Give me all cryptographic records for this domain") can result in a massive response payload, open DNS servers are a favorite tool for generating volumetric DDoS attacks.

## Echoes on the Network: Credential Replay Attacks

Finally, we must address how attackers [move laterally](https://en.wikipedia.org/wiki/Lateral_movement_%28cybersecurity%29) once they are inside the environment. Just as a physical attacker might record and clone an RFID badge, a network attacker can record and clone your digital identity.

**A [credential replay attack](https://en.wikipedia.org/wiki/Replay_attack) involves intercepting valid authentication data over a network and reusing the data to gain unauthorized access.** 

To execute this, an attacker first needs visibility into the traffic. **[Network sniffers](https://en.wikipedia.org/wiki/Packet_analyzer) capture unencrypted credentials during network transmission to facilitate credential replay attacks.** If an administrator authenticates over [Telnet](https://en.wikipedia.org/wiki/Telnet) or legacy [HTTP](https://en.wikipedia.org/wiki/HTTP), their credentials traverse the wire in [plaintext](https://en.wikipedia.org/wiki/Plaintext), easily captured by tools like [Wireshark](https://en.wikipedia.org/wiki/Wireshark). 

But what if the network relies on [hashed passwords](https://en.wikipedia.org/wiki/Cryptographic_hash_function) rather than plaintext? Even here, the replay attack is a potent threat. 

### Pass-the-Hash
In certain older enterprise protocols, the hashed version of a password is used as the cryptographic key itself. If the attacker intercepts the hash, they do not need to [crack it](https://en.wikipedia.org/wiki/Password_cracking) to find the original password; they can simply present the hash to the server. 

**[Pass-the-hash](https://en.wikipedia.org/wiki/Pass_the_hash) is a credential replay attack allowing an attacker to authenticate using a captured password hash instead of the plaintext password.** Because of legacy architectural decisions, **Pass-the-hash credential replay attacks specifically target Microsoft [Windows NT LAN Manager](https://en.wikipedia.org/wiki/NTLM) (NTLM) authentication environments.** In NTLM, the hash is functionally equivalent to the password. If you hold the hash, you hold the keys to the kingdom.

![In a credential replay or pass-the-hash attack, an adversary intercepts a valid authentication hash traveling across the network and re-transmits it to the target server to fraudulently gain access.](https://wikipedia.org/wiki/Special:Redirect/file/Replay_attack_on_hash.svg)

### Defending the Timeline: Nonces and Kerberos
To defeat credential replay attacks, network architects must design systems where a captured authentication message becomes useless the moment it is intercepted. We do this by embedding time and uniqueness into the cryptography.

First, we use nonces. **[Cryptographic nonces](https://en.wikipedia.org/wiki/Cryptographic_nonce) prevent credential replay attacks by ensuring each authentication request incorporates a mathematically unique, single-use value.** (Nonce stands for "Number Used Once"). If an attacker captures a login request and replays it, the server rejects it because the nonce inside the message has already been "spent."

Second, modern Windows domains replaced vulnerable NTLM with [Kerberos](https://en.wikipedia.org/wiki/Kerberos_%28protocol%29), a protocol built entirely around chronological freshness. **The Kerberos network authentication protocol uses strict [timestamping](https://en.wikipedia.org/wiki/Trusted_timestamping) to validate the freshness of authentication tickets.** When a user requests access to a service, their cryptographic ticket includes the exact current time. 

If an attacker captures a Kerberos ticket and attempts to replay it hours later, the server will reject it because the timestamp is stale. For this to work, however, every [clock](https://en.wikipedia.org/wiki/Clock_synchronization) on the network must agree on what time it is. Therefore, **Kerberos network authentication enforces a maximum five-minute [time skew](https://en.wikipedia.org/wiki/Clock_skew) between [client and server](https://en.wikipedia.org/wiki/Client%E2%80%93server_model) to successfully prevent credential replay attacks.** If an IT administrator allows a [domain controller's](https://en.wikipedia.org/wiki/Domain_controller) clock to drift by more than five minutes, legitimate logins will fail, but more importantly, the narrow window that protects the network from replay attacks will collapse.

![The Kerberos protocol architecture. By requiring clients to negotiate with key distribution centers and embedding chronological timestamps into tickets, Kerberos ensures that any intercepted credentials quickly expire, neutralizing replay attacks.](https://wikipedia.org/wiki/Special:Redirect/file/Kerberos_protocol.svg)

***

By understanding these vectors—from the brute force destruction of a door lock to the mathematical elegance of a Kerberos timestamp—you build a holistic view of [infrastructure security](https://en.wikipedia.org/wiki/Infrastructure_security). The [adversary](https://en.wikipedia.org/wiki/Threat_actor) is constantly looking for the point where a signal, a session, or a secret can be exploited. Your job is to ensure that trust is never granted without absolute, unforgeable proof of identity and intent.