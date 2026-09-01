# The Binomial Distribution

> **Main concept:** Named Discrete Distributions

## Definition

A **binomial random variable** is a random variable with the binomial probability distribution. It **counts the number of "successes" in a fixed number of trials** (or measurements), where:

- Each trial has only **two** possible outcomes, which we label "0" for "failure" and "1" for "success."
- Each trial is **independent** from other trials.
- The probability of failure and success of each trial remains **constant** for all trials.
> Source: Discrete Random Variables - Copy.pdf

Such trials are called **independent identically distributed** (**iid** for short).
> Source: Discrete Random Variables - Copy.pdf

## Key Concepts

### Notation

- **n** = the number of trials (already fixed)
- **p** = P(1) = probability of success
- **q** = 1 − p = P(0) = probability of failure
> Source: Discrete Random Variables - Copy.pdf

### The Binomial Probability Formula

**P(X = k) = (ₙC_k) · pᵏ · q^(n−k)**

where k is the number of "successes", n is the total fixed number of trials, p is the probability of "success" in each single trial (p is a constant), and q = 1 − p is the probability of "failure" in each single trial.
> Source: Discrete Random Variables - Copy.pdf

### The Combination Factor

**ₙC_k** (read: "n choose k") counts the number of combinations in choosing k identical outcomes out of a total of n outcomes:

**ₙC_k = [ n(n−1)(n−2)…(n−(k−1)) ] / (1 × 2 × 3 × … × k) = n! / [ (n−k)! k! ]**

where n! = 1 × 2 × … × n and 0! ≡ 1. Other notations: ₙC_k = (ⁿ_k).
> Source: Discrete Random Variables - Copy.pdf

Useful special cases: ₙC₀ = 1, ₙC₁ = n, ₙC₂ = n(n−1)/2, ₙC₃ = n(n−1)(n−2)/6.
> Source: Discrete Random Variables - Copy.pdf

### Mean and Standard Deviation

For a binomial random variable X with n trials and probability of success p in each trial:

**μ_X = E(X) = np**
**σ_X = √( n p (1−p) ) = √(npq)**

where q = 1 − p is the probability of "failure" for each trial.
> Source: Discrete Random Variables - Copy.pdf

The binomial random variable has **two parameters** to define: n and p.
> Source: Discrete Random Variables - Copy.pdf

### Rule of Thumb for Independence When Sampling Without Replacement

When sampling **without replacement**, consider events to be independent if:

**n < 0.05 N**

where n is the sample size and N is the total population size.
> Source: Discrete Random Variables - Copy.pdf

### Spreadsheet Equivalents

- ₙC_k in Excel: `=COMBIN(n, k)`
- P(X = k) = ₙC_k · pᵏ q^(n−k) in Excel: `=BINOM.DIST(k, n, p, 0)`
- `BINOM.DIST(k, n, p, 1)` gives P(X ≤ k)
> Source: Discrete Random Variables - Copy.pdf

## Examples

### Deriving the Formula — Three Heads in Five Tosses

We toss a coin 5 times and want the probability of observing 3 heads. Always start with the random variable: let X be the random variable counting the number of heads in 5 tosses of the coin.

- n = 5
- "success" → observing a head → label **1**
- "failure" → observing a tail → label **0**
- Spectrum of X (the set of possible counts of heads in n = 5 tosses) = {0, 1, 2, 3, 4, 5}

We want P(X = 3), and the answer will be in terms of n, p, q and k = 3, where p = P(1) is the probability of observing a head on a *single* toss and q = 1 − p = P(0) is the probability of observing a tail on a single toss.
> Source: Discrete Random Variables - Copy.pdf

Enumerating the tree of all 5-toss sequences and grouping by the count of heads gives:

- P(X = 0) = (1) p⁰q⁵ = (₅C₀) p⁰ q^(5−0)
- P(X = 1) = (5) p¹q⁴ = (₅C₁) p¹ q^(5−1)
- P(X = 2) = (10) p²q³ = (₅C₂) p² q^(5−2)
- P(X = 3) = (10) p³q² = (₅C₃) p³ q^(5−3)
- P(X = 4) = (5) p⁴q¹ = (₅C₄) p⁴ q^(5−4)
- P(X = 5) = (1) p⁵q⁰ = (₅C₅) p⁵ q^(5−5)

(Remember p⁰ = 1 and q⁰ = 1.) Generalising gives **P(X = k) = ₙC_k pᵏ q^(n−k)**.
> Source: Discrete Random Variables - Copy.pdf

### Combination Values

₆C₀ = 1, ₆C₁ = 6, ₆C₂ = (6 × 5)/2 = 15, ₆C₃ = (6 × 5 × 4)/(1 × 2 × 3) = 20.
> Source: Discrete Random Variables - Copy.pdf

### Practice Problems Posed in the Notes

These problems appear in the source; the notes state the setup but do not work all of them through:

- Find the probability of getting exactly 7 French-Canadians when 12 jurors are randomly selected from a population that is 80% French-Canadian — that is, find P(7) given n = 12, x = 7, p = 0.8 and q = 0.2. Also find the mean and standard deviation for the number of French-Canadians on juries selected from this population.
  > Source: Discrete Random Variables - Copy.pdf
- The Medassist Pharmaceutical Company randomly selects and tests 24 aspirin tablets, then accepts the whole batch if there is only one or none that doesn't meet specifications. If a shipment actually has a 4% rate of defects, what is the probability the whole shipment will be accepted?
  > Source: Discrete Random Variables - Copy.pdf
- On a multiple choice test with 17 questions, each having four possible answers with one correct: for students who guess at all answers, (a) find the mean and standard deviation for the number of correct answers, and (b) find the probability that they get at least 2 correct.
  > Source: Discrete Random Variables - Copy.pdf
- A company manufacturing interface control modules has a 3.25% rate of defective modules. Using the binomial formula, find the probability that among a random sample of 25 selected control modules: (a) exactly 5 will be defective, (b) at most 3 will be defective, (c) at least 1 will be defective.
  > Source: Discrete Random Variables - Copy.pdf
- In a past presidential election the actual voter turnout was 61%, and 1002 subjects were surveyed. (a) Find the mean and standard deviation for the number of actual voters in groups of 1002. (b) In the survey, 701 said they voted — is this result consistent with an actual voter turnout of 61%, or is it unlikely to occur? Why or why not?
  > Source: Discrete Random Variables - Copy.pdf

### Binomial or Poisson? — Discrimination Problems

The notes close with a set of problems asking which distribution applies, including: ten percent of computer parts produced by a supplier are defective — what is the probability that a sample of 10 parts has no defective parts? And: 40% of voters support the Conservative party; take a random sample of 6 voters and let Y represent the number in the sample who support the Conservative party.
> Source: Discrete Random Variables - Copy.pdf

## Related Topics

- [The Poisson Distribution](poisson-distribution.md)
- [Random Variables and Probability Distributions](random-variables-and-distributions.md)
- [Expected Value, Variance and Standard Deviation](expected-value-variance-standard-deviation.md)
- [Permutations and Combinations](permutations-and-combinations.md)
