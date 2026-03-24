## The Nature of the Unknown: An Introduction to Probability

Imagine you're standing at the edge of the [universe](https://en.wikipedia.org/wiki/Universe), looking into the [future](https://en.wikipedia.org/wiki/Future). You don't know exactly what’s going to happen next. Will it [rain](https://en.wikipedia.org/wiki/Rain) tomorrow? Will you draw the [Ace of Spades](https://en.wikipedia.org/wiki/Ace_of_spades)? Will the bus arrive on time? We can't predict the future with absolute certainty—but nature has given us a trick. We can measure our ignorance. 

That measurement is what we call **probability**. At its core, **probability is a [mathematical](https://en.wikipedia.org/wiki/Mathematics) measure of the likelihood that a specific [event](https://en.wikipedia.org/wiki/Event_%28probability_theory%29) will occur.** It is the language we use to quantify [uncertainty](https://en.wikipedia.org/wiki/Uncertainty). 

For the [Praxis Core Mathematics exam](https://en.wikipedia.org/wiki/Praxis_test), you don't need to be a fortune teller to solve probability problems. You just need to understand the mechanics of how we count possibilities. Let’s roll up our sleeves and figure out how to mathematically map the unknown!

---

## The Anatomy of an Experiment

Before we can calculate anything, we have to define the sandbox we are playing in. In probability, we are always observing some sort of "experiment"—like [flipping a coin](https://en.wikipedia.org/wiki/Coin_flipping) or pulling a card from a [deck](https://en.wikipedia.org/wiki/Standard_52-card_deck). 

Whenever you run an experiment, you produce a **sample space**. Think of the sample space as the absolute boundaries of your universe. **A sample space is the complete set of all possible distinct outcomes of an experiment.** If a result isn't in the sample space, it simply doesn't exist in our experiment. 

Inside that sample space, we are usually looking for something specific to happen. We call this an **[event](https://en.wikipedia.org/wiki/Event_%28probability_theory%29)**. In mathematical terms, **an event is a defined set of outcomes resulting from a [statistical](https://en.wikipedia.org/wiki/Statistics) experiment.** 

When an event is as basic as it gets, we call it a **simple event**. **A simple event is a mathematical event that consists of exactly one single outcome.** For instance, if you are rolling a [die](https://en.wikipedia.org/wiki/Dice), rolling a "3" is a simple event. There is only one way it can happen. Conversely, rolling an "[even number](https://en.wikipedia.org/wiki/Parity_%28mathematics%29)" is a [compound event](https://en.wikipedia.org/wiki/Event_%28probability_theory%29), because it includes three distinct outcomes (2, 4, and 6).

Now, what do we call the outcomes we actually *want* to happen? We call them **favorable outcomes**. **Favorable outcomes are the specific outcomes from a sample space that satisfy the defined conditions of a target event.** The word "favorable" doesn't mean it's necessarily a *good* thing (your event could be "getting struck by lightning"), it just means it's the specific thing we are trying to measure.

---

## The Golden Rule: Theoretical Probability

How do we actually calculate the probability of an event? We use the foundational rule of theoretical probability. It is beautifully simple:

> **The theoretical probability of an event equals the number of favorable outcomes divided by the total number of possible outcomes.**
> 
> *Probability = (Favorable Outcomes) / (Total Possible Outcomes)*

But hold on! There is a catch. Nature isn't always fair, but our basic [math](https://en.wikipedia.org/wiki/Mathematics) assumes it is. **Theoretical probability requires the assumption that all possible outcomes in a given sample space are equally likely to occur.** If you are using a loaded die, or a coin with a weight taped to one side, this beautifully simple [formula](https://en.wikipedia.org/wiki/Formula) falls apart. 

### The Mathematical Boundaries of Reality (0 to 1)

How big or small can a probability be? Can you have a [negative](https://en.wikipedia.org/wiki/Negative_number) probability? Can you have a 200% probability? No! 

**The probability of any event is mathematically restricted to a numerical value between 0 and 1, inclusive.** This scale is absolute:
*   **An event with a probability of exactly 0 is impossible and cannot occur.** 
*   **An event with a probability of exactly 1 is absolutely certain to occur.** 

Because probability lives between 0 and 1, a **numerical probability value can be mathematically represented as a [fraction](https://en.wikipedia.org/wiki/Fraction)** (like $\frac{1}{2}$), **as a [decimal](https://en.wikipedia.org/wiki/Decimal)** (like $0.5$), or **as a [percentage](https://en.wikipedia.org/wiki/Percentage)** (like $50\%$). They are all just different dialects of the same mathematical language.

Furthermore, if we map out every single possibility in our universe, the parts must make up the whole. Therefore, **the [sum](https://en.wikipedia.org/wiki/Summation) of the individual probabilities of all distinct possible outcomes within a single sample space equals exactly 1.** If you add up the probabilities of every single thing that *could* happen, you get 100% certainty that *something* will happen.

### The Yin and Yang: Complements

Sometimes, it is incredibly difficult to calculate the probability of an event happening. But you know what might be incredibly easy? Calculating the probability of it *not* happening. 

This brings us to the concept of the **complement**. **The complement of an event includes every possible outcome in the sample space that does not belong to the target event.** It is everything else. If your event is "rolling a 6", the complement is "rolling a 1, 2, 3, 4, or 5."

Because the sum of all probabilities in a sample space equals 1, the math is delightfully simple:
> **The mathematical probability of the complement of an event equals 1 [minus](https://en.wikipedia.org/wiki/Subtraction) the probability of the target event occurring.**
>
> *P(Not Event) = 1 - P(Event)*

---

## The Classic Laboratory: Coins, Dice, and Cards

To test these ideas, probability relies on three classic instruments. You must be intimately familiar with them for the Praxis exam.

### 1. The Coin
The simplest universe possible. **A standard fair coin possesses exactly two distinct physical faces.** What are they? **The two faces of a standard coin are universally referred to as [heads and tails](https://en.wikipedia.org/wiki/Coin_flipping).** 
*   **Total possible outcomes:** 2
*   **P(Heads):** $\frac{1}{2}$, or $0.5$, or $50\%$

### 2. The Die
Let's step it up to six [dimensions](https://en.wikipedia.org/wiki/Dimension). **A standard fair six-sided [die](https://en.wikipedia.org/wiki/Dice) features the numerical values 1, 2, 3, 4, 5, and 6 on its respective faces.** 
*   **Total possible outcomes:** 6
*   **P(Rolling a 4):** $\frac{1}{6}$ (This is a simple event!)
*   **P(Rolling a 7):** $0$ (This is impossible!)

### 3. The Deck of Cards
This is where students often trip up, but if you look at the structure, it's a masterpiece of mathematical [symmetry](https://en.wikipedia.org/wiki/Symmetry). 

**A standard deck of playing cards contains exactly 52 cards when jokers are excluded.** This 52-card deck is perfectly compartmentalized: **a standard 52-card deck of playing cards is divided into exactly four equal suits.**

What are the suits? **The four suits in a standard deck of playing cards are hearts, diamonds, [clubs](https://en.wikipedia.org/wiki/Clubs_%28suit%29), and [spades](https://en.wikipedia.org/wiki/Spades_%28suit%29).** 

Because 52 divided by 4 is 13, **each individual suit in a standard 52-card deck of playing cards contains exactly 13 distinct cards** (Ace, 2 through 10, Jack, [Queen](https://en.wikipedia.org/wiki/Queen_%28playing_card%29), King).

| Suit | Color | Number of Cards | Probability of Drawing Suit |
| :--- | :--- | :--- | :--- |
| **Hearts** ♥ | [Red](https://en.wikipedia.org/wiki/Red) | 13 | $\frac{13}{52} = \frac{1}{4}$ or 25% |
| **Diamonds** ♦ | [Red](https://en.wikipedia.org/wiki/Red) | 13 | $\frac{13}{52} = \frac{1}{4}$ or 25% |
| **[Clubs](https://en.wikipedia.org/wiki/Clubs_%28suit%29)** ♣ | Black | 13 | $\frac{13}{52} = \frac{1}{4}$ or 25% |
| **[Spades](https://en.wikipedia.org/wiki/Spades_%28suit%29)** ♠ | Black | 13 | $\frac{13}{52} = \frac{1}{4}$ or 25% |

If the Praxis asks you for the theoretical probability of drawing a King, you count your favorable outcomes (there are 4 Kings in the deck) and divide by the total possible outcomes (52 cards). $\frac{4}{52}$ simplifies to $\frac{1}{13}$. Beautiful!

---

## When Math Meets Reality: Experimental and Geometric Probability

Theoretical probability tells us what *should* happen in a perfect, abstract universe. But what happens in the messy real world? 

### Experimental Probability
If you flip a fair coin 100 times, theoretically, you should get exactly 50 heads. But if you actually do it, you might get 54 heads, or 47 heads. 

This introduces our reality check: **experimental probability**. Instead of relying on abstract math, **experimental probability is calculated by dividing the observed number of times an event occurred by the total number of trials conducted.**

> *Experimental Probability = (Observed Occurrences) / (Total Number of Trials)*

If a baseball player gets a hit 30 times out of 100 at-bats, their experimental probability of getting a hit (their [batting average](https://en.wikipedia.org/wiki/Batting_average_%28baseball%29)!) is $\frac{30}{100}$ or $0.300$. We didn't deduce this from the shape of the bat; we deduced it from observing reality.

### Geometric Probability
Finally, what if our sample space isn't made up of [discrete](https://en.wikipedia.org/wiki/Discrete_mathematics), countable objects like cards or coin flips? What if our sample space is a continuous physical space, like a [dartboard](https://en.wikipedia.org/wiki/Darts) or a piece of string?

When we map probability onto physical dimensions, we use **geometric probability**.

1.  **Probability by Area:** Imagine throwing a dart randomly at a board. **Geometric probability calculates likelihood by dividing a specific target geometric area by the total available area.** If you have a square target of 10 [square inches](https://en.wikipedia.org/wiki/Square_inch) painted onto a wall that is 100 square inches, the probability of a random dart hitting the target is $\frac{10}{100}$ or $10\%$.
2.  **Probability by [Length](https://en.wikipedia.org/wiki/Length):** Now imagine a [bird](https://en.wikipedia.org/wiki/Bird) landing randomly on a [telephone wire](https://en.wikipedia.org/wiki/Utility_pole). **Geometric probability calculates likelihood by dividing a specific target geometric length by the total available length.** If a wire is 50 [feet](https://en.wikipedia.org/wiki/Foot_%28unit%29) long, and a 5-foot section of it sits directly above your newly washed car, the probability of the bird landing precisely on that 5-foot section is $\frac{5}{50}$ or $10\%$.

---

## Wrapping It Up

Probability is simply a [ratio](https://en.wikipedia.org/wiki/Ratio). It is the number of things you are looking for compared to the number of everything that exists in your specific scenario. Whether you are dealing with a standard fair die, tracking the experimental results of 1,000 trials, or measuring the geometric area of a target, the [logic](https://en.wikipedia.org/wiki/Logic) remains exactly the same. 

Remember your bounds: it will never be less than 0, and never more than 1. Find your total possible outcomes. Find your favorable outcomes. Divide them. That is the fundamental secret to decoding the mathematics of the unknown!