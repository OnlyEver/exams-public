Imagine a treehouse. It has a lock, maybe even a secret knock. But bad guys do not always play by the rules. They do not just try to guess the secret password. Sometimes they break the door, record your secret knock from far away to use later, or just crowd around the ladder so your friends cannot get inside. To protect computers and networks, we need to look at how these real-world attacks happen. We need to learn how hackers break things, overwhelm systems, mess with internet maps, and steal passwords.

## The Physical Perimeter: Breaking Doors and Stealing Signals

Before a hacker ever uses a computer, they might just walk right up to a building. People spend tons of money on fancy computer defenses, but they sometimes forget to protect the real, physical doors.

### The Brute Force Reality
When we hear "brute force" in movies, it usually means a hacker guessing passwords really fast on a computer screen. In real life, it can be a lot messier. **Physical brute force attacks involve using destructive force to bypass physical access controls.** This means someone might just smash a server room door with a hammer or break a lock with a drill. No fancy computer math can stop a broken door! 

Sometimes, brute force is just guessing numbers really, really patiently. **A physical brute force attack on an electronic keypad involves testing all possible numerical combinations to gain unauthorized entry.** Let's look at the math for how an attacker would guess a 4-digit keypad:
1. First, we figure out how many numbers can go into each of the 4 blank spots. There are 10 possible numbers for each spot (0 through 9).
2. Next, we multiply those possibilities together: 10 * 10 * 10 * 10.
3. Step one: 10 * 10 = 100.
4. Step two: 100 * 10 = 1,000.
5. Step three: 1,000 * 10 = 10,000 combinations.
So, an attacker acts like a slow robot, just typing 0000, then 0001, then 0002, all the way to 9999 until the door opens!

### The Invisible Pickpocket: RFID Cloning
Instead of metal keys, many buildings use plastic ID cards you tap on a reader. These are called RFID badges. But the radio waves they use do not stop right at the card reader—they float through the air!

If the door system is old, it is easy to copy the card. **RFID cloning involves capturing the radio frequency signal from a legitimate access badge and copying the badge data to a blank card.** 

> **The Mechanics of the Skim:** 
> Bad guys play spy to steal these signals. **Attackers use concealed RFID readers to surreptitiously capture access badge signals from targeted employees in public spaces.** (Surreptitiously just means sneakily!). Imagine you are sitting at a pizza shop. A hacker sits next to you with a hidden scanner in their backpack. **An RFID skimmer can read an unencrypted access card from a distance of up to three feet.** Your badge just shouted its secret code to the hacker's scanner, and you did not even notice!

To stop this, we make the badge and the door play a smarter game. **Encrypted smart cards prevent RFID cloning by requiring dynamic cryptographic handshakes instead of transmitting static identifiers.** Instead of the card shouting the exact same boring code every time, the door gives the card a math puzzle. The card solves it with a secret key and gives a unique answer. Because the answer is completely different every single time, a hacker who recorded yesterday's answer cannot use it today. It is like having a brand new secret password every second!

## Asymmetric Warfare on the Wire: DoS and DDoS Attacks

Moving from physical doors to the internet, we find a different kind of bullying. Sometimes a hacker does not want to steal your stuff; they just want to ruin your day so you cannot play your favorite game or run your business. 

**A Denial of Service (DoS) attack attempts to make a machine or network resource unavailable to legitimate users.** It is like one person blocking a playground slide so no one else can use it. But one computer usually is not strong enough to block a giant company network. So, they get friends to help. **A Distributed Denial of Service (DDoS) attack uses multiple compromised devices to overwhelm a single target system with excessive network traffic.** This is like millions of people crowding the slide all at once!

Where do they get all these extra devices? **The Mirai botnet historically launched massive Distributed Denial of Service attacks by compromising millions of Internet of Things (IoT) devices.** Hackers took over weak smart cameras, baby monitors, and Wi-Fi routers, turning random household gadgets into a giant, remote-controlled army.

### Exhausting the Network: Volumetric and Protocol Attacks
DDoS attacks try to use up different kinds of things on a network:

1. **Bandwidth Exhaustion:** Think of your internet connection like a water pipe. **Volumetric Distributed Denial of Service attacks aim to completely consume all available network bandwidth of a target organization.** If your pipe can only hold 10 gallons of water a minute, the hacker blasts 20 gallons of junk water into it. The pipe gets completely stuffed, and the good water (real internet traffic) spills out and never reaches you.
2. **State Exhaustion:** Other attacks mess with the computer's memory. **A SYN flood is a network layer attack that exhausts server resources by rapidly initiating incomplete Transmission Control Protocol (TCP) connections.** 

> **Analogy of a SYN Flood:** 
> Imagine a pizza shop where people call to order food. A person calls, and the worker writes their name down in a notebook to save a pizza for them. In a SYN flood, the hacker makes thousands of phone calls super fast but hangs up before confirming the order. The worker fills up their whole notebook with fake names and has no room left to write down orders from real, hungry customers!

### Weaponizing Trust: Amplification Attacks
Why do all the hard work yourself when you can trick bigger computers into doing it for you? 

**An amplification attack exploits vulnerable third-party servers to multiply the size of the malicious network traffic sent to a victim.** The hacker sends a tiny message to a big internet server, but they put *your* return address on the envelope. The big server then sends a massive, heavy reply to *you*. 

The size of these attacks can be unbelievable. **Attackers historically exploited the Memcached protocol to achieve a Distributed Denial of Service amplification factor of over 50,000 times.** Let's break down the math on how this multiplication works:
1. The attacker starts with just 1 Megabit of junk data.
2. They send it to the broken server.
3. The server multiplies it by the amplification factor (50,000).
4. 1 * 50,000 = 50,000 Megabits.
5. The hacker just turned a tiny pebble into a giant boulder, using the internet's own servers to crush the target!

## Subverting the Map: DNS Attacks

Computers use a system called DNS to turn easy names (like `coolmathgames.com`) into computer IP addresses (like `192.168.1.5`). Think of it as the internet's phonebook. If a hacker messes with this phonebook, they can send you anywhere they want. 

**DNS spoofing involves maliciously altering Domain Name System records to redirect users from a legitimate website to an attacker-controlled website.** You type the right name, but the fake phonebook sends you to a fake website made to steal your login!

How do they change the phonebook? Here are two ways:

| Attack Type | Mechanism of Action | Scope of Impact |
| :--- | :--- | :--- |
| **DNS Cache Poisoning** | **DNS cache poisoning introduces corrupt domain name resolution data into the cache of a Domain Name System resolver.** This means the hacker sneaks a fake address into your local internet provider's memory. | Only affects people using that one poisoned local memory until the memory gets wiped clean. |
| **Domain Hijacking** | **Domain hijacking occurs when an attacker gains unauthorized administrative control over a target domain name registration account.** The attacker breaks into the main account that owns the web name and changes the official master record. | Global impact. The whole world gets the bad directions. |

DNS can also be used as a weapon! **DNS amplification is a Distributed Denial of Service technique exploiting open DNS resolvers to send oversized response packets to a spoofed victim IP address.** A hacker asks an open phonebook a tiny question, and the phonebook sends a gigantic answer to the fake return address, crushing the victim.

## Echoes on the Network: Credential Replay Attacks

Finally, let's talk about what hackers do once they are inside the network. Just like a bad guy can record your radio badge, they can record your digital password over the network wires.

**A credential replay attack involves intercepting valid authentication data over a network and reusing the data to gain unauthorized access.** It is exactly like recording your friend saying "Open sesame!" and playing the recording later to open the clubhouse door yourself.

To do this, the hacker needs to listen. **Network sniffers capture unencrypted credentials during network transmission to facilitate credential replay attacks.** If you do not scramble (encrypt) your password, a listening program can see it clearly as it travels over the wires. 

### Pass-the-Hash
Even if a network scrambles your password into a long, messy code called a "hash," a replay attack can still work! 

**Pass-the-hash is a credential replay attack allowing an attacker to authenticate using a captured password hash instead of the plaintext password.** The computer does not care what the original password was; if you have the hash, you get in! **Pass-the-hash credential replay attacks specifically target Microsoft Windows NT LAN Manager (NTLM) authentication environments.** In these old Windows networks, the hash is just as good as the password.

### Defending the Timeline: Nonces and Kerberos
To stop people from playing back old recordings, we have to make sure every login is only good exactly one time.

First, we use special numbers. **Cryptographic nonces prevent credential replay attacks by ensuring each authentication request incorporates a mathematically unique, single-use value.** Think of a nonce like a movie ticket. Once the ticket taker rips it, you cannot use it again. If a hacker tries to replay your login, the computer sees the nonce is already "spent" and says no.

Second, newer networks use a super-strict clock system called Kerberos. **The Kerberos network authentication protocol uses strict timestamping to validate the freshness of authentication tickets.** Your digital ticket has the exact time stamped right on it. 

If a hacker grabs your ticket and tries to use it two hours later, the computer will reject it because the time is too old. For this to work, every computer has to have the exact same time. **Kerberos network authentication enforces a maximum five-minute time skew between client and server to successfully prevent credential replay attacks.** Let's check the math on how this protects the network:
1. Your computer's clock says it is 12:00 PM.
2. The server's clock says it is 12:06 PM.
3. We subtract the times to find the difference: 12:06 - 12:00 = 6 minutes.
4. We compare the 6 minutes to the 5-minute rule.
5. Since 6 is bigger than 5, the server blocks you!
If the clocks are too far apart, even good logins fail, but keeping this window small is what keeps the hackers out!

***

By learning about all these tricks—from smashing a real door to using strict computer clocks—you learn how to keep a network safe. Hackers are always looking for a sneaky way in. Your job is to make sure the computer never trusts anyone without real, fresh proof of who they are!