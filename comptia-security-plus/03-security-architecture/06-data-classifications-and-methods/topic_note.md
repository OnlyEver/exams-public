In a modern [biochemistry](https://en.wikipedia.org/wiki/Biochemistry) laboratory, researchers do not secure [distilled water](https://en.wikipedia.org/wiki/Distilled_water) with the same [retinal scanners](https://en.wikipedia.org/wiki/Retinal_scan) and heavy vault doors used to protect weaponizable [pathogens](https://en.wikipedia.org/wiki/Pathogen). Applying maximum security to everything paralyzes the organization and exhausts its budget, while applying baseline security to highly volatile assets invites catastrophe. [Information technology](https://en.wikipedia.org/wiki/Information_technology) operates on the exact same premise. As an [IT administrator](https://en.wikipedia.org/wiki/System_administrator) or [security engineer](https://en.wikipedia.org/wiki/Security_engineering), your primary job is not simply to "lock everything down." Your job is to understand the precise nature of the information flowing through your [infrastructure](https://en.wikipedia.org/wiki/IT_infrastructure), measure the [risk](https://en.wikipedia.org/wiki/IT_risk) of its exposure, and apply mathematical and systemic [controls](https://en.wikipedia.org/wiki/Security_controls) calibrated exactly to that risk. 

## The Anatomy of Information: Data Classification

You cannot defend what you do not understand. **[Data classification](https://en.wikipedia.org/wiki/Data_classification) is the process of categorizing information based on its sensitivity and the impact of its unauthorized disclosure.** This process is the foundation of all [cybersecurity](https://en.wikipedia.org/wiki/Computer_security) architecture. By labeling data, you provide [firewalls](https://en.wikipedia.org/wiki/Firewall_%28computing%29), [operating systems](https://en.wikipedia.org/wiki/Operating_system), and human [administrators](https://en.wikipedia.org/wiki/System_administrator) with the instructions they need to treat a marketing flyer differently than an [unencrypted](https://en.wikipedia.org/wiki/Encryption) database of [patient health records](https://en.wikipedia.org/wiki/Electronic_health_record).

How organizations name their classification tiers depends largely on the sector they operate within. 
*   **[Government](https://en.wikipedia.org/wiki/Government) data classification models typically use tiers such as Unclassified, Confidential, Secret, and [Top Secret](https://en.wikipedia.org/wiki/Top_Secret).** 
*   In contrast, **[corporate](https://en.wikipedia.org/wiki/Corporation) data classification models typically use tiers such as Public, Internal, Confidential, and Restricted.**

While the labels change, the fundamental logic remains universal. Let us look closely at how these tiers operate in a standard corporate environment:

### Public Data
**Public data is information intended for open distribution without any [access restrictions](https://en.wikipedia.org/wiki/Access_control).** Think of [press releases](https://en.wikipedia.org/wiki/Press_release), job postings, or product manuals on a company website. Because the data is designed to be seen by the world, **the unauthorized disclosure of public data causes no negative impact to an organization.** 

### Sensitive Data
As we move inward, the stakes change. **Sensitive data is information requiring protection against unauthorized access to prevent harm to individuals or an organization.** This is a broad category, but in your daily operations, **[Personally Identifiable Information](https://en.wikipedia.org/wiki/Personal_data) (PII) is a common categorization of sensitive data.** If an [attacker](https://en.wikipedia.org/wiki/Hacker) accesses names, home addresses, or phone numbers, the harm inflicted falls squarely on the human beings represented by that data.

### Confidential Data
**Confidential data is highly sensitive information restricted to authorized personnel within an organization.** This encompasses [trade secrets](https://en.wikipedia.org/wiki/Trade_secret), [merger](https://en.wikipedia.org/wiki/Mergers_and_acquisitions) strategies, and internal financial forecasts. Because of its nature, the **unauthorized disclosure of confidential data causes significant financial or [reputational damage](https://en.wikipedia.org/wiki/Reputation_management) to an organization.** 

![Trade secrets, such as the proprietary formula for Coca-Cola, are a classic example of highly confidential data that requires strict internal protection to avoid severe competitive damage.](https://wikipedia.org/wiki/Special:Redirect/file/15-09-26-RalfR-WLC-0098_-_Coca-Cola_glass_bottle_(Germany).jpg)

### Restricted Data
At the highest tier of corporate data models, we find information that must be protected at all costs. **Restricted data requires the highest level of [access control](https://en.wikipedia.org/wiki/Access_control) within an organization.** It is not enough to simply be an employee to see this data; **restricted data access is granted strictly based on the [principle of least privilege](https://en.wikipedia.org/wiki/Principle_of_least_privilege) and a direct [need-to-know](https://en.wikipedia.org/wiki/Need_to_know).** An administrator managing the [HR](https://en.wikipedia.org/wiki/Human_resources) [database server](https://en.wikipedia.org/wiki/Database_server), for example, should have [network](https://en.wikipedia.org/wiki/Computer_network) access to the [host machine](https://en.wikipedia.org/wiki/Host_%28network%29) but zero ability to query the restricted salary tables housed within it.

### Critical Data
Beyond just the secrecy of data, we must also consider its [availability](https://en.wikipedia.org/wiki/Information_security). **Critical data is information essential to the ongoing operational survival of an organization.** Consider the real-time [routing tables](https://en.wikipedia.org/wiki/Routing_table) of a major [logistics](https://en.wikipedia.org/wiki/Logistics) company or the transaction [ledgers](https://en.wikipedia.org/wiki/Ledger) of a [bank](https://en.wikipedia.org/wiki/Bank). **The loss or [corruption](https://en.wikipedia.org/wiki/Data_corruption) of critical data immediately halts primary business operations.** If this data goes offline, the business effectively ceases to exist until it is restored.

![A core network routing table. The corruption or loss of this critical data can immediately halt wide-scale operational availability for an organization.](https://wikipedia.org/wiki/Special:Redirect/file/Bgp_rtable.png)

> **Crucial Distinction:** Data can be both Restricted and Critical simultaneously, but they measure different risks. "Restricted" focuses on the impact of unauthorized *disclosure* ([confidentiality](https://en.wikipedia.org/wiki/Confidentiality)), while "Critical" focuses on the impact of *loss or corruption* (availability and [integrity](https://en.wikipedia.org/wiki/Data_integrity)).

## The Three States of Data

Once data is classified, [security engineers](https://en.wikipedia.org/wiki/Security_engineering) must map how it behaves in the physical world. Data constantly shifts between three distinct states, and the methods you use to protect it must shift accordingly.

![The lifecycle of information involves transitioning constantly between being stored at rest, transmitted in transit, and actively processed in use.](https://wikipedia.org/wiki/Special:Redirect/file/3_states_of_data.jpg)

1.  **[Data at rest](https://en.wikipedia.org/wiki/Data_at_rest) refers to inactive data stored physically in [databases](https://en.wikipedia.org/wiki/Database), [file systems](https://en.wikipedia.org/wiki/File_system), or [storage arrays](https://en.wikipedia.org/wiki/Disk_array).** When a [laptop](https://en.wikipedia.org/wiki/Laptop) is powered off in a backpack, the data on its [hard drive](https://en.wikipedia.org/wiki/Hard_disk_drive) is at rest. The primary threat here is physical theft. Therefore, **[Full Disk Encryption](https://en.wikipedia.org/wiki/Disk_encryption) is a security method used to protect the entirety of data at rest on a [storage volume](https://en.wikipedia.org/wiki/Volume_%28computing%29).** If a thief steals the laptop, they possess only an unreadable hard drive.

![Physical storage media, such as this hard disk drive, hold inactive data at rest. Full disk encryption protects this information against physical theft or unauthorized extraction.](https://wikipedia.org/wiki/Special:Redirect/file/Hard_drive.svg)

2.  **[Data in transit](https://en.wikipedia.org/wiki/Data_in_transit) refers to information actively moving across a network from one location to another.** When you log into a [web portal](https://en.wikipedia.org/wiki/Web_portal), your [credentials](https://en.wikipedia.org/wiki/Credential) traverse [copper wires](https://en.wikipedia.org/wiki/Copper_wire), [fiber optics](https://en.wikipedia.org/wiki/Optical_fiber), and wireless [frequencies](https://en.wikipedia.org/wiki/Radio_frequency). To protect this journey, **[Transport Layer Security](https://en.wikipedia.org/wiki/Transport_Layer_Security) (TLS) is a [cryptographic protocol](https://en.wikipedia.org/wiki/Cryptographic_protocol) used to encrypt data in transit.** 

![Bundles of optical fibers transmit data in transit across networks using pulses of light, a vulnerable journey typically protected by cryptographic protocols like TLS.](https://wikipedia.org/wiki/Special:Redirect/file/Fibreoptic.jpg)

3.  **[Data in use](https://en.wikipedia.org/wiki/Data_in_use) refers to information currently being processed or accessed by an application in computer [memory](https://en.wikipedia.org/wiki/Computer_memory).** Even if data is encrypted on the disk and encrypted over the network, it must eventually be decrypted in the system's [RAM](https://en.wikipedia.org/wiki/Random-access_memory) so the [CPU](https://en.wikipedia.org/wiki/Central_processing_unit) can process it. This makes data in use heavily targeted by memory-scraping malware and [side-channel attacks](https://en.wikipedia.org/wiki/Side-channel_attack).

![Data in use is actively loaded into volatile memory, such as this RAM module, where it must exist in an unencrypted state for the CPU to read and process it.](https://wikipedia.org/wiki/Special:Redirect/file/RAM_Module_(SDRAM-DDR4).jpg)

## Cryptographic Defenses: Encryption and Hashing

If classification is the architectural blueprint of security, [cryptography](https://en.wikipedia.org/wiki/Cryptography) is the steel and concrete used to build the walls. 

### Encryption: The Art of Secrecy
**[Encryption](https://en.wikipedia.org/wiki/Encryption) transforms [plaintext](https://en.wikipedia.org/wiki/Plaintext) data into unreadable [ciphertext](https://en.wikipedia.org/wiki/Ciphertext) using a [cryptographic algorithm](https://en.wikipedia.org/wiki/Cipher) and a specific [key](https://en.wikipedia.org/wiki/Cryptographic_key).** This is the ultimate fallback mechanism for confidentiality: **encryption prevents unauthorized users from reading the contents of intercepted or stolen data.** Even if your network defenses fail entirely and an attacker [exfiltrates](https://en.wikipedia.org/wiki/Data_exfiltration) your database, strong encryption renders their prize mathematically useless.

There are two primary mechanisms for encryption:
*   **[Symmetric encryption](https://en.wikipedia.org/wiki/Symmetric-key_algorithm) uses the same cryptographic key to both encrypt and decrypt data.** It is incredibly fast and highly efficient for encrypting massive volumes of data at rest. However, if you and a remote server need to communicate safely, how do you safely share that single key across an untrusted network?

![Symmetric encryption utilizes a single shared key for both the encryption of plaintext and the decryption of ciphertext.](https://wikipedia.org/wiki/Special:Redirect/file/Symmetric_key_encryption.svg)

*   To solve this, **[asymmetric encryption](https://en.wikipedia.org/wiki/Public-key_cryptography) uses a [public key](https://en.wikipedia.org/wiki/Public-key_cryptography) for encryption and a mathematically linked [private key](https://en.wikipedia.org/wiki/Public-key_cryptography) for decryption.** You can distribute your public key to the entire world. Anyone can use it to encrypt a message to you, but only you hold the private key necessary to decrypt it.

![Asymmetric encryption solves the key distribution problem by using a freely distributable public key for encryption and a closely guarded private key for decryption.](https://wikipedia.org/wiki/Special:Redirect/file/Public_key_encryption.svg)

### Hashing: The Fingerprint of Integrity
While encryption protects confidentiality (secrecy), [hashing](https://en.wikipedia.org/wiki/Hash_function) protects integrity (accuracy). **Hashing converts variable-length input data into a fixed-length [string of characters](https://en.wikipedia.org/wiki/String_%28computer_science%29) called a [hash value](https://en.wikipedia.org/wiki/Hash_function).** 

Unlike encryption, which is designed to be reversed (decrypted), **[cryptographic hashing](https://en.wikipedia.org/wiki/Cryptographic_hash_function) is a [one-way mathematical function](https://en.wikipedia.org/wiki/One-way_function).** This means **hashing cannot be mathematically reversed to reveal the original input data.** You cannot look at a hash value and work backward to reconstruct the document that created it. 

So, why do we use it? **Hashing is utilized to verify [data integrity](https://en.wikipedia.org/wiki/Data_integrity) by ensuring the data has not been altered.** If you download an [operating system image](https://en.wikipedia.org/wiki/Disk_image), you want to be certain a [hacker](https://en.wikipedia.org/wiki/Hacker) hasn't secretly injected [malware](https://en.wikipedia.org/wiki/Malware) into the file. Because of the mathematical properties of hashing, **changing a single [bit](https://en.wikipedia.org/wiki/Bit) in an input file produces a completely different hash value.** By comparing the hash value of your downloaded file against the hash value published by the vendor, you can mathematically prove the file is perfectly intact. Today, **[SHA-256](https://en.wikipedia.org/wiki/SHA-2) is a widely used cryptographic hashing algorithm** for exactly this purpose.

![Cryptographic hashing acts as a fingerprint for data. As shown here, changing even a single letter in the input data produces a drastically different hash value, proving the original file was altered.](https://wikipedia.org/wiki/Special:Redirect/file/Cryptographic_Hash_Function.svg)

## Data Obfuscation: Masking and Tokenization

Often in IT, personnel need to work *with* systems that contain sensitive data, without actually *seeing* the sensitive data itself. 

### Data Masking
**[Data masking](https://en.wikipedia.org/wiki/Data_masking) obscures specific parts of sensitive information to protect it from unauthorized exposure.** You see this in daily life: **data masking is commonly used to display only the last four digits of a [credit card number](https://en.wikipedia.org/wiki/Payment_card_number) on a receipt.** 

![Data masking is routinely deployed in consumer environments to obscure all but the final four digits of a payment card number, minimizing the risk of exposure.](https://wikipedia.org/wiki/Special:Redirect/file/Credit_card-first_4_digits.jpg)

Administrators deploy masking in two distinct ways:
*   **Static data masking creates a permanently sanitized copy of a database for use in non-production environments.** If your [software developers](https://en.wikipedia.org/wiki/Software_developer) need real-world data to test a new application, you perform static masking to permanently overwrite the real names and [SSNs](https://en.wikipedia.org/wiki/Social_Security_number) with fake ones before handing the database over to the dev team.
*   **Dynamic data masking obscures sensitive information in real-time as a user accesses a production database.** The underlying database retains the real, unmasked data, but a [proxy](https://en.wikipedia.org/wiki/Proxy_server) intercepts the [query](https://en.wikipedia.org/wiki/Query_language) and masks the output on the screen based on the user's permission level. 

### Tokenization
What if you run a business that processes credit cards, but you completely refuse to accept the legal liability of holding those credit card numbers on your servers? 

You use [tokenization](https://en.wikipedia.org/wiki/Tokenization_%28data_security%29). **Tokenization replaces sensitive data with a randomly generated string of characters called a token.** Unlike an encrypted file—which contains the secret inside it, just locked by math—**a token possesses no extrinsic or exploitable value if stolen by an attacker.** It is simply a random placeholder. 

How does the placeholder function? Behind the scenes, **tokenization systems map the generated token back to the original sensitive data using a secure database.** This heavily guarded, isolated server is isolated from normal business operations: **the highly secured database storing the relationship between a token and original data is called a token vault.** 

Because the real data is locked entirely in the vault, **[payment card processing](https://en.wikipedia.org/wiki/Payment_processor) systems frequently use tokenization to avoid storing actual credit card numbers** on [point-of-sale](https://en.wikipedia.org/wiki/Point_of_sale) terminals or [e-commerce](https://en.wikipedia.org/wiki/E-commerce) [web servers](https://en.wikipedia.org/wiki/Web_server). If a hacker [breaches](https://en.wikipedia.org/wiki/Data_breach) the web server, they steal nothing but millions of worthless, random alphanumeric tokens.

![Tokenization systems issue valueless, random placeholders to represent sensitive information. This ensures that real payment credentials are never stored directly on a merchant's point-of-sale terminal or mobile application.](https://wikipedia.org/wiki/Special:Redirect/file/How_mobile_payment_tokenization_works.png)

## Removing Identity: Anonymization vs. Pseudonymization

When organizations share vast datasets for research, [analytics](https://en.wikipedia.org/wiki/Analytics), or [machine learning](https://en.wikipedia.org/wiki/Machine_learning), they must strip out the identities of the human beings tied to that data. Security professionals use two distinct methods, and the difference between them is legally vital.

*   **[Data anonymization](https://en.wikipedia.org/wiki/Data_anonymization) permanently removes personally identifiable information from a dataset.** The link between the data and the human is deliberately destroyed. Because the destruction is absolute, **properly anonymized data cannot be [reverse-engineered](https://en.wikipedia.org/wiki/Reverse_engineering) to identify an individual user.**
*   **[Data pseudonymization](https://en.wikipedia.org/wiki/Pseudonymization) replaces directly identifying information with artificial identifiers.** It hides the person's identity, but a master key or mapping table is kept somewhere safe. Therefore, **pseudonymized data can be re-identified by mapping the artificial identifiers back to the original source.**

> **Compliance Warning:** Under privacy frameworks like the [GDPR](https://en.wikipedia.org/wiki/General_Data_Protection_Regulation), *pseudonymized* data is still legally considered [personal data](https://en.wikipedia.org/wiki/Personal_data) because the capacity for re-identification exists. Truly *anonymized* data is generally exempt from privacy regulations because the human identity has been permanently erased.

## Enforcing the Boundaries: DLP, DRM, and Watermarking

Classifications and cryptographic protocols are highly effective, but humans remain the ultimate variable. Employees will attempt to email sensitive [spreadsheets](https://en.wikipedia.org/wiki/Spreadsheet) to their personal accounts, or download [proprietary](https://en.wikipedia.org/wiki/Proprietary_software) code they shouldn't. To combat this, administrators implement technical guardrails.

**[Data Loss Prevention](https://en.wikipedia.org/wiki/Data_loss_prevention_software) (DLP) systems detect and block the unauthorized transfer of sensitive data outside an organization.** A DLP [agent](https://en.wikipedia.org/wiki/Software_agent) monitoring an [endpoint](https://en.wikipedia.org/wiki/Host_%28network%29) will actively inspect outbound emails, web uploads, or [USB drive](https://en.wikipedia.org/wiki/USB_flash_drive) transfers. If it sees data matching the classification of "Restricted" (such as a string of Social Security Numbers), the DLP system instantly terminates the transfer and alerts the [security operations center](https://en.wikipedia.org/wiki/Security_operations_center).

Once a document is legally and safely acquired by an authorized user, how do you control what they do with it? **[Digital Rights Management](https://en.wikipedia.org/wiki/Digital_rights_management) (DRM) enforces access policies on proprietary data or [intellectual property](https://en.wikipedia.org/wiki/Intellectual_property).** DRM travels *with* the file. Even if an employee legitimately downloads a confidential [PDF](https://en.wikipedia.org/wiki/PDF), **Digital Rights Management restricts user actions such as viewing, printing, or forwarding specific documents.** 

![Digital Rights Management (DRM) enforces hard technical limits on digital media, such as actively blocking users from copying or transferring protected files.](https://wikipedia.org/wiki/Special:Redirect/file/Copyprotection_6810.jpg)

Finally, if data does leak, an organization must be able to prove ownership and identify the source of the leak. **[Digital watermarking](https://en.wikipedia.org/wiki/Digital_watermark) embeds a hidden identifier into [digital media](https://en.wikipedia.org/wiki/Digital_media) to track ownership and unauthorized distribution.** By weaving imperceptible patterns into the [pixels](https://en.wikipedia.org/wiki/Pixel) of a video or the [code](https://en.wikipedia.org/wiki/Source_code) of a document, administrators can trace exactly which user's account was used to steal and leak the asset. 

![Digital watermarking can embed hidden identification data directly into the individual pixels of an image or video, allowing administrators to definitively trace the source of a data leak.](https://wikipedia.org/wiki/Special:Redirect/file/Pixel-example.png)

As a security professional, you must master these concepts not as a list of abstract terms, but as an interconnected [ecosystem](https://en.wikipedia.org/wiki/Digital_ecosystem). You classify the data so you know its worth; you track its state to know its vulnerabilities; you apply encryption, hashing, masking, or tokenization to strip attackers of their leverage; and you enforce strict boundaries using DLP and DRM. This is how order is maintained in the chaotic landscape of modern information technology.