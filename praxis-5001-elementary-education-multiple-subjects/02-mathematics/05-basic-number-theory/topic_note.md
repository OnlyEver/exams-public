# The Architecture of [Numbers](https://en.wikipedia.org/wiki/Number): A [Praxis](https://en.wikipedia.org/wiki/Praxis_test) Study Guide to [Number Theory](https://en.wikipedia.org/wiki/Number_theory)

Imagine you are a [physicist](https://en.wikipedia.org/wiki/Physicist), but instead of taking apart [rocks](https://en.wikipedia.org/wiki/Rock_%28geology%29), [stars](https://en.wikipedia.org/wiki/Star), or [molecules](https://en.wikipedia.org/wiki/Molecule), you are taking apart *[numbers](https://en.wikipedia.org/wiki/Number)*. You want to know what they are made of. You look at a [number](https://en.wikipedia.org/wiki/Number) like [12](https://en.wikipedia.org/wiki/12_%28number%29), and you wonder, "Can I break this apart? Are there hidden gears inside?" 

Welcome to [Number Theory](https://en.wikipedia.org/wiki/Number_theory)! For your [Praxis exam](https://en.wikipedia.org/wiki/Praxis_test), you don’t just need to memorize definitions; you need to understand the *machinery* of numbers. Once you see how numbers are built, the rules stop being random facts and start becoming a beautiful, interconnected [puzzle](https://en.wikipedia.org/wiki/Puzzle). Let's look under the hood.

---

## 1. The [Atoms](https://en.wikipedia.org/wiki/Atom) of [Mathematics](https://en.wikipedia.org/wiki/Mathematics): [Primes](https://en.wikipedia.org/wiki/Prime_number) and [Composites](https://en.wikipedia.org/wiki/Composite_number)

If you smash a [rock](https://en.wikipedia.org/wiki/Rock_%28geology%29) into pieces, eventually you get down to the [atoms](https://en.wikipedia.org/wiki/Atom)—the fundamental building blocks that cannot be broken down any further. In [mathematics](https://en.wikipedia.org/wiki/Mathematics), our "atoms" are called [prime numbers](https://en.wikipedia.org/wiki/Prime_number).

> **A [prime number](https://en.wikipedia.org/wiki/Prime_number) is a [whole number](https://en.wikipedia.org/wiki/Integer) greater than [1](https://en.wikipedia.org/wiki/1) that has exactly two distinct positive [divisors](https://en.wikipedia.org/wiki/Divisor).** 

What are those two [divisors](https://en.wikipedia.org/wiki/Divisor)? It's perfectly simple: **The two distinct positive divisors of a prime number are the number 1 and the prime number itself.** You can't break a prime number down into any smaller whole-number chunks. It is [irreducible](https://en.wikipedia.org/wiki/Irreducible_%28mathematics%29). 

Let’s look at the prime numbers. **The prime numbers less than [20](https://en.wikipedia.org/wiki/20_%28number%29) are [2](https://en.wikipedia.org/wiki/2), [3](https://en.wikipedia.org/wiki/3), [5](https://en.wikipedia.org/wiki/5), [7](https://en.wikipedia.org/wiki/7), [11](https://en.wikipedia.org/wiki/11), [13](https://en.wikipedia.org/wiki/13), [17](https://en.wikipedia.org/wiki/17), and [19](https://en.wikipedia.org/wiki/19).** Notice that we skipped a few numbers. Where did [4](https://en.wikipedia.org/wiki/4), [6](https://en.wikipedia.org/wiki/6), and [8](https://en.wikipedia.org/wiki/8) go? Those are what we call *[composites](https://en.wikipedia.org/wiki/Composite_number)*. 

![The Sieve of Eratosthenes is a classic mathematical algorithm that systematically identifies prime numbers by filtering out the expanding multiples of each known prime.](https://wikipedia.org/wiki/Special:Redirect/file/Sieve_of_Eratosthenes_animation.gif)

> **A [composite number](https://en.wikipedia.org/wiki/Composite_number) is a [whole number](https://en.wikipedia.org/wiki/Integer) greater than 1 that has more than two positive divisors.** 

The word "composite" literally means "made up of various parts." A number like 6 can be divided by 1, 2, 3, and 6. Because it has more than two divisors, it's a composite number. 

![Visualizing the difference: Composite numbers (like 4 and 6) can be arranged into rectangular grids because they have multiple factors. Prime numbers (like 3 and 5) lack these extra divisors and cannot be broken down this way.](https://wikipedia.org/wiki/Special:Redirect/file/Primes-vs-composites.svg)

### The Oddballs: [0](https://en.wikipedia.org/wiki/0), [1](https://en.wikipedia.org/wiki/1), and [2](https://en.wikipedia.org/wiki/2)

Now, I can hear you thinking: *What about 0 and 1?* 
To just say "they are [exceptions](https://en.wikipedia.org/wiki/Exception)" is sad, because that's not math! We have to look at the definitions:

*   **The number 1 is neither a prime number nor a composite number.** Why? Remember the definition of a prime: it must have *exactly two distinct* positive divisors. The number 1 only has *one* divisor (itself). It doesn’t have enough parts to be prime, and it certainly doesn't have enough to be composite!
*   **The number 0 is neither a prime number nor a composite number.** You cannot [divide](https://en.wikipedia.org/wiki/Division_%28mathematics%29) 0 by itself to get a meaningful distinct divisor. It breaks the machinery entirely.

Then there is the number 2. What a wonderfully strange little number. **The number 2 is the smallest prime number.** Its only divisors are 1 and 2. But here is the magnificent trick: **The number 2 is the only [even](https://en.wikipedia.org/wiki/Parity_%28mathematics%29) prime number** in existence! 

Because every other even number on the [planet](https://en.wikipedia.org/wiki/Planet) can be divided by 2, they all have *at least* three divisors (1, 2, and the number itself). Therefore, **every even whole number greater than 2 is a composite number.** 

Furthermore, if you take any two of these prime "atoms" and [multiply](https://en.wikipedia.org/wiki/Multiplication) them together, you are actively building a composite! By definition, **the mathematical [product](https://en.wikipedia.org/wiki/Product_%28mathematics%29) of any two prime numbers is always a composite number** (for example, [3](https://en.wikipedia.org/wiki/3) × [5](https://en.wikipedia.org/wiki/5) = [15](https://en.wikipedia.org/wiki/15)). 

---

## 2. The Anatomy of a Number: [Factors](https://en.wikipedia.org/wiki/Divisor) vs. [Multiples](https://en.wikipedia.org/wiki/Multiple_%28mathematics%29)

To teach math effectively, we have to distinguish between what *goes into* a number and what *comes out* of a number. That brings us to factors and multiples.

### Factors: The Ingredients
Think of **factors** as the ingredients used to bake a number. 

> **A factor is a whole number that divides exactly into another whole number without leaving a [remainder](https://en.wikipedia.org/wiki/Remainder).**

Because factors are the ingredients inside a number, they are limited. **Any specific whole number has a [finite](https://en.wikipedia.org/wiki/Finite_set) quantity of factors.** You can count them. For the number 12, the factors are 1, 2, 3, 4, 6, and 12. That’s it. There are no more. 

Notice two universal truths about these ingredients:
1.  **The number 1 is a factor of every whole number.** (Every recipe requires 1!)
2.  **Every whole number greater than [zero](https://en.wikipedia.org/wiki/0) is a factor of itself.** (12 fits perfectly into 12 exactly one time). 

### Multiples: The Footsteps
If factors are the ingredients hiding *inside* a number, **multiples** are the giant footsteps a number takes when it walks forward. 

> **A multiple is the product of a given whole number and any other whole number.**

If you are a 5, your footsteps land on 5, [10](https://en.wikipedia.org/wiki/10), [15](https://en.wikipedia.org/wiki/15), [20](https://en.wikipedia.org/wiki/20_%28number%29), [25](https://en.wikipedia.org/wiki/25_%28number%29)... and so on. 
Because you can keep multiplying forever, **every whole number greater than zero has an [infinite](https://en.wikipedia.org/wiki/Infinity) quantity of multiples.** The path never ends!

Just like with factors, there is a mirror-image rule here: **Every whole number is a multiple of itself.** (5 × 1 = 5). 

### Quick Comparison

| Feature | Factors | Multiples |
| :--- | :--- | :--- |
| **Concept** | "Ingredients" that divide *into* the number. | "Footsteps" that multiply *out* from the number. |
| **Quantity** | **[Finite](https://en.wikipedia.org/wiki/Finite_set)** (There is a limited number of them). | **[Infinite](https://en.wikipedia.org/wiki/Infinity)** (They go on forever). |
| **Relation to Itself** | **Every whole number > 0 is a factor of itself.** | **Every whole number is a multiple of itself.** |
| **Universal Rule** | **The number 1 is a factor of every whole number.** | All multiples grow from the base number. |

---

## 3. Smashing Numbers Apart: [Prime Factorization](https://en.wikipedia.org/wiki/Integer_factorization)

If composite numbers are made of prime atoms, how do we reverse-engineer them? 

**[Prime factorization](https://en.wikipedia.org/wiki/Integer_factorization) is the mathematical process of expressing a composite number as the product of prime numbers.** 

This isn't just a neat trick; it is a profound law of nature. In fact, it is so important that [mathematicians](https://en.wikipedia.org/wiki/Mathematician) gave it a grand title: **The [Fundamental Theorem of Arithmetic](https://en.wikipedia.org/wiki/Fundamental_theorem_of_arithmetic) states that every composite number can be uniquely expressed as a product of prime numbers.** 

Think of it like a mathematical [fingerprint](https://en.wikipedia.org/wiki/Fingerprint). The number [60](https://en.wikipedia.org/wiki/60_%28number%29) will *always* break down into 2 × 2 × 3 × 5. No other number in the [universe](https://en.wikipedia.org/wiki/Universe) has that exact prime factorization, and 60 can never be built any other way. 

![Just as a physical fingerprint uniquely identifies an individual, the Fundamental Theorem of Arithmetic ensures that every composite number possesses a single, entirely unique prime factorization.](https://wikipedia.org/wiki/Special:Redirect/file/Fingerprint_Whorl.jpg)

How do we find this fingerprint? We use a visual tool! **A factor tree is a visual [diagram](https://en.wikipedia.org/wiki/Diagram) used to break down a composite number into the composite number's [prime factors](https://en.wikipedia.org/wiki/Prime_factor).** 
You start with your composite number at the top, split it into any two factors, and keep splitting those branches until every branch ends in a prime number. Then, you circle the primes. You've successfully mined the atoms!

---

## 4. The Secret Codes: [Divisibility Rules](https://en.wikipedia.org/wiki/Divisibility_rule)

When you are breaking numbers down, you don't want to sit there doing [long division](https://en.wikipedia.org/wiki/Long_division) for hours to figure out if a number is a factor. You want a shortcut. Fortunately, our [base-10 number system](https://en.wikipedia.org/wiki/Decimal) has hidden cheat codes built right into it. 

### The "Final Digit" Rules
You can tell a lot about a number just by looking at its tail end:
*   **Divisibility by 2:** **A whole number is divisible by 2 if the number's final [digit](https://en.wikipedia.org/wiki/Numerical_digit) is 0, 2, 4, 6, or 8.** (This just means the number is even!)
*   **Divisibility by 5:** **A whole number is divisible by 5 if the number's final digit is exactly 0 or 5.** (Think about counting by 5s: 5, 10, 15, 20... the pattern is obvious).
*   **Divisibility by 10:** **A whole number is divisible by 10 if the number's final digit is exactly 0.** 

### The "Sum of the Digits" Rules
Here is where the math feels like magic. For the numbers 3 and [9](https://en.wikipedia.org/wiki/9), you don't look at the last digit; you add the digits together!
*   **Divisibility by 3:** **A whole number is divisible by 3 if the [sum](https://en.wikipedia.org/wiki/Summation) of the number's digits is a multiple of 3.** (Example: For [111](https://en.wikipedia.org/wiki/111_%28number%29), 1+1+1 = 3. Since 3 is divisible by 3, so is 111!)
*   **Divisibility by 9:** **A whole number is divisible by 9 if the sum of the number's digits is a multiple of 9.** (Example: For [81](https://en.wikipedia.org/wiki/81_%28number%29), 8+1 = 9. So 81 is divisible by 9). 

### The "Combination" Rules
Some rules require you to look at a chunk of the number, or combine previous rules:
*   **Divisibility by 4:** **A whole number is divisible by 4 if the two-digit number formed by the final two digits is a multiple of 4.** (Example: In 3,5**12**, we just look at the 12. Since 12 is a multiple of 4, the entire gigantic number is divisible by 4).
*   **Divisibility by 6:** This one is a team effort. **A whole number is divisible by 6 if the number is simultaneously divisible by the number 2 and the number 3.** (Because 2 × 3 = 6, it must pass both of those tests to pass the test for 6).

---

## 5. When Numbers Interact: [GCF](https://en.wikipedia.org/wiki/Greatest_common_divisor) and [LCM](https://en.wikipedia.org/wiki/Least_common_multiple)

Finally, what happens when two different numbers walk into a room together? We usually want to compare their anatomy (their factors) or their paths (their multiples). 

### [Greatest Common Factor](https://en.wikipedia.org/wiki/Greatest_common_divisor) (GCF)
If you want to divide two groups of things into the largest possible equal piles, you need the GCF. 

> **The Greatest Common Factor is the largest whole number that divides evenly into two or more specified whole numbers.** 

If we have 12 and [18](https://en.wikipedia.org/wiki/18_%28number%29), we list their factors:
*   Factors of 12: 1, 2, 3, 4, **6**, 12
*   Factors of 18: 1, 2, 3, **6**, 9, 18
The largest ingredient they share is 6. Therefore, the GCF is 6.

![Visualizing the Greatest Common Factor (GCF): A 24-by-60 rectangle can be perfectly covered by 12-by-12 square tiles, because 12 is the largest common ingredient (factor) shared by both dimensions.](https://wikipedia.org/wiki/Special:Redirect/file/24x60.svg)

But what if they don't share *any* meaningful ingredients? What if our numbers are 8 and 15?
*   Factors of 8: **1**, 2, 4, 8
*   Factors of 15: **1**, 3, 5, 15
The only factor they share is 1! When this happens, we have a special name for their relationship: **Two numbers are defined as [relatively prime](https://en.wikipedia.org/wiki/Coprime_integers) if the Greatest Common Factor of the two numbers is exactly 1.** They don't have to be prime numbers themselves (8 and 15 are both composite), but *relative to each other*, they share no common atomic [DNA](https://en.wikipedia.org/wiki/DNA) other than 1.

![In engineering, connected gears are often designed with relatively prime numbers of teeth (like 13 and 21). Because they share no common factors other than 1, the exact same teeth rarely meet, ensuring the entire gear wears down evenly over time.](https://wikipedia.org/wiki/Special:Redirect/file/Gears_large.jpg)

### [Least Common Multiple](https://en.wikipedia.org/wiki/Least_common_multiple) (LCM)
If the GCF is about looking backward into the ingredients, the LCM is about looking forward into the footsteps. If two [planets](https://en.wikipedia.org/wiki/Planet) are [orbiting](https://en.wikipedia.org/wiki/Orbit) the [sun](https://en.wikipedia.org/wiki/Sun) at different speeds, when will they align again? You need the LCM!

> **The Least Common Multiple is the smallest positive whole number that is a multiple of two or more specified whole numbers.**

If we have 4 and 6, we track their multiples (footsteps):
*   Multiples of 4: 4, 8, **12**, 16, 20...
*   Multiples of 6: 6, **12**, 18, 24...
The very first time their footsteps land on the exact same spot is 12. Therefore, 12 is the Least Common Multiple.

***

### Summary for the [Praxis](https://en.wikipedia.org/wiki/Praxis_test)
[Number theory](https://en.wikipedia.org/wiki/Number_theory) isn't just a list of [vocabulary](https://en.wikipedia.org/wiki/Vocabulary) words. It is the study of how numbers are built (Primes and Composites), what they are made of (Factors), where they are going (Multiples), and how they interact with one another (GCF and LCM). When you sit down for your [Praxis exam](https://en.wikipedia.org/wiki/Praxis_test), don't just try to remember the rules—visualize the machinery. You've got this!