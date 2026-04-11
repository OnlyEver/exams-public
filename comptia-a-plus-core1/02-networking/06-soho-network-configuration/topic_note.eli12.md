A computer network is like organizing a massive multiplayer video game. To send a message from your laptop to a game server across the world, every piece of information needs an exact address. Every machine needs to know who it is and how its message will travel over the wires or through the air. At home, you use a Small Office/Home Office (SOHO) network to connect everything. Understanding these networks isn't just about memorizing buttons; it's about learning the rules of how computers talk to each other.

## The Addressing Schema: IPv4 and IPv6

Before a device can play online, it needs a nametag. In computer talk, this nametag is an IP address. Think of it like your home's street address, but for a computer.

Right now, networks use two main types of addresses:

**IPv4 is a 32-bit network address format.** Reading 32 ones and zeros is really hard for humans. Here is a step-by-step math example of how we make it easier to read:
1. Start with the total size: an IPv4 address has 32 bits total.
2. Divide the bits evenly into 4 separate groups.
3. 32 / 4 = 8 bits per group (a group of eight is called an "octet").

Because of this grouping, **IPv4 addresses are written in four decimal octets separated by periods** (for example, 192.168.1.50). 

But think about how many phones, tablets, and computers exist in the world! We ran out of IPv4 addresses. So, we made a bigger version. **IPv6 is a 128-bit network address format.** Because this number is so huge, **IPv6 addresses are written in eight groups of hexadecimal characters separated by colons**.

But an IP address alone isn't enough. When your computer looks at an address, it has to ask: *Is my friend inside my own house, or in another city?*

### Delineating the Neighborhood: Subnet Masks

To figure out if a friend is in your house or far away, **an IPv4 address requires a subnet mask to distinguish the network portion from the host portion.** 

Think of the "network portion" as your street name and the "host portion" as your specific house number. **A subnet mask determines the specific network segment to which a host device belongs.**

**An IPv4 subnet mask is a 32-bit number**, and it looks just like an IP address (like 255.255.255.0). 

IPv6 does this same job without needing a separate mask. Instead, **IPv6 uses a prefix length designation to identify the network portion of the address**, written with a slash at the end (like /64).

### The Exit Door: Default Gateways

If your computer realizes your friend's IP address is not in your local neighborhood, it needs a way out of the house. 

**A default gateway is the router interface that connects a local subnet to external networks.** It's literally the front door to the internet! Because of this, **a host device sends traffic to the default gateway when the destination IP address is not on the local network.**

There is a very strict rule for this front door: **a default gateway IP address must be on the exact same local subnet as the connecting host device.** You can't use your neighbor's front door to leave your own house!

## The Mechanics of Assignment

How do your devices get all these important numbers? There are two ways.

### Dynamic Addressing

Imagine giving a custom jersey number to 100 kids at a sports camp. Doing it yourself would take forever. Instead, you get a coach to do it automatically. **Dynamic IP addressing uses the Dynamic Host Configuration Protocol to automatically assign network configurations.** (We call this coach DHCP).

When your phone connects to Wi-Fi, it asks the coach for a number. **A Dynamic Host Configuration Protocol server leases an IP address to a client device for a specific duration of time.** It’s just like checking out a library book. Because the coach keeps a careful list of who has which number, **dynamic IP addressing reduces the likelihood of duplicate IP address conflicts on a network.**

### Static Addressing

While automatic numbers are great for phones, some devices need to keep the exact same number forever. **Static IP addressing requires a technician to manually enter the IP address into the device configuration.** 

Why do this hard work? Because some machines are like the team captain—everyone always needs to know exactly where they are.
* **Network servers require static IP addresses to ensure uninterrupted availability for client requests.** If the server's address kept changing, your video game would keep crashing because it couldn't find the server.
* Also, **networked printers are typically assigned static IP addresses to maintain a reliable connection path for end users.** This way, when you print your homework, the computer always knows exactly where the printer is.

## When Things Go Wrong: APIPA

Sometimes, things break. You might check your computer and see a weird IP address starting with 169.254. This is actually a cool rescue trick your computer does!

**Automatic Private IP Addressing is a fallback mechanism used when a device cannot reach a DHCP server.** 

If your computer shouts for the DHCP coach and nobody answers, it gives itself a random emergency number. 
* **The Automatic Private IP Addressing range for IPv4 is 169.254.0.1 through 169.254.255.254.**
* **IPv6 utilizes link-local addresses starting with the fe80::/10 prefix for local subnet communication.**

This emergency number tells you something is broken! **The presence of an Automatic Private IP Addressing assignment strongly indicates a DHCP server failure.** Or, it could mean a wire is unplugged, because **the presence of an Automatic Private IP Addressing assignment strongly indicates a physical network connectivity issue preventing DHCP communication.**

These emergency addresses have big limits. Because the computer didn't get a front door (default gateway) from the coach, **a device with an Automatic Private IP Addressing assignment can only communicate with other devices on the exact same local subnet.** Because of this rule, **traffic from an Automatic Private IP Addressing assignment cannot be routed to the internet.** It only lets you talk to devices inside your own house.

## Naming and Translation

People are bad at memorizing long numbers. We like words better. **A Domain Name System server translates human-readable web addresses into numeric IP addresses.** It works like the contacts app in your phone, turning a name like "google.com" into the hidden numbers computers need.

But there is another trick happening behind the scenes. Even if you spend \$100 on your internet bill, your internet company only gives your house one single public IP address. But you have lots of devices! 

**Network Address Translation enables multiple local devices to share a single public IP address for internet access.** It acts like a parent managing the family's mail, putting the family's main address on all the letters going out and sorting the letters to the right kid when they come back.

## Anatomy of the SOHO Router

In huge office buildings, routers, switches, and Wi-Fi antennas are all separate, giant boxes. At your house, you just have one plastic box. **A Small Office/Home Office router typically combines routing, switching, and wireless access point features into one physical appliance.**

### Traffic Direction and Security

Because your router hides your home devices from the internet, outside players can't easily connect to your Minecraft server. To fix this, we use a special rule. **Port forwarding directs incoming internet traffic on a specific port to a designated internal IP address.**

Setting this up used to be super annoying. So, companies made a shortcut. **Universal Plug and Play allows network applications to automatically configure port forwarding rules on a router.** 

It sounds awesome, but it is actually really dangerous. **Security best practices recommend disabling Universal Plug and Play to prevent malware from automatically opening inbound firewall ports.** If a virus gets on your computer, UPnP lets the virus open your router's doors to hackers without even asking you!

### Prioritizing Packets

Some internet traffic is more important than others. If downloading a picture takes an extra second, you don't really care. But if your voice lags during a game, it ruins everything. **Quality of Service configurations prioritize specific network traffic types like Voice over IP to prevent transmission latency.** This acts like a VIP fast-pass at an amusement park, letting your voice chat skip to the front of the line.

## Securing and Tuning the Airwaves

The Wi-Fi inside your SOHO router uses invisible radio waves to send data through the air.

### The Identity of the Network

When you want to connect your tablet, you look at a list of names. **A Service Set Identifier is the broadcasted name of a wireless network.** 

Some people try to be sneaky by hiding this name. **Disabling Service Set Identifier broadcasting hides the wireless network name from casual user discovery.** But this is a bad way to stay safe!
* **Disabling Service Set Identifier broadcasting does not encrypt wireless network traffic.** (It doesn't scramble your data).
* **Disabling Service Set Identifier broadcasting does not prevent skilled attackers from discovering the wireless network.** A bad guy with the right tools can easily still see it.

To actually protect your Wi-Fi, you need secret math codes. **Wi-Fi Protected Access 2 and Wi-Fi Protected Access 3 are cryptographic protocols used to secure wireless network traffic.** They scramble your data so nobody can read it.

### Access Control

Every single computer or phone chip has its own permanent factory serial number. **A Media Access Control address is a 48-bit physical identifier assigned to a network interface controller.** 

Some routers use **Media Access Control filtering**, which **restricts network access based on the physical hardware addresses of the client devices.** It works like a bouncer at a club checking a VIP list to see if your device is allowed inside.

### The Physics of Frequencies

Home Wi-Fi uses two main types of radio waves: 2.4 GHz and 5 GHz. Understanding these waves helps you fix bad Wi-Fi!

| Frequency Band | Data Speed | Physical Range | Wall Penetration |
| :--- | :--- | :--- | :--- |
| **2.4 GHz** | Slower | Longer | High |
| **5 GHz** | Faster | Shorter | Low |

Think of the 2.4 GHz wave as a slow, heavy bowling ball, and the 5 GHz wave as a super-fast ping-pong ball.
* **The 2.4 GHz wireless frequency band provides a longer physical signal range than the 5 GHz wireless frequency band.** 
* Because of how it moves, it pushes through stuff easily. But, **the 2.4 GHz wireless frequency band provides slower maximum data transmission speeds than the 5 GHz wireless frequency band.**

On the other hand, the 5 GHz wave is built for speed. **The 5 GHz wireless frequency band provides faster maximum data transmission speeds than the 2.4 GHz wireless frequency band.** But because it's so fast and light, it gets blocked easily: **the 5 GHz wireless frequency band has less ability to penetrate solid walls than the 2.4 GHz wireless frequency band.**

Setting up a home network is like setting up the ultimate playground. When you understand how the addresses, translations, and invisible radio waves work, you can fix almost any problem!