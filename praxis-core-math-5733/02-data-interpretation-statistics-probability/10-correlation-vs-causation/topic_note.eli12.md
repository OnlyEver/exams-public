# Praxis Core Math Study Guide: Correlation vs. Causation

Hello there! Let’s talk about a really cool math idea that tricks people all the time in everyday life. 

Imagine you are playing a video game. You notice a weird pattern: every time you wear your lucky blue socks, you beat the boss level. You jump up and say, *“Aha! My blue socks give my thumbs super speed!”* 

Now, you and I know that’s silly. Your socks don't control your video game skills. But math data doesn't know that. Data just sees two things happening at the exact same time. Figuring out the difference between two things that just happen to move together, and two things where one actually *makes* the other happen, is what good science is all about!

In math, you need to understand this difference perfectly. We are going to explore how to read these number patterns, how to spot the tricks nature plays on us, and how to prove what is actually making things happen. Let’s dive in.

---

## Part 1: The Dance of Variables (Understanding Correlation)

Before we talk about cause and effect, we have to talk about how we observe the world. When we measure things, we often look at how two different things—called *variables*—behave next to each other. 

In math terms, **correlation is a statistical relationship indicating that two variables fluctuate together.** 

That’s a big way of saying that when Variable A does something, Variable B tends to do something predictable, too. They are dancing to the same beat. But this dance comes in a couple of different styles:

| Type of Correlation | What It Means | Everyday Example |
| :--- | :--- | :--- |
| **Positive Correlation** | **A positive correlation means that as one variable increases, the other variable also increases.** | As the number of extra chores you do goes up, your weekly allowance money goes up. |
| **Negative Correlation** | **A negative correlation means that as one variable increases, the other variable decreases.** | As the number of hours you play games on your phone goes up, your phone’s battery life goes down. |

### Visualizing the Dance: Scatterplots
How do we actually *see* this dance? We draw a graph. **Scatterplots visually display the statistical correlation between two quantitative variables.** 

Here is a step-by-step example of how to make a scatterplot out of data:
1. Pick your two variables. Let's use Variable A: "Slices of Pizza Eaten" and Variable B: "How Full You Feel" (measured on a scale of 1 to 10).
2. Look at your first piece of data. Let's say you ate 3 slices, and your fullness is at a 6.
3. Move your finger right along the bottom line (the x-axis) until you hit the number 3 for slices eaten.
4. From that 3, move your finger straight up until you are even with the number 6 on the side line (the y-axis) for fullness.
5. Draw a single dot right there. 

If you do this step-by-step for a lot of different meals, you get a cloud of dots!
* If the dots drift upward from left to right, you are looking at a positive correlation.
* If the dots drift downward from left to right, you have a negative correlation.
* If the dots look like sprinkles randomly thrown on a cupcake, there is no correlation.

### Measuring the Dance: The Correlation Coefficient
Math fans like to be very precise. We don’t just want to look at a picture; we want to know exactly *how strong* the connection is. 

To do this, we use a special number. **The correlation coefficient mathematically measures the strength of a linear relationship between two variables.** 

**The correlation coefficient is a numerical value ranging strictly from negative one to positive one.** 

* A score of **+1** means a perfect positive correlation. The two things always go up together perfectly.
* A score of **-1** means a perfect negative correlation. Like a perfect seesaw: as one goes exactly up, the other goes exactly down.
* A score of **0** means absolutely zero connection. Total randomness.

---

## Part 2: The Holy Grail (Understanding Causation)

Now we reach the single most important rule in statistics. It's so important that you should always remember it:

**The presence of a correlation between two variables does not prove that one variable causes the other to change.**

Why? Because correlation just tells us *what* is happening. **Causation indicates that a change in one variable directly produces a specific effect in another variable.** Causation is the *why*. It means one thing is physically making the other thing happen.

If you want to argue that Variable A makes Variable B happen, you need more proof. **A strong mathematical correlation is logically insufficient on its own to justify a claim of causation.** Just because two things happen together doesn't mean one is bossing the other around. 

Let's look at the tricky ways the world can fool us into seeing cause and effect where there is none.

---

## Part 3: When the Universe Lies to You (The Pitfalls)

If correlation doesn't mean causation, what else could be going on? When you see two variables moving together, you must watch out for three big traps.

### Trap 1: The Confounding Variable
This is the most common trick. **Confounding variables are unmeasured external factors that independently affect both of the correlated variables.** 

Think of a person holding two video game controllers, pretending that moving Controller A is making Controller B move. Controller A isn't really moving Controller B! The unmeasured external factor—the person's hands—is moving *both* of them. **The presence of a confounding variable can create a false appearance of a direct causal relationship between two observed variables.**

**The Classic Example:**
Let's look at real-world numbers. **Ice cream sales and sunburn rates exhibit a positive statistical correlation in real-world data.** The more ice cream a town buys, the more sunburns people get. They go up and down perfectly together. 

Now, imagine someone looking at this data and yelling: *"Oh no! Eating ice cream makes your skin burn! We must stop eating ice cream!"* 

**Assuming ice cream consumption causes sunburns based on their positive correlation is a common logical fallacy.** That means it's a big mistake in thinking! Why? Because of a confounding variable. **A confounding variable like hot weather can independently cause increases in both ice cream sales and sunburn rates.** When it's super hot outside, people buy lots of ice cream. When it's super hot outside, people also go to the beach and get sunburnt. The summer heat is the hidden factor driving both things at the same time.

### Trap 2: Reverse Causation
Sometimes things *do* cause one another, but you have it totally backward. **Reverse causation occurs when the assumed direction of cause and effect between two variables is actually the opposite of reality.**

Imagine noticing that every time you see a ton of umbrellas open outside, the grass gets wet. You might think, "Wow, open umbrellas cause the grass to get wet!" Nope! The wet rain causes people to open their umbrellas. The effect is actually the cause!

### Trap 3: Random Coincidence
If you collect enough numbers, sometimes things line up just by silly luck. **Two entirely unrelated variables can exhibit a strong statistical correlation purely by random coincidence.**

For example, math nerds once found that the amount of cheese people eat in a year matched up perfectly with how many people bought a specific brand of shoe. Does eating cheese make you buy shoes? No! If you test thousands of random things, pure math luck guarantees that a few of them will look like they are dancing together, even when they have nothing to do with each other.

---

## Part 4: The Detective's Toolkit (How We Know for Sure)

So, if correlation doesn't prove causation, how does a scientist *ever* prove that one thing causes another? We must use the right tools. 

### Observational Studies: Looking, Not Touching
**Observational studies gather data without manipulating the variables.** You just sit on a bench with a notebook and write down what you see happening normally. 

* **What they CAN do:** **Observational studies can establish mathematical correlations between variables.** They are great for spotting that kids who play soccer also tend to drink a lot of water.
* **What they CANNOT do:** Because you are just watching, you aren't controlling for hidden factors (like how hot it is outside). Because of that, **observational studies cannot definitively establish causation between variables.**

### Controlled Experiments: Poking the Universe
If you want to prove that one thing causes another, you have to run a test. **Controlled experiments measure the effect of an actively manipulated independent variable on a dependent variable.** 

You don't just ask people if they eat ice cream and check for sunburns. You take two groups of people into a dark room where there is no sun. You give one group ice cream (you *manipulate* the independent variable) and give the other group nothing. Then you shine special lights on them to measure their skin (the dependent variable). Because *you* control the room, the outside weather can't be a confounding variable anymore!

To make this test perfect, scientists use random choices. **Randomized controlled experiments are the primary statistical method used to establish true causation between variables.** By randomly picking who gets the ice cream and who doesn't, you make sure that all the hidden factors (like genetics or what they ate for breakfast) are split evenly, letting you see the true cause and effect.

---

## Part 5: Passing the Praxis (Evaluating Scenarios)

On your math test, you won't just memorize words. You will read stories and be asked to figure out what is really going on. 

When you read a question where someone claims "Variable A causes Variable B," put on your detective hat. **Evaluating a scenario for causation requires identifying alternative explanations for the observed relationship.** 

Ask yourself:
1. *Is there a confounding variable?* (Could something else be causing both?)
2. *Is it backward?* (Is Variable B really causing Variable A?)
3. *Did they just watch, or did they run a randomized experiment?*

To prove causation, finding another explanation isn't enough; you have to prove the other explanation is wrong. **Evaluating a scenario for causation requires ruling out alternative explanations for the observed relationship.** If an experiment doesn't block out the confounding variables, their claim isn't fair!

### Summary Checklist for Exam Day:
* **Fluctuate together?** That's correlation.
* **Directly produces an effect?** That's causation. 
* **Just a strong math link?** Not enough to prove causation.
* **Look but don't touch?** Observational study (shows correlation only).
* **Actively manipulate and randomize?** Controlled experiment (proves causation).

The world is full of cool math patterns! As you learn more, your job is to look past the simple numbers and find out *why* things really happen. When you see two things dancing together, it's okay to say they are correlated—but always demand proof before you say one caused the other!