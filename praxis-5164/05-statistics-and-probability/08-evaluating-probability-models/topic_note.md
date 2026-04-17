Imagine dropping a standard [six-sided die](https://en.wikipedia.org/wiki/Dice) and a standard plastic [thumbtack](https://en.wikipedia.org/wiki/Drawing_pin) onto a hard classroom floor. Both actions generate unpredictable physical outcomes. Yet, mathematically, we model them entirely differently. We expect the die to land on any of its six faces with equal likelihood because of its perfect [symmetry](https://en.wikipedia.org/wiki/Symmetry). The thumbtack, however, will land point-up or point-down with starkly different likelihoods dictated by its physical [geometry](https://en.wikipedia.org/wiki/Geometry). This distinction forms the bedrock of understanding how we construct [mathematical models](https://en.wikipedia.org/wiki/Mathematical_model) of chance, how we test those models against the messy reality of [experimental data](https://en.wikipedia.org/wiki/Experimental_data), and how we figure out what went wrong when our mathematical expectations do not match what we see.

![A standard six-sided die represents a perfectly uniform probability model due to its physical symmetry.](https://wikipedia.org/wiki/Special:Redirect/file/6sided_dice_(cropped).jpg)

![A thumbtack's asymmetrical physical geometry produces non-uniform outcomes, making it far more likely to land in one specific orientation than the other.](https://wikipedia.org/wiki/Special:Redirect/file/Brass_thumbtack.jpg)

## The Mathematical Blueprint: Defining the Model

Before we ever [flip a coin](https://en.wikipedia.org/wiki/Coin_flipping) or spin a spinner in the classroom, we must build a theoretical foundation. [Mathematics](https://en.wikipedia.org/wiki/Mathematics) requires a map before it can navigate the territory. 

A **[probability model](https://en.wikipedia.org/wiki/Probability_space)** is a mathematical representation consisting of a defined **[sample space](https://en.wikipedia.org/wiki/Sample_space)** and assigned [probabilities](https://en.wikipedia.org/wiki/Probability) for each outcome. The sample space is simply the exhaustive [set](https://en.wikipedia.org/wiki/Set_%28mathematics%29) of all possible outcomes for a given [probability experiment](https://en.wikipedia.org/wiki/Experiment_%28probability_theory%29). If you roll a standard die, the sample space is $\{1, 2, 3, 4, 5, 6\}$. There are no other possibilities. 

![A visual representation of a finite sample space detailing an exhaustive set of possible outcomes alongside specifically defined events.](https://wikipedia.org/wiki/Special:Redirect/file/Sample_space.png)

To ensure the model is mathematically valid, it must obey a strict [conservation law](https://en.wikipedia.org/wiki/Conservation_law): the sum of the assigned probabilities for all individual outcomes in a valid probability model must [equal exactly one](https://en.wikipedia.org/wiki/Probability_axioms) ($1.0$, or $100\%$). 

### Uniform vs. Non-Uniform Models

Nature and human design provide us with two distinct types of probability models:

1. **Uniform Probability Model**: A [uniform probability model](https://en.wikipedia.org/wiki/Discrete_uniform_distribution) assigns the exact same theoretical probability to every individual outcome in the sample space. A [fair coin](https://en.wikipedia.org/wiki/Fair_coin) and a fair die are modeled uniformly. 
2. **Non-Uniform Probability Model**: A [non-uniform probability model](https://en.wikipedia.org/wiki/Categorical_distribution) assigns different theoretical probabilities to at least some individual outcomes in the sample space. The thumbtack from our opening example, or a spinner where the "Red" section takes up half the [circle](https://en.wikipedia.org/wiki/Circle) while "Blue" and "Green" take up a quarter each, require a non-uniform model.

How we calculate the likelihood of an [event](https://en.wikipedia.org/wiki/Event_%28probability_theory%29) depends entirely on which model we are using:

> **Calculating Theoretical Probability**
> *   **In a Uniform Model:** The theoretical probability of an event is calculated by dividing the number of [favorable outcomes](https://en.wikipedia.org/wiki/Outcome_%28probability%29) by the total number of possible outcomes. *(Example: Rolling an [even number](https://en.wikipedia.org/wiki/Parity_%28mathematics%29) on a die is $3$ favorable outcomes out of $6$ total outcomes, or $\frac{1}{2}$.)*
> *   **In a Non-Uniform Model:** The theoretical probability of an event is calculated by adding the specific assigned probabilities of all outcomes that constitute the event. *(Example: On our [biased](https://en.wikipedia.org/wiki/Bias_%28statistics%29) spinner, the probability of landing on "Not Green" is the sum of the probability of Red ($\frac{1}{2}$) and Blue ($\frac{1}{4}$), which equals $\frac{3}{4}$.)*

**[Theoretical probability](https://en.wikipedia.org/wiki/A_priori_probability)** is pristine. It describes the mathematically expected outcome *without conducting any physical trials*. It is what should happen in a perfect universe. 

## The Messy Territory: Experimental Data

When your [middle schoolers](https://en.wikipedia.org/wiki/Middle_school) actually start flipping coins or running [simulations](https://en.wikipedia.org/wiki/Simulation) on their [graphing calculators](https://en.wikipedia.org/wiki/Graphing_calculator), they step out of theory and into reality. 

![Graphing calculators allow students to bypass manual physical trials, rapidly simulating thousands of expected probabilities to generate robust experimental data.](https://wikipedia.org/wiki/Special:Redirect/file/TI-84_Plus_graphing.jpg)

**[Experimental probability](https://en.wikipedia.org/wiki/Empirical_probability)** is the [ratio](https://en.wikipedia.org/wiki/Ratio) of the number of times a specific event actually occurs to the total number of trials performed. In rigorous [statistical](https://en.wikipedia.org/wiki/Statistics) contexts, experimental probability is also formally known as **[empirical probability](https://en.wikipedia.org/wiki/Empirical_probability)** or **[relative frequency](https://en.wikipedia.org/wiki/Frequency_%28statistics%29)**.

To compare our pristine mathematical map (theory) to the physical territory (experiment), we need a common language. We translate probabilities into [frequencies](https://en.wikipedia.org/wiki/Frequency_%28statistics%29).

*   **[Observed frequency](https://en.wikipedia.org/wiki/Frequency_%28statistics%29)** is the raw count of how many times a specific outcome happens during an actual experiment. If a student flips a coin $50$ times and sees $28$ heads, the observed frequency is $28$.
*   **Expected frequency | Expected value** is calculated by multiplying the theoretical probability of an event by the total number of experimental trials. For $50$ coin flips, the expected frequency of heads is $\frac{1}{2} \times 50 = 25$.

| Concept | Definition | Example ($50$ flips of a fair coin) |
| :--- | :--- | :--- |
| **Theoretical Probability** | Mathematically expected outcome. | $P(\text{Heads}) = 0.5$ |
| **Expected Frequency** | Theoretical probability $\times$ total trials. | $0.5 \times 50 = 25$ expected heads |
| **Observed Frequency** | Raw count from an actual experiment. | $28$ heads actually counted |
| **Experimental Probability** | Observed frequency / total trials. | $\frac{28}{50} = 0.56$ (Relative Frequency) |

## Evaluating the Model: When Math Meets Reality

**Evaluating a probability model** involves comparing the generated experimental frequencies against the mathematically expected theoretical frequencies. We are essentially asking: *Does the physical reality behave the way our math predicted it would?*

When the numbers don't perfectly align, we have a **discrepancy**. A discrepancy in a probability model refers to a [quantitative](https://en.wikipedia.org/wiki/Quantitative_research) difference between the expected theoretical frequency and the actual observed frequency. In our coin example, the expected frequency was $25$, but the observed frequency was $28$. We have a discrepancy of $3$. 

Is our model broken? Is the coin rigged? Usually, no. 

Small discrepancies between expected theoretical frequencies and observed frequencies are entirely normal due to natural **[sampling variability](https://en.wikipedia.org/wiki/Sampling_error)**. Sampling variability is the fundamental statistical principle that observed experimental outcomes will naturally fluctuate [randomly](https://en.wikipedia.org/wiki/Randomness) across different sets of trials. If every student in your classroom flips a coin $50$ times, almost no one will get exactly $25$ heads, and no two students will get the exact same [sequence](https://en.wikipedia.org/wiki/Sequence) of flips. 

### The Great Stabilizer: The Law of Large Numbers

If sampling variability makes every experiment unique, how can we ever trust our theoretical models? 

This is where the **[Law of Large Numbers](https://en.wikipedia.org/wiki/Law_of_large_numbers)** saves us. This mathematical [theorem](https://en.wikipedia.org/wiki/Theorem) dictates that as the number of experimental trials increases, the experimental probability will [converge](https://en.wikipedia.org/wiki/Convergence_of_random_variables) toward the theoretical probability. 

![As the number of dice-rolling trials increases, the observed experimental average strictly converges toward the mathematically expected theoretical value, neutralizing sampling variability.](https://wikipedia.org/wiki/Special:Redirect/file/Largenumbers.svg)

If a student flips a coin $10$ times, getting $8$ heads (an experimental probability of $0.80$) is unusual, but not impossible due to sampling variability. But if they use a graphing calculator to simulate $10,000$ flips, the experimental probability will tightly hug the theoretical $0.50$ mark. The "[noise](https://en.wikipedia.org/wiki/Statistical_noise)" of sampling variability is drowned out by the sheer volume of data.

## Diagnosing Failure: Sources of Discrepancy

As a teacher, you will encounter situations where the data absolutely refuses to match the model. When agreement between modeled and observed frequencies is poor, you must help students identify the source of the discrepancy. 

Here are the primary culprits you will need to identify on the [Praxis 5164 exam](https://en.wikipedia.org/wiki/Praxis_test) and in your classroom:

### 1. Small Sample Sizes
A **[small sample size](https://en.wikipedia.org/wiki/Sample_size_determination)** is a primary source of discrepancy between observed frequencies and a mathematically correct theoretical probability model. If a student complains that a die is "broken" because they rolled it four times and never got a $6$, they are simply victims of a small sample size. The model is fine; the trial count is just too low for the Law of Large Numbers to take effect.

### 2. Fundamentally Flawed Theoretical Models
If you flip a coin $10,000$ times and observe $7,200$ heads, you no longer have a small sample size. A persistent large discrepancy across a massive number of trials strongly suggests that the underlying theoretical probability model is fundamentally flawed. 

This usually happens because we made a false assumption about the physical object. Assuming a physical object like a die or coin is fair when the object is actually [weighted](https://en.wikipedia.org/wiki/Loaded_dice) leads to an inaccurate uniform probability model. Any inherent **[physical bias](https://en.wikipedia.org/wiki/Bias_%28statistics%29)** in a randomizing device necessitates the use of a non-uniform probability model to accurately predict long-term expected frequencies. 

### 3. Lack of Statistical Independence
**[Statistical independence](https://en.wikipedia.org/wiki/Independence_%28probability_theory%29)** means that the outcome of one trial does not influence the outcome of the next. Experimental trials that lack statistical independence can cause observed frequencies to deviate significantly from the theoretical probability model. 

For example, if students are drawing colored marbles from a bag to test a theoretical model but they *forget to put the marble back after each draw* ([drawing without replacement](https://en.wikipedia.org/wiki/Urn_problem)), the probabilities change with every single trial. Their experimental data will heavily disagree with a static theoretical model because the trials are no longer independent.

![Drawing colored objects from an urn without replacing them fundamentally alters the probability model for subsequent draws, resulting in events that critically lack statistical independence.](https://wikipedia.org/wiki/Special:Redirect/file/Stochastik_Bayestheorem_Urnenversuch.png)

### 4. Measurement Errors
Sometimes the math is right, and the object is fair, but the humans are flawed. **[Measurement errors](https://en.wikipedia.org/wiki/Observational_error)** during [data collection](https://en.wikipedia.org/wiki/Data_collection) create artificial discrepancies between observed frequencies and modeled expected frequencies. If a student is dropping a thumbtack but they miscount the [tally marks](https://en.wikipedia.org/wiki/Tally_marks), or they record a "point-up" as a "point-down," the resulting discrepancy is an artifact of bad bookkeeping, not a failure of probability.

![Simple observational errors during data collection, such as miscounting handwritten tally marks, create completely artificial discrepancies between mathematical expectations and physical reality.](https://wikipedia.org/wiki/Special:Redirect/file/Strike_symbol_(49778996432).jpg)

## Classroom Application: The Fair Game

One of the most profound applications of evaluating probability models in the [middle school curriculum](https://en.wikipedia.org/wiki/Middle_school) is analyzing games. 

A **fair probability game** is mathematically defined as a scenario where all participating players have an equal theoretical probability of winning. If you invent a game where Player A scores a point if a die lands on $1, 2,$ or $3$, and Player B scores a point if it lands on $4, 5,$ or $6$, this is a fair game (uniform model, both have a theoretical probability of $\frac{1}{2}$). 

However, if Player A scores on $1, 2, 3,$ or $4$ and Player B scores on $5$ or $6$, the game is mathematically unfair. Your students can prove this by creating the non-uniform theoretical model, calculating the expected frequencies, and then running a simulation on their calculators to demonstrate that over the long run (thanks to the Law of Large Numbers), Player A will systematically crush Player B.

By teaching students how to build probability models, how to translate them into expected frequencies, and how to rigorously compare them to observed reality, you are giving them a toolkit to detect bias, understand [randomness](https://en.wikipedia.org/wiki/Randomness), and navigate a world governed by [chance](https://en.wikipedia.org/wiki/Probability).