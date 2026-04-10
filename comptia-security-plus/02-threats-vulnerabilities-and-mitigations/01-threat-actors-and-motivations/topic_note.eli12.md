Imagine you are building a giant digital fort. You wouldn't just build walls without thinking about who might try to knock them down, right? In the computer world, we build defenses to protect against real people who have specific goals, budgets, and tools. To protect a computer network, you need to know exactly who is trying to break in, what they want, and what kind of gear they have. 

> A **threat actor** is any entity responsible for an event that impacts the security of a system or network. 

Whether you are a gaming server admin or a security pro, this is the most important thing to learn. A basic computer shield might block a random, automatic probe, but it won't stop a patient, well-funded human who is actively trying to outsmart you. To build the best defenses, **threat actors are systematically classified by their level of technical sophistication and available financial resources**. This means we sort them by how smart they are with computers and how much money they have.

But no matter who they are, all attackers start the same way. Before they even launch an attack, they snoop around. **Open-Source Intelligence (OSINT) is frequently used by all classifications of threat actors to gather target information before launching an attack**. Just like a rival sports team might watch videos of your past games, attackers look at public social media or open websites to learn about your network. 

From there, attackers are split into two main groups based on where they start: **External threat actors originate from outside the organization's network boundary**, while **internal threat actors originate from inside the organization's logical or physical network boundary**.

## The External Threat Landscape

When we look outside our fort's walls, we see different types of attackers. Some are like final bosses with unlimited money, and others are just curious kids downloading cheat codes.

### Nation-State Actors and APTs
At the very top of the danger list are **nation-state actors**. These are highly skilled cyber attackers sponsored by a national government. Because they have a whole country's government backing them, **nation-state threat actors possess the highest level of resources and funding among all attacker types**.

They don't usually care about stealing small bits of money. **The primary motivation for nation-state attackers is typically political espionage or military advantage.** Instead of robbing a bank, **nation-state attackers often seek to steal government secrets or proprietary intellectual property from other nations**. This lets them steal secret recipes for new technology instead of spending years building it themselves. Also, **state-sponsored actors frequently target critical infrastructure to cause national disruption during geopolitical conflicts**. This is like secretly turning off another country's power grid or water supply during a major disagreement.

Because they want to stay hidden for a long time, **Advanced Persistent Threats (APTs) are most commonly associated with nation-state threat actors**. 
> An **Advanced Persistent Threat (APT)** maintains long-term undetected access to a compromised network to continuously extract data. 

If you are dealing with an APT, it isn't a quick smash-and-grab robbery. It is a silent spy living inside your computer system for years.

### Organized Crime Syndicates
Next, we have **organized crime syndicates**, which operate as highly structured groups of professional cybercriminals. Think of them like a big company, but their business is stealing. 

**The primary motivation for organized crime threat actors is financial gain.** They just want to make money. To do this, **organized crime actors frequently deploy ransomware to extort money from targeted organizations**. Ransomware locks up a company's computers, and the criminals demand a payout to unlock them. 

Because they make so much money from these attacks, **organized crime syndicates often possess significant financial resources to purchase undocumented zero-day exploits** (which are secret, unpatched software flaws that no one else knows about yet). 

Here is a quick example of how an organized crime group's ransomware attack can cost a business money:
1. First, the criminals lock the business computers and demand a ransom of \$4,000.
2. Next, because the computers are locked, the business has to close for 2 days. The business normally makes \$1,500 each day. The lost sales equals 2 * \$1,500 = \$3,000.
3. Finally, you add the ransom amount and the lost sales together to find the total damage: \$4,000 + \$3,000 = \$7,000.

### Competitor Threat Actors
Sometimes, the bad guy is just a rival business. **Competitor threat actors attack rival organizations to gain an unfair market advantage.** In this case, **the primary motivation for competitor threat actors is corporate espionage** (which is just a fancy word for business spying). 

These attackers **actively seek to steal proprietary intellectual property or confidential customer data from business rivals**. Imagine a video game company spending five years making a game, and a rival simply steals the code to make their own version cheaper. Furthermore, aggressive **competitors sometimes fund external attacks against rivals to disrupt the rival organization's business operations**, like paying someone to crash a rival's online store on the biggest shopping day of the year.

### Hacktivists
Some attackers don't care about money at all. **Hacktivists are threat actors driven by political, social, or ideological beliefs.** 

**The primary motivation for a hacktivist is to promote a specific cause or publicize a grievance.** They want everyone to hear their message. Because of this, **hacktivists frequently use website defacement to spread a political message directly to the public**. This is like digital graffiti—they replace a company's homepage with their own poster. Also, **hacktivists often utilize Distributed Denial of Service (DDoS) attacks to disrupt target organizations associated with opposing ideologies**. A DDoS attack is like ordering 10,000 pizzas to the same house at the same time so that no one can get in or out.

### Vulnerability Brokers
Hidden in the shadows are the digital treasure hunters. **Vulnerability brokers are threat actors who discover zero-day vulnerabilities specifically to sell the exploit details to other attackers.** They don't usually launch attacks themselves. Instead, **a vulnerability broker's primary motivation is direct financial compensation**. They find a secret hole in a castle wall and sell the map to the highest bidder.

### Unskilled Attackers
At the very bottom of the ladder are **unskilled attackers**, who are threat actors who lack deep technical knowledge of cybersecurity. Because they don't really understand how computers work behind the scenes, **unskilled attackers rely entirely on pre-written scripts and automated tools to launch cyber attacks**. 

Because they just use tools other people built, **unskilled attackers are historically referred to in the cybersecurity industry as script kiddies**. They aren't super dangerous because **unskilled attackers typically lack external funding and advanced computing resources**. Unlike the big groups, **the motivation for unskilled attackers often includes bragging rights or simple curiosity**. They just want to see if they can break something to show off to their friends.

---

## The Internal Perimeter: Insider Threats

The tallest fort walls are useless if the bad guy already has the keys to the front gate. **An insider threat is a security risk originating from within the targeted organization.** 

These attackers are super dangerous because **insider threats bypass traditional perimeter security controls because the actors already operate inside the network boundary**. Firewalls keep outsiders out, but **insider threats already possess authorized access to the targeted organization's systems and physical facilities.** We have to remember that **insider threats include current employees, former employees, and trusted contractors.** 

### The Malicious Insider
When an employee intentionally turns bad, the damage is huge. **The motivation for a malicious insider threat is frequently revenge against an employer**, maybe because they got fired or missed out on a promotion. Because they are angry, **malicious insider threats deliberately sabotage corporate systems or steal sensitive data**, like deleting all the backup files or copying secret lists right before they quit.

### The Unintentional Insider
However, a person doesn't have to be angry to cause a disaster. **An unintentional insider threat occurs when an employee accidentally exposes sensitive data through negligence or poor security practices.** This is like accidentally leaving the front door of the fort wide open because you forgot to lock it. It isn't done on purpose, but the bad guys get in anyway.

### Shadow IT
A very common type of inside risk happens when workers try to bend the rules to make their jobs easier. 
> **Shadow IT** refers to information technology systems deployed without the explicit knowledge or approval of the organizational IT department. 

For example, if the company's official file-sharing system is too slow, a team might just secretly use their own personal cloud accounts. **Employees typically deploy Shadow IT to bypass corporate restrictions for convenience or perceived efficiency.** 

While they just want to get their homework or job done faster, the result is terrible for security: **Shadow IT creates severe internal vulnerabilities by bypassing corporate security policies and monitoring.** You can't protect a secret server if you don't even know it exists!

---

## The Architecture of Motivation

Understanding *who* is attacking helps you build defenses. Understanding *why* they attack tells you what they will go after. We can group what attackers want into three simple goals:

1. **Data Exfiltration:** This is **a primary actor motivation involving the unauthorized transfer of sensitive information out of an organization's network.** Whether it's a spy stealing missile blueprints or a competitor stealing code, the goal is to secretly copy data and carry it out the door.
2. **Blackmail and Extortion:** This goal is all about holding things hostage. **Blackmail and extortion involve threatening to release stolen data or disrupt systems unless the victim pays a ransom.** The bad guys lock your stuff up and say, "Pay us, or you never get this back."
3. **Disruption:** Sometimes the goal is just to cause a giant mess. **Disruption as a motivation aims to intentionally halt business operations or take critical systems offline.** This could be a hacktivist knocking a website offline with a DDoS attack, or a nation-state turning off a city's power grid.

### Summary Threat Matrix

To help you study for your exams, here is a simple cheat-sheet matrix to help you remember the bad guys:

| Threat Actor | Tech Skill Level | Money & Resources | Main Goal | Common Moves |
| :--- | :--- | :--- | :--- | :--- |
| **Nation-State** | Ultimate Boss / Highest | Unlimited (Government backed) | Spying, Military advantage | APTs, zero-days, attacking infrastructure |
| **Organized Crime** | Very High | Lots of money / Self-funded | Making money | Ransomware, extortion, buying zero-days |
| **Competitor** | Medium to High | Company budgets | Unfair business advantage | Stealing business secrets, paying to crash rivals |
| **Hacktivist** | Varies | Low to Medium | Promoting a belief or cause | Changing websites (defacement), DDoS attacks |
| **Vulnerability Broker** | High | Varies | Getting paid | Finding and selling secret zero-day weaknesses |
| **Unskilled (Script Kiddie)** | Lowest | None | Showing off, Curiosity | Using tools other people wrote |
| **Insider (Malicious)** | Varies | None (Relies on access) | Revenge | Breaking systems or stealing data from inside |
| **Insider (Unintentional)** | Varies | None | Convenience, Accidental | Leaving doors unlocked, using Shadow IT |

By learning these profiles, you turn cybersecurity from a confusing guessing game into a smart, strategic defense. You aren't just blocking random computer signals; you are stopping real people with real motives!