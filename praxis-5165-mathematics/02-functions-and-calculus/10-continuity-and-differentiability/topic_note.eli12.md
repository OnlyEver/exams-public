Imagine you are playing a racing video game, and you are designing a track. For the race cars to drive on it safely, the road has to be completely connected—no missing pieces, or the cars will fall off! But just connecting the track isn't enough. If two pieces of the track meet at a super sharp, jagged angle, the cars will crash when they try to turn. 

In math, these two rules—staying connected and staying smooth—are called continuity and differentiability. Understanding how these two ideas work together is like learning the secret code to how graphs behave. 

You might think of continuity as "drawing a line without picking up your pencil." That is a great way to picture it! But in math class, we have to look deeper. Let's learn the exact rules.

## The Three Pillars of Continuity

Let's say you are trying to meet your friends at a pizza place located at a spot called point c on a map. Continuity of a function at a point requires exactly three mathematical conditions to be met simultaneously. 

Here is how you check them:

1. **The first condition for a function f to be continuous at a point c is that the function value f(c) must be defined.** (The pizza place actually has to exist at that spot!)
2. **The second condition for a function f to be continuous at a point c is that the limit of f(x) as x approaches c must exist.** For this to happen, the existence of a limit at a point requires both the left-hand limit and the right-hand limit at that point to exist and be equal. In other words, if you walk down the street from the left side, and your friend walks down the street from the right side, you both have to be heading to the exact same spot.
3. **The third condition for a function f to be continuous at a point c is that the limit of f(x) as x approaches c must exactly equal the defined function value f(c).** (The spot you both walked to must actually be the pizza place!)

A function fails to be continuous at a point if any one of the three continuity conditions is not satisfied. If even one rule fails, the whole track is broken!

## Classifying the Breaks: Types of Discontinuities

Sometimes the track breaks. The way it breaks tells us a lot about the math. Here are the three main types:

| Discontinuity Type | Defining Characteristics | Visual Analogy |
| :--- | :--- | :--- |
| **Removable** | A removable discontinuity occurs when the limit of a function exists at a point while the function value at that point remains undefined. Or, a removable discontinuity occurs when the limit of a function exists at a point while the limit does not equal the defined function value at that point. | A single missing pixel in a video game wall. The shape of the wall goes right up to that spot, but the actual block is missing or moved somewhere else. |
| **Jump** | A jump discontinuity occurs when the left-hand limit and right-hand limit of a function at a point both exist and are finite while possessing different values. | Two separate platforms in a game like Super Mario. You walk along one level from the left, but the right side starts at a totally different height. |
| **Infinite** | An infinite discontinuity occurs when at least one of the one-sided limits of a function at a point approaches positive infinity or negative infinity. | A bottomless pit in Minecraft! The path suddenly drops straight down forever, or shoots straight up into the sky forever. |

## The Anatomy of Differentiability

If continuity means "connected," then differentiability means "smooth and predictable." If you zoom super close into a smooth hill on a graph, it will look just like a nice straight line. 

A function is differentiable at a point if the derivative of the function exists at that specific point. But what is a derivative? It's just a math word for slope, or how steep a line is! 

To find it, we use a formula called the difference quotient, which finds the change in height divided by the change in distance. The derivative of a function f at a point c is defined as the limit of the difference quotient (f(x) - f(c))/(x - c) as x approaches c. 

Here is a step-by-step breakdown of how you build that math formula:
1. Pick your starting point on the graph at x = c, and find its height, which we call f(c).
2. Pick another point super close to it at x, and find its height, which we call f(x).
3. Find the slope by subtracting the heights and dividing by the distance between the points: (f(x) - f(c)) divided by (x - c).

## The Core Relationship: Continuity vs. Differentiability

How do these two ideas connect? It is one-way traffic!

Differentiability at a point mathematically guarantees continuity at that exact same point. Think of a wooden skateboard ramp: if you know it is perfectly smooth (differentiable), you know for a fact it has to be connected. Therefore, if a function is differentiable at a point, the function must inherently be continuous at that point. 

Because of this fact, if a function is not continuous at a point, the function absolutely cannot be differentiable at that point. A lack of continuity at a point precludes the existence of a derivative at that point. If the skateboard ramp has a giant missing chunk, you can't smoothly ride over it. The slope at that missing spot just doesn't exist. 

But watch out! The reverse is a trick. Continuity at a point does not mathematically guarantee differentiability at that point. A function can be continuous at a point while failing to be differentiable at that exact point. Just because the ramp is connected doesn't mean it's smooth. It could have a crazy, jarring bump!

## Continuous but Not Differentiable: A Zoo of Exceptions

When a line is connected but not smooth, it usually has a weird shape. A continuous function is not differentiable at a point if the graph of the function features a sharp corner at that point. Also, a continuous function is not differentiable at a point if the graph of the function features a cusp at that point. Finally, a continuous function is not differentiable at a point if the graph of the function has a vertical tangent line at that point.

Let's look at the famous examples!

### 1. The Sharp Corner: f(x) = |x|
Think of a bouncing basketball hitting the floor. It goes straight down, hits the ground, and goes straight back up in a giant V-shape. 

The absolute value function f(x) = |x| is perfectly continuous at x = 0. You can trace it without lifting your pencil. However, the absolute value function f(x) = |x| is not differentiable at x = 0 due to a sharp corner in the graph. 

Why? Let's check the slope step-by-step:
1. First, find the slope of the left side. The left-hand derivative of the absolute value function f(x) = |x| at x = 0 is exactly -1 because it slides perfectly downward.
2. Next, find the slope of the right side. The right-hand derivative of the absolute value function f(x) = |x| at x = 0 is exactly 1 because it climbs perfectly upward.
3. Compare them! Because -1 is totally different from 1, the two sides don't agree. The race car crashes at the sharp turn!

### 2. The Sharp Cusp: f(x) = x^(2/3)
The function f(x) = x^(2/3) is continuous for all real numbers. If you draw it, it looks a bit like a seagull flying in the sky, completely connected. 

Yet, the function f(x) = x^(2/3) is not differentiable at x = 0 because the graph forms a sharp cusp at the origin. A cusp is like a sharp, pointy thorn on a rose bush. At the very tip of the point, the slope goes wild and tears itself apart.

### 3. The Vertical Tangent Line: f(x) = x^(1/3)
Sometimes there are no sharp points, but things are just too steep. The function f(x) = x^(1/3) is continuous for all real numbers. It curves nice and easy. 

However, the function f(x) = x^(1/3) is not differentiable at x = 0 because the graph contains a vertical tangent line at the origin. 

What is that? Think of a rollercoaster doing a loop where, for one split second, you are pointing straight up at the sky. A vertical tangent line occurs at a point c if the function is continuous at c and the absolute value of the derivative approaches infinity as x approaches c. Because "infinity" isn't a normal number we can measure, the math breaks down and there is no derivative there.

### 4. The Pathological Extreme: The Weierstrass Function
A long time ago, a math genius named Karl Weierstrass invented a monster of a graph! 

The Weierstrass function is a specific mathematical example of a function that is continuous everywhere. You could trace the whole thing over and over. But here is the crazy part: The Weierstrass function is a specific mathematical example of a function that is nowhere differentiable. 

It is completely made of sharp spikes. If you zoom in on it with a computer, it never looks like a smooth straight line. It just shows more and more spikes forever. It proves once and for all that just being connected (continuous) doesn't mean something is smooth (differentiable).

## Teaching at the Seams: Piecewise Functions

A piecewise function is like getting an allowance that changes depending on your age. For example: If you are under 10 years old, you get \$5 a week. If you are 10 or older, you get \$10 a week. The "rule" changes based on where you are. 

In math, a piecewise function must be checked for continuity at the boundary points between different rule definitions. (The boundary point is the exact age where your allowance changes). 

To make sure the graph is perfectly smooth at that changing point, it needs two things. First, differentiability of a piecewise function at a boundary point requires the function to be continuous at that point. Second, differentiability of a piecewise function at a boundary point requires the left-hand derivative to equal the right-hand derivative at that point.

If you are solving a math puzzle to make these sides match perfectly, here is how you do it step-by-step:
1. Write down the two different math rules that meet at the boundary point.
2. Set the two rules equal to each other so the heights match. This forces the graph to be continuous.
3. Find the derivative (the slope) for both of the rules.
4. Set those two left and right derivatives equal to each other. This forces the graph to be perfectly smooth.

By learning these rules, you won't just see messy squiggles on a page. You'll see the smooth, secret machinery of how graphs are built!