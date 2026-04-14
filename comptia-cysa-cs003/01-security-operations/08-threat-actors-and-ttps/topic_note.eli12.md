Think of a computer network like a giant, digital treehouse fort. A break-in isn't just a random accident; it's a planned attack by someone trying to beat the rules of your fort. Just like you know gravity pulls a dropped ball to the ground, security guards (called SOC analysts) know that hackers have to follow the rules of the computer systems they attack. To protect your fort, you can't just chase every loud noise. You have to understand who is attacking, exactly how they are doing it, and the patterns they follow.

## The Cast of Characters: Understanding Threat Actors

To beat the bad guys, you need to know what they want and what tools they have. We group these attackers into categories based on why they are trying to break in.

### Nation-States and APTs
At the very top of the hacker leaderboard are groups acting like digital secret agents. **Advanced Persistent Threats (APTs) are highly skilled and well-resourced threat actors that maintain long-term covert access to a target network.** Instead of a quick smash-and-grab, they hide in the shadows of the network for months or years. **APT groups are frequently sponsored by or affiliated with nation-state governments.** Because they have lots of time and money from their countries, **nation-state actors primarily engage in cyber espionage, intellectual property theft, or destructive attacks to advance geopolitical goals.** They aren't trying to steal your allowance; they want to steal top-secret government plans or break major systems.

### Cybercriminal Syndicates
While APTs care about spying, other groups just want cash. **Cybercriminal syndicates are highly organized groups motivated primarily by financial gain.** They run like a real, sneaky business, sometimes even having customer service desks for their victims! To make that money, **cybercriminals frequently use ransomware, data extortion, and business email compromise (BEC) to generate revenue.** 

Let's look at how the math works when they try to steal money using ransomware:
1. First, the criminals lock up a company's computers and demand money to unlock them. Identify the number of locked computers. Let's say there are 5 locked computers.
2. Next, look at the ransom price demanded for each computer. Let's say they want \$300 per computer.
3. Multiply the number of computers by the cost (5 * 300 = 1500).
4. The total ransom the criminals want the company to pay is \$1500.

### Hacktivists and Script Kiddies
Not everyone is a super-spy or a money-hungry criminal. **Hacktivists conduct cyberattacks to promote a political agenda, social cause, or ideological belief.** They are like protesters holding up big digital signs to make sure everyone sees their message. Because they want to be noticed loudly, **common hacktivist attack methods include website defacement, distributed denial-of-service (DDoS) campaigns, and doxing.** 

At the very bottom of the skill ladder are the beginners. **Script kiddies are unsophisticated threat actors who lack deep technical knowledge of computer systems.** Think of them like gamers using cheat codes they found online but don't actually understand how to program themselves. Because they can't write their own code, **script kiddies rely on pre-packaged exploitation tools and scripts created by more advanced hackers.**

### The Threat From Within
The tallest walls in the world won't help if the bad guy already has a key to the front door. **Insider threats possess legitimate, authorized access to an organization's network, facilities, or data.** We break these down into three types:
1. **Malicious insiders intentionally misuse legitimate access to steal data, commit fraud, or sabotage organizational systems.** This is like a team member purposely scoring on their own goal because they are mad at the coach.
2. **Negligent insiders unintentionally compromise security through carelessness, such as falling for phishing scams or misconfiguring systems.** This is like accidentally leaving the front door wide open when you go to bed.
3. **Shadow IT involves employees using unauthorized applications or devices to perform work duties.** For example, using a personal tablet for work stuff without telling the boss. Because the security team can't protect devices they don't know about, **Shadow IT creates an unintentional insider threat by bypassing organizational security controls and monitoring.**

## The Grammar of the Attack: Tactics, Techniques, and Procedures (TTPs)

When we watch how these hackers play the game, we use special words to describe their moves. If you want to track them, you have to learn about TTPs. 

*   **Tactics represent the high-level operational goals or objectives an adversary aims to achieve during a network intrusion.** (This is the *Why*, like "I want to get inside the base.")
*   **Techniques describe the specific methods or mechanisms an adversary uses to achieve a tactical goal.** (This is the *How*, like "I will trick someone into opening a window.")
*   **Procedures represent the exact, granular steps, commands, or tools an adversary uses to execute a specific attack technique.** (This is the *What*, like "I will use this exact crowbar tool to open the window.")

Let’s see this in action:
*   **Tactic:** **The MITRE ATT&CK framework uses tactics such as Initial Access, Persistence, and Lateral Movement to categorize adversary goals.** Let's say the hacker's goal is Initial Access (getting in for the first time).
*   **Technique:** To do this, they might decide that **spearphishing with a malicious attachment is a specific MITRE ATT&CK technique used to achieve the Initial Access tactic.** (Sending a highly targeted trick email).
*   **Procedure:** Once they trick their way inside, they use a specific program. **An adversary using the Mimikatz tool to dump credentials from memory is an example of a specific attack procedure.**

> **The Professor's Note:** TTPs are like a hacker's signature style. Two different bad guys might use the same trick, but the exact tools and typing commands they use will usually give away who they really are.

## Frameworks for Understanding Adversary Behavior

To make sense of all these attacks, defenders use guidebooks and models, almost like sports playbooks.

### The Lockheed Martin Cyber Kill Chain
Attacks aren't magic; they have to happen in a specific order. **The Lockheed Martin Cyber Kill Chain outlines the sequential phases an adversary must complete to achieve a successful cyberattack.** If you stop them at any one of these steps, their whole attack falls apart. **The seven phases of the Cyber Kill Chain are Reconnaissance, Weaponization, Delivery, Exploitation, Installation, Command and Control, and Actions on Objectives.** 

### MITRE ATT&CK
While the Kill Chain gives us the order of events, MITRE gives us the ultimate dictionary of hacker moves. **The MITRE ATT&CK framework is a globally accessible knowledge base of adversary tactics and techniques based on real-world observations.** It tells you what moves work on what computers; for example, **the MITRE ATT&CK Enterprise matrix categorizes attack techniques used against Windows, macOS, Linux, and cloud environments.**

In the real world, defenders use this cheat sheet to set traps. **Security Operations Center (SOC) analysts map observed threat actor behaviors to the MITRE ATT&CK framework to develop robust behavioral detection rules.** This means instead of just looking for one specific bad file, they look for the bad *behavior* itself.

### The Diamond Model of Intrusion Analysis
Defenders also use a special diamond-shaped chart to connect clues like a detective. **The Diamond Model of Intrusion Analysis focuses on the relationship between four core features: adversary, capability, infrastructure, and victim.** 

If you find a bad tool (Capability) talking to a bad computer address (Infrastructure), you can use this model to figure out who is attacking you. **The Diamond Model of Intrusion Analysis is primarily used to track threat actor campaigns and attribute attacks to specific groups based on observed TTPs.**

## Anatomy of a Modern Intrusion

Let's look at how a real break-in happens from start to finish.

### Infiltration and Evasion
Sometimes, hackers don't attack a heavily guarded fort directly. Instead, they attack the pizza guy who is delivering to the fort. **Supply chain attacks target vulnerabilities in third-party vendors, software updates, or hardware components to indirectly compromise a primary target.** 

Once inside, they want to stay hidden so the anti-virus software doesn't catch them. **Living off the Land (LotL) is an attack technique where adversaries use legitimate, pre-installed administrative tools to conduct malicious activities.** By using normal tools that are already supposed to be on the computer, **Living off the Land techniques help adversaries evade signature-based detection mechanisms by blending in with normal administrative traffic.** Some common tools they abuse are built right into the computer. **PowerShell, Windows Management Instrumentation (WMI), and PsExec are frequently used in Living off the Land attacks.**

### Movement and Escalation
Hackers rarely land right next to the treasure chest. To find the good stuff, they have to sneak from room to room. **Lateral movement involves an attacker expanding access from an initially compromised system to other systems within the same network.** 

To open locked doors inside the network, they need a VIP pass. **Privilege escalation occurs when an attacker obtains higher-level system permissions than were initially granted.** To get these superpowers, **attackers frequently exploit unpatched software vulnerabilities or misconfigurations to achieve local system privilege escalation.**

### Communication and Exfiltration
The hacker needs a way to secretly text their malware instructions from the outside. **Command and Control (C2) infrastructure allows threat actors to maintain communication with compromised systems inside a victim network.** 

Defenders naturally try to block the website addresses the hackers use to talk. To dodge this, **threat actors often use domain generation algorithms (DGAs) to dynamically create new C2 domains and evade static blocklists.** It’s like the hacker changing their phone number thousands of times a day so you can't block them!

Finally, the hacker grabs the prize. **Data exfiltration is the unauthorized transfer of sensitive information from a compromised network to an external location controlled by the attacker.**

## The Cost of Defense: Threat Intelligence and the Pyramid of Pain

How do we actually stop them? We look for digital fingerprints. **Indicators of Compromise (IoCs) are forensic artifacts that signal a potential computer intrusion.** Defenders get lists of these clues from special news networks: **threat intelligence feeds provide security teams with updated, actionable information on the latest adversary TTPs and associated IoCs.** 

Some clues are super obvious. **Common Indicators of Compromise include malicious IP addresses, known bad domain names, and file hash signatures.** But hackers can change these really easily. 

This brings us to a really cool idea for defenders. **The Pyramid of Pain model illustrates the relationship between indicators of compromise and the difficulty adversaries face when those indicators are blocked.**

| Level of the Pyramid | Indicator Type | Pain Caused to the Attacker when Blocked |
| :--- | :--- | :--- |
| Bottom (Trivial) | Hash Values | None. Attackers can just change a tiny bit of their file. |
| Middle (Moderate) | IP Addresses / Domain Names | Annoying. Attackers must rent new digital servers to hide in. |
| Top (Tough) | **Tactics, Techniques, and Procedures (TTPs)** | Devastating. Forces the attacker to learn a totally new game plan. |

Look at the very top. **Tactics, Techniques, and Procedures (TTPs) reside at the very top of the Pyramid of Pain.** If you block their main strategy, it ruins their whole day. **Blocking adversary TTPs forces attackers to completely reinvent their attack methodologies.** If you stop them from using their favorite trick, they have to start all over.

### The Complexity of Attribution
After the attack is stopped, we want to know "whodunnit?" 

**Threat attribution is the process of identifying the specific actor or group responsible for a cyberattack based on collected forensic evidence and TTPs.** But hackers lie. **False flag operations are deliberate attempts by threat actors to misdirect attribution by leaving artifacts typically associated with a different group.** It’s like a thief purposefully dropping someone else's wallet at the crime scene to frame them.

As a defender, your job is to see through the lies, track their TTPs, and protect the fort by making it as hard as possible for them to win!