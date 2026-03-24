Let’s play a little game of mathematical jeopardy. Usually, in [math](https://en.wikipedia.org/wiki/Mathematics), we give you a [number](https://en.wikipedia.org/wiki/Number), give you an [operation](https://en.wikipedia.org/wiki/Operation_%28mathematics%29), and ask you to find the result. "Take $7$, square it, what do you get?" Easy. You get $49$. 

But what if we play the tape backward? What if I tell you the *result* and ask you to figure out where we started? What if I say, "I am thinking of a number. When I [multiply](https://en.wikipedia.org/wiki/Multiplication) this number by itself, I get $49$. What number am I thinking of?"

Welcome to the world of quadratic equations!

At its heart, **a simple quadratic equation can be written in the form $x^2 = c$, where $x$ is a [variable](https://en.wikipedia.org/wiki/Variable_%28mathematics%29) and $c$ is a constant.** 

Solving this [equation](https://en.wikipedia.org/wiki/Equation) is a detective game. **Solving the equation $x^2 = c$ requires finding all numerical values of $x$ that produce the constant $c$ when multiplied by themselves.** It sounds straightforward, doesn't it? But nature, and mathematics, often hides wonderful little subtleties in the simplest places. Let’s investigate.

---

## The Two Paths to the Same Destination

Let's look at the constant we get when we multiply numbers.

We all know that if you have a [positive number](https://en.wikipedia.org/wiki/Sign_%28mathematics%29), let's say $3$, and you square it ($3 \times 3$), you get $9$. This is a universal truth: **the square of any positive [real number](https://en.wikipedia.org/wiki/Real_number) is always a positive real number.** 

But here is where the plot thickens. What happens when we venture into the negatives? What is $-3 \times -3$? It is *also* $9$. Why? Because of the fundamental rules of arithmetic, the [negative signs](https://en.wikipedia.org/wiki/Plus_and_minus_signs) cancel each other out. **Multiplying a [negative real number](https://en.wikipedia.org/wiki/Negative_number) by itself always results in a positive real number [product](https://en.wikipedia.org/wiki/Product_%28mathematics%29).**

Do you see the beautiful [symmetry](https://en.wikipedia.org/wiki/Symmetry_%28mathematics%29) here? Both the positive path and the negative path lead us to the exact same positive destination. 

### Unlocking $x^2 = 49$

Let's return to our initial mystery: $x^2 = 49$. 

If we want to solve this, we are asking: *what real numbers can I square to get $49$?* 

Because of the dual-path nature of multiplication we just discovered, **the quadratic equation $x^2 = 49$ has exactly two real number solutions.** 
1. **The [positive integer](https://en.wikipedia.org/wiki/Natural_number) $7$ is a valid solution to the equation $x^2 = 49$.** ($7 \times 7 = 49$)
2. But don't forget the mirror image! **The [negative integer](https://en.wikipedia.org/wiki/Negative_number) $-7$ is a valid solution to the equation $x^2 = 49$.** Why? Because **squaring the number $-7$ yields the positive number $49$.** ($-7 \times -7 = 49$)

---

## The Machinery Under the Hood: Absolute Values

Let’s look at *how* we solve this algebraically, step-by-step. The instinct is to just "take the [square root](https://en.wikipedia.org/wiki/Square_root) of both sides." But if you do this without thinking, you fall into a trap.

> **Warning: The Most Common Trap in [Algebra](https://en.wikipedia.org/wiki/Algebra)**  
> When students first learn to solve these, they write $x = \sqrt{49}$ and conclude $x = 7$. They stop there. **A common algebraic error when solving equations of the form $x^2 = c$ is omitting the negative square root solution.** If you do this on the [Praxis exam](https://en.wikipedia.org/wiki/Praxis_test), you will lose points!

Let's look at what is actually happening when you apply a square root to an unknown squared variable. 

When you take the square root of $x^2$, the math operation itself suffers a kind of "amnesia." The square root function only spits out positive [distances](https://en.wikipedia.org/wiki/Distance). It doesn't know if the original $x$ was positive or negative before it got squared! Therefore, in strict mathematical terms, **the algebraic expression $\sqrt{x^2}$ simplifies to the [absolute value](https://en.wikipedia.org/wiki/Absolute_value) of $x$, written as $|x|$.**

Because of this amnesia, **taking the square root of both sides of the equation $x^2 = c$ yields the intermediate algebraic equation $|x| = \sqrt{c}$.**

Let's apply this to $x^2 = 49$:
1. $x^2 = 49$
2. $\sqrt{x^2} = \sqrt{49}$
3. $|x| = 7$

Now, ask yourself: *What values can $x$ be so that its absolute value (its distance from [zero](https://en.wikipedia.org/wiki/0)) is $7$?* It can be $7$, or it can be $-7$. 

Boom! The math perfectly preserves the two solutions. We didn't just guess them; we *[proved](https://en.wikipedia.org/wiki/Mathematical_proof)* them.

---

## The Language of Mathematicians: Shorthand and Symbols

Mathematicians love efficiency. Writing out "$x$ equals the square root of $c$, or $x$ equals the negative square root of $c$" every single time is exhausting. So, we invented a tool called **The Square Root Property**. 

> **The Square Root Property**  
> **The square root property states that if $x^2 = c$ for a positive number $c$, the solutions are $x = \sqrt{c}$ and $x = -\sqrt{c}$.** 

To put it in the formal language of your exam: **the two solutions to the equation $x^2 = c$ for a positive constant $c$ are the [principal square root](https://en.wikipedia.org/wiki/Square_root) of $c$ and the negative square root of $c$.** (The "principal" square root simply means the positive one).

To write this even faster, mathematicians created a special symbol: $\pm$. 
**The mathematical symbol $\pm$ is read as "[plus or minus](https://en.wikipedia.org/wiki/Plus%E2%80%93minus_sign)".** 

Instead of writing two separate equations, **the [mathematical notation](https://en.wikipedia.org/wiki/Mathematical_notation) $x = \pm\sqrt{c}$ is a [shorthand](https://en.wikipedia.org/wiki/Shorthand) representation for the two independent solutions $x = \sqrt{c}$ and $x = -\sqrt{c}$.**

So, for $x^2 = 49$, an elite math student simply writes: 
$x = \pm 7$. 
Crisp, clear, and perfectly accurate.

---

## The Three Universes of $x^2 = c$

Depending on the constant $c$, our simple quadratic equation behaves in three completely different ways. You can think of these as three different mathematical "universes" you might encounter on your test.

### Universe 1: The Constant is Positive ($c > 0$)
We just spent a lot of time here. As we've established, **an equation of the form $x^2 = c$ has exactly two distinct real solutions when the constant $c$ is a positive number.** 
* *Example:* $x^2 = 25 \rightarrow x = \pm 5$.

### Universe 2: The Constant is Zero ($c = 0$)
What if I ask you, "What number multiplied by itself gives zero?" 
There is only one number in the universe that can do that. Zero has no positive or negative counterpart. Therefore, **an equation of the form $x^2 = c$ has exactly one real solution when the constant $c$ is equal to zero.** 
* *Example:* **The only real number solution to the equation $x^2 = 0$ is the number $0$.** ($x = 0$)

### Universe 3: The Constant is Negative ($c < 0$)
Now, what if I give you the equation $x^2 = -16$? 
Think about this carefully. We already proved that a positive times a positive is positive. We also proved that a negative times a negative is positive. **There is no real number that can be squared to produce a negative product.** 

If you try to type $\sqrt{-16}$ into a standard [calculator](https://en.wikipedia.org/wiki/Calculator), it will scream at you with an "ERROR" message. Therefore, **an equation of the form $x^2 = c$ has no real number solutions when the constant $c$ is a negative number.** (Later in your math journey, you might meet "[imaginary numbers](https://en.wikipedia.org/wiki/Imaginary_number)" that solve this, but strictly within the realm of *real numbers* tested on the Praxis Core, this is a dead end!)

### Summary Table: The Behavior of $x^2 = c$

| Value of Constant $c$ | Number of Real Solutions | Example | Solutions |
| :--- | :--- | :--- | :--- |
| **Positive ($c > 0$)** | Exactly Two | $x^2 = 81$ | $x = \pm 9$ |
| **Zero ($c = 0$)** | Exactly One | $x^2 = 0$ | $x = 0$ |
| **Negative ($c < 0$)** | None | $x^2 = -25$ | No real solutions |

---

## Final Thoughts for the Praxis Exam

When you sit down for the [Praxis Core Mathematics exam](https://en.wikipedia.org/wiki/Praxis_test) and you see a simple quadratic equation staring back at you, I want you to smile. 

You aren't just memorizing rules; you understand the *mechanics* of the equation. You know that equations like $x^2 = c$ are questions asking you to work backward. You know that positive targets offer two paths back home—a positive root and a negative root—linked together beautifully by the $\pm$ symbol. You know that if the target is negative, it's a trap, and no real number can take you there.

Remember the intermediate step ($|x| = \sqrt{c}$), don't forget your negative roots, and you will sail through these questions with absolute flying colors!