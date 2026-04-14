A computer that has been hacked isn't totally silent. It actually leaves behind a bunch of tiny clues! Think of a hacked computer like a muddy crime scene. When a "bad guy" (a hacker or adversary) breaks into a system, they have to sneak around, steal information, and try not to get caught. Every time they do something, they leave a messy footprint behind.

To find these bad guys, we can't just rely on regular virus scanners. We have to know exactly how a healthy, normal computer acts. If we know the normal rules of the computer—like what programs belong where, and how normal people type—we can spot the tiny, weird things that mean an attack is happening!

## The Anatomy of Host-Based Indicators

A running computer system is super strict, almost like a school where everyone has an exact schedule. Every program running on your computer has a specific "parent" program that started it, a specific folder it belongs in, and specific amounts of memory it’s allowed to use. When malware (bad software) runs, it breaks these rules. 

### Process Lineage and Masquerading

Computers keep track of "families" of programs. When you click your internet browser, your computer's main desktop screen (the parent) opens your browser (the child). We call this process lineage. **Abnormal parent-child process relationships serve as strong indicators of operating system host compromise.** If your calculator suddenly opens up a secret web browser, something is super wrong!

Let's look at a super important built-in Windows program called `svchost.exe` (Service Host). 
*   **The Parent:** **The legitimate Windows process `svchost.exe` always executes as a child of the `services.exe` process.** If you ever see `svchost.exe` being started by a video game or Microsoft Word, the computer has been hacked.
*   **The Path:** Programs belong in specific folders. **Legitimate `svchost.exe` processes only execute from the `System32` or `SysWOW64` operating system directories.** If you find it running out of your "Downloads" folder, it is a fake virus in disguise.

Hackers use a sneaky trick to hide: **Process masquerading involves renaming a malicious executable to match a legitimate operating system process name.** This is like a thief wearing a police uniform so nobody questions what they are doing! 

Also, watch out for how much energy a program uses. **Unusually high resource utilization by unfamiliar host processes frequently indicates unauthorized cryptojacking activity.** If a fake program is suddenly making your computer run super hot and slow, the hacker is probably using your computer's power to mine digital coins for themselves!

### Memory Exploitation and Credential Theft

Once a hacker gets into a computer, they want to steal passwords. 

In Windows, a special program helps check your passwords. Think of it like the school principal's locked safe. **Credential dumping attacks frequently target the Local Security Authority Subsystem Service (`lsass.exe`) process memory.** Because `lsass.exe` handles active users, its memory holds passwords. 

> **The Analyst's Toolkit:** **Mimikatz is an open-source post-exploitation tool primarily used for credential extraction from the `lsass.exe` process.** Think of Mimikatz as the bad guy's digital crowbar to pop open that safe!

To sneak past virus scanners, modern hackers sometimes don't even save a file to your hard drive. **Fileless malware leverages legitimate system tools like PowerShell to execute malicious code directly in memory.** This is like an intruder memorizing a map in their head instead of carrying a paper map that a security guard could find. 

To catch this, we have to watch the computer's built-in tools. **Unexpected outbound network connections originating from scripting engines indicate potential command and control communication.** If your computer’s built-in coding tools randomly try to talk to a stranger's computer across the world at 2:00 AM, a hacker is controlling it remotely.

### The Mechanics of Persistence 

If a hacker breaks into your computer, but then you restart it and they get kicked out, they lose. They want to stay hidden even after you turn the computer off and on again. We call this "persistence."

The Windows Registry is like the computer's giant master rulebook. **Adversaries frequently use Windows Registry run keys to achieve malicious payload persistence across system reboots.** This is like a hacker sticking a sticky note on your computer's alarm clock that tells the virus to wake up when you turn the computer on.

**The Windows Registry path `HKEY_LOCAL_MACHINE\Software\Microsoft\Windows\CurrentVersion\Run` is a primary location monitored for malware persistence.** Any program listed right there will automatically run the moment the computer turns on!

Hackers also mess with the rulebook to turn off your alarms. **Adversaries modify Windows Registry keys to intentionally disable native security solutions like Windows Defender.** Also, **unexpected changes to file extension associations in the Windows Registry indicate potential malware persistence techniques.** This means the hacker rewrites the rules so that when you try to open a boring text document, it secretly opens their virus instead!

Some hackers prefer using built-in task schedulers. **Scheduled tasks created by unknown user accounts indicate potential host-level persistence mechanisms.** Setting a hidden digital alarm to go off later is a big clue. **The `schtasks` command-line utility is frequently abused by threat actors to schedule malicious task execution on Windows systems.**

### Subverting Ground Truth: The Hosts File

When your computer wants to visit a website like Google, it normally asks the internet for directions. But first, it checks its own secret, local address book called the "hosts file."

**The legitimate Windows hosts file is located at the absolute path `%SystemRoot%\System32\drivers\etc\hosts`.** 

**Unexpected modifications to the local hosts file indicate an attempt to redirect system network traffic to malicious infrastructure.** Imagine changing "Mom" in your phone contacts to a scammer's phone number. When you try to call Mom, you get the scammer! The hacker changes this file so when your computer tries to download official updates, it downloads a virus instead.

---

## Application-Based Anomalies

Applications are things like video games, web browsers, or school grading websites. When hackers attack these, they leave clues in the application's "logs" (a diary of everything the app did).

### Authentication and Access Logs

The most obvious way a hacker tries to break in is just guessing your password over and over. **Repeated failed authentication attempts in application logs indicate a potential password spraying or brute-force attack.** 

Let's look at the math to see how fast a brute-force attack can be. Imagine a bad guy wrote a program to guess your password for you:
1.  Assume a simple lock has exactly 6,000 possible password combinations.
2.  The hacker's computer guesses 200 passwords every single second.
3.  We divide the total combinations by the guesses per second (`6000 / 200 = 30`). It only takes 30 seconds for the hacker to guess your password!

Once a hacker gets in, they try to give themselves super-powers. **Application logs showing unauthorized privilege escalation indicate a successful bypass of application access controls.** If a normal player in a game suddenly has the admin power to ban other players, the game's security is broken.

### Memory Exploitation in Applications

When software is coded poorly, it might not check how big a file is before opening it. 

**Application crash logs containing unexpected buffer overflows often indicate an active memory exploitation attempt.** Imagine pouring a whole gallon of milk into a tiny teacup. The cup overflows and milk spills everywhere, ruining the table! A buffer overflow is when a hacker stuffs too much information into a small space, crashing the app so they can take control of it.

### Web Application Vulnerabilities

Web application logs record everything people type into a website. By looking at weird things typed into websites, we can spot attacks!

| Vulnerability Type | Log Indicator | Explanation |
| :--- | :--- | :--- |
| **SQL Injection (SQLi)** | **Web application logs containing excessive single quotes indicate potential SQL injection attempts.** | The single quote character (`'`) is like a secret code used to confuse a website's database. |
| **SQLi (Definitive)** | **The presence of `UNION SELECT` statements in web application logs is a definitive indicator of SQL injection activity.** | Typing `UNION SELECT` tricks the website into coughing up all its secret hidden data. |
| **Cross-Site Scripting (XSS)** | **Cross-Site Scripting (XSS) attacks generate application logs containing unexpected HTML script tags.** | This is when an attacker types sneaky hidden code (like HTML script tags) into a public comment section to prank anyone who reads it. |
| **Directory Traversal** | **Directory traversal attacks generate application access logs containing repeated dot-dot-slash character sequences.** | **Directory traversal attacks generate application access logs containing repeated dot-dot-slash character sequences.** A hacker types `../../../` to sneak out of their allowed folder and poke around in the computer's top-secret files. |

---

## The Human Attack Surface

Sometimes, the easiest way to break into a computer isn't hacking the computer at all—it's tricking the person using it! **Social engineering attacks exploit human psychology rather than technical vulnerabilities to breach security boundaries.** Why spend weeks trying to hack a tough locked door when you can just politely ask someone inside to open it for you?

### Phishing Methodologies

Email is a hacker's favorite tool. **Phishing campaigns rely on spoofed sender addresses to deceive victims into trusting malicious communications.** Spoofing is like putting a fake return address on an envelope so you think a letter came from your principal instead of a stranger. 

While normal phishing is sent to millions of people, smart hackers take their time. **Spear-phishing attacks utilize customized open-source intelligence to target specific individuals within an organization.** This means the hacker looks up your favorite sports team or your dog's name online, and puts that in the email so you really believe they are your friend!

Hackers rarely just attach a virus that looks like a virus. **Malicious Office document macros serve as common payload delivery mechanisms in initial access phishing vectors.** This means the hacker hides their virus inside a totally normal-looking homework assignment or Excel spreadsheet. 

A super specific type of scam is all about stealing money. **Business Email Compromise (BEC) attacks focus on impersonating executives to authorize fraudulent financial transactions.** A BEC attack doesn't even need a virus! It's just a hacker pretending to be the boss of a company, sending an email saying, "I need you to wire \$5,000 to this new bank account right now!" 

### Telephony and Authentication Bypass

Hackers don't just use email. They will text and call you, too!

*   **Smishing:** **Smishing attacks utilize SMS text messaging protocols to deliver social engineering lures to mobile devices.** These are those fake text messages that say, "Your package couldn't be delivered, click here to fix it!" 
*   **Vishing:** **Vishing attacks employ Voice over IP (VoIP) or traditional telephone calls to manipulate victims into divulging sensitive data.** This is when a scammer calls you on the phone pretending to be from tech support and asks for your password.

Even if you have really good security, like an app on your phone where you have to click "Approve" to log in, hackers have a trick for that. **Multi-factor authentication (MFA) fatigue attacks involve flooding a user with approval requests to bypass authentication controls.** The hacker tries to log in 50 times in a row while you are trying to sleep. Your phone buzzes and buzzes and buzzes! Finally, you get so annoyed you just tap "Approve" to make it stop, and boom—the hacker is in!

## Conclusion

As a security analyst, your job is to play detective. The weird computer rules, broken files, weird web typing, and fake emails we talked about aren't just make-believe. They are the exact footprints you will look for when stopping real bad guys. By understanding how hackers change a computer, mess with apps, and trick humans, you can catch them before they win!