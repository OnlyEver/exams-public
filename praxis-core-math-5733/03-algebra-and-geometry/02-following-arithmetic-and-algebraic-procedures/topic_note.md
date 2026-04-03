Here’s a secret about [mathematics](https://en.wikipedia.org/wiki/Mathematics) that a lot of [textbooks](https://en.wikipedia.org/wiki/Textbook) try to hide: math is not a static object. It’s not just a dusty list of facts to memorize. Math is a *machine*, a choreography, a beautiful set of instructions that tells you exactly how to move from a state of ignorance to a state of [truth](https://en.wikipedia.org/wiki/Truth). 

When you look at a problem on the [Praxis Core exam](https://en.wikipedia.org/wiki/Praxis_test), it's not just sitting there staring at you; it is actively asking you to *do* something. Today, we are going to look under the hood of mathematical processes. We'll learn how to run the machine forward, how to run it backward, how to read its blueprints, and what happens when the machine talks to itself. 

Let's dive into the fascinating world of [arithmetic](https://en.wikipedia.org/wiki/Arithmetic) and [algebraic](https://en.wikipedia.org/wiki/Algebra) procedures.

---

## Part I: The Mechanics of Algebraic Procedures

Imagine you are standing in front of a giant funnel with [gears](https://en.wikipedia.org/wiki/Gear) attached to it. You drop a [number](https://en.wikipedia.org/wiki/Number) in the top, turn the crank, and a different number pops out the bottom. What you have just visualized is the essence of mathematical procedures. 

![A visual representation of an algebraic function acting as a machine, where an input is processed and transformed into a predictable output.](https://wikipedia.org/wiki/Special:Redirect/file/Function_machine2.svg)

At its core, **an [algebraic procedure](https://en.wikipedia.org/wiki/Algebraic_operation) is a sequence of defined [mathematical operations](https://en.wikipedia.org/wiki/Operation_%28mathematics%29) applied to an initial value.**

But what happens when the initial value is hidden from us? Often, we are handed an [expression](https://en.wikipedia.org/wiki/Expression_%28mathematics%29) with a letter—a [variable](https://en.wikipedia.org/wiki/Variable_%28mathematics%29) like $x$ or $y$—holding the place of our missing number. When we finally discover the missing number, we use **[substitution](https://en.wikipedia.org/wiki/Substitution_%28algebra%29)**, which **involves replacing variables in an [algebraic expression](https://en.wikipedia.org/wiki/Algebraic_expression) with specific numerical values.** 

Once you swap out the letter for a number, the machine is ready to be turned on. **Evaluating an expression requires applying [arithmetic operations](https://en.wikipedia.org/wiki/Arithmetic) after substituting variables with numbers.**

### The Rules of the Road: Order of Operations
Now, if you drop a number into the machine and start applying operations willy-nilly, chaos ensues. Nature has a strict hierarchy, and so does math. To guarantee that every [mathematician](https://en.wikipedia.org/wiki/Mathematician) on Earth gets the exact same result from the same expression, we follow a universal traffic code.

> **The Universal [Order of Operations](https://en.wikipedia.org/wiki/Order_of_operations)**
> 1. **The VIPs (Parentheses):** The **[order of operations](https://en.wikipedia.org/wiki/Order_of_operations) dictates that expressions inside [parentheses](https://en.wikipedia.org/wiki/Bracket) are evaluated first.** Whatever is trapped inside the brackets gets handled before the outside world is even considered.
> 2. **The Heavy Lifters (Exponents):** Next, the **order of operations dictates that [exponents](https://en.wikipedia.org/wiki/Exponentiation) are evaluated before multiplication and division.** If a number is [squared](https://en.wikipedia.org/wiki/Square_%28algebra%29) or [cubed](https://en.wikipedia.org/wiki/Cube_%28algebra%29), you unleash that power immediately.
> 3. **The Workers (Multiplication & Division):** Moving left to right, the **order of operations dictates that [multiplication](https://en.wikipedia.org/wiki/Multiplication) and [division](https://en.wikipedia.org/wiki/Division_%28mathematics%29) are evaluated before [addition](https://en.wikipedia.org/wiki/Addition) and [subtraction](https://en.wikipedia.org/wiki/Subtraction).**
> 4. **The Sweepers (Addition & Subtraction):** Finally, you handle the simple pluses and minuses to finish evaluating your expression.

![The standard order of operations dictates that parentheses and exponents are resolved first, followed by multiplication and division, and finally addition and subtraction.](https://wikipedia.org/wiki/Special:Redirect/file/Order_of_operations.svg)

### Running the Machine in Reverse: Solving Equations
What if you already know what popped out of the machine, and you want to figure out what was dropped in? You have to run the machine backward. 

To do this, you rely on an **[inverse operation](https://en.wikipedia.org/wiki/Inverse_operation)**, which is simply a tool that **reverses the effect of another specific mathematical operation.** If the machine added $5$, you [subtract](https://en.wikipedia.org/wiki/Subtraction) $5$. If it multiplied by $10$, you [divide](https://en.wikipedia.org/wiki/Division_%28mathematics%29) by $10$. 

But an [equation](https://en.wikipedia.org/wiki/Equation) is like a perfectly balanced scale. You can't just throw weight off one side without tipping the whole thing over. Therefore, **[solving an equation](https://en.wikipedia.org/wiki/Equation_solving) step-by-step requires applying inverse operations to both sides of the equation.** To keep the scales perfectly level from start to finish, **maintaining [equality](https://en.wikipedia.org/wiki/Equality_%28mathematics%29) requires performing the exact same mathematical operation on both sides of an equation.**

![An equation functions like a physical balance scale; to maintain mathematical equality, any operation performed on one side must be equally applied to the other.](https://wikipedia.org/wiki/Special:Redirect/file/Balance_scale.svg)

---

## Part II: Recurrence and Sequences - When Math Repeats Itself

Sometimes, the outcome of an operation doesn't just sit there—it gets immediately dropped *back* into the top of the machine. This creates a [chain reaction](https://en.wikipedia.org/wiki/Chain_reaction), generating a list of numbers. This is the mesmerizing reality of a **[recurrence relation](https://en.wikipedia.org/wiki/Recurrence_relation)**, which **is a mathematical equation that expresses the nth term of a [sequence](https://en.wikipedia.org/wiki/Sequence) as a [function](https://en.wikipedia.org/wiki/Function_%28mathematics%29) of previous terms.**

When we generate a list using this relation, we call it a **[recursive sequence](https://en.wikipedia.org/wiki/Recursion)**, because it **defines each term based on one or more previous terms in the sequence.**

### The Anatomy of Recursion
You can't build a sequence out of thin air. You need a starting point. Thus, **a recursive sequence requires at least one initial starting value known as the [base case](https://en.wikipedia.org/wiki/Recursion_%28computer_science%29).** 

Once you have your base case, the sequence can run forever. But there is a catch! Because each step depends intimately on the step right before it, there are no magical shortcuts. **Finding a specific term in a recursive sequence requires calculating all intermediate preceding terms.** If you want the 10th term, you absolutely must figure out the 9th term first, which means you need the 8th term, and so on.

### Flavors of Sequences
There are different rhythms to these mathematical loops.

| Sequence Type | How It Grows | Example |
| :--- | :--- | :--- |
| **Arithmetic Sequence** | An **[arithmetic sequence](https://en.wikipedia.org/wiki/Arithmetic_progression) adds a [constant](https://en.wikipedia.org/wiki/Constant_%28mathematics%29) numerical difference to the previous term to generate the next term.** Think of climbing stairs: steady, constant steps. | $2, 5, 8, 11...$ (Base case 2, add 3 each time) |
| **Geometric Sequence** | A **[geometric sequence](https://en.wikipedia.org/wiki/Geometric_progression) multiplies the previous term by a constant numerical [ratio](https://en.wikipedia.org/wiki/Ratio) to generate the next term.** Think of biological [cell division](https://en.wikipedia.org/wiki/Cell_division): explosive, [scaling growth](https://en.wikipedia.org/wiki/Exponential_growth). | $3, 6, 12, 24...$ (Base case 3, multiply by 2 each time) |

### The Crown Jewel: Fibonacci
Nature loves recursive sequences. Have you ever noticed the [spirals](https://en.wikipedia.org/wiki/Spiral) of seeds on a [sunflower](https://en.wikipedia.org/wiki/Common_sunflower) or the curve of a [nautilus shell](https://en.wikipedia.org/wiki/Nautilus)? They are governed by one of the most famous patterns in human history: the [Fibonacci sequence](https://en.wikipedia.org/wiki/Fibonacci_sequence). 

The **Fibonacci sequence is a mathematical recursive sequence.** Its rule is simple yet profoundly elegant: **The Fibonacci sequence adds the two immediately preceding terms to generate the next term.** 

Because it needs *two* previous terms, it requires *two* base cases: $0$ and $1$. 
* $0 + 1 = 1$
* $1 + 1 = 2$
* $1 + 2 = 3$
* $2 + 3 = 5$

![The Fibonacci spiral is constructed using squares whose side lengths correspond to successive numbers in the Fibonacci sequence, illustrating how recursive addition produces scaling geometric growth.](https://wikipedia.org/wiki/Special:Redirect/file/Fibonacci_Spiral.svg)

The sequence blooms as $0, 1, 1, 2, 3, 5, 8, 13, 21...$ and continues into [infinity](https://en.wikipedia.org/wiki/Infinity), a beautiful consequence of a remarkably simple procedure.

---

## Part III: Flowcharts - The Cartography of Logic

We have talked about these procedures abstractly, but what happens when an [algorithm](https://en.wikipedia.org/wiki/Algorithm) gets wildly complicated? How do we keep track of where we are, especially when [programming computers](https://en.wikipedia.org/wiki/Computer_programming) or analyzing complex Praxis math [logic](https://en.wikipedia.org/wiki/Logic)? 

We draw a map. A **[flowchart](https://en.wikipedia.org/wiki/Flowchart) is a visual representation of a step-by-step mathematical algorithm.**

### The Universal Language of Shapes
When you look at a flowchart, the geometry speaks to you before you even read the words. There is a universal standard for these diagrams:

1. **The Ovals (The Boundaries):** In standard algorithmic flowcharts, **[oval](https://en.wikipedia.org/wiki/Oval) shapes indicate the start point or end point of a process.** They are the greeting and the farewell of the algorithm.
2. **The Rectangles (The Actions):** In standard algorithmic flowcharts, **[rectangular](https://en.wikipedia.org/wiki/Rectangle) shapes represent processing steps or mathematical operations.** When you see a rectangle, it is an instruction: *add 4, square the result, divide by y.*
3. **The Diamonds (The Crossroads):** In standard algorithmic flowcharts, **[diamond](https://en.wikipedia.org/wiki/Rhombus) shapes denote decision points or [conditional branching](https://en.wikipedia.org/wiki/Conditional_%28computer_programming%29).** They are the moments of suspense. Is the number even? Is $x$ greater than $100$? The diamond forces the algorithm to ask a question.

### Branching and Looping
When the algorithm hits a diamond, it faces a fork in the road. A **[conditional branch](https://en.wikipedia.org/wiki/Conditional_%28computer_programming%29) in a flowchart directs a process along different paths based on a [true or false](https://en.wikipedia.org/wiki/Boolean_data_type) condition.** 

For example, if the diamond asks "Is $x < 10$?" and the answer is "True," the branch might send you left to add $5$. If "False," the branch might send you right to end the program. 

![A conditional flowchart diagram demonstrating a logical fork: the diamond represents a true/false condition that dictates which rectangular action path the algorithm takes next.](https://wikipedia.org/wiki/Special:Redirect/file/If-Then-Else-diagram.svg)

Sometimes, a branch sends you backwards, pointing an arrow to a step you've already completed. This creates a **[loop](https://en.wikipedia.org/wiki/Control_flow) in a flowchart [which] repeats a specific sequence of operations until a defined condition is met.** Loops are exactly how computer programs generate those recursive sequences we just talked about!

### The Art of Tracing
If you are faced with a flowchart on an exam, how do you solve it without losing your mind? You must become an incredibly meticulous [accountant](https://en.wikipedia.org/wiki/Accountant). 

**Tracing an algorithm requires recording the current value of all variables after every individual operation.** 

> **[Feynman's](https://en.wikipedia.org/wiki/Richard_Feynman) Tip for Tracing:** 
> Never try to hold the changing values in your head. Create a "T-chart" on your scratch paper. Label columns for every variable (e.g., $X$ and $Y$). Every time you pass through a rectangle in the flowchart, cross out the old number in your table and write the new one. Keep looping and updating your table until the diamond finally tells you to take the exit path to the "End" oval!

![Nobel laureate Richard Feynman, shown here during a 1964 lecture, emphasized using systematic tracking methods on paper rather than relying solely on mental calculations when solving complex logic problems.](https://wikipedia.org/wiki/Special:Redirect/file/Feynman_lecture_1964_(10481714045).jpg)

### Bringing It All Together
Math is movement. Whether you are maintaining equality across both sides of a static equation, hunting down the 14th term of a Fibonacci sequence, or tracing the true/false branches of a geometric flowchart, you are executing logic. 

Trust the order of operations. Respect the shapes. Keep a rigorous tally of your variables. If you follow the procedure step-by-step, the machine will never steer you wrong.