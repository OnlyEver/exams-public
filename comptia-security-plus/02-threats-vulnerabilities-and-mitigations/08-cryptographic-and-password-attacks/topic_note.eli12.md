Secret codes (cryptography) are like the ultimate cheat-proof rules in a video game. They protect your data as it travels across the internet. But hackers don't usually try to break the super-hard math. Instead, they look for glitches in the game, old rules that people forgot to turn off, or they just try to guess your password. We're going to look at how these attacks work, from tricking a computer into using weak security to doing super-fast math to break codes.

## The Illusion of Secure Channels: Cryptographic Attacks

When two computers talk to each other, they need to agree on a secret language. Because the internet is a mix of brand-new gaming PCs and really old computers, modern servers try to be polite. They want to use the newest, most secure secret language, but they will switch to older, weaker ones if the other computer says, "I don't understand the new stuff." Hackers use this politeness against them.

### Downgrade Attacks: Weaponizing Backward Compatibility

Imagine you have a super-secure walkie-talkie mode, but your friend only has an old toy walkie-talkie. You switch to the old mode so you can talk. **A downgrade attack forces a system or communication channel to abandon a high-security mode in favor of an older, less secure mode.** 

If a hacker steps into the middle of your connection, they can trick the server. When your computer says, "I can use strong security," the hacker drops those messages. The server thinks you have an old computer and agrees to use an outdated standard. Basically, **downgrade attacks exploit backward compatibility features implemented in networking and cryptographic protocols.** (Backward compatibility just means new stuff is designed to still work with old stuff). 

Why do hackers do this? Because **attackers use downgrade attacks to force targets into using obsolete cryptographic protocols with known vulnerabilities.** This lets them easily read all your secret traffic, like listening in on an unencrypted walkie-talkie channel.

> **Real-World Impact:**
> **POODLE is a historic downgrade attack that forced secure connections to fall back to the vulnerable SSL 3.0 protocol.** SSL 3.0 was a super old set of rules for the internet. By breaking the new connection on purpose, hackers tricked servers into using SSL 3.0, letting them easily steal secret login cookies.

### Hash Collisions and the Birthday Paradox

While encryption hides your data, "hashing" protects it from being messed with. A hash is like a digital fingerprint. If you run a giant video game file through a math formula, it spits out a short string of letters and numbers (the hash). 

But here is a weird problem. The number of files in the world is infinite, but the number of possible hash fingerprints is limited. So, eventually, two completely different files might end up with the exact same fingerprint! **A collision attack occurs when an attacker finds two completely different pieces of plaintext data that produce the exact same hash value.**

Why is this bad? Computers check these hashes to make sure a file is safe. **A successful collision attack allows an adversary to substitute a malicious file or certificate for a legitimate one without altering the digital signature.** It’s like pasting your photo onto someone else’s ID card. Because the computer sees a matching hash, it blindly trusts the bad file! Because computers got so fast at finding these matches, **the MD5 and SHA-1 hashing algorithms are deprecated because they are computationally vulnerable to collision attacks.** (Deprecated means we threw them in the trash).

Hackers don't just guess randomly to find these matches. They use a math trick. **A birthday attack is a statistical method used to find hash collisions more quickly than testing every possible combination.**

Let's look at the math for the "birthday paradox" step-by-step using a room of people:
1. Imagine you want to find someone who shares *your* exact birthday (for example, March 14).
2. Because there are 365 days in a year, you have to ask a lot of people. You need 253 people in the room to have a 50/100 (which is 50%) chance of finding your exact birthday twin.
3. But what if you just want to find *any* two people in the room who share a birthday with each other?
4. You compare person 1 to person 2, person 1 to person 3, and person 2 to person 3, and so on. 
5. Because the number of comparisons grows super fast, you only need 23 people in a room to have a 50/100 chance that two of them share a birthday!

**The birthday attack relies on the mathematical probability that two random inputs in a given group will produce the same hash output.** It speeds up the hacker's job a ton.

To stop this, we just make the fingerprint longer! **Increasing the bit length of a cryptographic hash function directly increases the computational difficulty of executing a birthday attack.** If we use a 256-bit hash instead of a 128-bit hash, the number of possible fingerprints gets so huge that even supercomputers can't find a match using the birthday math.

## The Human Element: Password Attack Vectors

If secret math is the heavy vault door, passwords are the keys. Hackers know it's silly to try to blow up the vault door if they can just guess your key! Password attacks depend on how and where the hacker guesses: online (live on the internet) or offline (on their own computer).

### The Live Battlefield: Online Attacks

**Online brute force attacks are performed directly against a live system's authentication interface.** This means the hacker is actively sending guesses right to your favorite game's login screen or your school email portal.

**A brute force attack involves systematically submitting all possible character combinations until the correct password or cryptographic key is discovered.** Imagine trying a bike lock by testing 0000, 0001, 0002, and so on, until it pops open.

Sometimes they want to be smarter than starting at AAAA. **A dictionary attack attempts to guess a password using a predefined list of likely words, common phrases, and leaked passwords.** (Like trying "password", "123456", or "baseball").

If you are watching the security logs, you can spot this easily. **Successive failed login attempts targeting a single account from the same IP address strongly indicate an online brute force attack.** 

Because these attacks are loud and obvious, they are easy to stop. **Account lockout policies and rate limiting are primary administrative defenses against online brute force attacks.** If the system locks your account after five bad tries, the hacker's online attack fails instantly.

#### Bypassing Lockouts: Password Spraying and Credential Stuffing

Hackers know about lockouts, so they get sneaky. **Password spraying is an attack technique where an adversary attempts to log in to many different user accounts using a single commonly used password.** (Like trying the password `Pizza2024!` on every single account in the school).

**Password spraying avoids triggering standard account lockout mechanisms by keeping the number of login attempts per account very low.** The hacker only guesses once or twice for each person, so no one gets locked out.

*   **Indicator of Compromise:** **An indicator of a password spraying attack is a large volume of failed authentication events across many different user accounts within a short timeframe.** 
*   **Indicator of Success:** **A sudden spike in successful logins using the exact same weak password across multiple distinct accounts indicates a successful password spraying attack.**

Another trick is recycling old passwords. People are lazy and reuse passwords for everything! **Credential stuffing uses automated scripts to inject stolen username and password pairs from previous data breaches into different website login pages.** If a hacker steals your password from a tiny blog, they will take that exact username and password and stuff it into your Xbox Live or email login to see if it works there too.

| Attack Type | Target Scope | Methodology | Primary Mitigation |
| :--- | :--- | :--- | :--- |
| **Traditional Online Brute Force** | One Account | Many Passwords | Account Lockout |
| **Password Spraying** | Many Accounts | One Password | Strong Password Policies / MFA |
| **Credential Stuffing** | Many Accounts | Known Stolen Pairs | MFA / Breached Credential Blocking |

### The Silent War: Offline Attacks

Sometimes, a hacker breaks into a server, steals the giant file holding everyone's scrambled passwords (hashes), and runs away to their own house. **Offline brute force attacks target stolen password hash files on an attacker's local machine.**

Since they are doing this in their basement, **offline brute force attacks do not interact with the target organization's live authentication system.** Because you aren't guessing on the real website, the website can't stop you. **Offline brute force attacks bypass network-based account lockout mechanisms entirely.** You have unlimited tries!

Also, **offline brute force attacks are significantly faster than online brute force attacks due to the elimination of network latency.** Latency is that annoying lag you get when playing games online. By guessing passwords offline, hackers don't have to wait for the internet to load. They can use powerful graphics cards (GPUs) to guess billions of times a second.

#### The Speed of Memory: Precomputation and Rainbow Tables

Even with fast gaming computers, doing the math to scramble passwords takes time. Hackers fix this by doing the homework ahead of time. **A rainbow table is a massive precomputed database of plaintext passwords and the corresponding hash values of those passwords.**

Instead of scrambling a guess and seeing if it matches the stolen file, they just look up the stolen scrambled hash in their giant cheat-sheet book. **Rainbow tables significantly reduce the computational time required to crack password hashes compared to a traditional offline brute force attack.**

#### The Antidote: Cryptographic Salts

If a rainbow table works like a giant cheat-sheet, how do we ruin the cheat-sheet? We add random junk to the password!

**A cryptographic salt is a random data value appended to a plaintext password before the hashing algorithm is applied.**

Let's look at how adding salt changes the math, step-by-step:
1. Imagine your password is the word "dog".
2. Without salt, the scrambled hash for "dog" might always equal a math result like 5555.
3. The hacker looks up 5555 in their rainbow table and sees it means "dog". They win!
4. Now, let's use a salt! The computer creates a random secret string, like "X9yZ".
5. The computer glues the salt to your password: "dogX9yZ".
6. The computer runs the math on "dogX9yZ", which gives a totally new math result, like 9999.

**Applying a unique cryptographic salt to every user password renders precomputed rainbow tables completely ineffective.** Even if two friends pick the exact same password, the computer gives them totally different random salts. Their final hashes will look completely different! To cheat a salted file, the hacker would need to build a brand new, giant cheat-sheet for every single person's unique salt, which takes too much computer space to actually do.