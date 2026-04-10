Imagine you are playing a video game. Your character will do exactly what you press on the controller. If you tell the character to jump off a cliff, it will jump off the cliff. It does not stop to ask, "Is this a good idea?"

Computers are the exact same way. They are incredibly fast and powerful, but they do exactly what they are told. When we study computer security, we are not looking at broken computers. We are looking at computers that are perfectly following bad instructions! The weaknesses we are going to learn about are moments where a bad guy (an attacker) uses a computer's rule-following nature against it to do sneaky things.

## The Physics of Software: Memory and Logic Flaws

To understand how hackers trick computers, you first need to know how computers store information. Programs use special boxes in their brain—called memory or buffers—to hold your inputs, like the name of your game character.

### Buffer Overflows and Integer Overflows
Think of a memory buffer like a small cup holding water. A buffer overflow occurs when a program writes more data to a memory block than the memory block is allocated to hold. It is like pouring a whole pitcher of water into a tiny cup. The extra water spills out! Inside a computer, writing data past the allocated bounds of a buffer can overwrite adjacent memory locations. 

Why is this bad? Because the memory right next door might hold the actual instructions for the game. Overwriting adjacent memory via a buffer overflow can alter the execution flow of a program. This means the computer might start following new rules! Attackers exploit buffer overflows to execute arbitrary malicious code on a target system. Even if their trick does not work perfectly, it still causes chaos. The memory corruption resulting from buffer overflows can cause system crashes and denial of service, which simply means the computer freezes or breaks and nobody can use it.

Sometimes, a buffer overflow happens because of a math mistake. An integer overflow occurs when an arithmetic operation produces a value larger than the maximum representable value of the data type. 

Let's look at a math example. Imagine a video game where the highest possible coin score a computer box can hold is 255. What happens if you get more coins?
Step 1: You have a starting score of 250 coins.
Step 2: You pick up a treasure chest worth 10 coins.
Step 3: The game calculates your new score: 250 + 10 = 260.
Step 4: Because 260 is larger than the maximum of 255, the game's math breaks. The number rolls over like a broken car odometer and goes back to a tiny number, like 4.

If the computer uses that broken math to build a memory box, it might make a tiny box for a giant file. Because of this, integer overflows can lead to memory corruption and subsequent buffer overflow vulnerabilities.

### Null Pointer Dereferences
Programs use "pointers" to find things in memory. Think of a pointer like a treasure map that tells the computer where to look. But what if the map is blank? A null pointer dereference occurs when an application attempts to access memory through a pointer that has a null value. A "null value" just means zero, or nothing. When the computer tries to read a map that points to nowhere, it gets totally confused. Because of this confusion, null pointer dereferences typically cause the application to crash.

## Hijacking the Process: Execution and Timing

When a computer runs a program, it is called a "process." Hackers love to mess with these running processes because it leaves fewer clues behind.

### Memory Injection
Instead of downloading a bad file to your hard drive, hackers can put bad instructions directly into a running game. Memory injection involves inserting malicious code into the memory space of a running process. Because the bad code is hiding in the memory and not saved as a normal file, attackers use memory injection techniques to evade file-based antivirus detection. 

Once it is inside, the bad code acts like it belongs there. Memory injection allows malicious code to execute with the security privileges of the compromised process. If the game has permission to use your microphone, the injected code now has that permission too! A very common way to do this is called Dynamic Link Library (DLL) injection. Dynamic Link Library (DLL) injection is a technique where a malicious DLL is forced to load into the address space of a target process. It is like slipping a fake rulebook into a board game box so the players follow the hacker's rules.

### Race Conditions and TOCTOU
Computers do millions of things in a single second. Sometimes, bad guys try to beat the clock. A race condition occurs when the behavior of a system depends on the uncontrolled sequence or timing of events. Imagine two players grabbing for the same power-up at the exact same millisecond—the game might glitch! Attackers exploit race conditions to escalate privileges or access unauthorized files.

> Time-of-check to time-of-use (TOCTOU) is a specific type of race condition vulnerability. 

A TOCTOU vulnerability happens when a system verifies an access condition prior to executing an action. Let's say your mom checks if your room is clean before giving you your \$10 allowance. She peeks in, sees it is clean, and turns around to get her wallet. In a TOCTOU exploit, an attacker alters the validated condition between the validation step and the execution step. In the few seconds her back is turned, you dump all your toys back onto the floor, but still get the money! You exploited the gap between the "check" and the "use."

## Operating System Vulnerabilities & Authentication

The Operating System (like Windows or Mac) is the boss of the whole computer. 

At the heart of the operating system is the kernel. Operating system kernel vulnerabilities are highly critical because the kernel has unrestricted access to all system hardware. If a hacker controls the kernel, they control the screen, the keyboard, the camera—everything. This is why you must update your computer! Unpatched operating systems expose systems to exploitation via publicly known vulnerabilities. 

Even if your computer is updated, bad settings can cause trouble. Misconfigured operating system permissions can allow unauthorized users to modify sensitive system configuration files. When hackers do this, they are usually trying to level up their account. Privilege escalation involves an attacker gaining higher-level access rights than initially authorized. 
*   Vertical privilege escalation occurs when a lower-privileged user gains access to functions reserved for administrators. (Like a regular player becoming the server owner).
*   Horizontal privilege escalation occurs when a user accesses the data of another user possessing the same privilege level. (Like you reading your friend's private messages without permission).

### Pass-the-Hash
Computers usually do not save your actual password. Instead, they scramble your password into a long, secret code called a "hash." Pass-the-hash is an authentication attack where an attacker extracts a stored password hash and uses the hash to authenticate. Think of it like stealing someone's VIP wristband for a concert. The security guard doesn't care what your name is; they just check the wristband. Because of this, pass-the-hash attacks bypass the need for an attacker to know the plaintext password.

## Web Application Vulnerabilities: Trusting the Untrustworthy

Websites let anyone on the internet type things into them. This makes them a huge target.

### SQL Injection (SQLi)
Websites use databases, which are like giant digital filing cabinets. SQL injection (SQLi) occurs when an application improperly sanitizes user input before sending the input to a database. Instead of typing a normal name like "John," the hacker types in actual database commands. 

Attackers use SQL injection to alter the logic of database queries. They trick the filing cabinet into doing things it shouldn't. A successful SQL injection attack allows unauthorized viewing of database contents, letting hackers see everyone's private information. Even worse, SQL injection vulnerabilities allow attackers to modify or delete database records. They could erase their debt or change their grades!

**Defense:** To stop this, programmers use parameterized queries. Parameterized queries prevent SQL injection by treating user input strictly as data rather than executable code. It makes the computer say, "I am just going to save exactly what you typed as a name, and I absolutely refuse to run it as an instruction."

### Cross-Site Scripting (XSS)
While SQL attacks the website's filing cabinet, XSS attacks the other people using the website. Cross-Site Scripting (XSS) occurs when an application includes untrusted data in a web page without proper validation or escaping. XSS attacks execute malicious client-side scripts within the web browser of the victim. Because the bad code runs right in your browser, attackers use XSS to steal session cookies and hijack user sessions. (A session cookie is like a temporary ID card that keeps you logged in).

There are three main types:
1.  **Reflected XSS:** Involves the immediate echoing of malicious input back to the browser within the web application response. This usually happens if you click a poisoned link.
2.  **Stored XSS:** Occurs when a malicious script is permanently saved on the target web server. Imagine a hacker leaving a poisoned comment on a video, and anyone who reads the comments gets hacked.
3.  **Document Object Model (DOM) based XSS:** Occurs when the vulnerability exists entirely within the client-side code. This means the bad stuff happens entirely inside your own browser window without the main web server ever knowing!

**Defense:** The best shield against this is called output encoding. Output encoding converts untrusted input into a safe form to prevent browsers from executing the input as code. It turns dangerous computer symbols into harmless text. Because it disarms the bad code, output encoding is a primary defensive measure against Cross-Site Scripting (XSS) attacks.

### Forgery Attacks: CSRF vs. SSRF

These attacks are all about tricking a computer into trusting the wrong thing:

| Attack Type | Mechanism | Exploit Target |
| :--- | :--- | :--- |
| **Cross-Site Request Forgery (CSRF)** | Forces a logged-in user to send a forged HTTP request to a vulnerable web application. | CSRF attacks exploit the trust a web application has in the authenticated browser of a user. |
| **Server-Side Request Forgery (SSRF)** | Occurs when a web application fetches a remote resource based on attacker-supplied URLs. | SSRF vulnerabilities allow an attacker to interact with internal network resources normally protected by a firewall. |

*In short: CSRF tricks your browser into buying a game item without you knowing it. SSRF tricks a website into opening a locked door from the inside!*

### Directory Traversal
Websites are only supposed to show you files from a specific public folder. Directory traversal vulnerabilities allow an attacker to read arbitrary files on the server running an application. It lets them snoop into the computer's secret system folders. Directory traversal attacks commonly use dot-dot-slash sequences to navigate outside the intended web document root directory. It is like typing `../` over and over to hit the "up" button until you escape the website's folder and find the computer's password files.

## The Broader Landscape: OWASP Design Failures

A group called OWASP keeps a list of the biggest mistakes programmers make. Here are some of them:

*   **Broken Access Control:** This is an OWASP vulnerability category where users can act outside of intended permissions. It is like sneaking into the VIP room when you only have a general admission ticket.
*   **Cryptographic Failures:** These occur when sensitive application data is transmitted or stored without proper encryption. It is like sending your friend a secret message written on a plain postcard that anyone can read.
*   **Security Misconfiguration:** This occurs when security settings are poorly defined or left at default vulnerable values. If you leave your home Wi-Fi password as "password123," that is a misconfiguration!
*   **Software and Data Integrity Failures:** These relate to application infrastructure that does not protect against code modification. For example, if a game downloads an update, but doesn't check to make sure a hacker didn't swap the file, that is an integrity failure.

### The Ultimate Baseline Defense: Input Validation
If there is one golden rule, it is to never trust what people type! Input validation checks whether provided data meets specific criteria before processing the data. If a form asks for your age, input validation makes sure you type a number and not a bunch of weird symbols. 

Using strict input validation on the server side mitigates many injection-based application vulnerabilities. It catches the bad instructions at the front door, keeping your computer safe and running perfectly!