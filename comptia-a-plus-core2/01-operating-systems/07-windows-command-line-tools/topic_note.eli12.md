A normal computer screen with a mouse and colorful icons is like playing a video game with a controller. When you click a folder or connect to Wi-Fi, you are just using a polite, easy menu. But when a computer breaks, the polite menus do not help anymore! To fix it, you need to open the hood of the car and look at the engine. The Windows command-line interface (CLI) is a black screen where you type secret instructions directly to the computer. By learning these commands, you can fix networks, save lost files, and bring a broken computer back to life!

## The Anatomy of Navigation: Orienting in the File System

Inside a computer, files are organized like an upside-down tree or a massive house with tons of rooms. In a normal window, you just double-click to open a folder. But in the command line, you have to type exactly where you want to go.

When you type it, the **`cd`** command changes the current working directory in the Windows command prompt. This just means it walks you from one room (folder) into another so you know exactly where you are standing. If you want to see what is inside that room, you use the **`dir`** command. The `dir` command lists files and subdirectories contained within the current working directory, kind of like turning on the lights to see all the toys and boxes in your room.

You also need to know how to move up and down the house:
* Typing **`cd ..`** in the Windows command prompt moves the current path up exactly one directory level. The two dots are just like taking one single step backward out of your bedroom and into the hallway.
* If you are lost way deep inside a bunch of folders, typing **`cd \`** in the Windows command prompt changes the current directory directly to the root of the current drive. It is like a magic teleport straight to the front door of the house (the main C: drive).

If you want to remodel the house, you use these codes:
* The **`md`** command creates a new directory in the Windows file system. (Like building a brand-new room).
* The **`rd`** command removes a directory from the Windows file system. (Like knocking down a room).
* If you just want to throw away one specific item, the **`del`** command deletes one or more specified files from a directory.

> **The Cheat Code Manual:** You do not have to memorize everything! Appending **`/?`** to a Windows command line tool displays the help documentation and available execution switches for that specific tool. It is exactly like opening a video game's instruction manual to find the secret cheat codes!

## Diagnosing the Nervous System: Network Troubleshooting

When a friend says "my internet is broken," it is like saying "I feel sick." Your job is to find out exactly *why* they are sick! The command line gives you doctor's tools to figure this out.

### Self-Identity: The `ipconfig` Command
First, check your computer's own nametag. The **`ipconfig`** command displays all current TCP/IP network configuration values for the local network adapters. This tells you your computer's basic internet address. For a super deep look, the **`ipconfig /all`** command displays advanced network adapter information including the physical MAC address and assigned DNS servers. That is like looking up the computer's unchangeable fingerprint and its favorite phonebook!

If the router gave your computer a messed-up address, you have to throw it away and ask for a new one.
1. First, the **`ipconfig /release`** command sends a message to the DHCP server to discard the current IPv4 address lease. Your computer drops its old address like a hot potato.
2. Second, the **`ipconfig /renew`** command requests a new IPv4 address lease from the local DHCP server, hopefully grabbing a fresh, working address.

Sometimes the computer gets confused because it remembers an old, wrong address for a website. The **`ipconfig /flushdns`** command clears the local DNS client resolver cache to resolve domain naming issues. It wipes the computer's memory so it has to go find the correct directions again. To test the phonebook manually, the **`nslookup`** command queries Domain Name System infrastructure to resolve an IP address to a hostname or to resolve a hostname to an IP address.

### Reachability and Pathfinding: `ping` and `tracert`
Next, see if your computer can shout out to the internet. The **`ping`** command verifies IP-level connectivity to another TCP/IP computer by sending ICMP Echo Request messages. It is exactly like shouting "Marco!" across the internet and waiting for another computer to shout "Polo!" back.
* Normally it shouts four times and stops. But if the Wi-Fi is acting glitchy, the **`ping -t`** command sends continuous ping requests to the specified destination until manually interrupted by the user. It shouts forever until you tell it to stop!

If the shout does not make it, you need to track the delivery guy to see where he got lost. The **`tracert`** command displays every router hop between the source computer and the destination IP address. 

> **How Tracert Math Works:**
> How does it track the delivery? The **`tracert`** command increments the Time-to-Live (TTL) value of packets to discover the path taken to a destination network. It uses math to map the path! Here is the step-by-step math to show how TTL increments work:
> 1. The computer sets the TTL limit to 1. The message takes 1 jump to the first router. The router subtracts 1 (1 - 1 = 0). Because the answer is zero, the router drops the message and sends an error back. Now we know the name of Router #1!
> 2. Next, the computer sets the TTL to 2. It safely passes Router #1 (2 - 1 = 1), but when it hits Router #2, it does the math again (1 - 1 = 0). Router #2 sends an error back. Now we know the name of Router #2!
> 3. It keeps adding 1 to the TTL until the message finally reaches the final computer.

### Observing Active Traffic: `netstat`
If your computer is acting really slow, maybe a sneaky app is using the internet without you knowing. The **`netstat`** command displays active TCP connections, listening network ports, and Ethernet statistics. It shows you exactly who your computer is secretly talking to!
* The **`netstat -a`** command displays all active TCP connections and all listening TCP and UDP ports on the local machine. 
* Sometimes reading full website names takes too long. The **`netstat -n`** command displays active TCP connections using numerical IP addresses and port numbers instead of resolving hostnames. This just shows their raw phone numbers instead of their names!

## Storage Anatomy and Surgical File Transfers

Sometimes you have to add a brand-new hard drive to a computer or move a massive amount of saved games and homework. 

### Preparing and Healing Disks
When you buy a brand-new hard drive, it is totally blank, like a plain sheet of paper. The **`diskpart`** command is a text-mode command interpreter used to manage storage disks, partitions, and volumes. Because this tool is so powerful it could accidentally wipe out everything, the `diskpart` utility requires administrative command prompt privileges to execute successfully. You need special permission! Once it is ready, the **`format`** command prepares a raw storage drive to hold data by creating a new file system.

Over time, hard drives can get scratched or messy. The **`chkdsk`** command checks the file system metadata of a storage volume for logical and physical errors. It has two ways to heal the drive:
1. The **`chkdsk /f`** command fixes logical file system errors on the targeted storage drive. It fixes the messy handwriting on the page.
2. The **`chkdsk /r`** command locates bad sectors on a physical disk and recovers readable information into healthy sectors. It finds actual rips in the paper and safely moves your stuff to a clean spot!

Executing the `chkdsk /r` command automatically implies and includes the file-fixing functionality of the `/f` switch! But there is a huge rule: The `chkdsk /f` command requires exclusive access to the target storage volume to perform file system repairs. You cannot fix a bicycle chain while someone is currently riding the bike! If you try to fix the main drive you are currently using, the `chkdsk` utility will schedule a disk scan to run automatically during the next system restart if the target volume is currently in use by the operating system.

### Migrating Data: From Simple to Robust
Moving files is easy, but moving *lots* of files takes special tools. 
* The standard **`copy`** command duplicates files from one location to another without retaining advanced NTFS permissions. It is fine for one small picture, but bad for secret files.
* The **`xcopy`** command copies files and entire directory trees while retaining original file attributes.
* For giant, massive moves, use the ultimate tool. The **`robocopy`** command is a robust file copying tool designed for reliable duplication of massive directory trees over network connections. Its best superpower? The `robocopy` command can automatically resume interrupted file transfers after a temporary network disconnection. If your dog trips over the Wi-Fi plug, it just waits patiently and starts right back up where it left off!

## Governing the Operating System

Computers in a school or business have strict rules set by the principal or boss. Sometimes your computer acts up and you need to force it to behave.

### Active Directory and Group Policy
These rules are called Group Policy. If the boss changes a rule, your computer might not notice right away. The **`gpupdate`** command applies new or modified local and Active Directory-based Group Policy settings to the machine. If your computer is stubbornly ignoring the new rules because it wants to save energy, the **`gpupdate /force`** command ignores all background processing optimization rules and forcefully reapplies all Group Policy settings!

If you want to know exactly what rules are placed on you, the **`gpresult`** command displays the Resultant Set of Policy information for a specific user or computer. The **`gpresult /r`** command displays Group Policy summary data and lists the specific Group Policy Objects currently applied to the system.

### System Integrity and Repair
If your computer is crashing with blue screens, some important invisible game files might be broken. The System File Checker (**`sfc`**) command scans all protected system files and replaces corrupted versions with a cached healthy copy. To do this right now, the **`sfc /scannow`** command immediately initiates the scanning and repairing process for all protected Windows system files.

If the secret backup box that `sfc` uses is *also* broken, you have to fix the backup box first! The Deployment Image Servicing and Management (**`dism`**) command services Windows images and repairs corruption in the underlying Windows component store. 

### Process and Power Management
Imagine your computer gets an allowance, like \$100 of memory, to spend on running apps. If a game freezes, it might eat all that money! 
The **`tasklist`** command outputs a comprehensive list of all currently running processes and their associated memory usage on a Windows machine. It shows you exactly who is stealing the money! 
To stop the frozen app, the **`taskkill`** command ends active processes by targeting either the numerical process ID or the executable image name. If the app is totally stuck and refuses to close nicely, the **`taskkill /f`** command forcefully terminates a running process without waiting for the application to close gracefully. It crushes it instantly!

Finally, you need to know how to manage power using commands. 
* The **`shutdown /s`** command performs a standard power off sequence for the local computer system.
* The **`shutdown /r`** command performs a full power off sequence and subsequently restarts the local computer system.
* If you change your mind, the **`shutdown /a`** command aborts a previously initiated system shutdown timer.
* To set a timer, the **`shutdown /t`** command specifies the exact time delay in seconds before a scheduled system shutdown event occurs.

> **Shutdown Math:**
> If you want the computer to reboot in exactly two hours, you have to convert hours into seconds! Here is the step-by-step math:
> 1. Find out how many minutes are in 2 hours (2 * 60 = 120 minutes).
> 2. Multiply those minutes by the seconds in a single minute (120 * 60 = 7200 seconds).
> 3. Type `shutdown /r /t 7200` to set the perfect timer!