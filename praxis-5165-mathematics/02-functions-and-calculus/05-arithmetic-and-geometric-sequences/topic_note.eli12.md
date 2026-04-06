Think about a skateboarder going down a smooth, continuous ramp versus walking down a flight of stairs. A ramp covers every tiny millimeter of space. But stairs? You have to take distinct, countable steps. In math, **a sequence is a mathematical function whose domain is a subset of integers.** "Domain" just means the numbers you are allowed to plug in, and "integers" are whole numbers without fractions. Because we use sequences to count real steps or events (like level 1, level 2, level 3 of a video game), **the domain of a mathematical sequence is typically restricted to positive integers.**

When we write formulas for sequences, we use the letter *n*. **The variable n in sequence formulas represents the ordinal position of the term.** "Ordinal position" is just a fancy way of saying 1st, 2nd, 3rd, and so on. Because you cannot stand on the 2.5th step of a staircase, **the sequence position variable n must be an integer.** 

## The Two Lenses: Recursive vs. Explicit

When you play a board game, there are two different ways to figure out where your character is. 

First, you can count one space at a time. This is a recursive way of thinking. **A recursive formula calculates the nth term of a sequence based on one or more previous terms in the sequence.** It is like the game telling you, "To find your next spot, take your current spot and move forward three." But if you only have the rule "move forward three," you don't know where to start! Because of this, **a recursive formula for a sequence must explicitly state at least one initial term to be completely defined.** You absolutely need a starting line.

Second, you could just know your exact spot immediately based on how many turns you have taken. This is an explicit way of thinking. **An explicit formula calculates the nth term of a sequence using only the position number n.** Think of an explicit formula like a fast-travel cheat code in a video game that lets you teleport straight to level 10 without playing levels 1 through 9. Because of this fast-travel ability, **an arithmetic sequence can be evaluated for any term directly using the explicit formula without calculating preceding terms.** The exact same superpower works for multiplying patterns, too: **a geometric sequence can be evaluated for any term directly using the explicit formula without calculating preceding terms.**

---

## Arithmetic Sequences: Linear Growth on a Grid

Imagine you get a weekly allowance. You start with \$10, and your parents give you exactly \$5 every single week. Your total money over time is an arithmetic sequence! **An arithmetic sequence is a sequence of numbers in which the difference between any two consecutive terms is a constant.** 

**The constant difference between consecutive terms in an arithmetic sequence is called the common difference.** To find this secret number from a list of values, **the common difference of an arithmetic sequence is calculated by subtracting a term from the immediately following term.** 

Let's do the math step-by-step for the sequence 10, 15, 20, 25:
1. Pick any term in the sequence. Let's pick the second term, which is 15.
2. Look at the term right before it. The first term is 10.
3. Subtract the earlier term from the later term: 15 - 10 = 5. 
Your common difference is 5!

### Formulas and Structure

**The recursive formula for an arithmetic sequence is a_n = a_{n-1} + d.** This is a short way of saying: "The term you want right now (a_n) equals the term right before it (a_{n-1}) plus the common difference (d)." 

But what if you want to use your fast-travel cheat code? 
> **The explicit formula for an arithmetic sequence is a_n = a_1 + (n-1)d.**

Let's look at the pieces of this fast-travel code:
*   **In the explicit arithmetic formula a_n = a_1 + (n-1)d, the variable a_1 represents the first term.**
*   **In the explicit arithmetic formula a_n = a_1 + (n-1)d, the variable d represents the common difference.**

Why do we multiply by (n-1)? Let's break it down:
1. Imagine you want to find the 5th term in your sequence.
2. You start at the 1st term. 
3. To get from the 1st term to the 5th term, you only have to jump exactly 4 times. You always jump one time less than your destination number! So, (n-1) just means "the number of jumps."

### Modeling and Graphing

Because an arithmetic sequence grows by the exact same amount every step, **arithmetic sequences model linear growth or linear decay over discrete intervals.** "Linear" means a straight line. If you were to draw dots for your allowance money on a piece of graph paper, **an arithmetic sequence generates a linear graph when the sequence values are plotted against the term position numbers.** 

If you have learned about lines in algebra, you know about slope. **In an arithmetic sequence, the constant rate of change is equivalent to the slope of a linear function.** They are the exact same concept!

In the real world, this steady math is everywhere:
*   **Real-world scenarios involving simple interest accumulation can be modeled using arithmetic sequences.** For example, if a bank pays you exactly \$50 every year just for keeping your money there, your balance grows in an arithmetic sequence.
*   **Real-world scenarios involving a constant addition or subtraction of items over discrete steps can be modeled using arithmetic sequences.** For example, a pizza parlor using exactly 20 pepperoni slices per hour.

---

## Geometric Sequences: Exponential Scaling

Now imagine a video game where a blob monster doubles in size every single minute. The blob doesn't just add a fixed amount; it multiplies! **A geometric sequence is a sequence of numbers in which the ratio of any term to the preceding term is a constant.**

**The constant ratio between consecutive terms in a geometric sequence is called the common ratio.** To figure out the multiplier from a list of sizes, **the common ratio of a geometric sequence is calculated by dividing a term by the immediately preceding term.** 

Let's find the common ratio for the blob's size: 3, 6, 12, 24.
1. Pick any term in the sequence. Let's pick 12.
2. Look at the term right before it, which is 6.
3. Divide your chosen term by the earlier term: 12 / 6 = 2.
Your common ratio is 2!

### Formulas and Structure

**The recursive formula for a geometric sequence is a_n = r * a_{n-1}.** The instruction is super simple: "Take the common ratio (r) and multiply it by the previous term."

To fast-travel straight to the blob's size on the 10th minute, we use the explicit form.
> **The explicit formula for a geometric sequence is a_n = a_1 * r^(n-1).**

Let's look at the pieces:
*   **In the explicit geometric formula a_n = a_1 * r^(n-1), the variable a_1 represents the first term.**
*   **In the explicit geometric formula a_n = a_1 * r^(n-1), the variable r represents the common ratio.**

Just like before, the exponent is (n-1) because you only multiply by the ratio (n-1) times to get to your target spot!

### Modeling and Graphing

Because things multiply over and over, they skyrocket or shrink super fast. **Geometric sequences model exponential growth or exponential decay over discrete intervals.** Visually, **a geometric sequence generates an exponential graph when the sequence values are plotted against the term position numbers.** Instead of a straight line, it looks like a skateboard ramp rocketing upward. 

In algebra, this matches right up with exponents. **In a geometric sequence, the common ratio is equivalent to the base of an exponential function.** 

Real-world examples of geometric sequences are incredibly powerful:
*   **Real-world scenarios involving compound interest over discrete intervals can be modeled using geometric sequences.** This is when your bank account earns interest *on* your interest, multiplying your money!
*   **Real-world scenarios involving population growth by a fixed percentage per discrete time period can be modeled using geometric sequences.** If a town's population grows by 5% every single year, that is a geometric sequence.

---

## Translating Between Recursive and Explicit Forms

Sometimes in math, you have to switch back and forth between the step-by-step instructions (recursive) and the fast-travel cheat code (explicit). 

### Translating Arithmetic Formulas
When you are moving between arithmetic forms, focus closely on the number you are adding.
*   **To translate a recursive arithmetic formula to an explicit formula, the added constant in the recursive step becomes the common difference in the explicit formula.** 
    1. Look at a recursive formula: a_n = a_{n-1} + 7. The added number is 7.
    2. Put that 7 directly into the explicit formula where the common difference goes: a_n = a_1 + (n-1)7.
*   **To translate an explicit arithmetic formula to a recursive formula, the linear coefficient of n becomes the common difference in the recursive step.** 
    1. Look at an explicit formula: a_n = 4n + 3. 
    2. Find the "coefficient" (the number directly attached to n). Here, it is 4.
    3. Make 4 the added number in your recursive step: a_n = a_{n-1} + 4.

### Translating Geometric Formulas
When dealing with geometric patterns, keep your eye on the multiplier.
*   **To translate a recursive geometric formula to an explicit formula, the constant multiplier in the recursive step becomes the common ratio in the explicit formula.** 
    1. Look at a recursive formula: a_n = 3 * a_{n-1}. The multiplier is 3.
    2. Make 3 the base of the exponent in the explicit formula: a_n = a_1 * 3^(n-1).
*   **To translate an explicit geometric formula to a recursive formula, the base of the exponent becomes the common ratio in the recursive step.** 
    1. Look at the explicit formula: a_n = 5 * (0.8)^(n-1). 
    2. Find the base number that has the exponent attached to it. Here, it is 0.8.
    3. Make 0.8 the multiplier in your recursive step: a_n = 0.8 * a_{n-1}.

| Sequence Type | Core Feature | Recursive Form | Explicit Form | Translation Key |
| :--- | :--- | :--- | :--- | :--- |
| **Arithmetic** | Common Difference (d) | a_n = a_{n-1} + d | a_n = a_1 + (n-1)d | Added constant turns into the linear coefficient of n |
| **Geometric** | Common Ratio (r) | a_n = r * a_{n-1} | a_n = a_1 * r^(n-1) | Constant multiplier turns into the base of the exponent |

---

## Teaching Context: Technology and Domain

When learning math, tools like calculators are super helpful to see what sequences look like in action. 

**Graphing calculators evaluate recursive and explicit sequences using a specialized sequence graphing mode.** If you take a calculator and switch it from normal "Function" mode to "Sequence" mode, everything changes. The calculator stops using the letter X and starts using the letter n instead. 

Why is this special mode so important? Because it forces the calculator to only accept whole numbers! Remember, sequences are about distinct steps. You cannot be on level 2.5 of a video game. By using this special mode, your calculator perfectly follows the rules of the real world, only letting you explore the sequence one whole step at a time.