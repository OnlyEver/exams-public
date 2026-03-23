Here’s a secret about mathematics that a lot of textbooks try to hide: math is not a static object. It’s not just a dusty list of facts to memorize. Math is a *machine*, a choreography, a beautiful set of instructions that tells you exactly how to move from a state of ignorance to a state of truth. 

When you look at a problem on the Praxis Core exam, it's not just sitting there staring at you; it is actively asking you to *do* something. Today, we are going to look under the hood of mathematical processes. We'll learn how to run the machine forward, how to run it backward, how to read its blueprints, and what happens when the machine talks to itself. 

Let's dive into the fascinating world of arithmetic and algebraic procedures.

---

## Part I: The Mechanics of Algebraic Procedures

Imagine you are standing in front of a giant funnel with gears attached to it. You drop a number in the top, turn the crank, and a different number pops out the bottom. What you have just visualized is the essence of mathematical procedures. 

At its core, **an algebraic procedure is a sequence of defined mathematical operations applied to an initial value.**

But what happens when the initial value is hidden from us? Often, we are handed an expression with a letter—a variable like $x$ or $y$—holding the place of our missing number. When we finally discover the missing number, we use **substitution**, which **involves replacing variables in an algebraic expression with specific numerical values.** 

Once you swap out the letter for a number, the machine is ready to be turned on. **Evaluating an expression requires applying arithmetic operations after substituting variables with numbers.**

### The Rules of the Road: Order of Operations
Now, if you drop a number into the machine and start applying operations willy-nilly, chaos ensues. Nature has a strict hierarchy, and so does math. To guarantee that every mathematician on Earth gets the exact same result from the same expression, we follow a universal traffic code.

> **The Universal Order of Operations**
> 1. **The VIPs (Parentheses):** The **order of operations dictates that expressions inside parentheses are evaluated first.** Whatever is trapped inside the brackets gets handled before the outside world is even considered.
> 2. **The Heavy Lifters (Exponents):** Next, the **order of operations dictates that exponents are evaluated before multiplication and division.** If a number is squared or cubed, you unleash that power immediately.
> 3. **The Workers (Multiplication & Division):** Moving left to right, the **order of operations dictates that multiplication and division are evaluated before addition and subtraction.**
> 4. **The Sweepers (Addition & Subtraction):** Finally, you handle the simple pluses and minuses to finish evaluating your expression.

### Running the Machine in Reverse: Solving Equations
What if you already know what popped out of the machine, and you want to figure out what was dropped in? You have to run the machine backward. 

To do this, you rely on an **inverse operation**, which is simply a tool that **reverses the effect of another specific mathematical operation.** If the machine added $5$, you subtract $5$. If it multiplied by $10$, you divide by $10$. 

But an equation is like a perfectly balanced scale. You can't just throw weight off one side without tipping the whole thing over. Therefore, **solving an equation step-by-step requires applying inverse operations to both sides of the equation.** To keep the scales perfectly level from start to finish, **maintaining equality requires performing the exact same mathematical operation on both sides of an equation.**

---

## Part II: Recurrence and Sequences - When Math Repeats Itself

Sometimes, the outcome of an operation doesn't just sit there—it gets immediately dropped *back* into the top of the machine. This creates a chain reaction, generating a list of numbers. This is the mesmerizing reality of a **recurrence relation**, which **is a mathematical equation that expresses the nth term of a sequence as a function of previous terms.**

When we generate a list using this relation, we call it a **recursive sequence**, because it **defines each term based on one or more previous terms in the sequence.**

### The Anatomy of Recursion
You can't build a sequence out of thin air. You need a starting point. Thus, **a recursive sequence requires at least one initial starting value known as the base case.** 

Once you have your base case, the sequence can run forever. But there is a catch! Because each step depends intimately on the step right before it, there are no magical shortcuts. **Finding a specific term in a recursive sequence requires calculating all intermediate preceding terms.** If you want the 10th term, you absolutely must figure out the 9th term first, which means you need the 8th term, and so on.

### Flavors of Sequences
There are different rhythms to these mathematical loops.

| Sequence Type | How It Grows | Example |
| :--- | :--- | :--- |
| **Arithmetic Sequence** | An **arithmetic sequence adds a constant numerical difference to the previous term to generate the next term.** Think of climbing stairs: steady, constant steps. | $2, 5, 8, 11...$ (Base case 2, add 3 each time) |
| **Geometric Sequence** | A **geometric sequence multiplies the previous term by a constant numerical ratio to generate the next term.** Think of biological cell division: explosive, scaling growth. | $3, 6, 12, 24...$ (Base case 3, multiply by 2 each time) |

### The Crown Jewel: Fibonacci
Nature loves recursive sequences. Have you ever noticed the spirals of seeds on a sunflower or the curve of a nautilus shell? They are governed by one of the most famous patterns in human history: the Fibonacci sequence. 

The **Fibonacci sequence is a mathematical recursive sequence.** Its rule is simple yet profoundly elegant: **The Fibonacci sequence adds the two immediately preceding terms to generate the next term.** 

Because it needs *two* previous terms, it requires *two* base cases: $0$ and $1$. 
* $0 + 1 = 1$
* $1 + 1 = 2$
* $1 + 2 = 3$
* $2 + 3 = 5$

The sequence blooms as $0, 1, 1, 2, 3, 5, 8, 13, 21...$ and continues into infinity, a beautiful consequence of a remarkably simple procedure.

---

## Part III: Flowcharts - The Cartography of Logic

We have talked about these procedures abstractly, but what happens when an algorithm gets wildly complicated? How do we keep track of where we are, especially when programming computers or analyzing complex Praxis math logic? 

We draw a map. A **flowchart is a visual representation of a step-by-step mathematical algorithm.**

### The Universal Language of Shapes
When you look at a flowchart, the geometry speaks to you before you even read the words. There is a universal standard for these diagrams:

1. **The Ovals (The Boundaries):** In standard algorithmic flowcharts, **oval shapes indicate the start point or end point of a process.** They are the greeting and the farewell of the algorithm.
2. **The Rectangles (The Actions):** In standard algorithmic flowcharts, **rectangular shapes represent processing steps or mathematical operations.** When you see a rectangle, it is an instruction: *add 4, square the result, divide by y.*
3. **The Diamonds (The Crossroads):** In standard algorithmic flowcharts, **diamond shapes denote decision points or conditional branching.** They are the moments of suspense. Is the number even? Is $x$ greater than $100$? The diamond forces the algorithm to ask a question.

### Branching and Looping
When the algorithm hits a diamond, it faces a fork in the road. A **conditional branch in a flowchart directs a process along different paths based on a true or false condition.** 

For example, if the diamond asks "Is $x < 10$?" and the answer is "True," the branch might send you left to add $5$. If "False," the branch might send you right to end the program. 

Sometimes, a branch sends you backwards, pointing an arrow to a step you've already completed. This creates a **loop in a flowchart [which] repeats a specific sequence of operations until a defined condition is met.** Loops are exactly how computer programs generate those recursive sequences we just talked about!

### The Art of Tracing
If you are faced with a flowchart on an exam, how do you solve it without losing your mind? You must become an incredibly meticulous accountant. 

**Tracing an algorithm requires recording the current value of all variables after every individual operation.** 

> **Feynman's Tip for Tracing:** 
> Never try to hold the changing values in your head. Create a "T-chart" on your scratch paper. Label columns for every variable (e.g., $X$ and $Y$). Every time you pass through a rectangle in the flowchart, cross out the old number in your table and write the new one. Keep looping and updating your table until the diamond finally tells you to take the exit path to the "End" oval!

### Bringing It All Together
Math is movement. Whether you are maintaining equality across both sides of a static equation, hunting down the 14th term of a Fibonacci sequence, or tracing the true/false branches of a geometric flowchart, you are executing logic. 

Trust the order of operations. Respect the shapes. Keep a rigorous tally of your variables. If you follow the procedure step-by-step, the machine will never steer you wrong.