When you play a video game and your favorite character runs across the screen, or when you zoom in on a map on your phone, you are watching math in action! Video game creators and mapmakers use a set of math rules called geometric transformations. A transformation is a rule that tells a shape exactly how to move, slide, spin, flip, or stretch on a giant grid (which we call a coordinate plane). For you to get the hang of this math, we just need to learn the simple game rules of how shapes behave when we move them around!

## The Architecture of Rigid Motions

Before we make a shape bigger or smaller, let's learn how to move it without changing its shape or size at all. 

In geometry, a rigid motion is a movement that keeps the shape perfectly stiff. To be exact, a rigid motion preserves the distance between points of a figure. It also means that a rigid motion preserves the angle measures of a figure. Basically, the shape does not get squished, bent, or warped!

Because rigid motions leave the shape and size completely alone, they are the secret to proving shapes match exactly. In fact, two geometric figures are congruent if a sequence of rigid motions maps one figure exactly onto the other. If you can slide, spin, or flip one shape to land perfectly on top of another, they are congruent.

To track these movements, we look at something called spatial orientation. Think of a triangle with corners labeled A, B, and C in a clockwise circle (like the numbers on a clock). If you move the triangle and A, B, and C are still in a clockwise circle, the spatial orientation stayed the same. If the letters suddenly go backward (counterclockwise), the spatial orientation was reversed. 

### 1. Translations: The Pure Slide

A translation is a rigid motion mapping every point of a figure the same distance in the same direction. It is the easiest movement to understand because it is just a pure slide! Because the shape is just sliding across the floor like it's on ice, translations preserve the spatial orientation of a geometric figure. The top stays at the top, and the left stays on the left.

In math, we use something called a vector, written as <a, b>, to tell the shape how far to slide. 
* A translation along vector <a, b> maps a coordinate point (x, y) to (x + a, y + b).

Here is exactly how you do the math, step-by-step:
1. Identify your starting point, like (3, 4). This means x = 3 and y = 4.
2. Identify your translation vector, like <2, 5>. This means you will slide the point right 2 spaces (a = 2) and up 5 spaces (b = 5).
3. Add the "a" number to the "x" coordinate: 3 + 2 = 5.
4. Add the "b" number to the "y" coordinate: 4 + 5 = 9.
5. Write your final translated point: (5, 9).

### 2. Reflections: Reversing the Universe

Have you ever looked in a mirror and raised your right hand, but your mirror twin raises their left hand? That is a reflection! A reflection is a rigid motion mapping a point to a new point across a specific line. Because it acts like a mirror, reflections reverse the spatial orientation of a geometric figure. Your clockwise shape flips into a counterclockwise shape.

The mirror itself has a special math rule. The line of reflection is the perpendicular bisector of the segment connecting a preimage point and its corresponding image point. "Preimage" just means the original starting dot, and "image" means the new mirrored dot. This rule means the mirror cuts the distance between the two dots exactly in half, crossing their path at a perfect 90-degree angle.

When you are flipping shapes on your math grid, you can use these cheat codes depending on where the mirror is:

* **x-axis (the horizontal floor line):** A reflection across the x-axis maps a coordinate point (x, y) to (x, -y).
* **y-axis (the vertical wall line):** A reflection across the y-axis maps a coordinate point (x, y) to (-x, y).
* **Line y = x (a diagonal line going up-right):** A reflection across the line y = x maps a coordinate point (x, y) to (y, x).
* **Line y = -x (a diagonal line going down-right):** A reflection across the line y = -x maps a coordinate point (x, y) to (-y, -x).
* **The Origin (the exact center (0,0)):** A reflection across the origin maps a coordinate point (x, y) to (-x, -y).

Let's do a step-by-step example of reflecting the point (4, 7) across the x-axis:
1. Identify the starting coordinates: x = 4 and y = 7.
2. Read the rule for the x-axis: it changes (x, y) to (x, -y).
3. Keep the x-coordinate exactly the same: it stays 4.
4. Change the sign of the y-coordinate: 7 becomes -7.
5. Write the final mirrored point: (4, -7).

### 3. Rotations: Spinning Around a Center

A rotation is a rigid motion turning a figure around a fixed center point by a specific angle. Imagine pinning a picture to a corkboard with a thumbtack and spinning it. Like translations, rotations preserve the spatial orientation of a geometric figure. You are just turning the steering wheel; you aren't flipping the car over!

In geometry, we have rules for which way the steering wheel turns:
* Positive angles of rotation indicate a counterclockwise direction in coordinate geometry. (Turning to the left).
* Negative angles of rotation indicate a clockwise direction in coordinate geometry. (Turning to the right).

If you are spinning your shape around the very center of the grid (the origin), here are the rules you need to know:
* **90 Degrees Counterclockwise:** A rotation of 90 degrees counterclockwise about the origin maps a coordinate point (x, y) to (-y, x).
* **180 Degrees:** A rotation of 180 degrees about the origin maps a coordinate point (x, y) to (-x, -y). (Notice this is the exact same rule as reflecting across the origin!)
* **270 Degrees Counterclockwise:** A rotation of 270 degrees counterclockwise about the origin maps a coordinate point (x, y) to (y, -x). 

Let's do a step-by-step example of rotating the point (3, 8) by 90 degrees counterclockwise:
1. Identify the starting coordinates: x = 3 and y = 8.
2. Look at the rule for 90 degrees counterclockwise: (x, y) becomes (-y, x).
3. Find your new first number by taking the original y (which is 8) and making it negative: -8.
4. Find your new second number by taking the original x: 3.
5. Write the final rotated point: (-8, 3).

## The Magic of Mirrors: Compositions of Reflections

Here is an awesome secret trick: every single slide and spin can actually be built using just mirrors! When we do one reflection after another, we call it a "composition."

### Reflecting Across Parallel Lines

Imagine standing between two mirrors that are parallel (facing each other like walls in a hallway). 
* The composition of two reflections across parallel lines always results in a translation. 

Because you flip the shape backward, and then flip it backward again, it returns to normal! The result is a simple slide. And there is a magic math shortcut for how far it slides:
* The translation distance resulting from two reflections across parallel lines is exactly twice the distance between the parallel lines.

Here is how you calculate that step-by-step:
1. Measure the gap between your two parallel mirrors. Let's say they are 4 units apart.
2. Multiply that gap distance by 2: 4 times 2 = 8.
3. The total distance the shape slid is 8 units.

### Reflecting Across Intersecting Lines

Now, imagine taking those two mirrors and angling them so they crash into each other like a "V" shape.
* The composition of two reflections across intersecting lines always results in a rotation.

When the mirrors cross, the double-flip turns into a spin! 
* The center of rotation formed by two reflections across intersecting lines is the intersection point of those two lines. (Where the mirrors touch is where the thumbtack goes).
* The rotation angle formed by two reflections across intersecting lines is exactly twice the acute angle between the lines.

Here is a step-by-step example of finding that spin:
1. Measure the inside angle where the two mirrors meet. Let's say they meet at a 30-degree angle.
2. Multiply that angle by 2: 30 times 2 = 60.
3. The final shape will have spun exactly 60 degrees.

## Breaking the Mold: Dilations and Similarity

So far, we have only talked about shapes that stay the exact same size. But what if we want to zoom in on a map or shrink a photo? That is called a dilation. 

A dilation is a transformation completely determined by a center point and a scale factor. The center point is where the zoom starts, and the scale factor is the multiplier telling you how much to grow or shrink. 

Unlike the other movements, a dilation alters the distance between points of a figure unless the scale factor is exactly one or negative one. If you multiply by 1, it stays the same. But if you multiply by anything else, the size changes! Even though the shape grows or shrinks, the corners stay just as sharp, because a dilation preserves the interior angle measures of a geometric figure. A triangle is still the exact same type of triangle, just bigger or smaller.

When two shapes have the exact same angles but different sizes, we say they are similar. Two geometric figures are similar if a sequence of rigid motions combined with a dilation maps one figure onto the other.

### The Scale Factor (k)

The scale factor is the boss of a dilation. In math, we usually call it "k".
* A dilation with an absolute scale factor greater than one produces an enlargement of the preimage. (It gets bigger!).
* A dilation with a positive scale factor strictly less than one produces a reduction of the preimage. (It gets smaller!).

When you are zooming in from the center of the grid, the math is just multiplication:
* A dilation centered at the origin with a scale factor of k maps a coordinate point (x, y) to (kx, ky).

Let's do a step-by-step example of dilating the point (2, 5) with a scale factor of 3:
1. Identify your starting coordinates: x = 2 and y = 5.
2. Identify your scale factor: k = 3.
3. Multiply your x-coordinate by 3: 2 times 3 = 6.
4. Multiply your y-coordinate by 3: 5 times 3 = 15.
5. Write your final zoomed-in point: (6, 15).

### Ratios of One and Two Dimensions

When we make things bigger, we have to be careful about measuring lines versus measuring flat space (area). 
If you are measuring a simple straight line (like the side of a square), the ratio of a dilated image segment length to the corresponding preimage segment length equals the absolute value of the scale factor. If the scale factor is 4, the side is 4 times longer.

But area is totally different! Area measures two dimensions. Think about a square piece of pizza. If you make the pizza twice as wide and twice as tall, you don't just get twice as much pizza—you get four times as much pizza!
* The ratio of the area of a dilated image to the area of the preimage equals the square of the scale factor.

Let's calculate pizza area step-by-step to prove it:
1. Identify the scale factor for how much wider/taller the pizza got. Let's say k = 4.
2. To find out how much the total area grew, square the scale factor (multiply it by itself): 4 times 4 = 16.
3. Your new pizza has an area 16 times bigger than the original! 

### Dilations on Infinite Lines

What happens if we zoom in on an endless line instead of a shape? It depends on where the line is sitting!
* A dilation maps a line not passing through the center of dilation to a parallel line. (If the line is drawn off to the side, zooming in just pushes a new, parallel line further out).
* A dilation maps a line passing through the center of dilation to the exact same line. (If the line goes right through your zoom point, sliding points along the line doesn't change the track itself).

## The Invariants of Form: Symmetry

Sometimes, you can transform a shape and it looks like nothing happened at all. The shape perfectly overlaps its old self. We call this symmetry! 

### Line Symmetry

A geometric figure possesses line symmetry if a reflection maps the entire figure exactly onto itself. 
Think about a perfect paper heart. If you draw a line right down the middle and fold it, the left side matches the right side perfectly. That fold is a line of symmetry.

### Rotational Symmetry

A geometric figure possesses rotational symmetry if a rotation strictly between 0 degrees and 360 degrees maps the figure onto itself.
Think of a standard steering wheel or a recycling symbol. You can spin it a little bit, and it looks exactly like it did before you touched it. 

To count how many times it matches while spinning, we use a special term: The order of rotational symmetry defines the number of distinct times a figure maps onto itself during a full 360-degree rotation. A square matches 4 times as you turn it, so it has an order of 4!

If you have a shape where all the sides and angles are equal (a regular polygon), finding the symmetry angle is easy:
* The smallest angle of rotational symmetry for a regular polygon with n sides is 360 divided by n degrees.

Let's do a step-by-step example for a stop sign (a regular octagon):
1. Count the number of sides on the shape (n). An octagon has 8 sides, so n = 8.
2. Set up your division problem: 360 divided by 8.
3. Calculate the answer: 360 / 8 = 45.
4. The stop sign maps onto itself every 45 degrees.

Finally, there is a cool trick for shapes that look exactly the same when you turn them totally upside down (like the letter "S" or the number "8"):
* Point symmetry is a specific case of rotational symmetry exactly equal to 180 degrees. 
If spinning a shape exactly halfway around (180 degrees) makes it perfectly match its starting position, it has point symmetry!