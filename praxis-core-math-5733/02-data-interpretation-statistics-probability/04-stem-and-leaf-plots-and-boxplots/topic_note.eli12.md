Welcome to the awesome, sometimes messy world of numbers! 

Imagine you and your friends just played 30 rounds of a new video game. When you finish, you don't just get one neat "winning" number. You get a giant, confusing list of 30 different scores. Raw numbers, just sitting in a list, are stubborn. They don't easily tell you a story. Are you getting better? Was the level too hard? Did someone get an insanely high score?

To answer these questions, we have to draw the data to give it a shape. 

A long time ago, a really smart math guy figured out a great fix. **The stem-and-leaf plot was popularized by statistician John Tukey in the 1970s**, along with its partner, the boxplot. 

These two graphs are like superpowers for looking at numbers. Let’s look at how they work, why they are so cool, and how to read them easily!

---

## 1. The Stem-and-Leaf Plot: Holding onto the Details

Sometimes, you want to see what all your video game scores look like together, but you don't want to lose the actual numbers. 

**A stem-and-leaf plot is a table that displays quantitative data by splitting each numerical value into a stem and a leaf.** Think of it like sorting trading cards: you group them by the team name (the stem), and then by the specific player number (the leaf). 

Here is how the pieces work:
*   **The Stem:** **In a stem-and-leaf plot, the stem represents the leading digit or digits of a numerical data value.** This is the main trunk of your chart.
*   **The Leaf:** **In a stem-and-leaf plot, the leaf represents the final, trailing digit of a numerical data value.** This is the tiny piece on the end.

Let’s look at why this is so helpful. 

### The Beauty of Preservation and Order
The coolest thing about this chart is that it doesn't hide anything. **A stem-and-leaf plot preserves the exact individual data points from the original dataset.** Unlike a normal bar chart where scores get lumped together and hidden inside a colored block, here, the numbers are just taken apart so they are easier to store.

To keep everything easy to read, **in a stem-and-leaf plot, the leaves are listed in ascending numerical order outward from the central stem.** That means they go from smallest to biggest as they move away from the center! Also, **each individual leaf in a stem-and-leaf plot represents exactly one data point in the dataset.** If you count 30 leaves, you know there were exactly 30 video game rounds played.

### The Secret Decoder Ring: The Key
If I tell you a score has a stem of "5" and a leaf of "2", what number is that? Is it 52? Is it 5.2? Is it 520? 

You can't know unless I give you the secret code! **A stem-and-leaf plot requires a key to explain the specific place value of the stem and the leaf.** 

**Reconstructing a specific data point from a stem-and-leaf plot requires combining the stem with one corresponding leaf according to the plot's key.** Here are the steps to do it:
1. Look at the plot's key (for example, the key might say `5 | 2 = 52`).
2. Find the stem you want to read on the left side (like `5`).
3. Find a leaf connected to it on the right side (like `2`).
4. Put them together exactly how the key tells you, giving you your final score of `52`.

### The 90-Degree Trick
Here is a super fun trick. Tip your head or turn your paper to the side! **When a stem-and-leaf plot is rotated 90 degrees counterclockwise, the plot's shape visually resembles a histogram.** The rows of leaves look just like the bars on a regular graph, showing you where most of your scores piled up!

---

## 2. The Boxplot: The Big Picture

Now, imagine you aren't looking at 30 scores, but 3,000 scores from a massive online gaming tournament. A stem-and-leaf plot would be thousands of numbers long. That's way too much to read! For massive lists, we need a quick summary. 

That is what the boxplot does. **A boxplot is a graphical representation of a dataset based on a five-number summary.** Because it looks like a rectangle with lines sticking out, **a boxplot is also commonly referred to as a box-and-whisker plot.**

Instead of showing every single score, it chops the whole list into neat chunks using five important guideposts. **A five-number summary consists of the minimum, first quartile, median, third quartile, and maximum values of a dataset.**

### The Anatomy of the Box
Let's build this from the middle going out! 

*   **The Median:** This is the exact middle score. **The median represents the 50th percentile of an ordered dataset.** Half the players scored lower, and half scored higher. **In a boxplot, a vertical line drawn inside the rectangular box marks the median value of the dataset.**
*   **The First Quartile (Q1):** This is the middle of the bottom half. **The first quartile represents the 25th percentile of an ordered dataset.** 
*   **The Third Quartile (Q3):** This is the middle of the top half. **The third quartile represents the 75th percentile of an ordered dataset.**

Next, we draw the main shape. **In a boxplot, a rectangular box is drawn spanning from the first quartile to the third quartile.** 

> **The Interquartile Range (IQR):** 
> **The length of the rectangular box in a boxplot represents the interquartile range of the dataset.** 
> **The interquartile range is calculated by subtracting the first quartile value from the third quartile value.** 
> 
> Here is how you calculate the IQR step-by-step:
> 1. Find the value for the third quartile (Q3) at the right edge of the box. Let's say it is 80.
> 2. Find the value for the first quartile (Q1) at the left edge of the box. Let's say it is 60.
> 3. Subtract the Q1 number from the Q3 number: 80 - 60.
> 4. The answer is 20. Your interquartile range is 20!

This box holds the most "average" scores. Because it goes from the 25th percentile to the 75th percentile, **the central box in a boxplot contains the middle 50 percent of the dataset's values.** 

### The Whiskers and the Weirdos (Outliers)
What about the highest and lowest scores? 
**In a boxplot, lines called whiskers extend outward from the central box to the minimum and maximum values.** They look like cat whiskers!

But sometimes you get a player who scores 5 points when everyone else scored around 100. That "5" is super weird. We call it an outlier. We don't want that one weird score to stretch our whisker out so far that the whole drawing looks messed up. 

So, there is a special rule for weird scores: **Some boxplots use individual dots or asterisks plotted beyond the whiskers to represent outlier data points.** 
When we draw the weird scores as dots, what happens to the whiskers? **When a boxplot includes outlier dots, the whiskers extend only to the lowest and highest data points that are not mathematically considered outliers.** They shrink back to where the normal scores are!

### The "25 Percent" Rule (A Massive Praxis Trap!)
Here is a very tricky part that confuses a lot of people. Because of those five guideposts, the whole list of scores is sliced into four chunks, just like slicing a pizza into 4 equal slices:

1.  **The segment from the minimum value to the first quartile in a boxplot contains approximately 25 percent of the dataset's values.** (The left whisker)
2.  **The segment from the first quartile to the median in a boxplot contains approximately 25 percent of the dataset's values.** (The left half of the box)
3.  **The segment from the median to the third quartile in a boxplot contains approximately 25 percent of the dataset's values.** (The right half of the box)
4.  **The segment from the third quartile to the maximum value in a boxplot contains approximately 25 percent of the dataset's values.** (The right whisker)

*Every single one of these 4 chunks has exactly the same number of scores inside it.* 

If you see a super long whisker, it does **not** mean there are more scores hiding in there! It just means those scores are stretched really far apart. A short box just means the scores are squeezed tightly together. Remember: length tells you how stretched out the numbers are, not how many numbers there are!

---

## 3. Reading the Shape: Skewness

Sometimes scores aren't perfectly balanced. Imagine if a test was super easy and everyone got a high score, pushing all the numbers to one side. We call this leaning "skewed." You can spot this easily on a boxplot.

*   **Inside the box:** **A skewed data distribution is visually indicated in a boxplot when the median line is noticeably closer to one end of the central box than the other.** If the middle line is pushed way over to the right side, the data is leaning!
*   **Outside the box:** Look at the whiskers. **An asymmetrical whisker length in a boxplot indicates that the data distribution is skewed.** (Asymmetrical just means they don't match). If the right whisker is super long and the left one is tiny, your data is skewed!

---

## Summary Comparison for the Praxis Exam

To remember these, just think about what each drawing is best at:

| Feature | Stem-and-Leaf Plot | Boxplot (Box-and-Whisker) |
| :--- | :--- | :--- |
| **Keeping the Numbers** | Shows you exactly what every single number is. | Summarizes things and hides the individual numbers. |
| **Best Used For** | Smaller lists where seeing every exact score matters. | Giant lists where you just want to see the middle, the spread, and weird outliers. |
| **The Secret Code** | Absolutely requires a key (like `4 | 1 = 41`). | Uses a number line at the bottom to read the 5-number summary. |
| **Finding the Middle 50%** | You have to count the leaves one by one to find it. | Super easy! It's just the big rectangle in the middle. |

Play around with these ideas. Think of a Stem-and-Leaf plot as saving every single detail, and a Boxplot as a quick zoomed-out summary. Once you picture how they work, you'll be a total master at reading data!