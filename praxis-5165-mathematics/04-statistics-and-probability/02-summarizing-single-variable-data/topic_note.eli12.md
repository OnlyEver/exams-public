Imagine a stack of 150 video game high scores sitting on your desk. Just looking at that giant list of numbers can make your brain spin! To understand the scores, we have to shrink that giant list into a summary. But in math, when we summarize, we have to make choices. The tools we pick will tell us cool things about how players did, but they might also hide some details. Our goal isn't just to find one magic number. Our goal is to understand the whole group of scores: to find the middle, see how spread out they are, look at their shape, and spot any really weird, unusual scores.

## The Anatomy of the Data: Visual Representations

Before doing any math, it helps to draw a picture. How we draw the picture changes what we see.

### The Dot Plot: Absolute Fidelity
If you are just looking at scores from a small group, like 25 kids in your class playing a game, keep it simple. A dot plot represents each value in a numerical data set as a single dot above a number line. 

Because every single kid's score gets its own dot, dot plots explicitly preserve the exact numerical values of a small data set. If three kids scored an 85, you just draw three dots stacked on top of the number 85. It tells the complete truth! But it only works for small groups. If you try to draw a dot for 3,000 players, the graph just becomes a giant, messy blob.

### Histograms: The Macroscopic View
When you have a huge number of scores, you need a zoomed-out view. A histogram visually represents continuous numerical data grouped into contiguous intervals. "Contiguous intervals" just means number ranges that are right next to each other, like levels 1-10, then 11-20.

The contiguous intervals used to group data in a histogram are called bins or classes. To keep the graph fair and not confusing, the bins in a histogram must be equal in width (like making every bin hold exactly 10 levels).

*   **Frequency Histogram:** The height of a histogram bar represents the frequency of data values falling within that specific bin. For example, if 40 kids scored between 70 and 80, the bar for that bin goes up to 40.
*   **Relative Frequency Histogram:** Instead of showing the exact number of kids, a relative frequency histogram displays the proportion or percentage of data values in each bin. Since it includes everyone who played, the sum of the relative frequencies of all bins in a relative frequency histogram equals exactly one (which is the same as 100%).

> **The Trade-off of Bins**
> Because we clump scores into bins, histograms do not preserve the exact individual data values of a data set. If a bin covers scores from 80 to 90, you know *how many* kids are in there, but you don't know if they scored an 81 or an 89. Also, changing the bin width of a histogram can alter the perceived shape of the data distribution. Making bins 2 points wide might look spiky and messy, but making bins 20 points wide might smooth the graph out into a nice hill!

### Boxplots: The Executive Summary
Sometimes you don't want dots or bins; you just want a quick summary of the basic facts. A boxplot is a graphical representation of the five-number summary of a numerical dataset. 

The five-number summary consists of the minimum, first quartile, median, third quartile, and maximum. 

Think of it like slicing a pizza into four equal pieces. Here is how those pieces match up to the boxplot:
*   The first quartile is the median of the lower half of an ordered data set.
*   The third quartile is the median of the upper half of an ordered data set.
*   The central box of a boxplot spans from the first quartile to the third quartile. This shows where the middle half of all your friends' scores are.
*   A vertical line drawn inside the central box of a boxplot represents the median of the dataset.

Boxplots also have lines sticking out of the box, called "whiskers." How we draw them depends on if we have super weird scores:
*   In a standard boxplot, the whiskers extend from the quartiles to the absolute minimum and maximum values of the dataset.
*   A modified boxplot plots suspected outliers as individual disconnected points beyond the whiskers. (Outliers are just super unusual scores). In this version, the whiskers of a modified boxplot extend to the lowest and highest data values that are not classified as outliers.

> **A Warning:** A boxplot conceals gaps and multiple peaks that might exist within a data distribution. If half your friends are amazing at the game and half are terrible, the boxplot just draws a big box over the middle and makes it look like everyone is perfectly average. It completely hides the fact that there are two totally different groups!

## Finding the Center: Mean, Median, and Mode

When someone asks, "How did your team do?", they want to know the middle score. But there are three different ways to find it!

### The Mean: The Balancing Point
The mean is the arithmetic average calculated by dividing the sum of all data values by the total number of values. 

Imagine you and two friends get allowances: \$10, \$10, and \$40. Here is an example of how to calculate the mean:
1.  Add all the values together: 10 + 10 + 40 = 60.
2.  Count how many values there are: There are 3 allowances.
3.  Divide the total sum by the number of values: 60 / 3 = 20. The mean is \$20.

Think of the mean like balancing kids on a seesaw. Because every score puts a physical weight on the seesaw, the mean is highly sensitive to extreme values or outliers in a dataset. If one friend gets an allowance of \$500, it ruins the balance and pulls the mean way up!

### The Median: The True Middle
If you just want to find the person standing exactly in the middle of a line, you use the median. The median is the exact middle value of a dataset when the numerical values are arranged in ascending order (from smallest to largest).

If you have 5 friends lined up by height, the 3rd friend is the median. But what if you have an even number of friends? For a dataset with an even number of values, the median is calculated as the arithmetic mean of the two middlemost values. 

Here is an example with four scores: 2, 4, 8, 10.
1.  Arrange the scores from smallest to largest: 2, 4, 8, 10.
2.  Find the two numbers in the exact middle: 4 and 8.
3.  Add the two middle numbers together: 4 + 8 = 12.
4.  Divide that sum by 2: 12 / 2 = 6. The median is 6.

Because it only looks at who is standing in the middle, the median is a robust statistic that resists being heavily influenced by extreme values or outliers. If the tallest kid suddenly grew 10 feet, the median wouldn't change at all!

### The Mode: The Peak
The mode is the value or values that appear most frequently in a given dataset. Think of it as the most popular choice.

Unlike the mean and median, a dataset can have zero modes, one mode, or multiple modes. If everyone gets a different score, there is no mode. If two scores tie for the most popular, you have two modes!

## Measuring the Spread: Range, IQR, and Standard Deviation

The center tells you what a normal score looks like, but the spread tells you how much the scores bounce around. 

### Range and Interquartile Range (IQR)
The range is a measure of spread calculated as the difference between the maximum value and the minimum value in a dataset. 

Here is an example for scores of 10, 50, and 100:
1.  Find the maximum (highest) value: 100.
2.  Find the minimum (lowest) value: 10.
3.  Subtract the minimum from the maximum: 100 - 10 = 90. The range is 90.

Because the range only uses the very highest and very lowest numbers, it can easily be messed up by one weird score. For a safer measurement, we use the interquartile range (IQR).

The interquartile range measures the spread of the middle fifty percent of a dataset. It focuses only on the center chunk of your group. The interquartile range is calculated by subtracting the first quartile from the third quartile. 

Here is an example:
1.  Find the third quartile (Q3). Let's say it is 80.
2.  Find the first quartile (Q1). Let's say it is 60.
3.  Subtract Q1 from Q3: 80 - 60 = 20. The IQR is 20.

Because it ignores the top 25% and the bottom 25% entirely, the interquartile range is resistant to extreme outliers.

### Variance and Standard Deviation
If we want to know how far, on average, a typical score bounces away from the mean, we use standard deviation. Standard deviation measures the typical or average distance of individual data values from the mean.

How we calculate it depends on if we are looking at *everyone* (a population) or just a *small test group* (a sample).

**Population Variance and Standard Deviation:**
If your group is the only group you care about (the entire population), here is an example using the scores 2, 4, and 6 (the mean is 4):
1.  Find the difference between each score and the mean: 2 - 4 = -2, 4 - 4 = 0, and 6 - 4 = 2.
2.  Square those differences: -2 x -2 = 4, 0 x 0 = 0, and 2 x 2 = 4.
3.  Population variance is the arithmetic average of the squared differences from the population mean. Add them up and divide by the number of scores (3): (4 + 0 + 4) / 3 = 8 / 3 (which is about 2.67).
4.  Population standard deviation is calculated as the principal square root of the population variance. The square root of 2.67 is about 1.63.

**Sample Variance and Standard Deviation:**
If your group is just a tiny sample used to guess how the whole school will do, the math changes slightly to be safe. Here is an example using the exact same scores (2, 4, and 6):
1.  Find the squared differences from the sample mean, just like before, and add them up: 4 + 0 + 4 = 8.
2.  Sample variance is calculated by dividing the sum of squared deviations from the sample mean by one less than the sample size. Since there are 3 scores, we divide by 2 (because 3 - 1 = 2): 8 / 2 = 4.
3.  Sample standard deviation is calculated as the principal square root of the sample variance. The square root of 4 is exactly 2.

Standard deviation acts like a giant rubber band stretching from the middle to every single kid. Because of this pulling, the standard deviation is highly sensitive to the presence of outliers. One giant score makes the whole standard deviation stretch out!

However, the standard deviation of a dataset is exactly zero if and only if all values in the dataset are identical. If everyone scores a 50, nobody is away from the mean, so the distance is zero!

## Shape, Skew, and the Mechanics of Outliers

When we put the center and spread together, we can see the shape of our data. How the mean and median compare tells us if the data is leaning to one side.

### Symmetry vs. Skew
*   **Symmetry:** A perfectly symmetric distribution has its mean and median located at exactly the same central value. The left side is a perfect mirror image of the right side.
*   **Right-Skewed:** Imagine a super hard level in a game. Most kids get low scores, but a few pros get really high scores. In a right-skewed distribution, the longer tail extends toward the higher positive values on the number line. Because the mean gets pulled toward those high scores by the pros, in a substantially right-skewed distribution, the mean is typically pulled to be greater than the median.
*   **Left-Skewed:** Imagine a super easy level. Most kids do great, but a few kids' controllers broke and they got low scores. In a left-skewed distribution, the longer tail extends toward the lower values on the number line. Those low scores pull the balance point down, meaning in a substantially left-skewed distribution, the mean is typically pulled to be less than the median.

| Shape | Tail Direction | Center Relationship | Typical Scenario |
| :--- | :--- | :--- | :--- |
| **Symmetric** | Equal tails | Mean = Median | A perfectly fair, balanced game |
| **Right-Skewed** | Points Right (+) | Mean > Median | A very hard game (most fail, few win) |
| **Left-Skewed** | Points Left (-) | Mean < Median | A very easy game (most win, few fail) |

### Defining and Removing Outliers
We talk about weird scores all the time, but math has specific rules for them. An outlier is a data point that differs significantly in magnitude from the majority of the data in a given dataset.

To find them, we set up invisible fences using the IQR, like out-of-bounds lines on a sports field. Any score outside the fence is an outlier.
*   The 1.5 IQR rule identifies lower outliers as values strictly less than the first quartile minus 1.5 times the interquartile range.
*   The 1.5 IQR rule identifies upper outliers as values strictly greater than the third quartile plus 1.5 times the interquartile range.

Here is an example for finding an upper outlier boundary if Q3 is 80 and the IQR is 10:
1.  Take the IQR: 10.
2.  Multiply the IQR by 1.5: 10 x 1.5 = 15.
3.  Take the third quartile (Q3): 80.
4.  Add the step 2 result to Q3: 80 + 15 = 95. Any score strictly higher than 95 is an upper outlier!

What happens if you find an outlier (like a kid who scored 10,000 points while everyone else scored 100) and delete it? 

Because the mean gets yanked around easily, removing a high outlier from a right-skewed dataset decreases the mean more drastically than it decreases the median. Also, because the standard deviation measures how spread out things are, that huge outlier made it stretch far. So, removing an extreme outlier from a dataset will decrease the standard deviation, making the whole group of scores look much closer together!