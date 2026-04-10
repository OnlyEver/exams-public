Have you ever been playing a video game, making awesome progress, when suddenly the power goes out? If you didn't save your game, everything you worked for is gone. For big businesses and real-life computer networks, a sudden crash or power failure is a lot worse than losing a high score—it can cost a company \$10,000 or more in just a few minutes! 

To survive these disasters, computer experts don't just rely on strong passwords. They survive by making sure their computers always have electricity, and by making perfect copies of their information that they can load back up if things go horribly wrong. Being great at computer security means knowing how to recover when everything falls apart!

## The Calculus of Data Preservation: Backup Strategies

Your computer data is changing all the time, kind of like a giant, growing Lego city. If we want to save our work so we can rebuild it later, we have to decide *how* we are going to save it. 

At the base of everything is the **full backup**. Think of this like taking a highly detailed photograph of your entire Lego city. A full backup copies all selected data regardless of when the data was last modified. It is great because absolutely everything is saved in one spot, but it takes a really long time to copy and takes up a huge amount of hard drive space. Because it takes too much time to copy everything every single day, we use clever shortcuts to save only the parts that have changed!

The first shortcut is an **incremental backup**. An incremental backup copies only the data that has changed since the *last backup of any type*. If you take a full picture on Sunday, Monday's incremental backup only snaps a picture of the new Lego pieces added on Monday. Tuesday's incremental only snaps Tuesday's new pieces. It's super fast! But there is a catch. Incremental backups require the last full backup and all subsequent incremental backups to perform a full restoration. If you lose Monday's picture, you can't properly load Tuesday's picture!

The second shortcut is a **differential backup**. A differential backup copies all data that has changed since the *last full backup*. 

Let's look at how the math for a differential backup works step-by-step:
1. Imagine you run a full backup on Sunday.
2. On Monday, you create 12 new files. Monday's backup saves those 12 files.
3. On Tuesday, you create 6 more new files. 
4. To calculate how many files Tuesday's differential backup needs to save, you must add Monday's new files and Tuesday's new files together.
5. We take Monday's 12 files and add Tuesday's 6 files (12 + 6 = 18).
6. Tuesday's backup saves all 18 files!

Why would we save Monday's files again on Tuesday? Because differential backups require only the last full backup and the most recent differential backup to perform a full restoration. Instead of hunting down lots of tiny daily files to fix a broken computer, you only ever need two files!

> **The Backup Speed Trade-Off**
> *   **Incremental:** Super fast to save, but slow to fix if things break (because you need to put lots of puzzle pieces together).
> *   **Differential:** A little slower to save, but super fast to fix (because you only need two pieces).

Sometimes, computers do a really cool trick called a **synthetic full backup**. A synthetic full backup consolidates an existing full backup with subsequent incremental backups to create a new full backup without reading the original data source. It’s like a smart computer program automatically stitching your old Lego pictures and your tiny new daily pictures together to make a brand-new, perfect full picture, saving your computer from doing all the hard work twice.

### Time Travel at the Block Level: Storage Snapshots

Regular backups are like slowly packing up a big backpack—it takes time. But what if your computer breaks and you need it fixed right this exact second? 

For instant fixes, we use a **storage snapshot**. A storage snapshot captures the exact state of a system or storage volume at a specific point in time. It is exactly like hitting "quick save" in a game right before a big boss fight. Snapshots allow for rapid recovery of a system to a previous state without restoring from traditional tape or disk backup media. If you accidentally delete a super important folder, you can just instantly rewind to the snapshot taken two minutes ago!

## Securing the Archive: The Geometry of Survival

A backup is completely useless if it gets destroyed in the exact same accident as your main computer. To stay safe, pros use a famous rule.

The **3-2-1 backup rule** dictates keeping three copies of data, on two different media types, with one copy stored offsite. 
1. **Three copies:** Your main data, plus two backup copies.
2. **Two different media types:** Like putting one copy on a hard drive and another on a magnetic tape. 
3. **One copy offsite:** Moving one copy far away!

What does that last part mean? **Offsite storage** involves keeping backup copies in a physical location separate from the primary data center. By ensuring your backups are kept across town (or in another state), offsite storage protects backup data against localized disasters affecting the primary facility, like a flood or a fire in your school building.

But if we put our backup drives in a truck to drive them across town, what if a thief steals them? That is why we use **backup encryption**. Backup encryption secures data at rest to prevent unauthorized access if the backup media is stolen or compromised. It mathematically scrambles your files into a secret code, so the thieves only see totally unreadable gibberish.

### The Ransomware Defense: Air Gaps and Immutability

Bad guys sometimes use nasty viruses called ransomware to lock up a company's files and demand money. These viruses specifically try to destroy your backups so you can't fix your computer! We stop them using two neat tricks.

First is the **air gap**. An air gap physically or logically disconnects backup media from the production network to prevent network-based attacks from reaching the backups. Basically, we unplug it! If a backup tape is sitting on a shelf in a safe, completely unplugged, a hacker on the internet cannot touch it.

Second, we use **immutable backups**. Immutable backups cannot be altered, deleted, or encrypted by ransomware during a specified retention period. It is just like writing in permanent marker. Even if a hacker breaks in, the computer system physically will not allow them to delete or change those backups until a set timer runs out!

## Proving the Theory: Disaster Recovery Testing

Having a backup plan is cool, but you have to practice it to make sure it works! We test our plans using different types of exercises, getting more and more realistic.

| Test Type | Description | Realism | Risk Level |
| :--- | :--- | :--- | :--- |
| **Tabletop Exercise** | A tabletop exercise is a discussion-based session where team members review their roles in disaster recovery scenarios without deploying actual resources. | Low | None |
| **Walkthrough Exercise** | A walkthrough exercise involves team members performing their disaster recovery duties step-by-step in a non-disruptive environment. | Moderate | Very Low |
| **Simulation Exercise** | A simulation exercise tests disaster recovery procedures by creating a mock disaster scenario requiring actual system configurations in an isolated environment. | High | Low |
| **Parallel Processing** | Parallel processing involves running the recovery site simultaneously with the primary site to verify functionality without interrupting primary operations. | Very High | Moderate |
| **Full Interruption Test** | A full interruption test shuts down the primary site completely to ensure the organization can operate entirely from the disaster recovery site. | Absolute | Extreme |

Notice how these get harder? We start with a **tabletop exercise**, which is just talking through the plan, kind of like a sports team drawing plays on a whiteboard. Next, we do a **walkthrough exercise**, where people sit at their keyboards and practice the steps without changing anything real. Then we do a **simulation exercise**, which is like a practice scrimmage inside a safe, isolated area on the network.

When we want to really test things, we use **parallel processing**. We play the real game and the practice game at the exact same time to make sure the backup computers are fast enough to handle the workload! 

Finally, the scariest test is the **full interruption test**. Because we are unplugging our real computers on purpose to see if the backup site catches everything perfectly, a full interruption test carries the highest risk of disruption to business operations compared to all other disaster recovery testing methods. If the backup fails, the whole company goes dark!

## The Physics of Continuity: Power Redundancy

None of this awesome computer stuff matters if the servers don't have electricity. To make sure the computers never turn off, we build incredibly smart power systems.

Inside the computer box itself, we use **dual power supplies**. Dual power supplies allow a single piece of equipment to draw power from two independent power circuits simultaneously. It’s like a laptop having two different power cords plugged into two different wall outlets at the exact same time! Because of this, dual power supplies prevent equipment failure if one power circuit or one power supply unit fails.

Those power cords plug into special smart power strips called **Managed Power Distribution Units (PDUs)**. Managed Power Distribution Units (PDUs) allow administrators to remotely monitor and control the electrical power distributed to individual networking devices. If a computer router freezes up, a worker sitting across the country can use an internet menu to turn off just that one single outlet and turn it back on, forcing the machine to restart!

### Bridging the Outage: The UPS and the Generator

What happens if the whole city loses power? A magical, fast-acting team of machines goes to work!

First, the **Uninterruptible Power Supply (UPS)** jumps in. An Uninterruptible Power Supply (UPS) provides immediate, short-term battery power to equipment during a main power failure. It's a giant battery pack that kicks on in a fraction of a second so the computers don't even blink.

But a battery doesn't last forever. An Uninterruptible Power Supply (UPS) bridges the power gap between a main power outage and the activation of a secondary power generator. 

While the UPS battery is keeping the computers alive, a smart robot sensor called an **Automatic Transfer Switch (ATS)** is watching. An Automatic Transfer Switch (ATS) automatically shifts the electrical load from the primary utility power to a backup generator when a power failure is detected.

This smart switch signals the **backup generator**, which is like a giant car engine. A backup generator provides long-term emergency electrical power during extended utility outages. Because it is a real rumbling engine, backup generators require a continuous external fuel supply such as diesel, natural gas, or propane to operate. As long as trucks keep bringing fuel for the engine, the computers stay on, the backups stay safe, and the game never ends!