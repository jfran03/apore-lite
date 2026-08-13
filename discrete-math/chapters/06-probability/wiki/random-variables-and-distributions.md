# Random Variables and Probability Distributions

> **Main concept:** Random Variables

## Definition

A **random variable** is a numerical value that represents the outcome of a random process or experiment. It's "random" because you can't predict its exact value in advance, and it's a "variable" because it can take on different values each time the process occurs.
> Source: Random Variables and Distributions.html

The lecture notes define it as a **place holder for the numeric labels for the events**.
> Source: Discrete Random Variables - Copy.pdf

We usually label random variables with capital letters like 𝑋, 𝑌 or 𝑍. Each value it can take, written as lowercase 𝑥, 𝑦 or 𝑧, is called an outcome.
> Source: Random Variables and Distributions.html; Discrete Random Variables - Copy.pdf

Random variables transform the uncertainty of the real world into data that can be computed, stored and reasoned about.
> Source: Random Variables and Distributions.html

### Why Numeric Labels?

We learned how to coarse-grain (i.e. bundle) events using labels for each bundle. So far, labels could be anything — their role was to *distinguish* different events (nominal level). Now we want to use **numeric** labels so we can add or subtract them (interval level), so we can do calculations with them, like calculating population mean and standard deviation.
> Source: Discrete Random Variables - Copy.pdf

## Key Concepts

### Spectrum

A random variable X has a **spectrum**, i.e. the set of allowed labels, {x}.
> Source: Discrete Random Variables - Copy.pdf

### Discrete vs. Continuous Random Variables

- **Discrete random variables** can take on only specific, countable values (often integers). Examples: number of emails in an inbox, number of errors in a log file, number of heads in 10 coin flips.
  > Source: Random Variables and Distributions.html
- **Continuous random variables** can take on any value within a range or interval. Examples: response time of a server (in seconds), CPU temperature, data download speed.
  > Source: Random Variables and Distributions.html

The lecture notes make the same distinction in terms of the spectrum:

- A **discrete random variable** has a discrete spectrum (i.e. the labels x have **gaps** between them and **can be listed**).
  > Source: Discrete Random Variables - Copy.pdf
- A **continuous random variable** has a continuous spectrum (i.e. the labels x have **no gaps** between them and **cannot be listed**).
  > Source: Discrete Random Variables - Copy.pdf

A discrete random variable also has a **probability distribution**, i.e. a set {P(x)} of probabilities for each label x in the spectrum. A continuous random variable has a probability distribution for each *interval* of labels: P(a ≤ x ≤ b).
> Source: Discrete Random Variables - Copy.pdf

The course focuses on discrete random variables: the kind you can list, count and assign specific probabilities to. Continuous random variables are handled differently (using calculus and probability density functions).
> Source: Random Variables and Distributions.html; Discrete Random Variables - Copy.pdf

### Probability Distributions

Probability tells you how likely each event is. A **probability distribution** takes that same idea and organizes it, showing every possible outcome of a random variable along with the probability for each one. In other words, a probability distribution turns random outcomes into a map of likelihoods, helping you answer: What outcomes can happen? How likely is each one? Which outcomes are most common, and which are rare?
> Source: Random Variables and Distributions.html

For a discrete random variable you can represent this in a table — each row lists one possible value and its probability, and all probabilities add up to 1.
> Source: Random Variables and Distributions.html

**To construct a probability distribution:**
1. Identify all possible values of the random variable.
2. Determine the probability for each value.
3. Verify that the total probability equals 1.
> Source: Random Variables and Distributions.html

### Rules for a Valid Probability Distribution

Every probability distribution must meet two conditions:

1. **Each probability must be between 0 and 1:** 0 ≤ P(X = xᵢ) ≤ 1. A probability can't be negative, and it can't exceed certainty.
2. **The total probability across all outcomes must equal 1:** ∑ P(X = xᵢ) = 1. The total probability of all possible outcomes together must represent certainty — something from the sample space will happen.
> Source: Random Variables and Distributions.html

These two properties act as your "sanity check" whenever you build or evaluate a distribution. If either condition fails, the table doesn't represent a valid random variable.
> Source: Random Variables and Distributions.html

The lecture notes state the same two conditions: (1) all probabilities 0 ≤ P(x) ≤ 1, and (2) the sum of all probabilities is 1, ∑ₓ P(x) = 1.
> Source: Discrete Random Variables - Copy.pdf

## Examples

- **Fair die:** Let 𝑋 be the number that comes up on a fair six-sided die. Possible values 1–6, each with probability 1/6, and 𝑃(1) + 𝑃(2) + … + 𝑃(6) = 1 because one of these outcomes must occur.
  > Source: Random Variables and Distributions.html; Discrete Random Variables - Copy.pdf
- **Fair coin:** spectrum {0, 1} with distribution P(0) = 1/2, P(1) = 1/2; sum = 1/2 + 1/2 = 1. Using {0, 1} instead of {H, T} gives a mean value of 0.5 and a standard deviation of √0.25 = 0.5.
  > Source: Discrete Random Variables - Copy.pdf
- **Non-fair coin:** spectrum {0, 1} with distribution P(0) = 1/3, P(1) = 2/3; sum = 1/3 + 2/3 = 1.
  > Source: Discrete Random Variables - Copy.pdf
- **Discrete or continuous?** (a) The *height* of a randomly selected NBA basketball player is **continuous** (arbitrary number of decimal places). (b) The *number of points scored* in a season by a randomly selected NBA player is **discrete** — the spectrum is the integers {0, 1, 2, …}, which have gaps between them.
  > Source: Discrete Random Variables - Copy.pdf
- **Not a genuine distribution:** the table with P(0) = 0.04, P(1) = 0.26, P(2) = 0.36, P(3) = 0.20, P(4) = 0.08 is **not** a genuine probability distribution, because the sum is 0.94 ≠ 1.00.
  > Source: Discrete Random Variables - Copy.pdf

### Two Births

Assume 𝑃(boy) = 𝑃(girl) = 0.5. Let 𝑋 = the number of girls in two births. The possible outcomes are:

| Birth 1 | Birth 2 | X (Number of Girls) |
|---|---|---|
| Girl | Girl | 2 |
| Girl | Boy | 1 |
| Boy | Girl | 1 |
| Boy | Boy | 0 |

Collecting by value of 𝑋:

| X | Possible Outcomes | Probability |
|---|---|---|
| 2 | Girl-Girl | 0.5 × 0.5 = 0.25 |
| 1 | Boy-Girl, Girl-Boy | 2 × (0.5 × 0.5) = 0.5 |
| 0 | Boy-Boy | 0.5 × 0.5 = 0.25 |

The most likely outcome is one girl (probability 0.5); the least likely are two girls or no girls (each 0.25).
> Source: Random Variables and Distributions.html

### Sum of Two Dice

Let 𝑋 = "sum of the two dice." The smallest sum is 2 (1+1) and the largest is 12 (6+6), but not all sums are equally likely — some occur in more ways than others.

| Sum (X) | Number of Ways | P(X) |
|---|---|---|
| 2 | 1 (1+1) | 1/36 |
| 3 | 2 (1+2, 2+1) | 2/36 |
| 4 | 3 | 3/36 |
| 5 | 4 | 4/36 |
| 6 | 5 | 5/36 |
| 7 | 6 | 6/36 |
| 8 | 5 | 5/36 |
| 9 | 4 | 4/36 |
| 10 | 3 | 3/36 |
| 11 | 2 | 2/36 |
| 12 | 1 (6+6) | 1/36 |

The probabilities total 1, confirming a valid distribution. The most likely sum is **7**, occurring in six different ways (about 16.7%); the rarest sums (2 and 12) occur only once each (about 2.8%). This shape — low at the ends, high in the middle — is one of the first examples of a distribution curve. In computing, this type of distribution models aggregated random events such as packet delays or retry counts, where many small random factors add up to one combined result.
> Source: Random Variables and Distributions.html

### Worksheet Problem — Recovering a Missing Probability

A random variable X has the probability distribution shown, with one entry missing:

| X | P(X) |
|---|---|
| −4 | 0.65 |
| 2 | ? |
| 3 | 0.10 |
| 5 | 0.05 |

**Determine the missing value P(X = 2).** The second validity condition — that the probabilities of a distribution must sum to 1 — pins the missing entry down. The three known probabilities total 0.65 + 0.10 + 0.05 = 0.80, so:

**P(X = 2) = 1 − 0.80 = 0.20**

This is the standard use of the ∑P(x) = 1 condition: it is not only a sanity check on a completed table but a tool for recovering a single unknown entry. (The expected value and variance for this same distribution are worked in [Expected Value, Variance and Standard Deviation](expected-value-variance-standard-deviation.md).)
> Source: Capture.PNG (problem and table as posed); validity conditions applied from Random Variables and Distributions.html; Discrete Random Variables - Copy.pdf

## Common Misconceptions

- **"A table of probabilities is automatically a distribution."** It is not — both validity conditions must hold. A table summing to 0.94 fails the second condition and is not a genuine probability distribution.
  > Source: Discrete Random Variables - Copy.pdf; Random Variables and Distributions.html
- **"All sums of two dice are equally likely."** They are not — the number of *ways* each sum can occur differs, so 7 is six times as likely as 2.
  > Source: Random Variables and Distributions.html

## Related Topics

- [Expected Value, Variance and Standard Deviation](expected-value-variance-standard-deviation.md)
- [The Binomial Distribution](binomial-distribution.md)
- [The Poisson Distribution](poisson-distribution.md)
- [Continuous Random Variables and the Normal Distribution](normal-distribution.md)
