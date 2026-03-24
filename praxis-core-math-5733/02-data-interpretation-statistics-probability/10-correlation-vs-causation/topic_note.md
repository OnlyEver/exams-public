# [Praxis Core](https://en.wikipedia.org/wiki/Praxis_test) Math Study Guide: Correlation vs. Causation

Hello there! Let’s talk about one of the most beautiful, dangerous, and frequently misunderstood ideas in all of [mathematics](https://en.wikipedia.org/wiki/Mathematics) and everyday [logic](https://en.wikipedia.org/wiki/Logic). 

Imagine you are a [detective](https://en.wikipedia.org/wiki/Detective), or perhaps an [alien](https://en.wikipedia.org/wiki/Extraterrestrial_life) looking down at [Earth](https://en.wikipedia.org/wiki/Earth), trying to figure out the rules of how our world operates. You start measuring things, and you notice a pattern: whenever a town has more [fire trucks](https://en.wikipedia.org/wiki/Fire_engine) at a scene, there is more fire damage! You leap to a conclusion: *Aha! Fire trucks must be causing the damage!* 

Now, you and I know that’s ridiculous. But mathematical [data](https://en.wikipedia.org/wiki/Data) doesn't know it. Data just sees two numbers moving together. Understanding the difference between numbers that merely move together and numbers where one actually *forces* the other to move is the entire difference between good [science](https://en.wikipedia.org/wiki/Science) and utter nonsense. 

For the [Praxis Core Mathematics exam](https://en.wikipedia.org/wiki/Praxis_test), you must master this distinction. We are going to explore how to read these [statistical](https://en.wikipedia.org/wiki/Statistics) patterns, how to find the hidden tricks [nature](https://en.wikipedia.org/wiki/Nature) plays on us, and how to prove what is actually causing what. Let’s dive in.

---

## Part 1: The Dance of Variables (Understanding Correlation)

Before we talk about cause and effect, we have to talk about [observation](https://en.wikipedia.org/wiki/Observation). When we measure the world, we often look at how two things—two *[variables](https://en.wikipedia.org/wiki/Dependent_and_independent_variables)*—behave relative to each other. 

> **Correlation** is a statistical relationship indicating that two variables fluctuate together. 

It simply means that when Variable A does something, Variable B tends to do something predictable, too. They are dancing to the same beat. But correlation comes in a few different flavors:

| Type of Correlation | What It Means | Real-World Example |
| :--- | :--- | :--- |
| **Positive Correlation** | A positive correlation means that as one variable increases, the other variable also increases. | As the number of hours you spend studying increases, your exam score increases. |
| **Negative Correlation** | A negative correlation means that as one variable increases, the other variable decreases. | As the miles driven on your car's tires increase, the amount of tread remaining on the tires decreases. |

### Visualizing the Dance: [Scatterplots](https://en.wikipedia.org/wiki/Scatter_plot)
How do we actually *see* this dance? We graph it. **[Scatterplots](https://en.wikipedia.org/wiki/Scatter_plot)** visually display the statistical correlation between two [quantitative variables](https://en.wikipedia.org/wiki/Quantitative_research). By plotting one variable on the [x-axis](https://en.wikipedia.org/wiki/Cartesian_coordinate_system) and the other on the [y-axis](https://en.wikipedia.org/wiki/Cartesian_coordinate_system), you get a cloud of dots. 
* If the dots drift upward from left to right, you are looking at a positive correlation.
* If the dots drift downward from left to right, you have a negative correlation.
* If the dots look like a random blast from a [shotgun](https://en.wikipedia.org/wiki/Shotgun), there is little to no correlation.

### Measuring the Dance: The Correlation Coefficient
But [scientists](https://en.wikipedia.org/wiki/Scientist) and [mathematicians](https://en.wikipedia.org/wiki/Mathematician) don’t just like looking at pictures; we like [precision](https://en.wikipedia.org/wiki/Accuracy_and_precision). We want to know exactly *how strong* the relationship is. 

To do this, we use a beautiful mathematical tool. **The correlation coefficient mathematically measures the strength of a [linear relationship](https://en.wikipedia.org/wiki/Linearity) between two variables.** 

> **The Correlation Coefficient (r)** is a numerical value ranging strictly from negative one to positive one ($-1 \le r \le 1$). 

* An $r$ of **+1** means a perfect positive correlation. They move in lockstep.
* An $r$ of **-1** means a perfect negative correlation. Like a perfect seesaw: one goes up, the exact other goes down.
* An $r$ of **0** means absolutely zero linear relationship. Total chaos.

---

## Part 2: The Holy Grail (Understanding [Causation](https://en.wikipedia.org/wiki/Causality))

Now we reach the most critical rule in [statistics](https://en.wikipedia.org/wiki/Statistics)—a rule so important it should be [tattooed](https://en.wikipedia.org/wiki/Tattoo) on the arm of every [researcher](https://en.wikipedia.org/wiki/Researcher). 

> **The presence of a correlation between two variables does not prove that one variable causes the other to change.**

Why? Because correlation is merely a description of *what* is happening. **[Causation](https://en.wikipedia.org/wiki/Causality)**, on the other hand, indicates that a change in one variable *directly produces* a specific effect in another variable. Causation is the *why*. 

If you want to argue that Variable A causes Variable B, **a strong mathematical correlation is logically insufficient on its own to justify a claim of causation.** Just because two things happen together doesn't mean one is pulling the strings. 

Let's look at the fascinating, tricky ways the [universe](https://en.wikipedia.org/wiki/Universe) can fool us into seeing a cause where none exists.

---

## Part 3: When the Universe Lies to You (The Pitfalls)

If correlation doesn't mean causation, what else could be going on? When you see two variables highly correlated, there are three major statistical traps you must watch out for.

### Trap 1: The [Confounding Variable](https://en.wikipedia.org/wiki/Confounding)
This is the most common trick in the book. **[Confounding variables](https://en.wikipedia.org/wiki/Confounding)** are unmeasured external factors that independently affect both of the correlated variables. 

Think of a [puppeteer](https://en.wikipedia.org/wiki/Puppetry) holding two puppets. Puppet A and Puppet B are moving in perfect harmony (a strong correlation). But Puppet A isn't moving Puppet B. The unmeasured external factor—the puppeteer—is moving *both*. **The presence of a confounding variable can create a false appearance of a direct causal relationship between two observed variables.**

**The Classic Example:**
Let's look at real data. **[Ice cream](https://en.wikipedia.org/wiki/Ice_cream) sales and [sunburn](https://en.wikipedia.org/wiki/Sunburn) rates exhibit a positive statistical correlation in real-world data.** The more ice cream a city buys, the more sunburns [hospitals](https://en.wikipedia.org/wiki/Hospital) treat. They rise and fall together perfectly. 

Now, imagine someone looking at this data and declaring: *"My god! Eating ice cream causes humans to burst into sunburns! We must ban ice cream!"* 

**Assuming ice cream consumption causes sunburns based on their positive correlation is a common [logical fallacy](https://en.wikipedia.org/wiki/Fallacy).** Why? Because of a confounding variable. **A confounding variable like hot [weather](https://en.wikipedia.org/wiki/Weather) can independently cause increases in both ice cream sales and sunburn rates.** When it's hot outside, people buy more ice cream. When it's hot outside, people go to the beach and get sunburnt. The heat is the hidden puppeteer driving both variables.

### Trap 2: Reverse Causation
Sometimes there *is* a causal relationship, but you have it completely backward. **Reverse causation occurs when the assumed direction of cause and effect between two variables is actually the opposite of reality.**

Remember our fire truck example? More fire trucks at a scene is positively correlated with more fire damage. But the trucks don't cause the damage; the size of the [fire](https://en.wikipedia.org/wiki/Fire) causes the [dispatcher](https://en.wikipedia.org/wiki/Dispatcher) to send more trucks. The effect is actually the cause!

### Trap 3: Random Coincidence
If you have enough data, the universe will occasionally throw you a curveball that means absolutely nothing at all. **Two entirely unrelated variables can exhibit a strong statistical correlation purely by random coincidence.**

Statistical researchers have famously pointed out that the [per capita](https://en.wikipedia.org/wiki/Per_capita) consumption of [cheese](https://en.wikipedia.org/wiki/Cheese) in the [United States](https://en.wikipedia.org/wiki/United_States) has mathematically correlated with the number of people who died by becoming tangled in their bedsheets. Does eating cheese make your sheets hostile? No! If you measure millions of random variables over time, just by sheer mathematical [luck](https://en.wikipedia.org/wiki/Luck), some of them will line up perfectly. It is pure, glorious nonsense.

---

## Part 4: The Detective's Toolkit (How We Know for Sure)

So, if correlation doesn't prove causation, how does a scientist or a mathematician *ever* prove that one thing causes another? We have to rely on the right tools. We must understand the profound difference between just looking at the world, and actively poking it.

### [Observational Studies](https://en.wikipedia.org/wiki/Observational_study): Looking, Not Touching
**[Observational studies](https://en.wikipedia.org/wiki/Observational_study) gather data without manipulating the variables.** You just sit back with your clipboard and record what is naturally happening in the world. 

* **What they CAN do:** **Observational studies can establish mathematical correlations between variables.** They are great for finding patterns, like the link between smoking habits and [lung capacity](https://en.wikipedia.org/wiki/Lung_volumes) over decades. 
* **What they CANNOT do:** Because you are just watching, you aren't controlling for hidden puppeteers. Therefore, **observational studies cannot definitively establish causation between variables.**

### Controlled Experiments: Poking the Universe
If you want to prove causation, you have to get your hands dirty. **Controlled experiments measure the effect of an actively manipulated [independent variable](https://en.wikipedia.org/wiki/Dependent_and_independent_variables) on a [dependent variable](https://en.wikipedia.org/wiki/Dependent_and_independent_variables).** 

You don't just ask people if they eat ice cream and measure their sunburns. You take two groups of people in a windowless room. You forcefully feed one group ice cream (manipulating the independent variable) and give the other group nothing. Then you shine identical [UV lights](https://en.wikipedia.org/wiki/Ultraviolet) on them to measure sunburns (the dependent variable). Because *you* controlled the environment, the weather can no longer act as a confounding variable!

The gold standard of this process relies on randomness. **Randomized controlled experiments are the primary statistical method used to establish true causation between variables.** By [randomly assigning](https://en.wikipedia.org/wiki/Random_assignment) subjects to different groups, you mathematically ensure that all the hidden confounding variables (like [genetics](https://en.wikipedia.org/wiki/Genetics), [diet](https://en.wikipedia.org/wiki/Diet_%28nutrition%29), sleep) are evenly distributed, isolating the pure causal effect of your test variable.

---

## Part 5: Passing the Praxis (Evaluating Scenarios)

On the Praxis Core exam, you won't just be asked for definitions. You will be given real-world scenarios and asked to evaluate them. 

When you are reading a test question where someone claims "Variable A causes Variable B," put on your detective hat. **Evaluating a scenario for causation requires identifying alternative explanations for the observed relationship.** 

Ask yourself:
1. *Is there a [confounding variable](https://en.wikipedia.org/wiki/Confounding)?* (What else could cause both of these to happen?)
2. *Could the causation be reversed?* (Is B actually causing A?)
3. *Was this an [observational study](https://en.wikipedia.org/wiki/Observational_study), or a randomized controlled experiment?*

To legitimately claim causation, you can't just find an alternative explanation; you have to destroy it. **Evaluating a scenario for causation requires ruling out alternative explanations for the observed relationship.** If an experiment doesn't rule out the confounding variables, then the causal claim is unjustified.

### Summary Checklist for Exam Day:
* **Fluctuate together?** That's correlation.
* **Directly produces an effect?** That's [causation](https://en.wikipedia.org/wiki/Causality). 
* **Just a strong math link?** Not enough to prove causation.
* **Look but don't touch?** [Observational study](https://en.wikipedia.org/wiki/Observational_study) (correlation only).
* **Actively manipulate and randomize?** Controlled experiment (proves causation).

The universe is full of fascinating patterns. As an educator and a mathematical thinker, your job is to look past the superficial dance of the numbers and uncover the hidden truth of *why* things happen. When you see a correlation, admire it—but demand proof before you call it a cause. Good luck!