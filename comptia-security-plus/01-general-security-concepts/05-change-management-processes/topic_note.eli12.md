Think of a computer network like a giant, multiplayer Minecraft server. If one admin changes a rule without telling anyone, they might accidentally delete the whole world or let griefers in. **Unauthorized system changes introduce undocumented vulnerabilities into an information technology environment**, which is basically like leaving a secret window open that hackers can sneak through without anyone knowing. 

To stop this mess, companies use a strict set of rules. **Change management is a formal process for overseeing modifications to information systems.** It might sound like boring paperwork stopping you from just fixing things, but it has a very important job. **The primary security goal of change management is mitigating risks associated with system alterations.** It keeps things safe when we add updates or change settings, so fixing one thing doesn’t accidentally break everything else.

## The Bureaucracy of Survival: From RFC to CAB

You can't just change a major setting on a Tuesday afternoon because you feel like it. It all starts with a form. **A Request for Change (RFC) is a formal document initiating the change management process.** To be useful, **a Request for Change must detail the specific system modifications requested by a user or administrator.** This means you have to write down exactly what you want to change, what computers it will affect, and why you are doing it. 

Next, we do a deep check called an impact analysis to see what could go wrong. We have to look at two main things:
1. First, **an impact analysis evaluates the potential security risks of a proposed system change.** This answers the question: if we open this digital door, will bad guys get in?
2. Second, **an impact analysis evaluates the potential operational downtime of a proposed system change.** This answers the question: how long will the game server or business website be offline while we install the update?

Let's look at how we calculate the cost of that downtime with some simple math:
Step 1: Find out how much money the company makes in one hour. Let's say the company makes \$500 per hour.
Step 2: Find out exactly how long the system will be turned off for the update. Let's say the update takes 3 hours.
Step 3: Multiply the hourly money by the hours of downtime (500 * 3 = 1500). 
The downtime will cost the company \$1500.

After this check, the plan goes to the **Change Advisory Board (CAB)**. **The Change Advisory Board (CAB) is a committee responsible for reviewing proposed system changes.** This group has people from different parts of the company—like security guards, computer builders, and business bosses. **The Change Advisory Board (CAB) must approve or reject a Request for Change before implementation begins.** They hold the power to say "yes" or "no". 

Crucially, the CAB enforces a major rule called separation of duties. **Separation of duties in change management prevents the developer of a change from being the sole approver of that change.** If you wrote the code, you can't be the only one who says it’s safe to use. You always need someone else to double-check your homework.

## Engineering the Deployment: Staging, Windows, and Reversions

Even after everyone says "yes," you don't just throw the new code onto the live computers. That’s like trying a brand-new skateboard trick for the first time while rolling down a giant hill. Instead, **change management requires testing all proposed system changes in an isolated staging environment prior to production deployment.** A staging environment is a safe, fake version of the real network where you can test things out without breaking the real system.

Putting the change into the real system requires a solid plan, using two main guides:

| Document Type | Definition |
| :--- | :--- |
| **Rollout Plan** | A document that **defines the specific technical steps required to implement a system change.** This is your step-by-step instruction manual for making the change happen. |
| **Rollback Plan** | A document that **details the exact procedures to revert a system to a previous state if a change fails.** This is your giant "undo" button. |

> **Note on Terminology:** You might also hear the term **backout plan**. Just remember that a **backout plan is an alternative term for a rollback plan used in change management documentation.** They both mean exactly the same thing: putting things back to how they were before you messed up.

To make sure these changes don't annoy the people using the system, **organizations schedule system changes during predefined maintenance windows to minimize business operations disruption.** This is why video game updates usually happen at 3:00 AM on a Tuesday. If something breaks and they need to use the rollback plan, most players are asleep, so nobody even notices!

## The Fire Alarm: Managing Emergency Changes

Normal rules are great for normal days. But what if a hacker is breaking into the system right now? You can't wait a whole week for the CAB committee to have a meeting.

**Emergency changes are expedited modifications required to resolve critical security incidents.** When your house is on fire, you don't ask for permission to use the fire extinguisher. Because of this, **emergency changes bypass standard approval timelines to address immediate system threats.** A boss or security leader will just yell, "Do it now!"

But skipping the waiting time doesn't mean you get to skip the paperwork forever. **Organizations must document emergency changes retroactively to maintain an accurate security audit trail.** "Retroactively" means doing it *after* the fact. Once the bad guy is kicked out and the system is safe, you have to go back and write down exactly what you changed, so the rulebook is still totally accurate.

## Time Machines and Automation: Version Control, CI/CD, and IaC

Large companies change their computer code hundreds of times a day. To keep track of all this without losing their minds, they use a tool called version control. **Version control is the practice of tracking and managing changes to software code over time.**

Think of it like saving your progress in a video game right before a big boss fight. **Version control systems maintain a historical record of all configuration file modifications.** It remembers every single change ever made. Because of this magic trick, **version control enables security administrators to restore systems to a known secure configuration state** with just one click if a new update breaks everything. 

This idea isn't just for coding anymore. It’s used to build the whole network automatically:
*   **Continuous Integration and Continuous Deployment (CI/CD) pipelines utilize automated version control for software updates.** This means when a coder writes a new update, the computer system automatically checks it for mistakes and sends it out to users without a human needing to push a button.
*   **Infrastructure as Code (IaC) applies software version control practices to automated infrastructure provisioning.** Instead of plugging in real wires and physical servers, computer builders write code that creates virtual servers. If they want a new server, they just change the code. Since everything is just code, every single change is tracked, checked, and easy to undo.

## Closing the Loop: Documentation, Diagrams, and Audit Trails

After a change is completely finished, you still have one last job: updating the maps and instructions. If you move things around in your bedroom but don't tell anyone, your mom might trip over your laundry basket in the dark. The same is true for computers. Post-change documentation keeps everyone safe.

*   **Network Diagrams:** A network diagram is a map of all the computers connected together. **Administrators must update network diagrams following any structural network changes to ensure accurate security monitoring.** If you add a new router, the security team needs to see it on the map so they can watch it for hackers.
*   **Asset Inventories:** An asset inventory is a giant list of everything the company owns. **Administrators must update asset inventories after adding or removing hardware to maintain an accurate attack surface map.** If you plug in a new laptop, it must go on the list. If it isn't on the list, bad guys might sneak into it because no one is guarding it.
*   **Standard Operating Procedures (SOPs):** These are the everyday rulebooks for workers. **Standard Operating Procedures (SOPs) must be updated when a system change alters daily administrative workflows.** For example, if a change makes workers use a secret passcode to log in, the rulebook needs to be updated so everyone knows the new steps.

Finally, the company tracks exactly who made the changes so nobody can play the blame game. **Change management systems maintain an audit log of the specific personnel who approved system modifications.** This proves exactly who said "yes" to the change. Also, **change management systems maintain an audit log of the specific personnel who implemented system modifications.** This proves who actually typed in the new code.

By keeping these records, if something goes wrong later, the company can look at the logs to see exactly who asked for the change, who checked it, who said it was okay, and who did the final work. In the computer security world, making sure everyone takes responsibility is just as important as the passwords themselves!