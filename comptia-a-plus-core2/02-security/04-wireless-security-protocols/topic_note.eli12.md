Sending data over Wi-Fi is just like shouting secrets across a crowded school cafeteria. Because Wi-Fi uses radio waves—which float invisibly in the air everywhere—anyone with a simple antenna can listen in. To keep our secrets safe, we use math. We use special secret codes (called cryptographic protocols) that scramble our words. Even if someone hears the data, it sounds like complete gibberish to them.

For someone learning how to fix computers, understanding these secret codes is super important. When a friend's laptop won't connect to the Wi-Fi, or a teacher can't log into the school server, the problem is usually a mix-up with these secret codes. Let's look at how devices lock up their data, how networks check who you are, and how we build walls to keep hackers out.

## The Evolution of Wireless Armor

To protect wireless messages, we have to scramble the data so only the sender and the right receiver can read it. Over the years, people who build networks have made this scrambling better and better, because hackers kept figuring out our old math tricks.

### The Legacy Gap: TKIP and RC4
In the early days of Wi-Fi, the very first security lock was called WEP, and it was super easy for hackers to break. To fix it quickly without making everyone buy brand new internet routers, engineers created a software update to hold things over. 

This temporary fix was called TKIP. **TKIP is a deprecated wireless encryption protocol originally created as a stopgap replacement for the insecure WEP standard.** ("Deprecated" just means it is old and we don't use it anymore.) 

How did it scramble things? **TKIP uses the RC4 stream cipher for encrypting wireless network traffic.** Think of a stream cipher like putting a secret code on a continuous stream of water from a hose, locking the data piece by tiny piece as it flows. 

But computers got a lot faster and smarter. Because of this, **TKIP is considered insecure against modern cryptographic attacks.** If you ever see a router still using TKIP today, you should turn it off immediately!

### The Modern Standard: WPA2 and AES
When routers got stronger computers inside them, the tech world introduced **WPA2** (Wi-Fi Protected Access 2). **WPA2 is a wireless security protocol that requires the use of the Advanced Encryption Standard for data encryption.** 

What is this Advanced Encryption Standard? Think of it like a super-strong, heavy-duty padlock. **The Advanced Encryption Standard is a symmetric block cipher mandated for use in WPA2 and WPA3 wireless networks.** Unlike the old stream method, a "block cipher" chunks your data into big, solid blocks and locks them all at once. It is "symmetric," meaning you use the exact same key to lock the block and to unlock it.

To make sure these locked blocks travel safely through the air, WPA2 wraps them up in a very specific way. **WPA2 uses the Counter Mode with Cipher Block Chaining Message Authentication Code Protocol for data encapsulation.** That is a gigantic mouthful! But it basically means the data is put in an armored car before it drives across the internet, ensuring it stays locked and nobody tampers with it.

WPA2 comes in two flavors, depending on where you are:
1. **WPA2 Personal mode uses a Pre-Shared Key to authenticate clients joining the wireless network.** This is the normal Wi-Fi password taped to your home router. Everyone in your family uses the exact same password (the "Pre-Shared Key").
2. **WPA2 Enterprise mode uses the IEEE 802.1X standard and an authentication server to authenticate individual wireless users.** This is for big schools or businesses. Instead of one password for everyone, you use your own personal username and password. An "authentication server" (like a security guard computer) checks your ID and gives you a special, unique lock just for your device.

### The New Frontier: WPA3
WPA2 is great, but hackers eventually found a trick. If a hacker records your device sending that Pre-Shared Key through the air, they can take the recording home, put it on a super-fast gaming computer, and guess the password millions of times until they get it right. 

**WPA3 is the latest generation of Wi-Fi security designed to mitigate vulnerabilities found in WPA2.** It fixes the old weak spots with some big upgrades:

* **WPA3 replaces the Pre-Shared Key authentication method with Simultaneous Authentication of Equals.** Now, an attacker can't take the secret code home to guess passwords on their supercomputer. They have to talk directly to your router for *every single guess*.
* Because of this change, **Simultaneous Authentication of Equals prevents offline dictionary attacks by requiring a live network interaction for every password guess.** 

Let's see why this matters with some simple step-by-step math! Imagine a hacker steals a password puzzle and wants to guess passwords until they break in.

1. Step 1: Write down the total number of guesses the hacker needs to make: 5,000,000.
2. Step 2: Note how fast the hacker's offline supercomputer can guess: 1,000,000 times per second.
3. Step 3: Divide the total guesses by the supercomputer's speed to find the time: 5,000,000 / 1,000,000 = 5. It takes only 5 seconds to crack the password!
4. Step 4: Now look at WPA3's new "live interaction" rule. Because the hacker must talk to the router directly, the router slows them down and only allows 10 guesses per second.
5. Step 5: Divide the total guesses by the new live speed: 5,000,000 / 10 = 500,000. It now takes 500,000 seconds (almost 6 whole days) to crack!

* **WPA3 mandates the use of Protected Management Frames to defend wireless networks against deauthentication attacks.** In the past, a bully could send a fake message to your computer saying "disconnect," kicking you out of your game. Protected Management Frames act like a shield to stop those fake messages.
* **WPA3 Enterprise mode offers an optional 192-bit cryptographic strength mode for highly sensitive network environments.** This means the padlock's key is incredibly long and complex, perfect for keeping bank accounts or government secrets safe.

## The Gatekeepers: Network Authentication Protocols

When you try to join a big WPA2 Enterprise or WPA3 Enterprise network, the Wi-Fi router doesn't actually decide if you get in. The router is just a messenger. It takes your username and password and sends them to a back-room boss—the authentication server.

We use special rules to help the router and the boss server talk safely.

### EAP and PEAP
How does your computer package your password before sending it to the router? 

**The Extensible Authentication Protocol provides a universal framework for deploying diverse authentication methods over wireless networks.** Think of it like a standardized mailing envelope. Whether you use a password, a smart card, or a secret code, this protocol provides the perfect envelope to carry it.

But sending a plain envelope through the air is risky! So, we use something called PEAP. **Protected Extensible Authentication Protocol establishes an encrypted TLS tunnel to securely transmit client authentication credentials.** This means before you even send your envelope, PEAP builds a safe, hidden tunnel (like a secret underground pipe) between your laptop and the boss server. Anyone spying only sees the outside of the pipe.

### RADIUS vs. TACACS+
Once the Wi-Fi router gets your envelope, it passes it over the wires to the boss server using one of two languages: RADIUS or TACACS+. 

| Feature | RADIUS | TACACS+ |
| :--- | :--- | :--- |
| **Origin** | An open rulebook anyone can use. | **TACACS+ is a proprietary network authentication protocol developed by Cisco.** (Proprietary means Cisco owns it). |
| **Transport Protocol** | **RADIUS is an authentication protocol that operates over the User Datagram Protocol** (UDP). It **conventionally operates on UDP ports 1812 and 1813.** (Ports are like numbered doors on a building). | **TACACS+ operates over the Transmission Control Protocol to guarantee reliable packet delivery.** TCP is like sending mail with a tracking number. **TACACS+ operates on TCP port 49.** |
| **Encryption** | **RADIUS encrypts only the user password field within the access-request packet.** The password is hidden, but your username is totally readable. | **TACACS+ encrypts the entire payload of the authentication packet.** It hides the username, the password, and everything else! |
| **Process Architecture** | **RADIUS combines the user authentication and user authorization processes into a single network operation.** It checks who you are (authentication) and what you are allowed to do (authorization) all at the exact same time. | **TACACS+ separates the authentication, authorization, and accounting functions into completely independent processes.** It treats checking your ID and checking your permissions as totally separate steps. |

### Kerberos: The Ticket Master
RADIUS and TACACS+ help you connect to the network. But once you are inside, how do you open a file or print a paper without typing your password every single time? We use Kerberos!

**Kerberos is a network authentication protocol that utilizes secure tickets to grant access to network services.** Think of it like going to an amusement park. You don't pay money at every single ride. You show your ID once at the front gate, and they give you a wristband (a ticket). Now, you just show your wristband to ride the rollercoasters. 

**Microsoft Active Directory environments use Kerberos as the default authentication protocol.** If you use a Windows computer at a big school, you are using Kerberos.

Instead of sending your password everywhere, it uses a central boss:
> **Key Distribution Center (KDC):** **Kerberos relies on a centralized Key Distribution Center to verify identities and issue ticket-granting tickets.** The KDC is the ticket booth at the front of the park. It gives you your master wristband (the ticket-granting ticket).

There are two really important facts about how Kerberos works:
1. **Kerberos operates on TCP and UDP port 88.**
2. **Kerberos requires strict time synchronization among all networked computers to prevent ticket replay attacks.** This means every computer's clock must match perfectly. If a bad guy copies your digital ticket and tries to use it later (a "replay attack"), the system will look at the clock, see the ticket is old, and block it. If your laptop's clock is wrong by just a few minutes, none of your tickets will work!

## Layering Defenses: Multifactor Authentication (MFA)

Math-based locks like AES are incredibly hard to pick. Bad guys know this, so they don't try to break the math. Instead, they try to trick you into giving them your password. 

To stop this, we use a strategy called MFA. **Multifactor authentication mitigates the risk of enterprise network breaches resulting from compromised passwords.** It builds extra walls so that if a hacker steals your password, they still can't get in.

**Multifactor authentication requires a user to present at least two distinct categories of authentication credentials.** It’s like needing both a metal house key and a secret alarm code to open a door.

Here are the three categories you can mix and match:
1. **The Knowledge Factor ("Something you know"):** **A standard password or personal identification number represents the knowledge factor in multifactor authentication.** It is something hidden in your brain.
2. **The Possession Factor ("Something you have"):** **A hardware token or a mobile authenticator app represents the possession factor in multifactor authentication.** This is a physical thing you hold in your hand, like your smartphone showing a random secret number.
3. **The Inherence Factor ("Something you are"):** **A fingerprint scan or facial recognition system represents the inherence factor in multifactor authentication.** This relies on a part of your own body.

By stacking these up—using a password, an app on your phone, and a super-strong WPA3 lock—we create an amazing shield around our networks. Even if one piece fails, the others step up to keep the bad guys out!