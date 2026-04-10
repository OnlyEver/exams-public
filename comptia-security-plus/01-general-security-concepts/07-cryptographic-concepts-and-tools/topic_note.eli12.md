Imagine a hard drive sitting on your desk. Physically, it looks like a thick metal notebook. But this notebook doesn't care if the information inside it is a boring grocery list or a top-secret video game code. If someone steals that physical hard drive, they can read everything on it. That is, unless we use secret math codes to scramble the data so that even if they have the drive, they can't read the words. 

This idea is called cryptography. It means we use special math rules and computer chips to lock our files. To keep computers safe, we need to know exactly how and where to put these locks!

## The Geometry of Encryption at Rest

When a computer expert wants to lock up data, the first big question is: *How much of the computer should we lock at once?* We can lock the whole computer, just one section, or just a few specific files.

### Full-Disk Encryption (FDE)

Think of a hard drive like a giant backpack. **Full-disk encryption protects data at rest by encrypting every bit of data on a storage medium.** That means it locks the entire backpack and everything inside it into one big scrambled mess. **Full-disk encryption prevents unauthorized data access if a physical device is stolen.** If a bad guy steals your laptop, they can't get anything out of it because they don't have the key.

Because it covers everything, **full-disk encryption encrypts the operating system files** (the main files that make the computer run). It also covers the secret "scratchpad" areas of your computer: **full-disk encryption encrypts temporary files and swap spaces on the storage drive.**

Because everything is locked tight, **a system utilizing full-disk encryption requires user authentication before the operating system boots.** You literally have to type in a password before the computer can even finish turning on!

> **Real-World Implementation:** 
> If you use a Windows PC, **BitLocker is a Microsoft Windows tool used to provide full-disk encryption.** If you use an Apple Mac, **FileVault is an Apple macOS tool used to provide full-disk encryption.**

### Partition Encryption

Sometimes, locking the whole backpack is too much work. Instead, you might just want a special locked pocket inside your backpack. **Partition encryption applies cryptographic protection to a specific logical division of a hard drive.** 

You chop the hard drive into separate areas. **Partition encryption allows an operating system to reside on an unencrypted volume while sensitive data resides on a separate encrypted volume.** This means the basic computer can start up totally normal and unlocked, but your super-secret diary files stay locked in their own special area until you put in a password.

### File-Level Encryption

What if you just want to lock one single piece of paper? **File-level encryption applies cryptographic protection to individual files or folders.** 

This gives you a lot of choices. **File-level encryption allows an administrator to apply different encryption keys to different files on the same system.** For example, you can have your key for your files, and your brother can have a totally different key for his files, all on the same computer! Also, **file-level encryption operates independently of the underlying disk architecture.** If you copy your locked file onto a USB thumb drive to take to a friend's house, the file stays locked.

But watch out! When you open a locked file to read it, the computer sometimes makes a quick, temporary copy of the file to work with. **File-level encryption does not automatically encrypt temporary files created by applications.** If the computer crashes, that temporary copy might be left behind completely unlocked.

> **Real-World Implementation:**
> **The Encrypting File System is a file-level encryption feature available in Microsoft Windows.** 

### Encryption Scope Comparison

| Feature | Full-Disk Encryption (FDE) | Partition Encryption | File-Level Encryption |
| :--- | :--- | :--- | :--- |
| **What it Locks** | Every bit on the physical drive. | Specific sections of the drive. | Individual files/directories. |
| **Computer Brain (OS) Locked?** | Encrypts OS files automatically. | OS can remain unlocked. | OS remains unlocked. |
| **Scratchpad/Temp Files** | Completely protected. | Protected only if temp folder is in the locked section. | **Not automatically protected.** |
| **Who gets the Keys?**| One master key for the whole drive. | One key for that specific section. | Special keys for each user/file. |

---

## Anchoring Trust in Silicon: Hardware Cryptographic Tools

If your computer uses a secret digital key to lock your hard drive, where does it hide the key while the computer is turned off? It's like writing the combination to a safe on a sticky note and putting it on the safe itself! To fix this, we put the keys inside special computer chips.

### The Trusted Platform Module (TPM)

Look closely at the main board inside a good computer, and you'll find a tiny, super-secure guard. **A Trusted Platform Module is a hardware chip embedded directly on a computer motherboard.** 

This chip is awesome at math. **A Trusted Platform Module provides secure generation of cryptographic keys**, meaning it can roll digital dice to create passwords that are impossible to guess. Then, **a Trusted Platform Module provides secure hardware storage of cryptographic keys.** It acts like a tiny vault, hiding the keys so no virus can sneak in and steal them.

When you turn on the power, it goes to work. **A Trusted Platform Module verifies hardware and software integrity during the computer boot sequence.** It checks to make sure nobody tampered with your computer while you were asleep. Because this chip is so trustworthy, **full-disk encryption systems frequently rely on a Trusted Platform Module to securely store the volume master key.** 

### The Hardware Security Module (HSM)

If a TPM is a tiny vault for your home computer, an HSM is a massive bank vault for giant companies protecting \$5,000,000 worth of data. **A Hardware Security Module is a dedicated physical device used to safeguard digital keys.** 

Big companies have to encrypt thousands of things every second. **A Hardware Security Module offloads cryptographic processing from a host system to improve overall system performance.** It does the heavy math so the main computer doesn't get slowed down.

**Large enterprise environments use Hardware Security Modules to securely manage Public Key Infrastructure root keys.** These "root keys" are the master keys for the whole company, so they are incredibly important. Because they are so important, **Hardware Security Modules are typically deployed as external network appliances or internal PCIe expansion cards** (meaning they are heavy-duty boxes you plug in, or big circuit boards you snap inside a server).

These boxes are built like tanks. **Hardware Security Modules provide tamper-evident physical enclosures for cryptographic keys**, which means if someone tries to break into it, it leaves a big physical mark so you know you were attacked. Even cooler, **Hardware Security Modules provide tamper-resistant physical enclosures designed to erase keys if physical access is attempted.** If a bad guy tries to pry it open, the machine instantly deletes all the keys to stop the thief from getting them!

---

## The Illusions of Security: Obfuscation and Steganography

Sometimes people try to hide things without using real math. **Obfuscation is the process of intentionally making code or data difficult for humans and analysis tools to understand.** It's like writing a note backwards or in Pig Latin. 

But here is the catch: **obfuscation does not provide true cryptographic confidentiality.** Because it isn't locked with a real math key, anyone with enough patience can eventually read it. 

Still, people use it for a few reasons:
1. **Software developers use obfuscation to protect intellectual property from reverse engineering attempts.** They scramble their video game code so copycats can't easily figure out how they built the game.
2. Bad guys use it too. **Malware authors use obfuscation techniques to evade detection by signature-based antivirus software.** They scramble their computer viruses so your antivirus program thinks it's just random noise instead of a dangerous file.

One really sneaky trick is steganography. **Steganography is a form of obfuscation that hides data within another file format.** Imagine hiding a secret text message inside a digital picture of a cat! The picture looks totally normal, but the hidden data is tucked inside.

---

## The One-Way Streets: Hashing Algorithms

Encryption is a two-way street: you lock a file, and later you unlock it. But sometimes we want a one-way street!

**Hashing is a one-way mathematical function that converts input data of any size into a fixed-size output string.** Whether you put in a single letter or a massive 50-gigabyte video game, a hash function scrambles it into a code of the exact same length. 

Here is a really simple step-by-step math example to show how a hash function scrambles something in one direction. Let's pretend our "hash function" converts the word "CAT" into a final number.

1. First, we match each letter to a number in the alphabet (A=1, B=2, C=3, ..., T=20). So, C=3, A=1, and T=20.
2. Next, we add all those numbers together: 3 + 1 + 20 = 24.
3. Finally, we multiply that answer by 5 to get our final hash: 24 * 5 = 120.

Our final output is 120! If you hand someone the number 120, they can't mathematically run the steps backwards to know for sure that you started with the word "CAT". It's totally one-way!

Because it's a one-way street, **hashing provides a cryptographic method to verify data integrity.** If a single pixel in a picture changes, the hash output changes completely. Because of this, **a digital signature relies on hashing to prove that a message has not been altered in transit.**

### Collisions and Vulnerabilities

For hashing to work properly, **a secure cryptographic hash function must produce a unique output for every unique input.** Every single file needs its own totally unique hash output. 

When the math breaks, a disaster happens. **A hash collision occurs when two different inputs produce the exact same hash output.** If a bad guy's virus has the exact same hash as a good computer update, your computer might get confused and let the virus in!

Because computers get faster every year, old math rules break down. **Message Digest 5 is an obsolete hashing algorithm due to mathematically proven collision vulnerabilities.** It's broken, so we never use it anymore. Instead, **Secure Hash Algorithm 256 is an example of a widely used hashing algorithm** because it is incredibly strong.

---

## Seasoning the Math: Defeating Rainbow Tables with Salting

When you create an account for a video game, the game server doesn't actually save your real password. Instead, **authentication systems use hashing to securely store passwords instead of storing plaintext passwords.** They store the hash of your password!

But there is a problem. What if you and your friend both use the password `pizza123`? Your hashes would look exactly the same. Bad guys know this, so they build giant cheat sheets called "rainbow tables" that list common passwords and what their hashes look like. 

To beat the bad guys, we use "salting." **Salting involves appending random data to a plaintext input before applying a hash function.** Before the computer hashes your password, it tosses in a totally random string of letters—like throwing a random handful of sprinkles onto an ice cream cone! 

**Salting ensures that identical plaintext passwords produce entirely different hash outputs.** Even if you and a million other people use `pizza123` as a password, your unique salt makes your hash look totally different from everyone else's. 

Because the bad guy's cheat sheet didn't predict your specific random salt, **salting mitigates the effectiveness of precomputed rainbow table attacks against password databases.** Their cheat sheet becomes completely useless!

For this to work, we have to follow two rules:
1. **A unique cryptographic salt must be generated for each individual user password.** Everyone gets their own random batch of sprinkles.
2. When you log in tomorrow, the computer needs to remember which salt you used. Therefore, **the salt value is typically stored in plaintext alongside the hashed password in an authentication database.** 

Don't worry that the salt isn't kept secret! The salt is just random noise meant to change the math enough to ruin the bad guy's cheat sheet. By mixing secret passwords with random salt and one-way math, we make our computers incredibly strong!