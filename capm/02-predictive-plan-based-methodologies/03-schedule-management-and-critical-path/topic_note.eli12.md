Every big goal you want to achieve is a race against the clock! Whether you are building a giant LEGO castle, planning a multiplayer video game tournament, or organizing a school talent show, you need a plan for your time. This is where we learn about a special toolbox. The Project Schedule Management knowledge area includes the processes required to manage the timely completion of the project. You cannot just write down 100 chores on a piece of paper and hope they all naturally get done in time. We have to map out exactly how time flows so we know when our big project will be finished and where we might get stuck!

## Constructing the Schedule Model: The Precedence Diagramming Method

Before we can study our schedule, we have to build it. We do this using a very helpful drawing tool. The Precedence Diagramming Method is a technique used for constructing a schedule model. 

Think of it like a treasure map for your chores. In this map, the Precedence Diagramming Method represents project activities as nodes (which are usually just squares or boxes drawn on the paper). Then, the Precedence Diagramming Method graphically links activities by logical relationships to show the sequence of performance. That just means we draw arrows between the boxes to show the strict order of what we must do first, second, and third!

### Logical Relationships: The Rules of Connection

In our map, tasks do not happen all by themselves; they connect to each other. We decide exactly how one task hands off to another task using four specific rules:

1. **Finish-to-Start (FS):** A Finish-to-Start logical relationship means a successor activity cannot start until a predecessor activity has finished.
   * *Example:* You cannot start eating your pizza (the successor—what comes next) until the oven has finished baking it (the predecessor—what came before). This is the most common rule!
2. **Start-to-Start (SS):** A Start-to-Start logical relationship means a successor activity cannot start until a predecessor activity has started.
   * *Example:* If you and your friend are painting a huge banner, your friend cannot start painting the second half (successor) until you have started painting the first half (predecessor).
3. **Finish-to-Finish (FF):** A Finish-to-Finish logical relationship means a successor activity cannot finish until a predecessor activity has finished.
   * *Example:* Your soccer practice (successor) cannot finish until the coach's whistle-blowing (predecessor) has finished.
4. **Start-to-Finish (SF):** A Start-to-Finish logical relationship means a successor activity cannot finish until a predecessor activity has started.
   * *Example:* The babysitter cannot finish watching your little brother (successor) until your parents have started walking through the front door (predecessor).

### The Nature of Dependencies

Why do we connect tasks in a certain order? Sometimes it's physics, sometimes it's a rule, and sometimes it's just what we like best.

* **Mandatory dependencies** are logical relationships inherent in the nature of the project work. For example, you literally cannot put a roof on a treehouse before you build the walls! Also, mandatory dependencies are logical relationships that are contractually required. For instance, a signed agreement with your parents might say you must clean your room before you get your allowance.
* **Discretionary dependencies** are logical relationships established based on best practices. For instance, it is a best practice to do your math homework before your spelling homework when your brain is fresh. Also, discretionary dependencies are logical relationships established based on specific project team preferences. Your video game squad might just prefer to gather supplies before building a base, even if you don't strictly have to do it that way.
* **External dependencies** involve a logical relationship between project activities and non-project activities outside the project team's control. Waiting for the mail carrier to deliver your new video game before you can play it is an external dependency.
* **Internal dependencies** involve a logical relationship between project activities strictly within the control of the project team. If you decide to organize your trading cards before putting them in a binder, you and your brain are in total control of both tasks.

### Fine-Tuning Time: Leads and Lags

Sometimes, we need to tweak the timing between two tasks.
* A **lead** is the amount of time whereby a successor activity can be advanced with respect to a predecessor activity. Imagine you are making a giant sandwich. If you have a 1-minute lead, you can start putting the turkey on the bread 1 minute *before* your toaster is completely finished popping up the bread. You get a head start!
* A **lag** is the amount of time whereby a successor activity is delayed with respect to a predecessor activity. If you paint a model airplane, you have to wait 2 hours for it to dry before you can put the stickers on. That 2 hours of just waiting around with no active work is a lag.

## Finding the Rhythm: The Critical Path Method (CPM)

Now we get to the cool math part of scheduling. The Critical Path Method was originally developed in the late 1950s by Morgan R. Walker and James E. Kelley Jr. The Critical Path Method is a schedule network analysis technique used to estimate the minimum project duration.

Imagine you are cooking dinner. Making a salad takes 10 minutes, setting the table takes 5 minutes, but roasting a huge turkey takes 4 hours. It doesn't matter how fast you chop carrots, dinner won't be ready for at least 4 hours because of that turkey! 

The **critical path** is the sequence of activities representing the longest continuous path through a project network diagram. Because it is the longest path of work, the critical path determines the shortest possible time required to complete the entire project. The turkey is your critical path!

### The Forward and Backward Pass

To figure out our map, we do two sweeps over our drawing:

1. **The Forward Pass:** We sweep from the beginning of our project to the end. A forward pass calculates the Early Start dates for all project activities. Also, a forward pass calculates the Early Finish dates for all project activities.
   * The **Early Start date** is the earliest possible point in time an activity can begin based on schedule network logic.
   * The **Early Finish date** is the earliest possible point in time an activity can finish based on schedule network logic.
2. **The Backward Pass:** Now we start at the end and sweep backwards! A backward pass calculates the Late Start dates for all project activities. And a backward pass calculates the Late Finish dates for all project activities.
   * The **Late Start date** is the latest possible point in time an activity can start without delaying the project finish date.
   * The **Late Finish date** is the latest possible point in time an activity can finish without delaying the project finish date.

### Understanding Float (Slack)

When you compare your early dates to your late dates, you discover wiggle room! We call this wiggle room "float."

> **Total float** is the amount of time an activity can be delayed without delaying the overall project finish date.

Let's calculate total float step-by-step using the first formula:
1. Look at your task, for example, cleaning your room.
2. Find the Late Start date: Let's say you must start by Day 5 at the latest to keep your weekend free.
3. Find the Early Start date: You could start as early as Day 2.
4. The formula for total float is Late Start minus Early Start. 
5. Subtract your numbers: 5 - 2 = 3.
6. Your total float is 3 days! You have 3 days of wiggle room.

> An alternative formula for total float is Late Finish minus Early Finish.

But be super careful! Activities on the critical path typically have zero total float. That means zero wiggle room. If you delay the turkey by one hour, dinner is late by one hour.

Do not mix up Total Float with **Free Float**. Free float is the amount of time an activity can be delayed without delaying the Early Start date of any immediate successor activity. It is just the wiggle room between one task and the very next task in line!

### Schedule Risk and Multiple Paths

Sometimes a project is extra complicated. A project schedule network diagram can have multiple critical paths running concurrently. This is like roasting two turkeys at the exact same time!

The existence of multiple critical paths increases the overall schedule risk of a project. If you have three long paths of work, that means there are three different places where something could go wrong and make your whole project late.

You also have to watch out for the "almost-longest" paths. A **near-critical path** is a sequence of activities with a very small amount of total float. Why do we care? Because a near-critical path will become the new critical path if its activities experience delays exceeding their total float. If it only had 1 hour of wiggle room, and you delay it by 2 hours, boom! It is now the longest path holding up your project.

## Measuring Reality Against the Plan: Earned Value Management

Making a map is great, but what happens when you actually start working and things get messy? We have to measure our real progress against our plan. We use Earned Value Management metrics to do this.

To score our progress, we use two budget values linked to time:
* **Planned Value** represents the authorized budget assigned to the scheduled work expected to be accomplished. Think of it as the allowance you *planned* to earn by today.
* **Earned Value** represents the authorized budget assigned to the scheduled work that has actually been completed. Think of it as the allowance you *actually* earned because you finished the chores.

### Schedule Variance (SV)

**Schedule Variance** is an Earned Value Management metric used to measure overall schedule performance. It just asks: How many points are we off by?

Let's calculate Schedule Variance step-by-step:
1. Find your Earned Value: Let's say you actually finished \$20 worth of chores.
2. Find your Planned Value: You planned to have finished \$25 worth of chores by today.
3. The formula for Schedule Variance is Earned Value minus Planned Value.
4. Subtract the numbers: 20 - 25 = -5.
5. Your Schedule Variance is -5.

| If Schedule Variance is... | It means... |
| :--- | :--- |
| **Positive (> 0)** | A positive Schedule Variance indicates that the project is currently ahead of schedule. You are beating the game! |
| **Exactly Zero (= 0)** | A Schedule Variance of exactly zero indicates that the project is perfectly on schedule. |
| **Negative (< 0)** | A negative Schedule Variance indicates that the project is currently behind schedule. You need to catch up! |

### Schedule Performance Index (SPI)

While Variance is like a subtraction score, the **Schedule Performance Index** is an Earned Value Management metric used to measure schedule efficiency. It tells you your speed rating!

Let's calculate the Schedule Performance Index step-by-step:
1. Find your Earned Value: You finished \$30 worth of chores.
2. Find your Planned Value: You planned to finish \$20 worth of chores.
3. The formula for the Schedule Performance Index is Earned Value divided by Planned Value.
4. Divide the numbers: 30 / 20 = 1.5.
5. Your Schedule Performance Index is 1.5!

| If Schedule Performance Index is... | It means... |
| :--- | :--- |
| **Greater than 1.0** | A Schedule Performance Index greater than 1.0 indicates more work was completed than originally planned. You are super fast! |
| **Exactly equal to 1.0** | A Schedule Performance Index exactly equal to 1.0 indicates the project work is proceeding exactly as planned. |
| **Less than 1.0** | A Schedule Performance Index less than 1.0 indicates less work was completed than originally planned. You are moving too slow! |

## When Time Runs Short: Schedule Compression Techniques

Imagine you look at your score and you are falling behind, but you still have to finish the project before your family gets home! What do you do? 

You use tricks to squeeze time. **Schedule compression techniques** shorten the project schedule duration without reducing the project scope. This means you still have to do all the work (no skipping chores!), you just have to find a way to finish faster. We have two main tricks:

### 1. Crashing
**Crashing** is a schedule compression technique used to shorten the schedule duration by adding extra resources. 
* *The Reality:* If it takes you 4 hours to clean the garage alone, crashing means paying three of your friends to help so you finish in 1 hour. Because you had to pay your friends, the crashing schedule compression technique typically results in increased overall project costs. You are spending more allowance to go faster!

### 2. Fast Tracking
**Fast tracking** is a schedule compression technique where activities normally done in sequence are instead performed in parallel.
* *The Reality:* Normally, you wait for your brother to finish vacuuming before you mop the floor. Fast tracking means you start mopping right behind him at the exact same time!
* *The Risk:* Because you are doing things at the same time, the fast tracking schedule compression technique often results in increased project risk. What if your brother steps back onto your wet floor with dirty shoes? You will have to mop again! This is why the fast tracking schedule compression technique frequently results in increased project rework.

### Final Synthesis

Being great at Project Schedule Management means treating time like puzzle pieces. By mapping out arrows and rules (Precedence Diagramming Method), finding the longest string of tasks (Critical Path Method), keeping score with math (Schedule Variance and Schedule Performance Index), and knowing how to hit the turbo button when time runs out (Crashing and Fast Tracking), you turn from a kid just watching the clock into a master of finishing big goals!