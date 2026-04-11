Imagine you are running a huge multiplayer video game server for your whole school. If you just start changing the rules or adding game mods while people are in the middle of building a giant castle, the game will crash, and players will lose all their hard work. You need a careful plan. 

In the computer world, IT change management provides a structured methodology to minimize service disruptions when altering production environments. This is just a fancy way of saying we have a step-by-step plan to make sure we don't break the system when we change things. When businesses rely on computers to make money and help people, any sloppy change is a big danger. Making a computer setup perfect on your own is only half the job. The other half is actually putting it into the real world safely.

***

## The Anatomy of the Request

Before you change anything on that big game server, you have to write down your idea. This starts with a Request for Change (RFC), which is a formal document submitted to initiate a proposed alteration to an IT system. It is a lot like asking your parents for a bigger allowance by handing them a typed letter instead of just yelling across the house. 

This RFC isn't just busywork; it's your master plan. To be valid, a Request for Change must include a clear description of the purpose of the proposed system alteration. This tells everyone *why* you are making the change (like, "We need this update so players can fly"). Furthermore, a Request for Change must detail the technical scope of the proposed system alteration. This means listing exactly *what* parts of the computer or network you are going to touch. 

After you write the RFC, we do a risk analysis. Think of this like looking both ways before crossing a busy street. Risk analysis assesses the potential negative impact a proposed IT change might have on continuous business operations. For example, let's say a game company makes \$500 a day. If a bad update crashes the game for half a day, we can calculate the money lost:

1. Find the daily money made: \$500.
2. Divide by the total hours in a day (24) to get the hourly rate: 500 / 24 = \$20.83 per hour.
3. Multiply the hourly rate by the hours offline (12 hours): 20.83 * 12 = \$249.96.

So, a half-day crash costs the company about \$250! Risk analysis asks: If we take this server down, do we lose money or break the game for everyone?

## Safeguarding the Environment: Testing and Contingency

Nobody should try a dangerous skateboard trick without knee pads, and no computer person should change a system without a safety net. The change process requires strict rules to protect the computers.

### 1. Peer Review and Sandbox Testing
Before a change goes live, it needs to be double-checked. 
*   **Peer review** involves having a secondary technical professional evaluate a proposed change configuration to identify potential errors. This is just like asking a friend to proofread your history essay. Another set of eyes can catch a tiny spelling mistake or a mixed-up rule that you totally missed.
*   **Sandbox testing** involves applying a proposed IT change in an isolated environment that mirrors the production network. Imagine having a private copy of your game server where only you can play. Sandbox testing allows technicians to identify potential configuration failures without affecting actual business operations. If your new update is going to blow up a server, you want it to blow up the fake, private server in your sandbox instead of the real one everyone is using.

### 2. Backup and Rollback Plans
Just hoping things go well is a terrible idea. Even a well-tested plan can fail. You need an "undo" button.

> **Backup Plan:** A backup plan guarantees that existing production data can be restored if an IT change causes unexpected data corruption. This saves the *information*—like making sure your game save files are copied to a USB drive before you install a new update.
> 
> **Rollback Plan:** A rollback plan is a step-by-step procedure designed to revert an IT system to its previous functional state if a change fails. This fixes the *computer parts and software*. Rollback plans are often referred to as **back-out plans** within official IT change management frameworks.

If you add a new plugin that ruins everyone's high scores, your rollback plan uninstalls the bad plugin, and your backup plan brings back the saved scores.

## The Three Classifications of Change

Not all computer updates are a big deal. Buying a new car takes lots of planning, but buying a pizza takes almost none. IT change management puts changes into three different buckets to decide how much planning is needed.

| Change Type | Characteristics | Approval Required | Example Scenario |
| :--- | :--- | :--- | :--- |
| **Standard Change** | Low-risk, happens all the time, easy to follow steps. | Pre-approved; no extra permission needed. | Resetting a user password is an example of a standard IT change. |
| **Normal Change** | Moderate to high operational risk. | Needs full checking and permission before doing it. | Upgrading an organization's primary database server is an example of a normal IT change. |
| **Emergency Change** | Super urgent; skips the normal waiting line. | Needs fast approval to fix a major broken thing. | Applying a security patch for an actively exploited zero-day vulnerability is an example of an emergency IT change. |

A **standard change** is a low-risk, frequently occurring IT alteration that follows a well-documented procedure. Because they are so common, standard changes do not require additional authorization before execution due to their pre-approved nature. Think of it like taking out the trash; you don't need to ask your parents for permission every single time because you already know how to do it safely. Resetting a user password is an example of a standard IT change.

A **normal change** requires a complete evaluation and authorization process before the implementation phase. These are bigger deals. Normal changes carry moderate to high operational risk. Because of this, normal changes must be approved by the Change Advisory Board prior to scheduling. Upgrading an organization's primary database server is an example of a normal IT change.

An **emergency change** is implemented immediately to resolve a critical IT incident. Emergency changes bypass the standard scheduling process to restore vital business services quickly. If a water pipe bursts in your house, you don't ask for permission to turn off the water; you just do it! Applying a security patch for an actively exploited zero-day vulnerability is an example of an emergency IT change. (A zero-day vulnerability just means a brand-new hacker trick that we need to block right this second!)

## The Gatekeepers: The Change Advisory Board

For normal changes, one person doesn't get to make the decision alone. It is decided by the **Change Advisory Board (CAB)**. 

The Change Advisory Board is a designated committee composed of technical and business stakeholders. Stakeholders are just people who care about the business, like store managers and computer experts. Why include business people? Because computers are there to help the business! A computer expert might want to update a server, but a store manager might say, "No, that update will shut down our cash registers during our busiest time of the day!"

The Change Advisory Board reviews the risk level and business impact of proposed normal changes. Most importantly, the Change Advisory Board holds the formal authority to approve or reject proposed normal changes. They are the umpires who make the final call on whether the good parts of the change are worth the risk.

But what if something terrible happens, like a hacker attack or a completely broken network, and you can't wait days for the next CAB meeting? Emergency changes are typically evaluated and approved by an expedited group called the **Emergency Change Advisory Board** (ECAB). This is a smaller, faster team of bosses who can give a thumbs-up right away to save the day.

## Timing the Execution: Windows and Freezes

Getting permission is great, but picking the right time is just as important.

To stop people from getting mad when their computers stop working, IT teams use a **maintenance window**, which is a pre-approved, scheduled timeframe designated specifically for implementing IT changes. Maintenance windows are typically scheduled during off-peak business hours to mitigate disruption to affected system users. This means doing the work when everyone is asleep, like at 2:00 AM on a Sunday. But you still can't be sneaky about it! Affected system users must receive prior notification of the scheduled maintenance window downtime before an IT change begins. This way, they can save their homework or game progress before the computer goes offline.

On the flip side, sometimes you just need everything to stay exactly the way it is. When this happens, a company uses a **change freeze**. A change freeze is a designated time period during which normal and standard IT changes are strictly prohibited. You aren't allowed to touch anything! Organizations implement change freezes during critical business periods to guarantee maximum system stability. 

An e-commerce company banning non-critical server updates during the week of Black Friday is an example of a change freeze. Black Friday is the biggest shopping day of the year. When a company is making thousands of dollars every minute, they actively choose *not* to mess with the computers, just in case something breaks.

## The Final Phase: Acceptance and Documentation

A change isn't finished just because the loading bar hits 100%. The job is only done when you know it works and you write down what you did.

Once the system is turned back on, the computer workers must get **end-user acceptance**. End-user acceptance involves gathering confirmation from affected personnel that a completed IT change functions correctly. Think of it like cooking dinner for your family. You can't just say, "The dinner is done!" You have to ask them to taste it. If the computer team updates a school program, they have to ask the teachers, "Can you actually log in and see your students?" The people using it get to decide if it was a success.

Finally, you have to clean up your mess and leave good notes. The final phase of the change management workflow requires updating institutional documentation to reflect the new IT environment state. This means updating the rulebooks and maps. If a future worker tries to fix the internet using old maps, they will be totally lost and might break things worse. Because of this, post-change documentation updates must include revising network topology diagrams if physical infrastructure routing was altered. (A network topology diagram is just a treasure map that shows how all the cables and computers connect to each other!) 

By following these steps, computer experts turn messy, risky changes into a safe and predictable routine.