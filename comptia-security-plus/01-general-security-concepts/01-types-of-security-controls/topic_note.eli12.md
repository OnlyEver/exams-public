When protecting a computer network, relying on just one defense is a terrible idea. Imagine you build an amazing fort in your backyard. You might buy the biggest, heaviest padlock for the front door. But if your friend accidentally leaves a window wide open, all your hard work is useless! Security isn't just one magic app you download. It is a giant, overlapping system of different traps, rules, and locks meant to keep the bad guys out and fix things if they sneak in.

To build the best defense, we have to sort our tools into two main groups: *how* the tool is put to work, and *what* job it is supposed to do. If you only focus on putting passwords on computers, you are forgetting to lock the actual doors to the building. Understanding how to group these security tools helps us find our weak spots so we can build an unbeatable defense.

## The Axis of Implementation: Security Control Categories

**Security controls are divided into categories based on how the controls are implemented within an organization.** 

When we talk about categories, we are asking: *What is the thing doing the actual work?* Is it a computer program? Is it a human being? Is it a set of rules written on paper? Or is it a heavy metal door?

### Technical Controls (Logical Controls)
Think of these like the forcefields in a video game. **Technical controls use technology and automated processes to reduce vulnerabilities and protect digital assets.** Because these tools live entirely inside computers and use computer logic to work, **technical controls are frequently referred to as logical controls.**

These tools don't need a human to remember to turn them on; the computer does the work automatically. **Examples of technical controls include network firewalls, data encryption algorithms, and antivirus software.** If a hacker tries to steal a file, the technical control acts like a robot guard, doing the math to check their password and locking them out if they are wrong.

### Managerial Controls (Administrative Controls)
Before you can build your robot guards, someone has to write the rulebook! **Managerial controls focus on the management of risk and the development of overarching organizational security policies.** Because these controls come from the bosses and the people running the organization, **managerial controls are frequently referred to as administrative controls.**

Think of these as the game plan a coach makes before a big match. They don't block the hacker directly, but they guide everyone else on what to do. **Examples of managerial controls include acceptable use policies, risk assessments, and vulnerability management plans.** 

### Operational Controls
If managerial controls are the rulebook, operational controls are the players actually playing the game. **Operational controls are security measures executed by people on a day-to-day basis to support organizational security.**

Computers can't do everything by themselves; human beings have to help out every single day. **Examples of operational controls include security awareness training, incident response procedures, and change management processes.** When you learn how to spot a fake email (phishing) or practice a fire drill at school, you are performing an operational control!

### Physical Controls
A lot of computer hacks actually start in the real world. **Physical controls restrict physical access to physical facilities, computing hardware, and networking equipment.** There is a famous rule in computer security: *If a bad guy can actually touch your computer, it's not your computer anymore.*

If a thief can just walk into your room and steal your hard drive, all your passwords are useless. **Examples of physical controls include door locks, perimeter fences, and anti-ram bollards** (those heavy concrete pillars you see outside stores so cars can't crash into them). 

---

## The Axis of Function: Security Control Types

While categories tell us *how* a tool is built, **security control types describe the functional intent or specific action of a given security control.** Now we are asking: *When does this tool step in to help, and what is its main goal?*

### Directive Controls
**Directive controls are designed to mandate specific behaviors to ensure personnel compliance with security policies.** To "mandate" means to make a strict rule. **Directive controls dictate the strict rules that employees and systems must follow within an organization.** 

Think of this like your parents saying, "You must wear a helmet when you ride your bike." It is a hard rule everyone has to obey. **Examples of directive controls include government compliance regulations, posted safety procedures, and signed acceptable use agreements.** When a worker signs a paper promising never to plug a random USB drive into their work computer, that is a directive control.

### Deterrent Controls
**Deterrent controls are designed to discourage attackers from attempting to compromise a system.** A deterrent doesn't actually fight the bad guy; instead, **a deterrent control relies on the psychological effect of potential consequences to prevent a malicious action.** 

It plays mind games! It convinces the attacker that messing with you is a bad idea. **Examples of deterrent controls include warning signs, highly visible security cameras, and bright exterior lighting.** If a thief sees a "Beware of Dog" sign, they might get scared and decide to walk away, even if the dog is actually asleep.

### Preventive Controls
If scaring them away doesn't work, we have to stop them for real. **Preventive controls are designed to stop a security incident from occurring in the first place.** These don't play mind games; they act like solid brick walls.

**Examples of preventive controls include locked server room doors, biometric authentication systems (like fingerprint scanners), and firewall rules.** If your firewall is set to block certain bad internet traffic, it will crush that traffic instantly, no matter what the hacker tries to do.

### Detective Controls
No wall is perfect. If someone sneaks over it, you need to know immediately! **Detective controls are designed to identify and record security incidents after the incidents have occurred.** 

It is very important to know that **detective controls do not actively stop an ongoing cyber attack.** They are just the alarm bells or the security cameras recording the event. **Examples of detective controls include security event logs, intrusion detection systems, and motion sensors.** If someone sneaks into a computer network at 3:00 AM, the detective control leaves a trail of clues so the security team can investigate later.

### Corrective Controls
Once the alarm goes off and the bad guys are kicked out, you have to clean up the mess. **Corrective controls are designed to fix or mitigate the damage caused by a successful security incident.** 

Think of these like healing potions in a video game. **A corrective control aims to restore a compromised system back to a normal state of operation.** **Examples of corrective controls include data backups, operating system patching, and fire suppression systems (like water sprinklers).** If a virus deletes your files, you use your backup to put the files back exactly the way they were.

### Compensating Controls
Sometimes, the absolute best security fix is just impossible to use. **Compensating controls are alternative security measures implemented when a primary security control is financially or technically unfeasible.** Unfeasible just means it won't work or costs too much. 

For example, imagine a hospital has a giant MRI machine (a machine that takes pictures of your bones) connected to a super old Windows computer. The primary fix would be to install a software patch, but doing so might permanently break the MRI machine! 

Is it financially unfeasible to just buy a brand new machine? Let's do the math:
1. The hospital checks its piggy bank and finds their technology budget is \$50,000.
2. The hospital checks the price tag on a brand new MRI machine: \$2,000,000.
3. We subtract the budget from the cost: \$2,000,000 - \$50,000 = \$1,950,000.
4. Because the hospital is short by \$1,950,000, replacing the machine is impossible!

They can't shut down the hospital, but they also can't leave a weak computer exposed. **Compensating controls do not completely eliminate an underlying vulnerability.** The old computer is still weak. However, **compensating controls reduce the risk associated with a known vulnerability to a level deemed acceptable by management.** 

**An example of a compensating control is network segmentation used to isolate an unsupported legacy operating system from the internet.** They put the old MRI computer in its own digital "timeout" corner where it can't touch the internet at all. It's not a perfect fix, but it keeps the machine safe!

---

## The Intersection: Controls in the Matrix

To really understand this like a pro, you have to realize that these tools can do double duty. **A single security measure can belong to multiple control categories and control types simultaneously.** 

Let's look at three examples of how the "How" and the "What" combine:

1. **The Human Security Guard**
   * *Category:* Operational (It relies on a human doing a daily job).
   * *Type:* Preventive (The guard will physically block a bad guy from entering).
   * **Result: A human security guard is classified as both an operational control and a preventive control.**

2. **The Obvious Camera**
   * *Category:* Physical (It is a real, touchable object bolted to a wall).
   * *Type:* Deterrent (Because everyone can see it, it scares bad guys away mentally).
   * **Result: A highly visible security camera functions as both a physical control and a deterrent control.**

3. **The Automated Defender**
   * *Category:* Technical (It uses computer code and automation to protect things).
   * *Type:* Preventive (Instead of just sounding an alarm, an Intrusion Prevention System actively deletes the bad hacker traffic).
   * **Result: An intrusion prevention system functions as both a technical control and a preventive control.**

### Summary Matrix

| Security Control | Category (The "How") | Type (The "What") |
| :--- | :--- | :--- |
| **Acceptable Use Policy** | Managerial | Directive |
| **Firewall Rule** | Technical | Preventive |
| **Security Guard** | Operational | Preventive |
| **CCTV Camera (Visible)** | Physical | Deterrent |
| **Data Backup** | Technical / Operational | Corrective |
| **Network Segmentation (for Legacy OS)** | Technical | Compensating |

Once you understand how these tools overlap, you become like a master architect. You can look at a whole network, figure out exactly what kind of physical, logical, or human defenses are missing, and pick the perfect tool for the job!