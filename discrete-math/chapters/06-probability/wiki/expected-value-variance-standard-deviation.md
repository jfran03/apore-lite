# Expected Value, Variance and Standard Deviation

> **Main concept:** Random Variables

## Definition

The **expected value** (also called the mean or expectation) of a random variable represents its average outcome over the long run. It combines each possible value of the random variable with its probability:

**μ = E[X] = ∑ₓ [ x · P(x) ]**

Think of it as the centre of the probability distribution, or a balance point. It tells you the value you'd expect if you repeated the experiment infinitely many times.
> Source: Expected Value, Variance and Standard Deviation.html; Discrete Random Variables - Copy.pdf

The lecture notes write it as ⟨X⟩ = μ_X = E(X) = ∑ₓ [x · P(x)] — multiply each x by P(x), then add all the outcomes. (μ is the old symbol for the mean of the population; E is the symbol for "expected outcome.")
> Source: Discrete Random Variables - Copy.pdf

It's not about predicting any one trial: it's about describing what happens on average across many trials. It's the value that the system gravitates toward over time.
> Source: Expected Value, Variance and Standard Deviation.html

## Key Concepts

### The Mean Need Not Be a Possible Outcome

The expected value doesn't have to be a possible outcome of the experiment.
> Source: Expected Value, Variance and Standard Deviation.html

The mean value of X need not be (and usually isn't) in the spectrum of X — but **min x ≤ μ_X ≤ max x** always.
> Source: Discrete Random Variables - Copy.pdf

### Why Spread Matters

The expected value tells you the centre of a distribution, but it doesn't say anything about how consistent or variable those results are. Two random variables can have the same mean but behave very differently: in one system outcomes cluster tightly around the mean (very predictable); in another they swing wildly from trial to trial (very unpredictable).
> Source: Expected Value, Variance and Standard Deviation.html

In computing and data science this distinction matters everywhere: two algorithms might have the same average runtime, but one might fluctuate far more depending on input size; two servers might have the same average load, but one spikes unpredictably — a higher variance system.
> Source: Expected Value, Variance and Standard Deviation.html

### Variance

**Variance** measures how far outcomes deviate from the mean, on average. For a discrete random variable 𝑋 with mean 𝜇:

**σ² = ∑ (xᵢ − μ)² · P(X = xᵢ)**

This formula does two things: it calculates how far each outcome 𝑥ᵢ is from the mean (𝑥ᵢ − 𝜇), then squares those deviations (to avoid negatives) and weights them by their probabilities. The result is the average of the squared deviations from the mean. Because of the squaring, variance is measured in **squared units**.
> Source: Expected Value, Variance and Standard Deviation.html

### Standard Deviation

To return to the original units of measurement, take the square root of the variance:

**σ = √( ∑ (xᵢ − μ)² · P(X = xᵢ) )**

The standard deviation tells you, roughly, how far typical outcomes fall from the mean. A **small σ** → outcomes are tightly clustered (low variability, predictable). A **large σ** → outcomes are spread out (high variability, unpredictable).
> Source: Expected Value, Variance and Standard Deviation.html

The lecture notes give both the definition and the shortcut side by side:

**σ_X = √( ∑ₓ [x − μ]² · P(x) )** ← definition
**σ_X = √( ∑ₓ [x² · P(x)] − μ² )** ← shortcut formula
> Source: Discrete Random Variables - Copy.pdf

### The Shortcut Formula

Sometimes it's easier to compute variance using an equivalent form:

**Var(X) = E[X²] − (E[X])²**, where **E[X²] = ∑ xᵢ² · P(X = xᵢ)**

You calculate the expected value of the squares, then subtract the square of the expected value.
> Source: Expected Value, Variance and Standard Deviation.html

Equivalently, σ²_X = ∑ₓ [x − μ]² · P(x) = ∑ₓ [x² · P(x)] − μ². As the notation suggests, the variance of X is the square of the standard deviation.
> Source: Discrete Random Variables - Copy.pdf

### Units

The mean (expected outcome) and the standard deviation of X have the **same unit** as the values of labels in the spectrum of X. The variance has the unit **squared**.
> Source: Discrete Random Variables - Copy.pdf

### The "Rule of Thumb" Normal Range

The lecture notes use a rule-of-thumb range for what counts as a usual value:

**μ_X − 2σ_X ≤ x ≤ μ_X + 2σ_X**
> Source: Discrete Random Variables - Copy.pdf

## Examples

- **Rolling one fair die:** Let 𝑌 = outcome on a fair six-sided die. E[Y] = (1)(1/6) + (2)(1/6) + (3)(1/6) + (4)(1/6) + (5)(1/6) + (6)(1/6) = 21/6 = **3.5**. You'll never roll a 3.5, but it's the mean outcome over many rolls — the number a simulation of millions of dice rolls would approach.
  > Source: Expected Value, Variance and Standard Deviation.html
- **Variance of one fair die:** E[X²] = 91/6 ≈ 15.167, so Var(X) = 15.167 − (3.5)² = 15.167 − 12.25 = 2.917 ≈ **2.92**.
  > Source: Expected Value, Variance and Standard Deviation.html/practice/config-1763423573247.practice.json
- **Number of girls in two births:** With P(0) = 0.25, P(1) = 0.50, P(2) = 0.25, the mean is μ = E[X] = 1. The squared deviations weighted by probability give σ² = 0.25 + 0 + 0.25 = **0.5**, so σ = √0.5 = **0.707**. On average there's one girl per two births, and the number of girls typically varies by about 0.7 around that mean — so while 1 girl is the expected outcome, you'll often see families with 0 or 2 girls, results that sit within one standard deviation of the mean.
  > Source: Expected Value, Variance and Standard Deviation.html
- **Failed test cases per day:** A QA tester models failures per day as P(0) = 0.1, P(1) = 0.4, P(2) = 0.3, P(3) = 0.2. Then E[X] = 0(0.1) + 1(0.4) + 2(0.3) + 3(0.2) = **1.6**; E[X²] = 0²(0.1) + 1²(0.4) + 2²(0.3) + 3²(0.2) = **3.4**; Var(X) = 3.4 − (1.6)² = 3.4 − 2.56 = **0.84**; σ = √0.84 ≈ **0.916**. On average, 1.6 tests fail per run, with typical variation of about 0.916 failures around that mean.
  > Source: Expected Value, Variance and Standard Deviation.html
- **Unfair die (lecture worked example):** For the die with P(1) = 1/12, P(2) = 1/12, P(3) = 1/12, P(4) = 1/4, P(5) = 1/6, P(6) = 1/3, the probabilities sum to 1 and μ_X = E(X) = 13/3 = **4.3̄**. Using the shortcut with ∑ x²P(x) = 21.3̄: σ_X = √(21.3̄ − (4.3̄)²) = √(21.3̄ − 18.7̄) = √2.5̄ ≈ 1.599 ≈ **1.6**, and the variance is σ²_X = **2.5̄**.
  > Source: Discrete Random Variables - Copy.pdf
- **Prior DWI sentences:** For the distribution P(0) = 0.512, P(1) = 0.301, P(2) = 0.132, P(3) = 0.055, ∑xP(x) = 0.730 and ∑x²P(x) = 1.324. So μ_X = **0.7 people**, σ²_X = 1.324 − (0.730)² = 0.7911 ≈ **0.8 people²**, and σ_X = √0.7911 = 0.889 ≈ **0.9 people**. Applying the rule of thumb, the normal range is 0.7 − 1.8 ≤ x ≤ 0.7 + 1.8, i.e. 0 ≤ x ≤ 2.5 (the lower bound is truncated at 0 because a negative count is impossible), so 0 ≤ x ≤ 2.
  > Source: Discrete Random Variables - Copy.pdf
- **Length of a baseball World Series:** With P(4) = 0.1809, P(5) = 0.2234, P(6) = 0.2234, P(7) = 0.3723, ∑xP(x) = 5.7871 and ∑x²P(x) = 34.7645. So μ_X ≈ **5.8 games** and σ_X = √(34.7645 − 5.7871²) ≈ 1.128 ≈ **1.1 games**. The usual range is 5.8 − 2.2 ≤ x ≤ 5.8 + 2.2, i.e. 3.6 ≤ x ≤ 8.0, so 4 ≤ x ≤ 7 games. It is therefore **not** unusual for a team to "sweep" by winning in four games.
  > Source: Discrete Random Variables - Copy.pdf
- **Comparing two algorithms:** Two algorithms both average 10 ms. Algorithm A has σ = 0.2 ms, Algorithm B has σ = 3.5 ms. **Algorithm A is more predictable because its standard deviation is smaller** — a smaller standard deviation means results stay close to the mean, so A's times vary very little.
  > Source: Expected Value, Variance and Standard Deviation.html/practice/config-1763423722051.practice.json

## Common Misconceptions

- **"The expected value is a likely outcome."** It isn't — the expected value is the average of all possible outcomes, weighted by their probabilities. You'll never roll a 3.5 on a die.
  > Source: Expected Value, Variance and Standard Deviation.html/practice/config-1763423476164.practice.json
- **"A larger standard deviation means more predictable."** The opposite — a larger standard deviation indicates greater variation, so run times fluctuate more and are less predictable.
  > Source: Expected Value, Variance and Standard Deviation.html/practice/config-1763423722051.practice.json
- **"Two processes with the same mean are equally predictable."** The mean describes the central value, not the spread. Two processes can share the same mean but differ drastically in variability.
  > Source: Expected Value, Variance and Standard Deviation.html/practice/config-1763423722051.practice.json
- **Using the mean instead of the mean *squared* in the shortcut formula.** Var(X) = E[X²] − (E[X])² — check the subtraction and make sure no squared term is missed.
  > Source: Expected Value, Variance and Standard Deviation.html/practice/config-1763423573247.practice.json

## Related Topics

- [Random Variables and Probability Distributions](random-variables-and-distributions.md)
- [The Binomial Distribution](binomial-distribution.md)
- [The Poisson Distribution](poisson-distribution.md)
- [Conditional Probability and Bayes' Theorem](conditional-probability-and-bayes.md)
