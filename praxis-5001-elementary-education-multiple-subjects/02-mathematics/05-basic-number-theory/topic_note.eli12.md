# The Architecture of Numbers: A Praxis Study Guide to Number Theory

Imagine you are taking apart a video game console to see how it works. Instead of taking apart electronics, we are going to take apart *numbers*! You look at a number like 12 and wonder, "What is this made of? Are there hidden pieces inside?" 

Welcome to Number Theory! For your test, you don't just memorize rules; you learn how numbers are built. Once you see how numbers are put together, the rules feel like solving a fun puzzle. Let's look under the hood!

---

## 1. The Atoms of Mathematics: Primes and Composites

If you break down a Lego creation, you eventually get down to the smallest, single-bump bricks that cannot be snapped apart into anything smaller. In math, our smallest, unbreakable "bricks" are called prime numbers.

**A prime number is a whole number greater than 1 that has exactly two distinct positive divisors.** 

What are those two divisors? It's perfectly simple: **The two distinct positive divisors of a prime number are the number 1 and the prime number itself.** You can't break a prime number down into any smaller whole-number pieces. 

Let's look at a list of them. **The prime numbers less than 20 are 2, 3, 5, 7, 11, 13, 17, and 19.** Notice that we skipped numbers like 4, 6, and 8. Those are what we call *composites*. 

**A composite number is a whole number greater than 1 that has more than two positive divisors.** 

The word "composite" means "made up of different parts." A number like 6 can be divided by 1, 2, 3, and 6. Because it has more than two divisors, it's a composite number. 

### The Oddballs: 0, 1, and 2

Now, you might be wondering: *What about 0 and 1?* 
We have to look at the exact rules:

*   **The number 1 is neither a prime number nor a composite number.** Why? Remember the rule for a prime: it must have *exactly two distinct* positive divisors. The number 1 only has *one* divisor (itself). It doesn't have enough pieces to be prime, and it definitely doesn't have enough to be composite!
*   **The number 0 is neither a prime number nor a composite number.** You cannot divide 0 by itself to get a real answer. It just breaks the rules of math entirely.

Then there is the number 2. What a cool little number. **The number 2 is the smallest prime number.** Its only divisors are 1 and 2. But here is the awesome trick: **The number 2 is the only even prime number** in the world! 

Because every other even number on the planet can be divided by 2, they all have *at least* three divisors (1, 2, and the number itself). Because of this, **every even whole number greater than 2 is a composite number.** 

Also, if you take any two of those unbreakable prime "bricks" and multiply them together, you are building a composite! By rule, **the mathematical product of any two prime numbers is always a composite number.**

Step-by-step example:
1. Pick a prime number: 3.
2. Pick another prime number: 5.
3. Multiply them together: 3 x 5 = 15.
4. The answer, 15, is a composite number (it can be divided by 1, 3, 5, and 15). 

---

## 2. The Anatomy of a Number: Factors vs. Multiples

To really get math, we have to know the difference between what goes *into* a number and what comes *out* of a number. That brings us to factors and multiples.

### Factors: The Ingredients
Think of **factors** as the ingredients used to bake a number, just like making a pizza. 

**A factor is a whole number that divides exactly into another whole number without leaving a remainder.**

Because factors are the ingredients hiding inside a number, there is a limit to them. **Any specific whole number has a finite quantity of factors.** "Finite" means you can count them and they stop. 

Step-by-step example for finding the factors of 12:
1. Think of numbers that multiply to make 12.
2. 1 x 12 = 12 (so 1 and 12 are factors).
3. 2 x 6 = 12 (so 2 and 6 are factors).
4. 3 x 4 = 12 (so 3 and 4 are factors).
5. The full list of factors for 12 is: 1, 2, 3, 4, 6, and 12. That's it! There are no more.

Notice two rules that are always true about these ingredients:
1.  **The number 1 is a factor of every whole number.** (Every pizza needs crust!)
2.  **Every whole number greater than zero is a factor of itself.** (12 fits perfectly into 12 exactly one time). 

### Multiples: The Footsteps
If factors are the ingredients *inside* a number, **multiples** are the giant footsteps a number takes when it jumps forward in a game. 

**A multiple is the product of a given whole number and any other whole number.**

If your character jumps by 5s, your footsteps land on 5, 10, 15, 20, 25... and so on. 
Because you can keep jumping forever, **every whole number greater than zero has an infinite quantity of multiples.** The path never ends!

Just like with factors, there is a mirror rule here: **Every whole number is a multiple of itself.** 

Step-by-step example:
1. Start with the number 5.
2. Multiply it by 1: 5 x 1 = 5.
3. Because the answer is 5, 5 is a multiple of itself!

### Quick Comparison

| Feature | Factors | Multiples |
| :--- | :--- | :--- |
| **Concept** | "Ingredients" that divide *into* the number. | "Footsteps" that multiply *out* from the number. |
| **Quantity** | **Finite** (There is a limited amount of them). | **Infinite** (They go on forever). |
| **Relation to Itself** | **Every whole number greater than zero is a factor of itself.** | **Every whole number is a multiple of itself.** |
| **Universal Rule** | **The number 1 is a factor of every whole number.** | All multiples grow from the starting number. |

---

## 3. Smashing Numbers Apart: Prime Factorization

If composite numbers are made of prime Lego bricks, how do we take them apart to see the bricks? 

**Prime factorization is the mathematical process of expressing a composite number as the product of prime numbers.** 

This isn't just a neat trick; it is a massive rule of nature. In fact, mathematicians gave it a grand title: **The Fundamental Theorem of Arithmetic states that every composite number can be uniquely expressed as a product of prime numbers.** 

Think of it like a secret password for a video game level. The number 60 will *always* break down into 2 x 2 x 3 x 5. No other number in the world has that exact same password, and 60 can never be built any other way. 

How do we find this password? We draw a picture! **A factor tree is a visual diagram used to break down a composite number into the composite number's prime factors.** 

Step-by-step example for a factor tree of 12:
1. Write your composite number, 12, at the top.
2. Draw two branches pointing down and pick any two numbers that multiply to 12. Let's use 3 and 4.
3. Look at the 3. Since 3 is a prime number, draw a circle around it. That branch is completely done!
4. Look at the 4. Since 4 is a composite number, draw two more branches pointing down from it.
5. Pick two numbers that multiply to 4. We use 2 and 2.
6. Look at both 2s. Since 2 is a prime number, draw a circle around both of them.
7. Now every branch ends in a circled prime number! The prime factorization of 12 is 2 x 2 x 3.

---

## 4. The Secret Codes: Divisibility Rules

When you are breaking numbers down, you don't want to sit there doing long division for hours just to see if a number fits. You want a shortcut. Luckily, our number system has hidden cheat codes built right in!

### The "Final Digit" Rules
You can tell a lot about a number just by looking at its tail end:
*   **Divisibility by 2:** **A whole number is divisible by 2 if the number's final digit is 0, 2, 4, 6, or 8.** (This just means the number is even!)
*   **Divisibility by 5:** **A whole number is divisible by 5 if the number's final digit is exactly 0 or 5.** (Think about counting by 5s: 5, 10, 15, 20... the pattern is easy to spot).
*   **Divisibility by 10:** **A whole number is divisible by 10 if the number's final digit is exactly 0.** 

### The "Sum of the Digits" Rules
Here is where the math feels like magic. For the numbers 3 and 9, you don't look at the last digit. Instead, you add all the digits together!
*   **Divisibility by 3:** **A whole number is divisible by 3 if the sum of the number's digits is a multiple of 3.** 
    Step-by-step example for 111:
    1. Take the digits of 111 and add them up: 1 + 1 + 1 = 3.
    2. Check if the answer (3) is a multiple of 3. Yes, it is!
    3. Because it works, the entire number 111 is divisible by 3.
*   **Divisibility by 9:** **A whole number is divisible by 9 if the sum of the number's digits is a multiple of 9.** 
    Step-by-step example for 81:
    1. Take the digits of 81 and add them up: 8 + 1 = 9.
    2. Check if the answer (9) is a multiple of 9. Yes, it is!
    3. Because it works, the entire number 81 is divisible by 9.

### The "Combination" Rules
Some rules ask you to look at a chunk of the number, or they combine previous rules together as a team:
*   **Divisibility by 4:** **A whole number is divisible by 4 if the two-digit number formed by the final two digits is a multiple of 4.** 
    Step-by-step example for 3,512:
    1. Look only at the final two digits of 3,512. That gives us 12.
    2. Check if 12 is a multiple of 4. (4 x 3 = 12). Yes, it is!
    3. Because 12 works, the giant number 3,512 is divisible by 4.
*   **Divisibility by 6:** **A whole number is divisible by 6 if the number is simultaneously divisible by the number 2 and the number 3.** ("Simultaneously" just means at the exact same time).
    Step-by-step example for 18:
    1. Check the rule for 2: Is the final digit even? Yes, 8 is even.
    2. Check the rule for 3: Do the digits add up to a multiple of 3? (1 + 8 = 9, and 9 is a multiple of 3). Yes!
    3. Because it passes BOTH tests, 18 is divisible by 6.

---

## 5. When Numbers Interact: GCF and LCM

Finally, what happens when two different numbers are in the same math problem? Like friends pooling their allowances together, we might want to compare their ingredients (factors) or the paths they walk on (multiples). 

### Greatest Common Factor (GCF)
If you have two big piles of candy and want to divide them into the largest possible equal piles, you need the GCF. 

**The Greatest Common Factor is the largest whole number that divides evenly into two or more specified whole numbers.** 

Step-by-step example for the GCF of 12 and 18:
1. List the factors (ingredients) of 12: 1, 2, 3, 4, **6**, 12.
2. List the factors (ingredients) of 18: 1, 2, 3, **6**, 9, 18.
3. Look for the biggest number that shows up on both lists.
4. The largest shared ingredient is 6. So, the GCF is 6.

But what if they don't share *any* good ingredients? What if our numbers are 8 and 15?
Step-by-step example for 8 and 15:
1. List the factors of 8: **1**, 2, 4, 8.
2. List the factors of 15: **1**, 3, 5, 15.
3. The only factor they share is 1!
When this happens, we have a special name for how they match up: **Two numbers are defined as relatively prime if the Greatest Common Factor of the two numbers is exactly 1.** They don't have to be prime numbers all by themselves (8 and 15 are both composite), but *compared to each other*, they don't share any matching bricks except the number 1.

### Least Common Multiple (LCM)
If the GCF is about looking backward at the ingredients inside, the LCM is about looking forward at their footsteps. If you and your friend are running laps on a track, but you run at different speeds, when will you cross the starting line at the exact same time? You need the LCM!

**The Least Common Multiple is the smallest positive whole number that is a multiple of two or more specified whole numbers.**

Step-by-step example for the LCM of 4 and 6:
1. List the multiples (footsteps) of 4: 4, 8, **12**, 16, 20...
2. List the multiples (footsteps) of 6: 6, **12**, 18, 24...
3. Look for the very first number that shows up on both lists.
4. The first time their footsteps land on the exact same spot is 12. Therefore, 12 is the Least Common Multiple.

***

### Summary for the Praxis
Number theory isn't just a list of vocabulary words. It is learning how numbers are built (Primes and Composites), what they are made of (Factors), where they are going (Multiples), and how they share with one another (GCF and LCM). When you take your test, don't just try to memorize rules—think about Lego bricks, pizza ingredients, and video game cheat codes. You've got this!