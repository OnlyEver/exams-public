Welcome to one of the coolest, trickiest topics in math. We call it "counting," but honestly, that's a pretty boring name for it. When we talk about counting techniques, we are not talking about using your fingers to tally things up one by one. Who has the time to do that? 

If someone asks you how many different teams you can make by picking 10 players out of 50 kids at gym class, counting them out loud would take you forever! Instead, we are talking about figuring out the hidden math behind your choices. We are learning how to calculate huge numbers of choices instantly. 

Let’s roll up our sleeves and look at how fast your choices can multiply!

## The Universe of Possibilities

Before we calculate anything, we have to know exactly what we are choosing from. Imagine a giant restaurant menu. In math, the sample space of an experiment is the exhaustive set of all possible distinct outcomes. It is the complete list of absolutely everything that could possibly happen. 

On the other hand, an event is a specific outcome or a defined set of outcomes within a larger sample space. If the sample space is the entire restaurant menu, an event is the exact meal you end up eating!

To help picture how these events happen step-by-step, we often use a drawing. A tree diagram represents all possible outcomes of a sequence of events by using branches to connect each initial choice to subsequent choices. Imagine the storyline in a video game where you have to make a choice. You stand at a fork in the road—that's your first choice. When you go down the left path, you hit another choice, and another. By tracing every possible path from the start of the tree to the end of each branch, you can see the whole sample space. 

But drawing big trees takes up way too much paper. Instead, we can use simple math rules to do the heavy lifting.

---

## The Two Great Engines of Counting

Math uses a couple of very easy rules when it comes to possibilities. You just need to know when to multiply and when to add.

### 1. The Fundamental Counting Principle (The "AND" Rule)

If you want to know how many ways a few different things can happen together in a row, you use multiplication. The Fundamental Counting Principle dictates multiplying the number of choices for each successive independent event to find the total possible outcomes. 

We use this when we are dealing with independent events. Independent events are events where the occurrence of one event does not affect the possible outcomes of the other events. 

Let's look at a classic example: flipping coins and rolling dice. 

*   A standard coin flip generates exactly two possible outcomes (Heads or Tails). 
*   A standard number cube features exactly six distinct faces (the numbers 1 through 6).

What happens if we flip a coin *and* roll a number cube at the exact same time? The coin doesn't care what the cube does, so these are independent events. Tossing a standard coin and a standard number cube simultaneously generates exactly twelve possible outcomes. Here is how we figure that out:

1. Step 1: Count the outcomes for the coin (2 possible outcomes).
2. Step 2: Count the outcomes for the number cube (6 possible outcomes).
3. Step 3: Multiply those choices together (2 x 6 = 12 total outcomes).

Look at how fast the numbers grow when we roll multiple cubes!
*   Tossing a single standard number cube generates exactly six possible outcomes. 
    1. Step 1: Count the faces on one cube (6). 
    2. Step 2: The total is just 6.
*   Tossing two standard number cubes simultaneously generates exactly thirty-six possible outcomes. 
    1. Step 1: Count the faces on the first cube (6).
    2. Step 2: Count the faces on the second cube (6).
    3. Step 3: Multiply them together (6 x 6 = 36).
*   Tossing three standard number cubes simultaneously generates exactly 216 possible outcomes. 
    1. Step 1: Look at the outcomes for each of the three cubes (6, 6, and 6).
    2. Step 2: Multiply them all together (6 x 6 x 6 = 216).

This same cool math trick works for coins. The total number of outcomes for flipping a coin multiple times is calculated by raising two to the power of the number of flips. Let's say you flip a coin 5 times:

1. Step 1: Write down the number of outcomes for one coin (2).
2. Step 2: Write down the number of flips as your power, or exponent (5 flips).
3. Step 3: Set up your math problem (2^5).
4. Step 4: Multiply it out (2 x 2 x 2 x 2 x 2 = 32 distinct outcomes).

### 2. The Addition Principle (The "OR" Rule)

What if you aren't doing multiple things in a row, but you just have to pick one thing from different categories? 

The Addition Principle dictates adding the number of outcomes for mutually exclusive events to find the total possible outcomes. 

Mutually exclusive events are two or more specific events that cannot occur simultaneously. Basically, you can't pick both at the same time. 

Imagine you are spending your allowance, and you can only afford one treat. You can choose from 3 types of candy *or* 4 types of ice cream. Because you are only picking one treat, and a treat cannot be both candy and ice cream at the exact same time, these events are mutually exclusive. 

Here is how you find your total choices:
1. Step 1: Count your candy options (3).
2. Step 2: Count your ice cream options (4).
3. Step 3: Add them together (3 + 4 = 7 possible treats).

---

## The Illusion of Independence: How Choices Alter the Universe

Things get really fun when the choices you make actually change what happens next. 

When the occurrence of one event alters the total number of possible outcomes for subsequent events, we are dealing with dependent events. 

A great way to test this is by reaching into a bag of marbles. It all depends on whether you put the marble back!

### Sampling With Replacement
Sampling with replacement means an item is returned to the selection pool before the next item is drawn. 

Because you put the item back, your choices start fresh every time! Sampling with replacement keeps the total number of available choices constant for each successive selection. If you have 10 marbles in a bag, here is how you calculate drawing a marble three times with replacement:

1. Step 1: For your first draw, count the marbles in the bag (10 choices). 
2. Step 2: Put the marble back.
3. Step 3: For your second draw, count the marbles again (Still 10 choices).
4. Step 4: Put the marble back again.
5. Step 5: For your third draw, count the marbles (Still 10 choices).
6. Step 6: Multiply your independent events (10 x 10 x 10 = 1,000 possible outcomes).

### Sampling Without Replacement
Sampling without replacement means a chosen item is removed from the selection pool permanently after being drawn. 

Now, your options are shrinking! Sampling without replacement decreases the total number of available choices by exactly one for each successive selection. You eat the candy instead of putting it back! Here is how you calculate drawing three marbles without replacement:

1. Step 1: For your first draw, count the marbles in the bag (10 choices).
2. Step 2: Keep the marble out of the bag. 
3. Step 3: For your second draw, count what is left in the bag (9 choices).
4. Step 4: Keep that second marble out, too.
5. Step 5: For your third draw, count what is left (8 choices).
6. Step 6: Multiply your dependent events (10 x 9 x 8 = 720 possible outcomes).

---

## The Mathematical Exclamation Point: The Factorial

When we sample without replacement down to the very last item, we get to use my absolute favorite math symbol: the factorial. 

A factorial represents the mathematical product of a positive integer and all the positive integers below that integer down to one. 

Because math teachers get really excited about this cool trick, the mathematical symbol for a factorial is an exclamation mark placed immediately after an integer! 

Let's say you want to line up 5 of your favorite video games on a shelf. Since you can't put the same physical game in two spots at once, this is a dependent event. 

1. Step 1: Count your choices for the first spot on the shelf (5 games).
2. Step 2: Count your choices for the next spot (4 games left).
3. Step 3: Count your choices for the next spot (3 games left).
4. Step 4: Count your choices for the next spot (2 games left).
5. Step 5: Count your choice for the final spot (1 game left).
6. Step 6: Multiply them all together (5 x 4 x 3 x 2 x 1 = 120 ways to organize your shelf).

Instead of writing all those numbers out, we just write 5! (which you read out loud as "five factorial"). 

There is one mind-blowing rule about factorials you should always remember: The value of zero factorial (written as 0!) is defined mathematically as exactly one. 

Why? Think about it like a riddle. How many ways can you arrange zero items on a shelf? There is exactly *one* way to do it: by leaving the shelf totally empty! 

---

## Committees vs. Lineups: Combinations and Permutations

Now for the grand finale. When we pick a group of items without putting them back, we have to ask ourselves a super important question: **Does the sequence of the items matter?**

Depending on your answer, you will use either a Permutation or a Combination. 

| Feature | Permutation | Combination |
| :--- | :--- | :--- |
| **Definition** | A permutation is an arrangement of a specific number of items where the sequence of the items strictly matters. | A combination is a selection of a specific number of items where the sequence of the items does not matter. |
| **Real-World Example** | Arranging distinct objects in a straight line utilizes permutation calculations because the specific sequence of objects changes the outcome. (If you are in a race, coming in 1st place is very different from coming in 3rd place!) | Forming a generalized committee from a larger group utilizes combination calculations because the specific order of selection is irrelevant. (If you pick a team of Alice, Bob, and Charlie, it's the exact same team as Charlie, Bob, and Alice). |

### The Relationship Between The Two

Because permutations care about who is 1st, 2nd, and 3rd, every single rearranged lineup counts as a brand-new outcome. Combinations are more relaxed. A combination looks at "Alice, Bob, Charlie" and "Charlie, Bob, Alice" and says, "Hey, that's just the same three friends. That only counts as one group."

Because combinations group identical sets of friends together into a single outcome, the number of possible combinations for a subset of items is always less than or equal to the number of possible permutations for that same subset. 

How do we do the math for combinations? We find the permutations first, and then we divide to get rid of the repeat groups. 

Let's say we pick 3 friends from a big group. 
1. Step 1: Figure out how many ways we can shuffle our 3 chosen friends (this is just 3!, which is 3 x 2 x 1 = 6 ways to shuffle them).
2. Step 2: Use your permutation math to find out the total number of ordered lineups.
3. Step 3: Divide your big permutation number by your shuffle number (6). 

So, the formula for calculating combinations divides the total number of permutations by the factorial of the number of chosen items. You are basically just cleaning up the math to remove the repeats!

## Summary for the Praxis Exam

When you take a big math test, don't sweat it when you see questions about coin flips, dice, or picking teams. Just take a breath and ask yourself these questions:
1.  **Am I doing a bunch of things in a row, or just picking one thing?** (Multiply for AND, Add for OR).
2.  **Am I putting the item back?** (Independent vs. Dependent).
3.  **Does the order of the items matter?** (Lineups = Permutations; Squads/Committees = Combinations).

If you remember these simple steps, you won't ever have to count on your fingers again. You'll just see the math making everything easy!