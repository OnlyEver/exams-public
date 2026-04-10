Imagine building a massive digital clubhouse. It has vaults, a snack room, and a place to hang out. The biggest problem isn't building the walls; it's figuring out who gets the keys to which rooms! If you don't have a good way to check who is at the door, the fanciest locks in the world won't keep the bad guys out. Checking who people are and what they are allowed to do is called Identity and Access Management (IAM). It's like tracking a player in a video game from the moment they create their account, making sure they only have the items they earned, and letting them safely jump between different game servers.

## The Anatomy of the Identity Lifecycle

Think about what happens when someone gets hired for a new job. They don't just magically appear in the computer system. **The identity lifecycle consists of creation, provisioning, modification, and deprovisioning phases.** If we don't manage these four steps like a careful referee, the network gets messy and unsafe!

When a new worker starts, we do something called **provisioning, which grants a new user the necessary access rights to perform assigned job functions.** This is like giving a new player their starter gear in a game. But jobs change. If a worker moves from the art team to the coding team, their account goes into the modification phase.

Here is a sneaky problem. **Privilege creep occurs when users accumulate unnecessary permissions as they change roles within an organization.** Imagine if a player kept all their starter gear, got the warrior gear, and then got the wizard gear, until their backpack was overflowing! To fix this, **account maintenance requires periodic reviews of user permissions to prevent privilege creep**. We regularly check their backpack and take away the old keys they don't need anymore.

Eventually, the worker leaves the company. **Deprovisioning revokes an employee's system access upon termination or role change.** This takes away their keys. But we shouldn't just delete their account completely! **Disabling an inactive account preserves the security audit trail better than immediately deleting the account.**

> **Why disabling matters:** Imagine if someone broke a rule in your game last month, and you want to look at the logs to see who did it. The logs track players by a hidden ID number. If you delete the player's account entirely, the game forgets whose name goes with that number. Your logs will just show random numbers instead of a name! Disabling an account locks the player out, but keeps their name in the records so you can still read your logs later.

## Architecting Access: The Rules of Governance

Once a user has an account, how do we decide what they can click on? We use some important rules.

The golden rule is **the principle of least privilege, which dictates granting users only the bare minimum permissions needed for specific tasks.** If your friend only needs to borrow your pencil, you don't give them your whole backpack. They get the pencil, and that's it!

To stop huge mistakes or cheating, we use **separation of duties, which requires dividing critical tasks among multiple users to prevent fraud or error.** Think of it like launching a rocket where two different people have to turn two different keys at the exact same time. No single person can launch it alone!

Giving out permissions one by one takes too long. Instead, we use **Role-Based Access Control (RBAC), which assigns permissions to job functions rather than individual user accounts.** If your friend is the "Scorekeeper" for your sports team, you just give the "Scorekeeper" role access to the scoreboard app. You don't give it to your friend by name.

Sometimes we need even smarter rules. **Attribute-Based Access Control (ABAC) uses dynamic policies evaluating user, resource, and environmental attributes.** This looks at clues to make a choice. Is the user on a school tablet? Are they trying to open a file marked "Teachers Only"? What time is it?

Speaking of time, **time-of-day restrictions reduce the attack surface by preventing authentication during unmonitored night hours.** If someone tries to log in at 3:00 AM when everyone is asleep, the system just says no. This stops hackers who might have stolen a password and are trying to sneak in late at night!

## Centralizing the Truth: Directory Services

To make these rules work, a computer network needs a giant, organized contact list.

**LDAP organizes identity information in a hierarchical tree structure called a Directory Information Tree.** Imagine a family tree or a bracket for a sports tournament. It groups people logically: Earth -> USA -> Your State -> Your School -> You!

But we have to be careful how this contact list sends messages. **The Lightweight Directory Access Protocol (LDAP) uses TCP port 389 for unencrypted directory communications.** "Unencrypted" means the messages are sent in plain text, like writing your password on a postcard for anyone to read. Hackers can easily peek at this.

To fix this, smart networks use **LDAPS (LDAP over SSL/TLS), which uses TCP port 636 to secure directory authentication traffic.** This puts your password in a locked, secret envelope before sending it!

## Eliminating Password Fatigue: SSO and Federation

Let's do a quick math problem. If an employee has to log into their email, their work schedule, the company chat, and the file server, how many passwords do they need?
1. Count the individual systems the employee uses: 1 (email) + 1 (schedule) + 1 (chat) + 1 (files).
2. Add these up to find the total number of systems: 1 + 1 + 1 + 1 = 4 systems.
3. Multiply the total systems by the number of unique passwords needed for each: 4 systems * 1 password = 4 total passwords.

Having to memorize all these gets exhausting! **Single Sign-On reduces password fatigue by minimizing the number of credentials a user must remember.**

**Single Sign-On (SSO) allows a user to authenticate once and access multiple independent software systems.** It's like getting a wristband at an amusement park. You show your ticket once at the front gate, and then that wristband gets you on all the rides without having to show a ticket again!

But what if you visit a completely different park? **Identity federation extends Single Sign-On capabilities across different organizations and trust domains.**

Federation splits the job into two teams:
1. **An Identity Provider (IdP) creates, maintains, and manages identity information.** This is your home base. They know exactly who you are.
2. **A Service Provider (SP) relies on an Identity Provider to assert the identity of a user.** This is the new place you are visiting. The SP basically says, "I don't know you, but if your home base promises you are cool, I'll let you in!"

### The Languages of Federation: SAML, OAuth, and OIDC

To make the home base (IdP) and the new place (SP) talk, they have to speak the same language. Here are three main ones:

| Protocol | Primary Purpose | Data Format | Core Function |
| :--- | :--- | :--- | :--- |
| **SAML** | Authentication & Authorization | XML | Web-based SSO across enterprise domains |
| **OAuth 2.0** | Delegated Authorization | JSON | Granting apps access to resources |
| **OIDC** | User Authentication | JWT (JSON Web Tokens) | Adds identity context to OAuth |

First is SAML. **Security Assertion Markup Language (SAML) is an XML-based framework for exchanging authentication and authorization data.** **SAML is primarily used for web-based single sign-on across different administrative domains.**

How does it work? **SAML delegates the authentication process to an Identity Provider rather than the Service Provider.** When you go to a website, it sends you back to your home base to log in. Once you log in, your home base writes a digital permission slip. **A SAML assertion is a digitally signed XML document from an Identity Provider confirming a user's authentication.** You hand that signed permission slip to the new website, and they let you in!

What if a website just needs to grab a picture from your cloud drive, but you don't want to give it your password? We use OAuth! **OAuth is an open standard framework specifically designed for delegated authorization.** Think of OAuth like a special guest pass you give to a friend. The pass lets them play your video game, but it doesn't let them change your password or delete your save file. **OAuth allows an application to access resources hosted by other web apps on behalf of a user.**

It is super important to know that **the OAuth protocol handles authorization rather than user authentication.** It tells the app *what* it is allowed to touch, but it doesn't actually prove *who* the user is.

To fix that, developers made OIDC. **OpenID Connect (OIDC) is an identity layer built on top of the OAuth 2.0 protocol.** While OAuth gives out a permission pass, **OpenID Connect provides user authentication capabilities to the OAuth authorization framework** by adding an ID card.

**OpenID Connect issues a JSON Web Token (JWT) to securely transmit information about the authenticated user.** This token is like a digital ID badge that shares safe facts about you, like your email. Together, OAuth and OIDC handle both what you can do and who you are!

## Measuring Trust: NIST Special Publication 800-63

How do we score how safe a login system is? We look at the official rulebook.

**NIST Special Publication 800-63 defines technical requirements for federal digital identity services.** This rulebook breaks safety into three big scores:

1. **Identity Assurance Level (IAL) refers to the robustness of the identity proofing process under NIST 800-63.** This is about proving you are really you *before* you get an account. A low score means you just typed in an email. A high score means you showed your real-life passport to a human!
2. **Authenticator Assurance Level (AAL) defines the strength of the authentication process under NIST 800-63.** Once you have an account, how hard is it to log in? A low score is just a simple password. A high score means using a special physical security key plugged into your computer that hackers can't steal. Let's say a special key costs \$50 to buy; it's a small price to pay for a high AAL score!
3. **Federation Assurance Level (FAL) measures the strength of the assertion used in a federated transaction under NIST 800-63.** When your home base sends that digital permission slip to another site, how safe is the trip? A high score means the slip is locked up in code so nobody can peek at it while it travels across the internet.

When you put all this together—giving out accounts carefully, using least privilege, keeping everything in a secure directory, sharing logins safely across the web, and scoring it with NIST rules—you become a master of digital safety. You aren't just making accounts; you are building the ultimate defensive shield for your network!