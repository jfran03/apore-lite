# Continuous Random Variables and the Normal Distribution

> **Main concept:** Continuous Distributions

## Definition

The labels in a discrete random variable can be listed and indexed: 1, 2, 3, …. This means the probability distribution can be drawn as a **histogram**. The condition ∑ᵢ P(xᵢ) = 1 means the area of all the rectangles in the histogram must add up to 1 (each rectangle has a height of P(xᵢ) and a width of 1).
> Source: Normal Distribution and the CLT - Copy.pdf

In a **continuous random variable**, the labels have no gaps, cannot be listed and indexed by integers, and so a **smooth curve replaces the sharp edges of the histogram**. The area under the curve for each interval gives the probability for the random variable to fall in that interval: **P(x₁ ≤ X ≤ x₂) = p**.
> Source: Normal Distribution and the CLT - Copy.pdf

The **Normal Distribution** is also known as the **bell-shaped** or **Gaussian** curve, with density

**f(x) = 1/(√(2π) σ_X) · e^( −(x − μ_X)² / (2σ_X²) )**, written **X ~ N(μ_X, σ_X)**

where μ_X is the mean (expected value) and σ_X is the standard deviation. Example: X ~ N(2.1, 0.7).
> Source: Normal Distribution and the CLT - Copy.pdf

## Key Concepts

### Probability Density

Since the random variable values (labels) do not come in rectangles of width 1, the height of the graph need not be below 1 for the area to still be less than 1. The height of the graph denotes the **probability density** associated with the random variable.
> Source: Normal Distribution and the CLT - Copy.pdf

### Conditions for a Legitimate Probability Density Distribution

For a function f to be a legitimate probability density distribution for a random variable X, it must satisfy:

1. **f(x) ≥ 0** for all x in the spectrum of X.
2. **The total area under the curve must equal 1.**

It follows that the area of each subset is less than or equal to 1.
> Source: Normal Distribution and the CLT - Copy.pdf

### Key Feature of Continuous Random Variables

Labels denote the result of a **measurement (with units)** rather than a number or count (without units). Examples: the length of an industrial shaft (in cm), the length of a time interval like a phone call (in seconds), the weight of a person (in kg), the volume of a wine barrel (in litres).
> Source: Normal Distribution and the CLT - Copy.pdf

### Properties of the Normal Curve

- The Normal curve is **symmetric** and **bell-shaped**.
- The **mean, mode and median are all equal**, located under the peak of the curve.
- The **tails on left and right approach zero asymptotically** — they are never zero but tend to zero as x approaches −∞ or +∞.
- Values on the horizontal axis are the labels of X, and represent outcomes that the random variable holds.
- The **area under the curve represents the probability**: P(x₁ ≤ X ≤ x₂) = p, with 0 ≤ p ≤ 1.
> Source: Normal Distribution and the CLT - Copy.pdf

### Probability of a Single Point Is Zero

Since probability equals the area, it follows that **P(X = x) ≡ 0**, since a point on the real line corresponds to a zero (i.e. infinitesimal) interval and thus to zero (i.e. infinitesimal) area. Therefore:

**P(x₁ ≤ X ≤ x₂) = P(x₁ ≤ X < x₂) = P(x₁ < X ≤ x₂) = P(x₁ < X < x₂)**
> Source: Normal Distribution and the CLT - Copy.pdf

### Symmetry

If μ_X = 0, then symmetry around μ_X means:

**P(X > x₁) = P(X < −x₁)** and **P(X > −x₁) = P(X < x₁)**
> Source: Normal Distribution and the CLT - Copy.pdf

### The Standard Normal Distribution

The **standard Normal distribution** has **μ_X = 0** and **σ_X = 1**, with density f(z) = 1/√(2π) · e^(−z²/2).

By convention we denote the random variable with standard Normal distribution by the letter **Z**. The values of random variable Z are called **z-scores**.
> Source: Normal Distribution and the CLT - Copy.pdf

The area for a given z-score interval is called its **p-value**: P(Z < z) = p.
> Source: Normal Distribution and the CLT - Copy.pdf

### Combining Areas

**P(z₁ < Z < z₂) = P(Z < z₂) − P(Z < z₁)**
> Source: Normal Distribution and the CLT - Copy.pdf

Due to symmetry around 0, for any z-score z: **P(Z ≤ −z) = P(Z ≥ z)**.
> Source: Normal Distribution and the CLT - Copy.pdf

### Critical Values

We denote a z-score as **z_α** when **P(Z ≥ z_α) = α** and **P(Z ≤ −z_α) = α** (where α is the p-value).

A **critical value** is a z-score that separates unlikely values from those that are likely to occur.
> Source: Normal Distribution and the CLT - Copy.pdf

Standard examples:

- α = 0.05 → **z₀.₀₅ = 1.645**, so P(−1.645 < Z < 1.645) = 0.90
- α = 0.025 → **z₀.₀₂₅ = 1.96**, so P(−1.96 < Z < 1.96) = 0.95
> Source: Normal Distribution and the CLT - Copy.pdf

### Converting Between a General Normal and the Standard Normal

For a general Normal distribution N(μ_X, σ_X), convert to and from the standard by:

**z = (x − μ_X) / σ_X** and **x = μ_X + z σ_X**
> Source: Normal Distribution and the CLT - Copy.pdf

Consequently:

**P(X < x₁) = P(Z < z₁)**
**P(x₁ < X < x₂) = P(X < x₂) − P(X < x₁) = P(Z < z₂) − P(Z < z₁) = P(z₁ < Z < z₂)**
> Source: Normal Distribution and the CLT - Copy.pdf

### The Cumulative Standard Normal Table

The formula booklet supplies **Table 1: Cumulative Standard Normal Distribution**, split into negative and positive z-scores, giving the cumulative area from the left for z from −3.4 to +3.4 in steps of 0.01. Selected anchor values: the area left of z = 0.00 is .5000; left of z = 1.00 is .8413; left of z = 1.96 is .9750; left of z = −1.00 is .1587; left of z = −2.50 is .0062.

- **For values of z below −3.49, use 0.0001 for the area.**
- **For values of z above 3.49, use 0.9999 for the area.**
> Source: Normal Distribution and the CLT - Copy.pdf

## Examples

- **Uniform distribution:** Given the illustrated uniform distribution over voltage levels 123.0 to 125.0 with density 0.5, the probability that a randomly selected voltage level is greater than 124.5 volts is the shaded area = 0.5 × 0.5 = **0.25**.
  > Source: Normal Distribution and the CLT - Copy.pdf
- **Reading the z-table:** P(z < 1.27) = **0.8980** — here 1.27 is the z-score and 0.8980 is the p-value, found by locating row 1.2 and column .07 in Table A-2.
  > Source: Normal Distribution and the CLT - Copy.pdf

### Bone Density Test (Standard Normal)

A bone mineral density test can be helpful in identifying the presence of osteoporosis. The result is commonly measured as a z-score, which has a normal distribution with a mean of 0 and a standard deviation of 1.

- (a) Find the probability that the result is a reading less than 1.27.
- (b) Find the probability that a randomly selected person has a result above −1.00 (considered to be in the "normal" range of bone density readings).
- (c) A bone density reading between −1.00 and −2.50 indicates osteopenia. Find this probability. **Worked:** the area to the left of z = −2.50 is 0.0062; the area to the left of z = −1.00 is 0.1587; the area between them is the difference, 0.1587 − 0.0062 = **0.1525**.
- (d) Find the bone density scores that separate the bottom 2.5% and the top 2.5%.
> Source: Normal Distribution and the CLT - Copy.pdf

### Nonstandard Normal Problems

- **Aircraft cabins:** When designing aircraft cabins, what ceiling height will allow 95% of men to stand without bumping their heads? Men's heights are normally distributed with a mean of 69.5 inches and a standard deviation of 2.4 inches.
  > Source: Normal Distribution and the CLT - Copy.pdf
- **Tall Clubs International:** requires that women be at least 70 inches tall. Given that women have normally distributed heights with a mean of 63.8 inches and a standard deviation of 2.6 inches, find the percentage of women who satisfy that height requirement.
  > Source: Normal Distribution and the CLT - Copy.pdf

## Related Topics

- [Sampling Distributions and the Central Limit Theorem](sampling-distributions-and-clt.md)
- [Random Variables and Probability Distributions](random-variables-and-distributions.md)
- [Expected Value, Variance and Standard Deviation](expected-value-variance-standard-deviation.md)
