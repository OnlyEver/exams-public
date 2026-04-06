Nature behaves in both continuous sweeps and discrete jumps. When a [physicist](https://en.wikipedia.org/wiki/Physicist) models the [trajectory](https://en.wikipedia.org/wiki/Trajectory) of a thrown ball, they use a continuous curve because the ball occupies every infinitesimally small [point in space](https://en.wikipedia.org/wiki/Point_%28geometry%29) along its path. However, when a school board allocates funding based on yearly enrollment, or a [bank](https://en.wikipedia.org/wiki/Bank) computes [interest](https://en.wikipedia.org/wiki/Interest) at the end of a month, the timeline fractures into distinct, countable steps. In [mathematics](https://en.wikipedia.org/wiki/Mathematics), **a [sequence](https://en.wikipedia.org/wiki/Sequence) is a [mathematical function](https://en.wikipedia.org/wiki/Function_%28mathematics%29) whose [domain](https://en.wikipedia.org/wiki/Domain_of_a_function) is a [subset](https://en.wikipedia.org/wiki/Subset) of [integers](https://en.wikipedia.org/wiki/Integer)**. More specifically, to align with the act of counting events or steps, **the domain of a mathematical sequence is typically restricted to [positive integers](https://en.wikipedia.org/wiki/Natural_number)**. 

When we introduce [sequence notation](https://en.wikipedia.org/wiki/Sequence), the [variable](https://en.wikipedia.org/wiki/Variable_%28mathematics%29) $n$ is not merely an arbitrary placeholder like $x$ in a continuous equation; **the variable $n$ in sequence formulas represents the [ordinal position](https://en.wikipedia.org/wiki/Ordinal_number) of the term**—the first term, the second term, the third, and so on. Because it denotes a [discrete](https://en.wikipedia.org/wiki/Discrete_mathematics) position, **the sequence position variable $n$ must be an integer**. As a [secondary mathematics teacher](https://en.wikipedia.org/wiki/Mathematics_education), your task is to help students bridge their understanding of [continuous functions](https://en.wikipedia.org/wiki/Continuous_function) (lines and curves drawn without lifting the pencil) to these discrete, stepwise realities.

![Sequences operate on a discrete domain of positive integers, which can be visualized as distinct, countable points on a number line rather than a continuous span.](https://wikipedia.org/wiki/Special:Redirect/file/Number-line.svg)

## The Two Lenses: Recursive vs. Explicit

To describe a sequence mathematically, we have two distinct languages at our disposal: [recursive](https://en.wikipedia.org/wiki/Recursion) and [explicit](https://en.wikipedia.org/wiki/Closed-form_expression). They are fundamentally different ways of answering the question, "What is the next number?"

> **A [recursive formula](https://en.wikipedia.org/wiki/Recurrence_relation) calculates the $n$th term of a sequence based on one or more previous terms in the sequence.** 

Think of a recursive formula as a set of walking instructions. If you want to know where you will be after ten steps, you must physically take step one, then step two, then step three. Because a recursive formula relies entirely on relative positioning, **a recursive formula for a sequence must explicitly state at least one initial term to be completely defined.** Without an initial term, you have instructions for taking a step, but no starting location.

> **An [explicit formula](https://en.wikipedia.org/wiki/Closed-form_expression) calculates the $n$th term of a sequence using only the position number $n$.**

If recursive formulas are walking instructions, explicit formulas are a teleportation machine. You input the destination coordinates ($n$), and you arrive immediately. Whether you are dealing with [arithmetic](https://en.wikipedia.org/wiki/Arithmetic_progression) or [geometric patterns](https://en.wikipedia.org/wiki/Geometric_progression), **an [arithmetic sequence](https://en.wikipedia.org/wiki/Arithmetic_progression) can be evaluated for any term directly using the explicit formula without calculating preceding terms.** The exact same advantage holds true for multipliers: **a [geometric sequence](https://en.wikipedia.org/wiki/Geometric_progression) can be evaluated for any term directly using the explicit formula without calculating preceding terms.**

---

## Arithmetic Sequences: Linear Growth on a Grid

Imagine a [subway train](https://en.wikipedia.org/wiki/Rapid_transit) that boards $15$ new [passengers](https://en.wikipedia.org/wiki/Passenger) at every single stop. This perfectly illustrates an [arithmetic progression](https://en.wikipedia.org/wiki/Arithmetic_progression). **An arithmetic sequence is a sequence of numbers in which the difference between any two consecutive terms is a constant.** 

**The constant difference between consecutive terms in an arithmetic sequence is called the [common difference](https://en.wikipedia.org/wiki/Arithmetic_progression)**, typically denoted by $d$. To find this value from a list of numbers, **the common difference of an arithmetic sequence is calculated by subtracting a term from the immediately following term** ($d = a_n - a_{n-1}$). 

![A visual representation of an arithmetic progression, where each step increases by a constant common difference, akin to stacking an identical number of blocks in each successive column.](https://wikipedia.org/wiki/Special:Redirect/file/Arithmetic_progression.svg)

### Formulas and Structure

**The recursive formula for an arithmetic sequence is $a_n = a_{n-1} + d$.** It simply states: "To get the current term, take the previous term and add $d$." 

However, if we want to bypass the stepping-stones, we need the explicit form. 
> **The explicit formula for an arithmetic sequence is $a_n = a_1 + (n-1)d$.**

In this formula:
*   **In the explicit arithmetic formula $a_n = a_1 + (n-1)d$, the variable $a_1$ represents the first term.**
*   **In the explicit arithmetic formula $a_n = a_1 + (n-1)d$, the variable $d$ represents the common difference.**

Why $(n-1)$? This is a critical concept for students to grasp. If you want to arrive at the $5$th term, you start at the $1$st term and make exactly $4$ "jumps" of size $d$. You always make one fewer jump than your destination's position number.

### Modeling and Graphing

Because an arithmetic sequence changes by a fixed amount at each step, **arithmetic sequences model [linear growth](https://en.wikipedia.org/wiki/Linear_growth) or linear decay over discrete intervals.** If you were to plot the values on a [coordinate plane](https://en.wikipedia.org/wiki/Cartesian_coordinate_system), **an arithmetic sequence generates a linear graph when the sequence values are plotted against the term position numbers.** 

![When plotted, the discrete terms of an arithmetic sequence align to form a linear graph, where the common difference functions geometrically as the slope of the line.](https://wikipedia.org/wiki/Special:Redirect/file/Gerade.svg)

The [algebraic](https://en.wikipedia.org/wiki/Algebra) connection here is profound. If you expand the explicit formula $a_n = a_1 + dn - d$, and rearrange it to $a_n = d(n) + (a_1 - d)$, it perfectly mirrors the [slope-intercept form](https://en.wikipedia.org/wiki/Linear_equation) $y = mx + b$. Therefore, **in an arithmetic sequence, the constant rate of change is equivalent to the [slope](https://en.wikipedia.org/wiki/Slope) of a [linear function](https://en.wikipedia.org/wiki/Linear_function).** 

In the real world, this behavior governs many linear [financial](https://en.wikipedia.org/wiki/Finance) and [physical systems](https://en.wikipedia.org/wiki/Physical_system):
*   **Real-world scenarios involving [simple interest](https://en.wikipedia.org/wiki/Interest) accumulation can be modeled using arithmetic sequences.** If you invest \$1,000 at $5\%$ simple interest, you earn exactly \$50 every single year. The balance sequence (\$1,050, \$1,100, \$1,150...) is arithmetic because the addition is constant.
*   More broadly, **real-world scenarios involving a constant addition or subtraction of items over discrete steps can be modeled using arithmetic sequences**, such as a [reservoir](https://en.wikipedia.org/wiki/Reservoir) draining at a steady 500 [gallons](https://en.wikipedia.org/wiki/Gallon) per hour.

---

## Geometric Sequences: Exponential Scaling

Now, imagine a scenario where a [bacteria culture](https://en.wikipedia.org/wiki/Microbiological_culture) doubles every hour. The growth is no longer a steady addition; it is a steady [multiplication](https://en.wikipedia.org/wiki/Multiplication). **A geometric sequence is a sequence of numbers in which the [ratio](https://en.wikipedia.org/wiki/Ratio) of any term to the preceding term is a constant.**

![Bacterial colonies multiplying under optimal conditions provide a real-world model of a geometric sequence, where each time interval results in scaling by a constant ratio.](https://wikipedia.org/wiki/Special:Redirect/file/E.coli-colony-growth.gif)

**The constant ratio between consecutive terms in a geometric sequence is called the [common ratio](https://en.wikipedia.org/wiki/Geometric_progression)**, denoted by $r$. To identify this multiplier empirically, **the common ratio of a geometric sequence is calculated by dividing a term by the immediately preceding term** ($r = \frac{a_n}{a_{n-1}}$). 

### Formulas and Structure

**The recursive formula for a geometric sequence is $a_n = r \cdot a_{n-1}$.** The instruction is simple: "Multiply the previous term by $r$."

To jump directly to the $n$th hour of bacterial growth, we use the explicit form.
> **The explicit formula for a geometric sequence is $a_n = a_1 \cdot r^{n-1}$.**

In this formula:
*   **In the explicit geometric formula $a_n = a_1 \cdot r^{n-1}$, the variable $a_1$ represents the first term.**
*   **In the explicit geometric formula $a_n = a_1 \cdot r^{n-1}$, the variable $r$ represents the common ratio.**

Again, the [exponent](https://en.wikipedia.org/wiki/Exponentiation) is $(n-1)$ because starting from the first term, we apply the multiplication $r$ exactly $(n-1)$ times to reach the $n$th position.

### Modeling and Graphing

Because the sequence is built on [repeated multiplication](https://en.wikipedia.org/wiki/Exponentiation), **geometric sequences model [exponential growth](https://en.wikipedia.org/wiki/Exponential_growth) or [exponential decay](https://en.wikipedia.org/wiki/Exponential_decay) over discrete intervals.** Visually, **a geometric sequence generates an [exponential graph](https://en.wikipedia.org/wiki/Exponential_function) when the sequence values are plotted against the term position numbers.** 

![When plotted against their ordinal position numbers, the terms of a geometric sequence map along an exponential curve, with the common ratio acting as the base multiplier.](https://wikipedia.org/wiki/Special:Redirect/file/Exponentielles_wachstum2.svg)

Just as the common difference mirrors linear slope, the common ratio has an algebraic counterpart. **In a geometric sequence, the common ratio is equivalent to the [base](https://en.wikipedia.org/wiki/Base_%28exponentiation%29) of an [exponential function](https://en.wikipedia.org/wiki/Exponential_function).** If $y = a \cdot b^x$, the base $b$ behaves exactly like the common ratio $r$.

Real-world applications of geometric sequences are everywhere, driving the most powerful forces in [economics](https://en.wikipedia.org/wiki/Economics) and [biology](https://en.wikipedia.org/wiki/Biology):
*   **Real-world scenarios involving [compound interest](https://en.wikipedia.org/wiki/Compound_interest) over discrete intervals can be modeled using geometric sequences.** If an account earns $5\%$ compound interest, the balance is multiplied by $1.05$ each year. 
*   Similarly, **real-world scenarios involving [population growth](https://en.wikipedia.org/wiki/Population_growth) by a fixed percentage per discrete time period can be modeled using geometric sequences.**

---

## Translating Between Recursive and Explicit Forms

On the [Praxis 5165 exam](https://en.wikipedia.org/wiki/Praxis_test), you will frequently be required to translate fluently between these mathematical perspectives. The key to translating sequences is recognizing how the core parameters ($d$ and $r$) manifest in each format.

### Translating Arithmetic Formulas
When moving between forms, focus on the constant difference:
*   **To translate a recursive arithmetic formula to an explicit formula, the added constant in the recursive step becomes the common difference in the explicit formula.** If $a_n = a_{n-1} + 7$, then $7$ takes the place of $d$ in $a_n = a_1 + (n-1)7$.
*   **To translate an explicit arithmetic formula to a recursive formula, the [linear coefficient](https://en.wikipedia.org/wiki/Coefficient) of $n$ becomes the common difference in the recursive step.** Consider $a_n = 4n + 3$. Because $4$ is the coefficient of $n$ (the "slope"), the common difference is $4$. The recursive formula must be $a_n = a_{n-1} + 4$.

### Translating Geometric Formulas
When dealing with geometric patterns, track the multiplier:
*   **To translate a recursive geometric formula to an explicit formula, the constant multiplier in the recursive step becomes the common ratio in the explicit formula.** If $a_n = 3 \cdot a_{n-1}$, then $3$ is the base in the explicit formula $a_n = a_1 \cdot 3^{n-1}$.
*   **To translate an explicit geometric formula to a recursive formula, the [base of the exponent](https://en.wikipedia.org/wiki/Base_%28exponentiation%29) becomes the common ratio in the recursive step.** In the explicit formula $a_n = 5 \cdot (0.8)^{n-1}$, the base is $0.8$. This means the sequence decays by multiplying by $0.8$ at each step, yielding the recursive step $a_n = 0.8 \cdot a_{n-1}$.

| Sequence Type | Core Feature | Recursive Form | Explicit Form | Translation Key |
| :--- | :--- | :--- | :--- | :--- |
| **Arithmetic** | Common Difference ($d$) | $a_n = a_{n-1} + d$ | $a_n = a_1 + (n-1)d$ | Added constant $\leftrightarrow$ Linear coefficient of $n$ |
| **Geometric** | Common Ratio ($r$) | $a_n = r \cdot a_{n-1}$ | $a_n = a_1 \cdot r^{n-1}$ | Constant multiplier $\leftrightarrow$ Base of the exponent |

---

## Teaching Context: Technology and Domain

As an educator, bridging the gap between [abstraction](https://en.wikipedia.org/wiki/Abstraction_%28mathematics%29) and application often involves [technology](https://en.wikipedia.org/wiki/Technology). Modern classrooms rely heavily heavily on graphing technology to visualize mathematics. 

**[Graphing calculators](https://en.wikipedia.org/wiki/Graphing_calculator) evaluate recursive and explicit sequences using a specialized sequence graphing mode.** When you switch a calculator like the [TI-84 Plus](https://en.wikipedia.org/wiki/TI-84_Plus_series) from "Function" to "Seq" (Sequence) mode, the environment fundamentally changes. The standard $Y=$ screen is replaced by $u(n)$, and the variable key inputs $n$ instead of $X$. 

![Graphing calculators feature a dedicated "Sequence" mode that enforces mathematical domain constraints by only accepting discrete integer inputs for position numbers.](https://wikipedia.org/wiki/Special:Redirect/file/TI-84_Plus_graphing.jpg)

Why is this [pedagogical](https://en.wikipedia.org/wiki/Pedagogy) shift so crucial? Because it physically enforces the mathematical domain constraint. In function mode, a student can easily calculate $Y(2.5)$. But in sequence mode, the calculator will only accept integer inputs for $n_{Min}$, $n_{Max}$, and the table parameters. By using sequence mode, you reinforce to the student that sequences are a progression of discrete events. You cannot evaluate a sequence at step $2.5$ any more than a bank can give you the $2.5$th monthly interest payout. 

Mastering these models—understanding their structure, graphing them accurately, and translating effortlessly between their explicit teleportation and recursive stepping-stones—equips you to help students model the precise, countable rhythms of the real world.