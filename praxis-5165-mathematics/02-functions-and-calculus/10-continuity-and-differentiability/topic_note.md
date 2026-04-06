Imagine constructing a physical bridge spanning a deep gorge. For a vehicle to successfully cross, the physical path must be completely unbroken—any missing segment means catastrophe. Yet, merely connecting the road is not sufficient for a safe journey. If the bridge sections meet at a harsh, jagged angle, the wheels will abruptly change direction, subjecting the vehicle to immense, infinite forces that will shatter its suspension. In [calculus](https://en.wikipedia.org/wiki/Calculus), these two physical necessities—connectedness and smoothness—are mathematically formalized as [continuity](https://en.wikipedia.org/wiki/Continuous_function) and [differentiability](https://en.wikipedia.org/wiki/Differentiable_function). Understanding the precise relationship between these two properties is central to mastering [single-variable calculus](https://en.wikipedia.org/wiki/Calculus). 

As mathematics educators, you will find that students intuitively understand continuity as "drawing a graph without lifting your pencil." While this [heuristic](https://en.wikipedia.org/wiki/Heuristic) is a helpful starting point, it spectacularly fails when dealing with rigorous analytical definitions or when a [graphing calculator's](https://en.wikipedia.org/wiki/Graphing_calculator) pixelated screen obscures a single [undefined](https://en.wikipedia.org/wiki/Undefined_%28mathematics%29) point. To prepare your students—and to master the [Praxis 5165 exam](https://en.wikipedia.org/wiki/Praxis_test) yourself—we must transition from geometric intuition to strict algebraic conditions.

![Due to the limited resolution of their pixelated screens, graphing calculators can visually obscure a single undefined point, tricking students into assuming a function is entirely continuous.](https://wikipedia.org/wiki/Special:Redirect/file/TI-84_Plus_graphing.jpg)

## The Three Pillars of Continuity

Continuity of a function at a point requires exactly three mathematical conditions to be met simultaneously. We evaluate continuity at a specific point, let us call it $c$, before we can declare a function continuous over an entire [interval](https://en.wikipedia.org/wiki/Interval_%28mathematics%29). 

To determine if a function $f$ is continuous at $x = c$, we apply the following test:

1. **The function value $f(c)$ must be defined.** The point must actually exist on the [Cartesian plane](https://en.wikipedia.org/wiki/Cartesian_coordinate_system). If substituting $c$ into the function yields [division by zero](https://en.wikipedia.org/wiki/Division_by_zero) or the [logarithm](https://en.wikipedia.org/wiki/Logarithm) of a [negative number](https://en.wikipedia.org/wiki/Negative_number), the condition fails instantly.

![A calculator returning an error for division by zero. If a function's algebraic definition requires dividing by zero at a specific point, the function value is undefined, and the first pillar of continuity instantly fails.](https://wikipedia.org/wiki/Special:Redirect/file/TI86_Calculator_DivByZero.jpg)

2. **The [limit](https://en.wikipedia.org/wiki/Limit_of_a_function) of $f(x)$ as $x$ approaches $c$ must exist.** For this to occur, we look to the [one-sided limits](https://en.wikipedia.org/wiki/One-sided_limit). The existence of a limit at a point requires both the [left-hand limit](https://en.wikipedia.org/wiki/One-sided_limit) ($\lim_{x \to c^-} f(x)$) and the [right-hand limit](https://en.wikipedia.org/wiki/One-sided_limit) ($\lim_{x \to c^+} f(x)$) at that point to exist and be exactly equal. The paths from the left and the right must aim at the identical destination.
3. **The limit of $f(x)$ as $x$ approaches $c$ must exactly equal the defined function value $f(c)$.** The destination the paths aim toward must be exactly where the point actually resides.

> **The Fundamental Rule of Continuity:**
> A function fails to be continuous at a point if any one of the three continuity conditions is not satisfied. Missing even one pillar causes the entire structure of continuity to collapse.

## Classifying the Breaks: Types of Discontinuities

When continuity fails, the manner in which it fails tells us profound things about the function's behavior. We categorize these failures into three distinct types of [discontinuities](https://en.wikipedia.org/wiki/Classification_of_discontinuities). Recognizing these analytically is critical, as a graphing calculator will often gloss over [removable discontinuities](https://en.wikipedia.org/wiki/Classification_of_discontinuities), displaying what appears to be an unbroken line.

| Discontinuity Type | Defining Characteristics | Visual / Pedagogical Analogy |
| :--- | :--- | :--- |
| **[Removable](https://en.wikipedia.org/wiki/Classification_of_discontinuities)** | Occurs when the limit of a function exists at a point while the function value at that point remains undefined, **OR** when the limit of a function exists at a point while the limit does not equal the defined function value at that point. | A pothole in an otherwise perfect road. The road intends to go there, but the exact spot is either missing or displaced. |
| **[Jump](https://en.wikipedia.org/wiki/Classification_of_discontinuities)** | Occurs when the left-hand limit and right-hand limit of a function at a point both exist and are finite while possessing different values. | A sheer cliff drop. The road approaches a specific height from the left, but abruptly continues at a different height on the right. |
| **[Infinite](https://en.wikipedia.org/wiki/Classification_of_discontinuities)** | Occurs when at least one of the one-sided limits of a function at a point approaches [positive infinity](https://en.wikipedia.org/wiki/Infinity) or [negative infinity](https://en.wikipedia.org/wiki/Infinity). | A [vertical asymptote](https://en.wikipedia.org/wiki/Asymptote). The road curves violently upward or downward into the abyss, never crossing the boundary. |

![A visual representation of a removable discontinuity. The limit exists as the paths converge, but the actual function value is displaced, acting as a mathematical "pothole" in the graph.](https://wikipedia.org/wiki/Special:Redirect/file/Discontinuity_removable.eps.png)

## The Anatomy of Differentiability

If continuity is about connectedness, differentiability is about *smoothness* and *predictability*. Geometrically, if you zoom in infinitely close to a point on a differentiable curve, it will look exactly like a straight line. We call this "[local linearity](https://en.wikipedia.org/wiki/Linear_approximation)."

![An illustration of local linearity. When zoomed in closely enough, a smooth, differentiable curve becomes visually indistinguishable from its straight tangent line.](https://wikipedia.org/wiki/Special:Redirect/file/Approximation_of_cos_with_linear_functions_without_numbers.svg)

A function is differentiable at a point if the [derivative](https://en.wikipedia.org/wiki/Derivative) of the function exists at that specific point. But what does it mean for a derivative to exist analytically? 

The derivative of a function $f$ at a point $c$ is defined as the limit of the [difference quotient](https://en.wikipedia.org/wiki/Difference_quotient) $\frac{f(x) - f(c)}{x - c}$ as $x$ approaches $c$. 

$$ f'(c) = \lim_{x \to c} \frac{f(x) - f(c)}{x - c} $$

Because the derivative itself is a limit, it inherits all the strict requirements of a limit. Specifically, the [rate of change](https://en.wikipedia.org/wiki/Derivative) as we approach from the left must perfectly match the rate of change as we approach from the right.

## The Core Relationship: Continuity vs. Differentiability

One of the most frequently tested concepts on the Praxis 5165 exam is the unidirectional relationship between these two properties. 

Differentiability at a point mathematically guarantees continuity at that exact same point. If you know a function has a derivative at $x=c$, you possess total certainty that the graph is connected there. Therefore, if a function is differentiable at a point, the function must inherently be continuous at that point. 

By the logical principle of the [contrapositive](https://en.wikipedia.org/wiki/Contraposition), we can flip this relationship to yield an incredibly powerful diagnostic tool: **If a function is not continuous at a point, the function absolutely cannot be differentiable at that point.** A lack of continuity at a point precludes the existence of a derivative at that point. If the bridge is broken, we cannot calculate the [slope](https://en.wikipedia.org/wiki/Slope) of the curve spanning the gap. 

However, the [converse](https://en.wikipedia.org/wiki/Converse_%28logic%29) of our first statement is a trap that easily snares students. **Continuity at a point does not mathematically guarantee differentiability at that point.** A function can be continuous at a point while failing to be differentiable at that exact point. Connectedness does not guarantee smoothness.

## Continuous but Not Differentiable: A Zoo of Exceptions

When a function is continuous but fails to be differentiable, it typically exhibits a specific geometric feature. A continuous function is not differentiable at a point if the graph of the function features a sharp corner, a [cusp](https://en.wikipedia.org/wiki/Cusp_%28singularity%29), or a [vertical tangent line](https://en.wikipedia.org/wiki/Vertical_tangent) at that point. 

Let us examine the canonical examples you must be prepared to teach and test:

### 1. The Sharp Corner: $f(x) = |x|$
The [absolute value function](https://en.wikipedia.org/wiki/Absolute_value) $f(x) = |x|$ is perfectly continuous at $x = 0$. However, the absolute value function $f(x) = |x|$ is not differentiable at $x = 0$ due to a sharp corner in the graph. 

Why? Remember that a derivative requires the left-hand and right-hand difference quotients to agree. For this function, the left-hand derivative of the absolute value function $f(x) = |x|$ at $x = 0$ is exactly -1. The right-hand derivative of the absolute value function $f(x) = |x|$ at $x = 0$ is exactly 1. Because $-1 \neq 1$, the limit of the difference quotient does not exist. 

![The absolute value function is continuous everywhere but features a sharp corner at the origin. Since the slope abruptly changes from -1 to 1, it cannot be differentiated at x = 0.](https://wikipedia.org/wiki/Special:Redirect/file/Absolute_value.svg)

### 2. The Sharp Cusp: $f(x) = x^{2/3}$
The function $f(x) = x^{2/3}$ is continuous for all [real numbers](https://en.wikipedia.org/wiki/Real_number). You can trace its seagull-like shape without ever lifting your pencil. Yet, the function $f(x) = x^{2/3}$ is not differentiable at $x = 0$ because the graph forms a sharp cusp at the origin. As $x$ approaches 0, the slopes of the tangent lines approach $-\infty$ from the left and $+\infty$ from the right. The rate of change rips itself apart at the [origin](https://en.wikipedia.org/wiki/Origin_%28mathematics%29).

![A continuous curve forming a sharp cusp. The tangent slopes approach opposite infinities from the left and right, making the derivative undefined at the peak.](https://wikipedia.org/wiki/Special:Redirect/file/Cusp_at_(0%2C0.5).svg)

### 3. The Vertical Tangent Line: $f(x) = x^{1/3}$
Sometimes, the issue isn't an abrupt change in direction, but an extreme rate of change. The function $f(x) = x^{1/3}$ is continuous for all real numbers. It glides smoothly through the origin. However, the function $f(x) = x^{1/3}$ is not differentiable at $x = 0$ because the graph contains a vertical tangent line at the origin. 

A vertical tangent line occurs at a point $c$ if the function is continuous at $c$ and the absolute value of the derivative approaches [infinity](https://en.wikipedia.org/wiki/Infinity) as $x$ approaches $c$. Because "infinity" is not a real number, the limit of the difference quotient fails to exist in a finite sense, rendering the function non-differentiable at that instant.

![A vertical tangent line on a continuous curve. Although the curve itself lacks sharp corners, the rate of change momentarily becomes infinite, meaning a finite derivative cannot exist.](https://wikipedia.org/wiki/Special:Redirect/file/Vertical_tangent.svg)

### 4. The Pathological Extreme: The Weierstrass Function
In the late 19th century, mathematicians discovered functions that defied all geometric intuition. The [Weierstrass function](https://en.wikipedia.org/wiki/Weierstrass_function) is a specific mathematical example of a function that is continuous everywhere, yet the Weierstrass function is a specific mathematical example of a function that is *nowhere* differentiable. 

Constructed as an [infinite sum](https://en.wikipedia.org/wiki/Series_%28mathematics%29) of [cosines](https://en.wikipedia.org/wiki/Trigonometric_functions), its graph is a [fractal](https://en.wikipedia.org/wiki/Fractal). If you zoom in on a graphing calculator, rather than smoothing out into a straight line (local linearity), it reveals infinitely more jagged corners and cusps. It is an unbroken path made entirely of sharp turns, proving once and for all that continuity and differentiability are fundamentally distinct properties.

![The Weierstrass function is the ultimate pathological example: a curve that is continuous everywhere but differentiable nowhere due to its infinitely jagged, fractal nature.](https://wikipedia.org/wiki/Special:Redirect/file/WeierstrassFunction.svg)

## Teaching at the Seams: Piecewise Functions

In secondary mathematics, [piecewise functions](https://en.wikipedia.org/wiki/Piecewise) represent the ultimate testing ground for these concepts. Because they are stitched together from different algebraic rules, the boundaries between these rules are highly suspect.

A piecewise function must be checked for continuity at the boundary points between different rule definitions. To do this, you evaluate the three conditions of continuity: Does the boundary point belong to one of the [domain](https://en.wikipedia.org/wiki/Domain_of_a_function) intervals? Does the rule governing the left side limit match the rule governing the right side limit? 

If the function is continuous at the seam, we can then test for differentiability. Differentiability of a piecewise function at a boundary point requires the function to be continuous at that point (our foundational prerequisite). Furthermore, differentiability of a piecewise function at a boundary point requires the left-hand derivative to equal the right-hand derivative at that point. 

When your students encounter a problem asking them to find constants $a$ and $b$ to make a piecewise function differentiable everywhere, they are fundamentally being asked to solve a [system of two equations](https://en.wikipedia.org/wiki/System_of_equations):
1. Set the two rule expressions equal to each other at the boundary point (forcing continuity).
2. Set the derivatives of the two rule expressions equal to each other at the boundary point (forcing smoothness).

Mastering this topic requires treating mathematical definitions not as mere jargon, but as exact diagnostic tools. By internalizing these conditions, you equip yourself not only to pass your certification but to illuminate the magnificent machinery of calculus for the next generation of thinkers.