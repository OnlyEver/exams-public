When we attempt to [calculate](https://en.wikipedia.org/wiki/Calculation) the [probability](https://en.wikipedia.org/wiki/Probability) of a future occurrence, we must first map the entirety of what is possible. [Counting](https://en.wikipedia.org/wiki/Counting), in the [mathematical](https://en.wikipedia.org/wiki/Mathematics) sense, is not merely tallying objects one by one; it is the systematic unearthing of hidden structures within [sets](https://en.wikipedia.org/wiki/Set_%28mathematics%29) of choices. It is the [geometry](https://en.wikipedia.org/wiki/Geometry) of branching paths. Before we can determine how likely an [event](https://en.wikipedia.org/wiki/Event_%28probability_theory%29) is, we must rigorously define the boundaries of the universe in which that event takes place. 

## The Architecture of Possibility: [Sample Spaces](https://en.wikipedia.org/wiki/Sample_space) and [Events](https://en.wikipedia.org/wiki/Event_%28probability_theory%29)

To study [outcomes](https://en.wikipedia.org/wiki/Outcome_%28probability%29), we first require a framework. In [mathematics](https://en.wikipedia.org/wiki/Mathematics), **the [sample space](https://en.wikipedia.org/wiki/Sample_space) of an [experiment](https://en.wikipedia.org/wiki/Experiment_%28probability_theory%29) is the exhaustive [set](https://en.wikipedia.org/wiki/Set_%28mathematics%29) of all possible distinct outcomes.** It is the absolute limit of what can happen in a given scenario. Within that universe, we look for specific occurrences. An **[event](https://en.wikipedia.org/wiki/Event_%28probability_theory%29) is a specific outcome or a defined set of outcomes within a larger sample space.** 

![A visual representation of a finite sample space, encompassing the entire set of possible outcomes, with specific events identified within it.](https://wikipedia.org/wiki/Special:Redirect/file/Sample_space.png)

Consider the simplest engines of [randomness](https://en.wikipedia.org/wiki/Randomness). **A standard [coin flip](https://en.wikipedia.org/wiki/Coin_flipping) generates exactly two possible outcomes**: heads or tails. Our sample space has a size of two. If we look at a [die](https://en.wikipedia.org/wiki/Dice), **a standard number cube features exactly six distinct faces.** Therefore, **tossing a single standard number cube generates exactly six possible outcomes.** 

But what happens when the universe gets slightly more complicated? What if we toss a coin *and* roll a number cube? 

### Mapping the Branches: Tree Diagrams
To visualize compound choices, we use a geometric tool. **A tree diagram represents all possible outcomes of a [sequence](https://en.wikipedia.org/wiki/Sequence) of events by using branches to connect each initial choice to subsequent choices.** 

![A tree diagram maps all possible branches of sequential events, allowing us to visually track every distinct outcome from root to leaf.](https://wikipedia.org/wiki/Special:Redirect/file/Probability_tree_diagram.svg)

Imagine a starting point that splits into two branches: Heads and Tails. From the end of the Heads branch, six new branches sprout (1 through 6). From the Tails branch, another six sprout. By tracing every path from the root to the tip of the leaves, we see every distinct reality. By following this diagram, we find that **tossing a standard coin and a standard number cube simultaneously generates exactly twelve possible outcomes** ($2 \times 6 = 12$).

## The Governing Laws: [Multiplication](https://en.wikipedia.org/wiki/Multiplication) and [Addition](https://en.wikipedia.org/wiki/Addition)

Drawing a tree diagram is wonderfully intuitive, but it becomes agonizingly tedious as the number of events grows. Instead, we extract the mathematical essence of the tree diagram to create rules.

> **[The Fundamental Counting Principle](https://en.wikipedia.org/wiki/Rule_of_product)**
> This principle dictates [multiplying](https://en.wikipedia.org/wiki/Multiplication) the number of choices for each successive [independent event](https://en.wikipedia.org/wiki/Independence_%28probability_theory%29) to find the total possible outcomes. 

![A visual application of the Fundamental Counting Principle, demonstrating how choices multiply when sequential events are combined.](https://wikipedia.org/wiki/Special:Redirect/file/Multiplication-principle.svg)

Because every branch of our first choice blossoms into a full set of secondary choices, [multiplication](https://en.wikipedia.org/wiki/Multiplication) is the natural shorthand. 
* If you flip a coin twice, it is $2 \times 2 = 4$ outcomes. 
* Flip it three times, $2 \times 2 \times 2 = 8$. 
* We can generalize this elegantly: **The total number of outcomes for flipping a coin multiple times is calculated by raising two to the [power](https://en.wikipedia.org/wiki/Exponentiation) of the number of flips** ($2^n$).

The exact same multiplication governs the rolling of number cubes:
* **Tossing two standard number cubes simultaneously generates exactly thirty-six possible outcomes** ($6 \times 6 = 36$).
* **Tossing three standard number cubes simultaneously generates exactly 216 possible outcomes** ($6 \times 6 \times 6 = 216$).

### [The Addition Principle](https://en.wikipedia.org/wiki/Rule_of_sum)
There are moments, however, when choices are parallel rather than sequential. Suppose you are allowed to roll *either* one number cube *or* flip one coin, but not both. You are dealing with entirely separate timelines. 

> **[The Addition Principle](https://en.wikipedia.org/wiki/Rule_of_sum)**
> This principle dictates [adding](https://en.wikipedia.org/wiki/Addition) the number of outcomes for [mutually exclusive events](https://en.wikipedia.org/wiki/Mutual_exclusivity) to find the total possible outcomes.

What does it mean to be [mutually exclusive](https://en.wikipedia.org/wiki/Mutual_exclusivity)? **Mutually exclusive events are two or more specific events that cannot occur simultaneously.** You cannot simultaneously pull a single card that is both an [Ace](https://en.wikipedia.org/wiki/Ace) and a [King](https://en.wikipedia.org/wiki/King_%28playing_card%29). If you are choosing one action from two mutually exclusive sets (6 die faces or 2 coin faces), your total sample space is $6 + 2 = 8$ possible outcomes. 

## The Flow of Time: [Independence](https://en.wikipedia.org/wiki/Independence_%28probability_theory%29) and [Dependency](https://en.wikipedia.org/wiki/Conditional_probability)

When navigating multiple events, we must ask a critical question: *Does the first choice care about the second?*

**[Independent events](https://en.wikipedia.org/wiki/Independence_%28probability_theory%29) are events where the occurrence of one event does not affect the possible outcomes of the other events.** A coin has no [memory](https://en.wikipedia.org/wiki/Memorylessness). If you flip ten heads in a row, the coin does not know this; the eleventh flip still has exactly two outcomes. The sample space remains rigid and unchanging.

However, many physical systems in reality do have memory. **[Dependent events](https://en.wikipedia.org/wiki/Conditional_probability) are events where the occurrence of one event alters the total number of possible outcomes for subsequent events.** 

### The Mechanics of [Sampling](https://en.wikipedia.org/wiki/Sampling_%28statistics%29)
Nowhere is the distinction between independent and dependent events clearer than when drawing items from a [finite](https://en.wikipedia.org/wiki/Finite_set) pool—a process known as [sampling](https://en.wikipedia.org/wiki/Sampling_%28statistics%29).

| Condition | Mechanism | Mathematical Impact |
| :--- | :--- | :--- |
| **[Sampling with replacement](https://en.wikipedia.org/wiki/Sampling_%28statistics%29)** | **An item is returned to the selection pool before the next item is drawn.** | Because the item goes back, it **keeps the total number of available choices constant for each successive selection.** These are *[independent](https://en.wikipedia.org/wiki/Independence_%28probability_theory%29)* events. |
| **[Sampling without replacement](https://en.wikipedia.org/wiki/Simple_random_sample)** | **A chosen item is removed from the selection pool permanently after being drawn.** | Because the item is gone, it **decreases the total number of available choices by exactly one for each successive selection.** These are *[dependent](https://en.wikipedia.org/wiki/Conditional_probability)* events. |

## The Engine of Arrangement: [Factorials](https://en.wikipedia.org/wiki/Factorial)

Let us push sampling without replacement to its absolute limit. Suppose you have 5 different books and you want to arrange all of them on a shelf. 

For the first slot on the shelf, you have 5 choices.
For the second slot, you have 4 choices (one book is already placed).
For the third, 3 choices.
For the fourth, 2 choices.
For the last, exactly 1 choice.

According to the [Fundamental Counting Principle](https://en.wikipedia.org/wiki/Rule_of_product), we multiply these together: $5 \times 4 \times 3 \times 2 \times 1 = 120$. 

This descending multiplication occurs so frequently in probability that [mathematicians](https://en.wikipedia.org/wiki/Mathematician) gave it its own name and symbol. 

> **[Factorial](https://en.wikipedia.org/wiki/Factorial)**
> **A factorial represents the mathematical [product](https://en.wikipedia.org/wiki/Product_%28mathematics%29) of a positive [integer](https://en.wikipedia.org/wiki/Integer) and all the positive integers below that integer down to one.**
>
> **The mathematical symbol for a factorial is an [exclamation mark](https://en.wikipedia.org/wiki/Exclamation_mark) placed immediately after an integer** (e.g., \$5!$).

Before we move forward, we must address a brilliant, necessary quirk of mathematics. What happens if we have zero objects to arrange? **The value of [zero factorial](https://en.wikipedia.org/wiki/Empty_product) is defined mathematically as exactly one** (\$0! = 1$). Why? Because there is exactly *one* way to arrange zero items: by doing nothing. The [empty set](https://en.wikipedia.org/wiki/Empty_set) has exactly one configuration. 

## The Architecture of Order: [Permutations](https://en.wikipedia.org/wiki/Permutation) vs. [Combinations](https://en.wikipedia.org/wiki/Combination)

We have arrived at the pinnacle of counting techniques. The [Praxis exam](https://en.wikipedia.org/wiki/Praxis_test) will relentlessly test your ability to differentiate between two concepts: [Permutations](https://en.wikipedia.org/wiki/Permutation) and [Combinations](https://en.wikipedia.org/wiki/Combination). The entire difference rests on one word: **[Sequence](https://en.wikipedia.org/wiki/Sequence)**.

### [Permutations](https://en.wikipedia.org/wiki/Permutation) (Order Matters)
**A [permutation](https://en.wikipedia.org/wiki/Permutation) is an arrangement of a specific number of items where the sequence of the items strictly matters.** 

Imagine assigning three unique titles—President, Vice President, and Treasurer—to three students chosen from a class of twenty. If Alice is President and Bob is Vice President, that is a profoundly different outcome than if Bob is President and Alice is Vice President. The sequence of the names creates a brand-new outcome. 

Because of this, **arranging distinct objects in a [straight line](https://en.wikipedia.org/wiki/Line_%28geometry%29) utilizes permutation calculations because the specific sequence of objects changes the outcome.**

![All six distinct permutations of three unique items. Because the sequence matters, each specific arrangement constitutes a distinct outcome.](https://wikipedia.org/wiki/Special:Redirect/file/Permutations_RGB.svg)

The [formula](https://en.wikipedia.org/wiki/Formula) for finding the number of permutations of choosing $k$ items from a pool of $n$ items is:
$$P(n, k) = \frac{n!}{(n - k)!}$$

### [Combinations](https://en.wikipedia.org/wiki/Combination) (Order is Irrelevant)
Now, imagine a different scenario. **A [combination](https://en.wikipedia.org/wiki/Combination) is a selection of a specific number of items where the sequence of the items does not matter.** 

Suppose instead of electing officers, we are merely picking three students to serve on a cleanup crew. If I pick Alice, Bob, and Charlie, it is the exact same cleanup crew as picking Charlie, Bob, and Alice. The sequence does not create a new reality; it merely describes the same reality in a different way. 

Because order does not generate unique outcomes here, **forming a generalized committee from a larger group utilizes combination calculations because the specific order of selection is irrelevant.**

![Combinations illustrate the selection of items where internal ordering is ignored. Each unique grouping represents a single combination, regardless of how its elements are arranged.](https://wikipedia.org/wiki/Special:Redirect/file/Combinations_without_repetition%3B_5_choose_3.svg)

### Unifying the Two Concepts
If combinations ignore the different orderings of the same items, it stands to reason that combinations will always yield a smaller total number than permutations. In fact, **the number of possible combinations for a [subset](https://en.wikipedia.org/wiki/Subset) of items is always less than or equal to the number of possible permutations for that same subset.**

But *how much* smaller? 

Think like a [mathematician](https://en.wikipedia.org/wiki/Mathematician). Let's say we have already calculated the permutations for choosing 3 students from 20. We have counted every distinct arrangement. But wait—for any specific group of 3 students (say, Alice, Bob, and Charlie), how many different ways did we arrange them in our permutation count? We arranged them \$3!$ ways (which is 6 ways). To convert our permutations into combinations, we must divide out this redundancy! We must group those 6 overlapping arrangements together and count them as just 1 combination.

> **The Combination Formula**
> **The formula for calculating combinations divides the total number of permutations by the [factorial](https://en.wikipedia.org/wiki/Factorial) of the number of chosen items.**

Mathematically, this elegant correction looks like this:
$$C(n, k) = \frac{P(n, k)}{k!} = \frac{n!}{k!(n - k)!}$$

By dividing by $k!$, we effortlessly erase the illusion of order, leaving behind only the pure, unordered selections. 

When you sit down to calculate outcomes on your exam, ask yourself these core questions: Are the events [independent](https://en.wikipedia.org/wiki/Independence_%28probability_theory%29) or [dependent](https://en.wikipedia.org/wiki/Conditional_probability)? Are we replacing the items or leaving them out? And, most importantly, *does the order of the final result matter?* Once you answer those, the [geometry](https://en.wikipedia.org/wiki/Geometry) of possibility resolves itself into clear, calculable certainty.