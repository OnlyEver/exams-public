Imagine walking into your middle school on a Monday morning. One student walks in yawning because they stayed up until 2:00 AM playing video games; another student walks in wide awake after getting nine hours of sleep. We might naturally wonder: is there a connection between how many hours of sleep you get and your score on a math quiz the next day? Or think about your classes: is a student’s grade level connected to whether or not they play a school sport?

To figure this out, we can't just look at one piece of information anymore. We aren't just asking, "What is the average test score?" or "How many students play sports?" We are asking how two different traits match up or affect each other. This is called bivariate data ("bi" means two, and "variate" means variables). Our goal here is to learn how to spot these hidden connections, whether they are numbers in a table or dots on a graph!

## The Architecture of Categorical Bivariate Data

Sometimes, we group data by categories instead of numbers. Categorical variables are just ways to put people or things into groups, like "Grade Level" or "Lunch Choice." When we want to look at two categories at the same time, we use a special chart. **A two-way frequency table displays the frequencies of two categorical variables collected from the same set of subjects.** 

Let's look at a group of 100 middle schoolers. We are looking at two categorical variables: Grade Level (7th Grade vs. 8th Grade) and Sports (On a Team vs. Not on a Team).

| | On a Team | Not on a Team | **Total** |
| :--- | :---: | :---: | :---: |
| **7th Grade** | 15 | 35 | **50** |
| **8th Grade** | 40 | 10 | **50** |
| **Total** | **55** | **45** | **100** |

This chart is super helpful when you break down its parts. 

### Joint and Marginal Frequencies
Look at the inner numbers of the chart—the 15, 35, 40, and 10. **The entries located in the inner body cells of a two-way frequency table are called joint frequencies.** These numbers tell us a very specific story. **Joint frequencies represent the number of subjects that share a specific characteristic from each of the two categorical variables.** For example, the joint frequency of 40 tells us the exact number of students who are simultaneously *8th Graders* AND *On a Team*.

Now look at the outer edges of the table. **The sums of the individual rows and individual columns in a two-way frequency table are called marginal frequencies.** The 50 7th Graders, 50 8th Graders, 55 kids On a Team, and 45 kids Not on a Team are our margins. They only tell us the total for a single group, ignoring the other category.

Finally, look at the bottom right corner at the 100. **The grand total in a two-way frequency table is the sum of all joint frequencies** (you also get this number by adding up the row marginal frequencies or the column marginal frequencies). It represents every single kid we surveyed!

## Proportions and The Power of Conditionals

Just looking at raw counts can be tricky, especially if the groups are different sizes. To make fair comparisons, we turn these counts into fractions or percentages. 

**A relative frequency is the ratio of a specific frequency to the grand total.** 

Here is how we find the different types using step-by-step math:

**A joint relative frequency is calculated by dividing a joint frequency by the grand total.** 
Let's find the joint relative frequency for 7th graders on a team:
1. Find the joint frequency (7th graders on a team), which is 15.
2. Find the grand total, which is 100.
3. Divide the joint frequency by the grand total: 15 / 100 = 0.15.
4. Read this as a percentage: 15%.

**A marginal relative frequency is calculated by dividing a marginal frequency by the grand total.** 
Let's find the marginal relative frequency for all kids on a team:
1. Find the marginal frequency for kids on a team, which is 55.
2. Find the grand total, which is 100.
3. Divide the marginal frequency by the grand total: 55 / 100 = 0.55.
4. Read this as a percentage: 55%.

But the most amazing trick a two-way table can do is change the total we divide by. 

> **A conditional relative frequency is calculated by dividing a joint frequency by a marginal frequency.**

This changes everything! When we calculate this, we pretend the grand total doesn't exist and we only look at one specific row or column. **Conditional relative frequencies show the distribution of one categorical variable among a specific subgroup of another categorical variable.**

What if we ask: *What percentage of 7th Graders are on a team?* 
Here are the steps to solve it:
1. Look ONLY at the subgroup's total (the marginal frequency of 7th Graders), which is 50.
2. Find the joint frequency for the specific kids we want (7th Graders on a team), which is 15.
3. Divide the joint frequency by the marginal frequency: 15 / 50.
4. Calculate the math: 15 / 50 = 0.30.
5. Read as a percentage: 30%.

Now ask: *What percentage of 8th Graders are on a team?*
1. Marginal frequency of 8th Graders: 50.
2. Joint frequency of 8th Graders on a team: 40.
3. Divide: 40 / 50.
4. Calculate: 40 / 50 = 0.80.
5. Read as a percentage: 80%.

### Association Versus Independence
Why did we do all that math? To find secret connections! 

**An association exists between two categorical variables if the conditional relative frequencies differ significantly across categories.** In our example, being on a sports team is very different depending on whether you are in 7th Grade (30%) or 8th Grade (80%). Because 30% and 80% are so different, there is a strong association between grade level and playing sports. 

On the flip side, **independence between two categorical variables means that the conditional relative frequencies are approximately equal across categories.** Imagine if we did the math and found that 40% of 7th Graders played sports and 41% of 8th Graders played sports. Because the numbers are basically the same, knowing a kid's grade wouldn't help you guess if they played sports or not. The two traits would be totally independent!

## Mapping Quantitative Bivariate Data: The Scatterplot

When our data changes from categories (like grades) to quantitative data (numbers we can actually measure, like test scores or how many \$ you get for your allowance), we stop using tables and start drawing graphs.

**A scatterplot displays quantitative bivariate data as individual points plotted on a Cartesian coordinate plane.** (A Cartesian coordinate plane is just your standard graphing paper with an x-axis and a y-axis). Every single dot on the graph represents one person's two measurements.

Where you put the data matters:
*   **The explanatory variable is typically plotted on the horizontal axis of a scatterplot.** This is the x-axis, and it's the thing that we think "explains" what happens next (like hours spent studying).
*   **The response variable is typically plotted on the vertical axis of a scatterplot.** This is the y-axis, and it's the result or the "response" (like the actual score on the quiz).

### Reading the Constellation: Direction, Form, and Strength

When we look at a scatterplot, we are looking for patterns in the dots. We describe the pattern using three words: direction, form, and strength.

1. **Direction**
   *   **A positive association in a scatterplot occurs when the response variable increases as the explanatory variable increases.** The dots travel uphill from left to right. (For example, as hours of studying go up, test scores go up).
   *   **A negative association in a scatterplot occurs when the response variable decreases as the explanatory variable increases.** The dots travel downhill from left to right. (For example, as hours spent watching TV increases, test scores decrease).

2. **Form**
   *   **The form of an association in a scatterplot can be described as linear or nonlinear.** 
   *   **A linear association is indicated when the plotted points in a scatterplot cluster around a straight line.** 
   *   **A nonlinear association is indicated when the plotted points in a scatterplot cluster around a curve.** (Think of the curved path a basketball makes when you shoot it into a hoop!).

3. **Strength**
   *   **The strength of an association in a scatterplot is determined by how closely the plotted points follow a specific mathematical form.** If the dots are packed super tightly into a line, it is a strong association. If the dots look like a messy cloud but vaguely head in one direction, it is a weak association.

### Anomalies: Outliers and Clusters
Sometimes, a dot does not follow the rules. 
*   **An outlier in a scatterplot is a data point that falls substantially outside the overall pattern of the other data points.** It is the weird oddball! Imagine a student who studied for 0 hours but still got a 100%. Their dot would be far away from everyone else's.
*   **A cluster in a scatterplot is a distinct grouping of data points that are located close together.** If you see a tight clump of dots, it usually means those specific kids share a hidden secret—like maybe that cluster of high scores belongs to kids who all stayed for after-school tutoring.

## Measuring the Relationship: Correlation and Causation

Looking at a graph is cool, but in math, we like exact numbers. We want to measure the pattern!

**Correlation measures the strength and direction of a relationship between two quantitative variables.** To measure a strictly straight-line (linear) relationship, we use a special math score called $r$.

> **The correlation coefficient measures the strength and direction of a linear relationship between two quantitative variables.**

The rule for this $r$ score is super strict: **the correlation coefficient is always a value between negative one and positive one inclusive.** 

The number gives away the scatterplot's secret identity:
*   **A correlation coefficient of exactly positive one indicates a perfect positive linear relationship.** Every single dot lines up perfectly on an uphill straight line.
*   **A correlation coefficient of exactly negative one indicates a perfect negative linear relationship.** Every single dot lines up perfectly on a downhill straight line.
*   **A correlation coefficient of zero indicates that there is no linear relationship between the two quantitative variables.** The dots look completely random and scattered. 

The closer the number gets to 1 or -1, the tighter the dots hug an invisible straight line!

### The Ultimate Caveat: Causation
Now for the most important rule in all of math and science. You will hear this until you graduate high school:

**A strong association between two variables in a scatterplot does not prove that one variable causes changes in the other.**

Imagine we draw a scatterplot showing ice cream sales (in \$) and the number of sunburns. The graph shows a super strong positive association! Does that mean eating ice cream causes your skin to burn? No! 

**Causation indicates that an event or change in one variable directly produces a corresponding change in another variable.** In our ice cream example, there is no causation. Eating ice cream doesn't cause sunburns. Both things are just happening because of a hidden third reason: the hot summer sun! 

When you study bivariate data, you are acting like a math detective. Whether you are finding a conditional relative frequency in a table, or spotting an outlier on a scatterplot, you are hunting for clues. But remember, the math gives you the clues—it's up to your own smart brain to solve the mystery correctly!