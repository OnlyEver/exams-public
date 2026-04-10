Every time someone sets up a computer, makes a new user account, or plugs in a server, they are trying to teach the computer how to trust people. A computer network is really just electricity moving through wires. It doesn't inherently know the difference between a teacher checking grades and a hacker trying to steal a test. To help computers learn who to trust, cybersecurity uses two big ideas: the CIA triad to set our goals, and the AAA framework to handle users.

## Defining the Target: The CIA Triad

Before we can make a system safe, we need to know what "safe" actually means. **The CIA triad is a foundational information security model consisting of Confidentiality, Integrity, and Availability.** 

This isn't just a good idea someone made up; **the National Institute of Standards and Technology (NIST) formally defines the CIA triad as the core principles of information security.** If any of these three pieces break, the whole system becomes unsafe.

### Confidentiality: Protecting the Secret
**Confidentiality ensures that sensitive information is not disclosed to unauthorized individuals, entities, or processes.** Think of it like keeping your diary locked so your little brother can't read it. We build confidentiality in steps.

First, we set up rules at the door. **Access control lists (ACLs) are mechanisms used to restrict system access and maintain data confidentiality.** An ACL is like a VIP guest list at a birthday party—if your name isn't on the list, you don't get in to see the data.

But what if someone sneaks in anyway? **Encryption algorithms protect data confidentiality by converting plaintext into unreadable ciphertext.** It scrambles the words so they look like nonsense without the secret key. 

To understand how encryption works, here is a simple math example using a +3 shift cipher to encrypt the letter "A":
1. Take your starting letter ("A").
2. Find its number in the alphabet (A = 1).
3. Add the secret shift number of 3 (1 + 3 = 4).
4. Find the new 4th letter in the alphabet (4 = D).
So, the letter "A" safely becomes "D"!

Sometimes, we don't just scramble the message; we hide it completely. **Steganography supports confidentiality by hiding the existence of a message within a seemingly benign file.** This is like writing a secret message in invisible ink on the back of a normal homework assignment.

### Integrity: Defending the Truth
It’s not enough to keep secrets; we also need to make sure nobody messes with our stuff. **Integrity guarantees that information and systems remain accurate, complete, and unaltered by unauthorized parties.** 

Imagine you have \$100 in your bank account. If a hacker changes that number to \$1, that’s an integrity failure! To stop this, we use special math. **Cryptographic hashing algorithms generate fixed-size outputs used to verify data integrity.** Think of a hash like a tamper-evident sticker on a new video game case. If the sticker is ripped, you know someone messed with the disc.

For sending messages, we use a similar trick. **Digital signatures provide integrity verification by allowing a recipient to confirm a message has not been altered in transit.** It's like a wax seal on an envelope—if the seal matches the sender's special stamp, you know the letter wasn't opened and changed by the mail carrier.

### Availability: Maintaining the Lifeline
A super safe computer is totally useless if you can't turn it on when you need it. **Availability ensures that authorized users have timely and reliable access to information and systems when needed.**

Things can break, so we prepare for the worst:

*   **Broken parts:** **Redundant hardware components support system availability by eliminating single points of failure.** If one video game controller breaks, you have a spare one ready to go immediately.
*   **Power outages:** **Uninterruptible Power Supplies (UPS) maintain system availability during short-term electrical power outages.** It's a giant backup battery that keeps the Wi-Fi on just long enough to save your game during a thunderstorm.
*   **Fake traffic:** Sometimes internet bullies try to break websites by sending millions of fake requests at once. **Distributed Denial of Service (DDoS) mitigation services are implemented to protect the availability of internet-facing network resources.** This is like having a bouncer who blocks millions of prank phone calls so real customers can still call in to order pizza.

## The Binding Agent: Non-Repudiation

We also need to make sure nobody can lie about what they did. **Non-repudiation is the security principle ensuring that a subject cannot successfully deny having performed a specific action.** 

If someone deletes a shared Minecraft world, they can't just say, "It wasn't me!" We prove it in two ways:

1.  **Math Proof:** **Asymmetric cryptography enables non-repudiation because only the private key holder can generate a specific digital signature.** If a document is signed with your secret key, the math proves that *you* did it, because nobody else has your key.
2.  **Computer Proof:** **Immutable audit logs support non-repudiation by securely and permanently recording user actions and system events.** It’s like a permanent instant replay in sports that the referee can't erase.

## Controlling the Gates: Identification and the AAA Framework

Now that we know our goals, how do we handle the people using the computer? 

First, a user has to say who they are. **Identification is the initial access phase where a subject claims a specific system identity.** For almost everything we do online, **a username is the most common form of digital identification.**

But claiming to be someone isn't enough. We need rules. 

> **The AAA framework manages access to computer resources, enforces security policies, and audits resource usage.**

AAA stands for Authentication, Authorization, and Accounting. It is the lifecycle of trust.

### 1. Authentication (Proving Who You Are)
**Authentication is the security process of verifying the validity of a claimed identity.** When you type in a username, the computer asks you to prove it. 

We use three main ways to prove who you are:

| Authentication Factor | What It Means | Real-World Example |
| :--- | :--- | :--- |
| **Knowledge-based** | Something you know. | **Passwords and Personal Identification Numbers (PINs) serve as knowledge-based authentication factors.** |
| **Possession-based** | Something you have. | **Smart cards and hardware security keys serve as possession-based authentication factors.** |
| **Inherence-based** | Something you are. | **Biometric scanners evaluating fingerprints or facial features serve as inherence-based authentication factors.** |

### 2. Authorization (Dictating What You Can Do)
Once the computer knows who you are, what are you allowed to do? **Authorization is the process of determining the specific rights, privileges, and access levels granted to a successfully authenticated user.**

To make this easy for large groups, we sort people by their jobs. **Role-Based Access Control (RBAC) is an authorization model that grants permissions based strictly on a user's job function.** If you join the school soccer team, your "role" lets you use the soccer field, but not the band room.

No matter what, we always follow one major rule: **the principle of least privilege is an authorization guideline requiring users to receive only the absolute minimum permissions necessary to perform their duties.** If your chore is just to wash the dishes, you don't need the keys to the family car!

### 3. Accounting (Recording What You Did)
Finally, we need to keep track of everything. **Accounting is the security process of tracking, recording, and logging user activities and resource consumption over time.**

Every time you log in or open a file, the computer writes it down. **Accounting provides the empirical data necessary to perform security audits, forensic investigations, and compliance reporting.** It's like checking the receipts to see exactly how you spent your allowance.

Because computers do millions of things a day, a human can't read all those logs. Instead, **Security Information and Event Management (SIEM) systems aggregate accounting logs from multiple sources for security analysis.** A SIEM is like a super-smart robot that reads the diaries of every computer on the network and immediately alerts you if it spots a hacker.

## The Protocols: Implementing AAA on the Network

To make AAA work across an entire school or company, we use special network rules (called protocols) so we don't have to set up passwords on every single computer one by one.

*   **RADIUS is a standard network protocol that implements the Authentication, Authorization, and Accounting (AAA) framework.** It is used a lot for things like connecting to Wi-Fi. It lumps checking who you are and what you can do into one big step.
*   **TACACS+ is a Cisco-developed network protocol that separates Authentication, Authorization, and Accounting functions into distinct processes.** Because it breaks them apart, it gives administrators extreme control. They can use it to let you log into a router, but block you from running specific commands once you are inside.