# Sampling Distributions and the Central Limit Theorem

> **Main concept:** Continuous Distributions

## Definition

Take a sample of size **n** from values of a random variable X. Then consider a statistic of the sample, like the mean x̄. Now take a *different* sample of size n and repeat — the mean x̄ will most likely be different this time. Repeat this many times and store the values of x̄ in a new random variable. The random variable place holder for values of x̄ we call **X̄ₙ**.
> Source: Normal Distribution and the CLT - Copy.pdf

X̄ₙ will typically have a **different** distribution than X. The distribution of X̄ is called the **sampling distribution**.
> Source: Normal Distribution and the CLT - Copy.pdf

## Key Concepts

### The Central Limit Theorem (C.L.T.)

**X can be any random variable** — it need not be Normal, and need not even be continuous.

The sample distribution X̄ₙ, however, if **n** (the sample sizes) are **large**, will have (approximately) a **Normal distribution**:

**X̄ₙ ~ N(μ_x̄, σ_x̄)** where **μ_x̄ = μ_X** and **σ_x̄ = σ_X / √n**
> Source: Normal Distribution and the CLT - Copy.pdf

### How Large Does n Need to Be?

- If **X is itself Normal**, n can be **any size**.
- If **X is not Normal**, then **n ≥ 30** is required for the C.L.T. to be a good approximation.
> Source: Normal Distribution and the CLT - Copy.pdf

### What the Theorem Buys You

Starting from an arbitrary — even multi-peaked — distribution for X with mean μ_X and standard deviation σ_X, drawing many samples of size n ≥ 30 and collecting their means produces a Normal distribution for X̄ centred at the same mean μ_x̄ = μ_X, but narrower, with σ_x̄ = σ_X/√n.
> Source: Normal Distribution and the CLT - Copy.pdf

## Examples

The notes illustrate convergence with three starting shapes. In each case, as we proceed from n = 1 to n = 50, we see that the distribution of sample means is approaching the shape of a normal distribution:

- **Normal distribution** starting shape
- **Uniform distribution** starting shape
- **U-shaped distribution** starting shape
> Source: Normal Distribution and the CLT - Copy.pdf

### Elevator Capacity

Suppose an elevator has a maximum capacity of 16 passengers with a total weight of 2500 lb. Assuming a worst case scenario in which the passengers are all male, what are the chances the elevator is overloaded? Assume male weights follow a normal distribution with a mean of 182.9 lb and a standard deviation of 40.8 lb.

- (a) Find the probability that 1 randomly selected male has a weight greater than 156.25 lb.
- (b) Find the probability that a sample of 16 males have a mean weight greater than 156.25 lb (which puts the total weight at 2500 lb, exceeding the maximum capacity).
> Source: Normal Distribution and the CLT - Copy.pdf

### Muffin Masses

The mass of muffins purchased at Hank's Store varies from 100 g to 150 g, uniformly distributed with a mean of 125.0 g and standard deviation 14.43 g.

- (a) Find the probability of getting a single muffin chosen at random that has a mass between 115 g and 130 g.
- (b) If a sample of 36 muffins were chosen, determine the probability that the sample mean would be between 115 g and 130 g.
- (c) If a sample of 36 muffins were chosen, determine the probability that the sample mean would be in excess of 128 g.
> Source: Normal Distribution and the CLT - Copy.pdf

Note that parts (a) and (b) of each problem contrast the distribution of a **single** observation against the distribution of a **sample mean** — the same mean, but a standard deviation reduced by a factor of √n.
> Source: Normal Distribution and the CLT - Copy.pdf

## Common Misconceptions

- **"The C.L.T. requires the underlying variable to be Normal."** It does not — X can be any random variable, not even necessarily continuous. What becomes Normal is the distribution of the *sample means*, provided n is large enough (n ≥ 30 when X is not itself Normal).
  > Source: Normal Distribution and the CLT - Copy.pdf

## Related Topics

- [Continuous Random Variables and the Normal Distribution](normal-distribution.md)
- [Expected Value, Variance and Standard Deviation](expected-value-variance-standard-deviation.md)
- [Random Variables and Probability Distributions](random-variables-and-distributions.md)
