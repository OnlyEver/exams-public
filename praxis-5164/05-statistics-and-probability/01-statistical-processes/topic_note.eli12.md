Imagine finding out the favorite video game of everyone in a giant school with thousands of kids. Asking everyone takes forever. Instead, you can ask a small group of 50 kids and figure out the whole school's favorite games using math. This is the superpower of statistics! It's super important to learn how to ask the right questions and pick the right group of kids so we don't get tricked by bad data online or on TV. Let's learn how this works!

## The Nature of a Statistical Question

In regular math, there is usually one exact answer. But in statistics, we deal with answers that change or vary. 

A **statistical question is a question that anticipates variability in the data collected to answer the question**. "Variability" just means that the answers will be different from person to person. 

For example, **the question 'How old am I?' is not a statistical question because the answer does not vary**. You have one exact age. 

But, **the question 'How old are the students in my school?' is a statistical question because the ages of the students will vary**. Some kids might be 11, some 12, some 14. 

Because the answers vary, **data collected to answer a statistical question will have a distribution with a center, spread, and overall shape**. Imagine stacking blocks for every student's age. The "shape" might look like a hill, the "center" tells you the middle age, and the "spread" shows how far apart the youngest and oldest kids are.

## Populations, Samples, and the Dream of the Census

Before we count anything, we have to know who we are counting. 

> **Population**: **A population is the entire group of individuals or objects under study.** If you want to know what kind of pizza 7th graders like, every 7th grader in your town is the population.
> 
> **Sample**: **A sample is a subset of individuals or objects selected from a population.** If you only ask your own math class about their favorite pizza, your class is the sample.

Sometimes, people try to ask absolutely everyone. **A census is a study that attempts to collect data from every individual in a population.** A census gives you a perfect answer, but it is really hard to pull off because asking thousands of people takes way too much time and money! That is why we usually use samples instead.

## The Pitfalls of Bad Sampling: Bias

If you want to know if your hot chocolate has enough sugar, you don't drink the whole mug (a census). You take one sip (a sample). But what if you didn't stir it, and all the sugar is stuck at the bottom? Your sip will taste bitter, and you'll get the wrong idea!

In statistics, an unstirred mug gives you a bad sample. **A biased sample systematically overrepresents or underrepresents certain segments of a population.** It means your sample is unfair from the start.

There are two really common bad ways to pick a sample (these are non-random methods):

1. **Convenience sampling is a non-random method where researchers select individuals who are easiest to reach.** Imagine you want to know the whole school's favorite sport, but you only ask the kids on your soccer team because they are standing right next to you. **Convenience sampling typically leads to a biased sample** because the easy-to-reach kids (soccer players) don't represent what everyone else likes.
2. **Voluntary response sampling is a non-random method where individuals choose themselves to participate in a study.** Think of an online poll asking, "Is the new superhero movie the worst movie ever?" People who don't care won't vote. **Voluntary response sampling typically overrepresents individuals with strong opinions**—usually people who are super angry or super happy.

## The Gold Standard: Random Sampling

To fix the unstirred hot chocolate, we need to stir it! In statistics, "stirring" means picking people by pure chance. **Random sampling uses a chance process to determine which members of a population are included in a sample.** It's like rolling dice or drawing names from a hat.

The best basic way to do this is a Simple Random Sample. For a sample to be a true simple random sample, it needs two rules:
1. **In a simple random sample, every individual in a population has an equal chance of being selected.**
2. **In a simple random sample, every possible group of a given size has an equal chance of being selected.**

Imagine putting all 500 kids' names in a giant bowl, mixing it up, and drawing 20 names blindfolded. Every single kid has the exact same chance of being picked, and every possible combination of 20 kids has the same chance, too!

### Advanced Random Sampling Techniques

Sometimes, we need slightly more advanced ways to pick names out of a hat to make sure all types of groups are included. 

| Method | How It Works | Everyday Analogy |
| :--- | :--- | :--- |
| **Stratified Random Sampling** | **Stratified random sampling involves dividing a population into homogeneous groups** (groups where everyone is similar). Then, **in stratified random sampling, a simple random sample is drawn from each separate homogeneous group**. | Think of dividing the school into 6th, 7th, and 8th graders (homogeneous by age). Then, pick names out of a hat to survey 10 kids from *each* grade to make sure every grade gets a voice. |
| **Cluster Sampling** | **Cluster sampling involves dividing a population into heterogeneous groups** (groups where everyone is mixed up and different). **In cluster sampling, entire heterogeneous groups are randomly selected and all individuals within the selected groups are surveyed.** | Think of homerooms, where each room has a mix of kids (heterogeneous). Put the homeroom numbers in a hat, pull out two rooms, and survey *every single kid* inside those two rooms. |
| **Systematic Random Sampling** | **Systematic random sampling involves selecting every kth individual from a population list after a random starting point.** | Take an alphabetical list of everyone in school. Roll a die to pick a random starting number (like 3). Then survey every 5th kid on the list after that (the 8th, 13th, 18th kid, etc.). |

## When Things Still Go Wrong: Sources of Bias

Even when you do a great job picking a random sample, human mistakes happen. You need to watch out for these errors:

* **Undercoverage bias occurs when the method of choosing a sample systematically excludes some part of a population.** Imagine surveying kids about their favorite video games, but you only hand out the survey at an Xbox club. You just excluded anyone who only plays PlayStation or Nintendo!
* **Nonresponse bias occurs when selected individuals cannot be contacted or refuse to participate in a study.** If you pick 50 kids randomly to fill out a survey, but 20 of them leave it in their backpacks and ignore you, those missing 20 kids create nonresponse bias.
* **Response bias occurs when the data collection method or question phrasing consistently produces misleading or untruthful answers.** If a teacher asks the class, "Raise your hand if you secretly cheated on my test," no one will raise their hand! The scary way the question is asked causes kids to lie.

## Parameters, Statistics, and the Leap of Inference

Why do we do all this work? Because we want to know a secret about the big group, but we only have time to look at a small group. Let's learn two matching words:

> **Parameter**: **A parameter is a numerical characteristic of an entire population.** (Remember: **P**arameter matches **P**opulation).
> 
> **Statistic**: **A statistic is a numerical characteristic calculated from a sample.** (Remember: **S**tatistic matches **S**ample).

If the true number of all kids in the school who like tacos is 70%, that 70% is a parameter. It is the big, hidden truth. If you ask a sample of 20 kids, and 75% of them like tacos, that 75% is a statistic. 

**Statistical inference is the process of using data from a sample to draw conclusions about an entire population.** It's like being a detective! In this process, **a sample statistic serves as an estimate for an unknown population parameter**. We use the 75% from our sample to guess that the whole school is probably somewhere near that number. 

But remember: **random sampling allows researchers to generalize conclusions from a sample to the broader population**. If you don't use random sampling, you can't guess what the big group thinks!

## The Laws of Variability and Sample Size

If you pick 10 kids at random and ask their favorite color, and then I pick 10 *different* kids at random, we will probably get slightly different answers. This is totally normal! **Sampling variability is the phenomenon where different random samples of the same size from the same population produce different sample statistics.**

How do we make our guesses better? Ask more people! 
* **Increasing the size of a random sample reduces the sampling variability.** The answers won't bounce around as much.
* Because the answers don't bounce around as much, **a larger random sample provides a more precise estimate of a population parameter than a smaller random sample.**

But wait! Asking a lot of people doesn't fix a bad survey. **Increasing the sample size does not correct for sampling bias.** If your hot chocolate is unstirred, taking a giant gulp from the bottom instead of a tiny sip won't help you figure out how the top tastes. Because of this, **a large biased sample will consistently produce misleading conclusions about a population.** A totally unfair survey of 1,000 people is much worse than a perfectly fair, random survey of 50 people!

## Scaling Up: Proportional Reasoning and Margin of Error

When we get our statistic from a sample, we know it might not be perfect. We use a safety net called the margin of error.

**The margin of error describes the expected maximum difference between a sample statistic and the true population parameter.** If a survey says 50% of kids want a longer recess, but it has a margin of error of 5%, that means the real answer is probably somewhere between 45% and 55%. If you want a smaller safety net, you just need a bigger sample, because **the margin of error decreases as the sample size increases**. 

Finally, we use proportional reasoning. **Proportional reasoning scales up a sample proportion to predict outcomes for an entire population.** It's like taking a pizza recipe meant for 2 people and doubling it so you can feed 4 people.

Here is an example: **If 20 percent of a random sample prefer a specific outcome, proportional reasoning predicts that 20 percent of the entire population prefers that outcome.**

Let's do the math step-by-step:
1. Identify the percentage from your random sample. In this case, 20% of kids love algebra.
2. Identify the total number of kids in the entire population. Let's say your school has 1,500 kids.
3. Turn the percentage into a simple decimal so you can multiply. To do this, divide by 100. So, 20 / 100 = 0.20.
4. Multiply that decimal by the total population to scale it up. The math is: 0.20 * 1,500.
5. Calculate the final answer: 0.20 * 1,500 = 300. 

By scaling up, you can predict that exactly 300 students in the whole school love algebra!