When you play a video game and move a character across the screen, the computer isn't drawing them from scratch every time. It uses a math rule to move the character! In math, moving or changing a shape is called a geometric transformation. A geometric transformation maps an original figure called a preimage onto a new figure called an image. Think of the preimage as the "before" picture, and the image as the "after" picture. Today, we are going to learn how space can be stretched, flipped, and spun using simple rules on a coordinate grid.

## The Geometry of Motion: Isometries

Imagine sliding a solid cardboard triangle across your desk. No matter how you push it, spin it, or flip it over, the cardboard stays exactly the same shape and size. In math, this is called a rigid transformation. Rigid geometric transformations are also referred to mathematically as isometries (which means "equal measure").

Let's look at the simple rules for these moves:
*   A rigid transformation preserves the absolute distance between any two points on a geometric figure. If the sides were 5 inches long before, they are 5 inches long after.
*   A rigid transformation preserves the angle measures of a geometric figure. A 90-degree corner stays exactly 90 degrees.
*   A rigid transformation maps parallel lines on a preimage to parallel lines on the resulting image. If two lines looked like train tracks before, they still look like train tracks after.
*   A rigid transformation preserves the collinearity of points from the preimage to the image. This means if dots were lined up straight before, they stay perfectly straight.

Because nothing about the shape breaks or stretches, a sequence consisting solely of rigid transformations maps a preimage to a geometrically congruent image. "Congruent" just means identical in size and shape!

There are exactly three kinds of these moves: A translation is categorized as a rigid transformation. A reflection is categorized as a rigid transformation. A rotation is categorized as a rigid transformation.

### Translations: The Glide

A translation slides a figure along a straight path without changing the orientation or size of the geometric figure. Think of a puck gliding perfectly smooth across an ice rink!

To tell the shape where to slide, a translation is uniquely specified by a translation vector. A translation vector defines both the horizontal shift (left or right) and the vertical shift (up or down) applied to a preimage. 

Here is how you do the math step-by-step:
A translation by a units horizontally and b units vertically maps a coordinate point (x, y) to the point (x + a, y + b).
1. Find your starting point, like an x-value of 2 and a y-value of 3. That is (2, 3).
2. Add the horizontal shift (let's say 4 spaces right) to the x-value: 2 + 4 = 6.
3. Add the vertical shift (let's say 5 spaces up) to the y-value: 3 + 5 = 8.
4. Your new shifted point is (6, 8).

Imagine walking around the edge of a shape from point A to point B to point C. Geometric orientation refers to the arrangement of points in a specific clockwise or counterclockwise sequence around a polygon perimeter. A translation preserves the geometric orientation of a polygon. If the corners went clockwise before the slide, they still go clockwise after!

### Reflections: The Mirror

A reflection flips a geometric figure across a specific line to create a mirror image. Because it relies entirely on where you place the mirror, a reflection transformation is uniquely specified by a single line of reflection.

When you flip a shape, a neat pattern happens. A line of reflection acts as the exact perpendicular bisector of the segment connecting a preimage point to the corresponding image point. In everyday words: the mirror line cuts right down the exact middle of the path between the old point and the new point, making a perfect 90-degree cross.

What if a point is already touching the mirror? It doesn't move! A fixed point is a coordinate location that maps to its exact original position after a geometric transformation. Every point located precisely on the line of reflection acts as a fixed point during a reflection transformation.

Unlike gliding, a reflection reverses the geometric orientation of a polygon. If you read the corners clockwise before, the mirror image makes them read counterclockwise!

Here are the step-by-step reflection rules for your math grid:

**Flipping over the x-axis (the flat middle line):**
1. Take your starting point (x, y).
2. Keep the x-value exactly the same.
3. Flip the sign of the y-value (make it negative if it was positive, or positive if it was negative).
4. A reflection across the x-axis maps a coordinate point (x, y) to the point (x, -y).

**Flipping over the y-axis (the tall middle line):**
1. Take your starting point (x, y).
2. Flip the sign of the x-value.
3. Keep the y-value exactly the same.
4. A reflection across the y-axis maps a coordinate point (x, y) to the point (-x, y).

**Flipping over the diagonal line y = x:**
1. Take your starting point (x, y).
2. Swap the places of the x and y numbers.
3. A reflection across the linear equation y = x maps a coordinate point (x, y) to the point (y, x).

**Flipping over the diagonal line y = -x:**
1. Take your starting point (x, y).
2. Swap the places of the numbers AND flip both their signs.
3. A reflection across the linear equation y = -x maps a coordinate point (x, y) to the point (-y, -x).

**Flipping completely through the center point (the origin):**
1. Take your starting point (x, y).
2. Flip the signs of both numbers.
3. A point reflection across the origin maps a coordinate point (x, y) to the point (-x, -y).

### Rotations: The Turn

A rotation turns a geometric figure around a fixed point by a specific angle measurement. Think of spinning a fidget spinner or turning a steering wheel! A rotation transformation is specified by a center of rotation, an angle of rotation, and a direction of rotation. 

Just like a slide, a rotation preserves the geometric orientation of a polygon (clockwise stays clockwise). Since the center of the spin never moves, the exact center of rotation acts as a fixed point during a rotation transformation.

On a math grid, we have strict rules for which way to spin:
* A positive angle of rotation in the coordinate plane dictates a counterclockwise turning direction (spinning left).
* A negative angle of rotation in the coordinate plane dictates a clockwise turning direction (spinning right).

Did you know that a rotation of 90 degrees clockwise about the origin produces identical coordinates to a rotation of 270 degrees counterclockwise? They land in the exact same spot!

Here are the step-by-step rules for turning around the middle of the grid (the origin):

**A 90-degree counterclockwise turn:**
1. Take a starting point, like (3, 4).
2. Swap the numbers to get (4, 3).
3. Make the first number negative.
4. A rotation of 90 degrees counterclockwise about the origin maps a coordinate point (x, y) to the point (-y, x).

**A 180-degree turn (a half-circle):**
1. Take a starting point, like (3, 4).
2. Make both numbers negative.
3. A rotation of 180 degrees about the origin maps a coordinate point (x, y) to the point (-x, -y).

**A 270-degree counterclockwise turn:**
1. Take a starting point, like (3, 4).
2. Swap the numbers to get (4, 3).
3. Make the second number negative.
4. A rotation of 270 degrees counterclockwise about the origin maps a coordinate point (x, y) to the point (y, -x).

#### Locating the Unseen Center of Rotation

What if a puzzle shows you a spun shape and asks, "Where is the center point it spun around?" You can play detective to find it! 

The geometric center of rotation lies exactly on the perpendicular bisector of every segment connecting a preimage point to the corresponding rotated image point.

Here is how you find it step-by-step:
1. Draw a straight line between an "old" point and its "new" spun point.
2. Find the exact middle of that line and draw a crossing line perfectly across it at a 90-degree angle.
3. Do this again for a second pair of points.
4. See where your two crossing lines crash into each other! The intersection coordinate of two perpendicular bisectors of segments connecting preimage points to corresponding rotated image points reveals the center of rotation.

## The Shape Shifter: Dilations

Now we stop talking about rigid moves. Imagine pinching the screen on your phone to zoom in on a photo. This is called a dilation! A dilation is a non-rigid transformation that changes the overall size of a geometric figure.

Even though it gets bigger or smaller, it does not turn into a wacky monster. A dilation preserves the proportional shape and angle measures of a geometric figure. A triangle is still a triangle. 

Just like rigid moves, a dilation preserves the collinearity of points from the preimage to the resulting image (straight lines stay straight). A dilation maps parallel lines on a preimage to parallel lines on the resulting image. Also, a dilation preserves the geometric orientation of a polygon (clockwise stays clockwise).

To do this trick, a dilation transformation is specified by a center of dilation and a numerical scale factor. Just like with spinning, the exact center of dilation acts as a fixed point during a dilation transformation.

The scale factor is the magic number that tells you how much to grow or shrink. The scale factor of a dilation is the ratio of a side length of the image to the corresponding side length of the preimage. The distance between any two points on a dilated image equals the corresponding preimage distance multiplied by the absolute value of the scale factor.

Here is how to do it step-by-step from the center of the grid:
1. Take your scale factor, let's say it is 2 (we call this k).
2. Take your starting point, like (3, 5).
3. Multiply both numbers by 2.
4. Your new point is (6, 10).
A dilation with the center at the origin and a scale factor of k maps a coordinate point (x, y) to the point (kx, ky).

### The Scale Factor Spectrum

The scale factor number acts like a remote control for size:
* A dilation produces an enlargement of the preimage if the absolute value of the scale factor is strictly greater than one (like 2 or 3).
* A dilation produces a reduction of the preimage if the absolute value of the scale factor is strictly between zero and one (like a fraction such as 1/2).
* A dilation with a scale factor of exactly one maps the preimage onto identical image coordinates. It multiplies the size by 1, so nothing changes!
* A dilation with a negative scale factor produces an image that is rotated 180 degrees around the center of dilation relative to the preimage. It gets bigger or smaller AND flips completely upside down!

If you mix up a bunch of transformations together, a sequence of transformations containing at least one dilation produces an image that is geometrically similar to the preimage. "Similar" is a math word meaning it has the exact same shape, but a different size.

### Dilations and Infinite Lines

When you zoom in on lines that go on forever, there are cool rules:
* A dilation maps a line not passing through the center of dilation to a strictly parallel line. It pushes the line further away, but keeps it going the same direction.
* A dilation maps a line passing through the center of dilation directly onto that exact same line. It just stretches the line along its own path!

If you need to find the zoom center, just play connect-the-dots: Straight lines connecting corresponding vertices on a dilated preimage and its image will always intersect at the specific center of dilation.

## Choreographing Space: Sequences and Compositions

Usually, shapes do more than one trick. The composition of geometric transformations involves the successive mathematical application of two or more transformations. That is just a fancy way of saying "doing one move, and then doing another move right after."

Here is a very important warning: The composition of geometric transformations is fundamentally not a commutative mathematical operation. "Commutative" means you can switch the order and get the same answer. But with moving shapes, order matters! 

Think of putting on your socks and then your shoes. If you reverse the order and put shoes on first, then socks, it doesn't work! Reversing the execution order of transformations in a composition sequence frequently alters the final coordinate positions of the image.

### The Double Reflection Phenomena

Bouncing a shape between two mirrors creates some awesome math shortcuts!

**Mirrors Side-by-Side:** The composition of two separate reflections across parallel lines is mathematically equivalent to a single translation. Instead of flipping it twice, you could have just slid it over! 

The overall distance of the translation resulting from two reflections across parallel lines is exactly twice the distance separating the parallel lines.
1. Find the distance between the two parallel mirror lines (let's say they are 3 inches apart).
2. Multiply that distance by 2: 3 times 2 = 6 inches.
3. The shape simply slides over 6 inches!

**Mirrors Crossing:** The composition of two separate reflections across intersecting lines is mathematically equivalent to a single rotation. 

The specific angle of the rotation resulting from two reflections across intersecting lines is exactly twice the angle formed between the intersecting lines.
1. Find the angle where the two mirror lines crash together (let's say it is 40 degrees).
2. Multiply that angle by 2: 40 times 2 = 80 degrees.
3. The shape simply spins 80 degrees around where the lines cross!

## Diagnostic Tools for the Middle School Teacher

When you are looking at a messy math puzzle with a start shape and an end shape, how do you figure out what happened?

First, trace the corners. Comparing the orientation of a preimage and an image helps mathematically identify the presence of a reflection in a transformation sequence. 
* An image demonstrating reversed orientation relative to the preimage indicates that an odd number of reflections occurred in the overall transformation sequence (like 1, 3, or 5 flips). If it was clockwise and is now counterclockwise, it flipped!
* An image demonstrating identical orientation relative to the preimage indicates that an even number of reflections occurred in the overall transformation sequence (like 2 or 4 flips). It flipped over and then flipped right back!

Finally, if you want to find the exact rule for how a shape moved, you don't need to track a million points. Three non-collinear preimage points and their corresponding image points are entirely sufficient to uniquely determine a two-dimensional rigid transformation. "Non-collinear" just means three dots that don't make a straight line—basically, the three corners of a triangle! If you track how those three dots move, you can solve the whole puzzle!