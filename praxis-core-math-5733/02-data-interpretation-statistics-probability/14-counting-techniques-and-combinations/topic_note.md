Welcome to one of the most wonderfully deceptive topics in all of [mathematics](https://en.wikipedia.org/wiki/Mathematics). We call it "[counting](https://en.wikipedia.org/wiki/Counting)," but that's a terrible name for it. When we talk about counting techniques for the [Praxis Core exam](https://en.wikipedia.org/wiki/Praxis_test), we aren’t talking about [tallying](https://en.wikipedia.org/wiki/Tally_marks) things up one by one on our [fingers](https://en.wikipedia.org/wiki/Finger_counting). Who has the time to do that? 

If I ask you to tell me how many ways you can arrange a 10-person [committee](https://en.wikipedia.org/wiki/Committee) from a room of 50 people, counting them one by one would take you the rest of your natural life. No, what we are really talking about is *the architecture of possibilities*. We are learning how to calculate the exact size of entire universes of choices without ever having to list them out. 

Let’s roll up our sleeves and look at how the universe multiplies!

## The Universe of Possibilities

Before we can calculate anything, we have to define the sandbox we are playing in. In mathematics, we call the exhaustive [set](https://en.wikipedia.org/wiki/Set_%28mathematics%29) of all possible distinct [outcomes](https://en.wikipedia.org/wiki/Outcome_%28probability%29) the **[sample space](https://en.wikipedia.org/wiki/Sample_space)** of an [experiment](https://en.wikipedia.org/wiki/Experiment_%28probability_theory%29). It is the complete menu of everything that could possibly happen. 

An **[event](https://en.wikipedia.org/wiki/Event_%28probability_theory%29)**, on the other hand, is just a specific outcome or a defined set of outcomes within a larger sample space. If the sample space is the entire menu at a [diner](https://en.wikipedia.org/wiki/Diner), an event is the specific meal you end up eating.

![A sample space represents the entire universe of possible outcomes, while an event represents a specific subset of those outcomes.](https://wikipedia.org/wiki/Special:Redirect/file/Sample_space.png)

To visualize how these events unfold, we often use a **[tree diagram](https://en.wikipedia.org/wiki/Tree_diagram_%28probability_theory%29)**. A tree diagram represents all possible outcomes of a [sequence](https://en.wikipedia.org/wiki/Sequence) of events by using branches to connect each initial choice to subsequent choices. Imagine standing at a [fork in the road](https://en.wikipedia.org/wiki/Fork_%28intersection%29)—that's your first choice. Once you take the left path, you hit another fork, and then another. By tracing every possible path from the root of the tree to the tip of every branch, you can visually see the entire sample space. 

![A tree diagram visualizes the total sample space of sequential events by mapping every possible path of choices.](https://wikipedia.org/wiki/Special:Redirect/file/Probability_tree_diagram.svg)

But drawing trees takes up too much paper when the numbers get large. We need principles. We need engines of [calculation](https://en.wikipedia.org/wiki/Calculation).

---

## The Two Great Engines of Counting

Nature behaves according to a couple of very simple rules when it comes to possibilities. Everything boils down to knowing when to [multiply](https://en.wikipedia.org/wiki/Multiplication) and when to [add](https://en.wikipedia.org/wiki/Addition).

### 1. The Fundamental Counting Principle (The "AND" Rule)

If I want to know how many ways a sequence of things can happen together, I use [multiplication](https://en.wikipedia.org/wiki/Multiplication). **[The Fundamental Counting Principle](https://en.wikipedia.org/wiki/Rule_of_product)** dictates multiplying the number of choices for each successive independent event to find the total possible outcomes. 

We use this when dealing with **[independent events](https://en.wikipedia.org/wiki/Independence_%28probability_theory%29)**—these are events where the occurrence of one event does not affect the possible outcomes of the other events. 

Let's look at the classic examples you will see on the [Praxis](https://en.wikipedia.org/wiki/Praxis_test): [coins](https://en.wikipedia.org/wiki/Coin_flipping) and number cubes ([dice](https://en.wikipedia.org/wiki/Dice)).

*   A **[standard coin flip](https://en.wikipedia.org/wiki/Coin_flipping)** generates exactly two possible outcomes (Heads or Tails). 
*   A **[standard number cube](https://en.wikipedia.org/wiki/Dice)** features exactly six distinct [faces](https://en.wikipedia.org/wiki/Face_%28geometry%29).

What happens if we flip a coin *and* roll a number cube simultaneously? Because they are completely [independent](https://en.wikipedia.org/wiki/Independence_%28probability_theory%29) of one another (the coin doesn't care what the cube does), we use the Fundamental Counting Principle. We multiply the 2 outcomes of the coin by the 6 outcomes of the cube. Therefore, tossing a standard coin and a standard number cube simultaneously generates exactly twelve possible outcomes ($2 \times 6 = 12$).

Look at how fast the universe of possibilities expands when we repeat independent events:
*   Tossing a single standard number cube generates exactly six possible outcomes ($6$).
*   Tossing two standard number cubes simultaneously generates exactly thirty-six possible outcomes ($6 \times 6 = 36$).
*   Tossing three standard number cubes simultaneously generates exactly 216 possible outcomes ($6 \times 6 \times 6 = 216$).

![A standard number cube provides 6 independent outcomes. When rolled multiple times, the total possible outcomes multiply exponentially.](https://wikipedia.org/wiki/Special:Redirect/file/6sided_dice_(cropped).jpg)

The same beautiful [logic](https://en.wikipedia.org/wiki/Logic) applies to coins. The total number of outcomes for [flipping a coin](https://en.wikipedia.org/wiki/Coin_flipping) multiple times is calculated by raising two to the [power](https://en.wikipedia.org/wiki/Exponentiation) of the number of flips ($2^n$). Five flips? That's $2^5$, or 32 distinct outcomes.

### 2. The Addition Principle (The "OR" Rule)

What if we aren't doing multiple things in sequence, but rather choosing between totally separate alternatives? 

**[The Addition Principle](https://en.wikipedia.org/wiki/Rule_of_sum)** dictates [adding](https://en.wikipedia.org/wiki/Addition) the number of outcomes for [mutually exclusive events](https://en.wikipedia.org/wiki/Mutual_exclusivity) to find the total possible outcomes. 

> **[Mutually exclusive events](https://en.wikipedia.org/wiki/Mutual_exclusivity)** are two or more specific events that cannot occur simultaneously. 

Imagine you are choosing a single [dessert](https://en.wikipedia.org/wiki/Dessert). You can choose from 3 types of [cake](https://en.wikipedia.org/wiki/Cake) *or* 4 types of [pie](https://en.wikipedia.org/wiki/Pie). Because you are only picking one, and a dessert cannot be both a cake and a pie simultaneously, these events are [mutually exclusive](https://en.wikipedia.org/wiki/Mutual_exclusivity). To find the total possible choices, you simply add them: $3 + 4 = 7$ possible desserts. 

---

## The Illusion of Independence: How Choices Alter the Universe

Things get incredibly interesting when the choices we make actually change the fabric of the choices that come next. 

When the occurrence of one event alters the total number of possible outcomes for subsequent events, we are dealing with **[dependent events](https://en.wikipedia.org/wiki/Statistical_dependence)**. 

A classic way the Praxis will test your understanding of dependent versus independent events is through the concept of "replacement." Imagine drawing [marbles](https://en.wikipedia.org/wiki/Marble_%28toy%29) from a bag.

### Sampling With Replacement
**[Sampling with replacement](https://en.wikipedia.org/wiki/Sampling_%28statistics%29)** means an item is returned to the selection pool before the next item is drawn. 
Because you put the item back, the universe resets. Sampling with replacement keeps the total number of available choices constant for each successive selection. If you have 10 marbles, you have 10 choices for the first draw, 10 choices for the second draw, and 10 for the third. These are [independent events](https://en.wikipedia.org/wiki/Independence_%28probability_theory%29). ($10 \times 10 \times 10$)

### Sampling Without Replacement
**[Sampling without replacement](https://en.wikipedia.org/wiki/Sampling_%28statistics%29)** means a chosen item is removed from the selection pool permanently after being drawn. 
Now, the universe is shrinking! Sampling without replacement decreases the total number of available choices by exactly one for each successive selection. You draw the first marble from 10. The next draw only has 9 options. The next has 8. These are [dependent events](https://en.wikipedia.org/wiki/Statistical_dependence). ($10 \times 9 \times 8$)

---

## The Mathematical Exclamation Point: The Factorial

When we start talking about sampling without replacement, we inevitably run into one of my favorite symbols in mathematics: the [factorial](https://en.wikipedia.org/wiki/Factorial). 

> A **[factorial](https://en.wikipedia.org/wiki/Factorial)** represents the mathematical [product](https://en.wikipedia.org/wiki/Product_%28mathematics%29) of a positive [integer](https://en.wikipedia.org/wiki/Integer) and all the positive integers below that integer down to one. 

Because [mathematicians](https://en.wikipedia.org/wiki/Mathematician) are quite enthusiastic about this concept, the mathematical symbol for a factorial is an [exclamation mark](https://en.wikipedia.org/wiki/Exclamation_mark) placed immediately after an integer! 

If I want to know how many ways I can arrange 5 different books on a shelf, I calculate it using dependent events: I have 5 choices for the first spot, 4 for the second, 3 for the third, 2 for the fourth, and 1 for the final spot. 

$5 \times 4 \times 3 \times 2 \times 1 = 120$

Instead of writing all that out, we just write **\$5!$** (read as "five factorial"). 

There is one brilliant, slightly mind-bending fact you must memorize for your exam: **The value of [zero factorial](https://en.wikipedia.org/wiki/Empty_product) (\$0!$) is defined mathematically as exactly one.** 
Why? Think about it logically. How many ways can you arrange absolutely nothing? There is exactly *one* way to do it: by doing nothing! It’s a beautifully elegant [mathematical truth](https://en.wikipedia.org/wiki/Truth).

---

## Committees vs. Lineups: Combinations and Permutations

Now we arrive at the grand finale of counting techniques. When we select items from a larger group without replacement, we have to ask ourselves one critical, absolute question: **Does the [sequence](https://en.wikipedia.org/wiki/Sequence) of the items matter?**

Depending on how you answer, you will use either a [Permutation](https://en.wikipedia.org/wiki/Permutation) or a [Combination](https://en.wikipedia.org/wiki/Combination). 

| Feature | Permutation | Combination |
| :--- | :--- | :--- |
| **Definition** | An arrangement of a specific number of items where the sequence of the items **strictly matters**. | A selection of a specific number of items where the sequence of the items **does not matter**. |
| **Real-World Example** | Arranging distinct objects in a straight line utilizes permutation calculations because the specific sequence of objects changes the outcome (e.g., A-B-C is different from C-B-A). | Forming a generalized committee from a larger group utilizes combination calculations because the specific order of selection is irrelevant (e.g., a team of Alice, Bob, and Charlie is the exact same team as Charlie, Bob, and Alice). |

### The Relationship Between The Two

Because [permutations](https://en.wikipedia.org/wiki/Permutation) care about order, every unique sequence counts as a totally separate outcome. [Combinations](https://en.wikipedia.org/wiki/Combination) don't care about order. A [combination](https://en.wikipedia.org/wiki/Combination) looks at the permutations "Alice-Bob-Charlie" and "Charlie-Bob-Alice" and says, "Relax, those are exactly the same people. That's just one group."

![In a permutation, sequence strictly matters. Arranging three distinct objects in different orders yields entirely different outcomes.](https://wikipedia.org/wiki/Special:Redirect/file/Permutations_RGB.svg)

Because [combinations](https://en.wikipedia.org/wiki/Combination) group identical sets of items together into a single outcome, **the number of possible combinations for a [subset](https://en.wikipedia.org/wiki/Subset) of items is always less than or equal to the number of possible [permutations](https://en.wikipedia.org/wiki/Permutation) for that same subset.** 

![In a combination, order is irrelevant. Choosing 3 items from a group produces unique subsets, regardless of how they are arranged internally.](https://wikipedia.org/wiki/Special:Redirect/file/Combinations_without_repetition%3B_5_choose_3.svg)

But how do we calculate combinations mathematically? We use our trusty permutations, and then we "[divide](https://en.wikipedia.org/wiki/Division_%28mathematics%29) out" the duplicates. 

If we choose 3 people from a group, there are \$3!$ (or 6) ways to rearrange those specific 3 people. To find the combinations, we calculate the permutations first, and then [divide](https://en.wikipedia.org/wiki/Division_%28mathematics%29) by the number of ways those chosen items can be internally arranged. 

Therefore, **the formula for calculating [combinations](https://en.wikipedia.org/wiki/Combination) [divides](https://en.wikipedia.org/wiki/Division_%28mathematics%29) the total number of [permutations](https://en.wikipedia.org/wiki/Permutation) by the [factorial](https://en.wikipedia.org/wiki/Factorial) of the number of chosen items.** 

If you understand *why* we divide—that we are simply stripping away the irrelevant shuffling of the sequence—you don't just know a formula. You actually understand the mechanics of the universe!

## Summary for the Praxis Exam

When you sit down to take the [Praxis Core Math exam](https://en.wikipedia.org/wiki/Praxis_test), don't panic when you see a question about [combinations](https://en.wikipedia.org/wiki/Combination), cubes, or [coin tosses](https://en.wikipedia.org/wiki/Coin_flipping). Just ask yourself these guiding questions:
1.  **Am I doing multiple things, or choosing between alternatives?** ([Multiply](https://en.wikipedia.org/wiki/Multiplication) for AND, [Add](https://en.wikipedia.org/wiki/Addition) for OR).
2.  **Am I replacing the items?** ([Independent](https://en.wikipedia.org/wiki/Independence_%28probability_theory%29) vs. [Dependent](https://en.wikipedia.org/wiki/Statistical_dependence)).
3.  **Does the sequence matter?** (Lineups = [Permutations](https://en.wikipedia.org/wiki/Permutation); Committees = [Combinations](https://en.wikipedia.org/wiki/Combination)).

Understand these rules, and you won't ever have to manually [count](https://en.wikipedia.org/wiki/Counting) possibilities again. You will simply see the matrix of numbers unfolding before you. Happy [calculating](https://en.wikipedia.org/wiki/Calculation)!