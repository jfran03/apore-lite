# The Poisson Distribution

> **Main concept:** Named Discrete Distributions

## Definition

In the binomial distribution, if the number of trials n becomes very large while the probability of success in each trial becomes proportionally small, so that the expected amount **μ = np** remains the same, we can approximate the binomial probability distribution (whose values are hard to calculate — ₙC_k involves many, many products for large n) by a simpler distribution called **Poisson**:

**P(X = k) = ₙC_k pᵏ q^(n−k) ≈ (μᵏ / k!) e^(−μ)**, where μ = np.
> Source: Discrete Random Variables - Copy.pdf

The exact value of the Poisson probability **P(X = k) = (μᵏ / k!) e^(−μ)** becomes exact when n becomes unbounded and infinite.
> Source: Discrete Random Variables - Copy.pdf

## Key Concepts

### Interpretation

The number of "moments," which are infinite, replaces n, the number of trials. Each moment in an interval is a trial; an event occurring at a moment is counted as a "success" for that trial.
> Source: Discrete Random Variables - Copy.pdf

A **Poisson random variable counts the number of (independent) occurrences of a certain event over an interval of time** (or space, area, lengths…).
> Source: Discrete Random Variables - Copy.pdf

### The Single Parameter

The only parameter determining the probability of each number of occurrences is the **mean or expected number of occurrences μ**:

**P(X = k) = (μᵏ / k!) e^(−μ)**

where k is the number of occurrences in the given interval and μ is the mean number of occurrences in **the same interval**.
> Source: Discrete Random Variables - Copy.pdf

### Parameters — Mean and Standard Deviation

X as a Poisson random variable has only **one** parameter, i.e. the mean number of occurrences μ:

**μ_X = μ** ← expected value
**σ_X = √μ** ← standard deviation
> Source: Discrete Random Variables - Copy.pdf

**Reminder:** the binomial random variable has **two** parameters to define, n and p, with μ_X = np and σ_X = √(npq). Note also that if n → ∞ and p → 0 (so q → 1), then np = μ and √(npq) = √(μ · 1) = √μ — the binomial parameters collapse into the Poisson ones.
> Source: Discrete Random Variables - Copy.pdf

### Matching the Interval

The value of μ used in the formula **must be the mean number of occurrences in the same interval** as the interval in which the variable is counting the number of occurrences. **If it isn't, you need to change it to the mean for that interval first, before calculating the probabilities.**
> Source: Discrete Random Variables - Copy.pdf

### The Constant e

e = 2.718281828… has an infinite number of decimal values. Use your calculator to approximate the value of e. It is the base of the natural logarithm.
> Source: Discrete Random Variables - Copy.pdf

### Rule of Thumb — When to Use Poisson to Approximate the Binomial

**n ≥ 100** and **np ≤ 10**
> Source: Discrete Random Variables - Copy.pdf

## Examples

The following problems are posed in the source notes:

- **Seismic activity:** On May 13, 2013, starting at 4:30 PM, the probability of moderate seismic activity for the next 48 hours in the Kuril Islands off the coast of Japan was reported at about 1.43%. Use this information for the next 100 days to find the probability that there will be low seismic activity in five of the next 100 days. Use **both** the binomial and Poisson distributions to calculate the probabilities — are they close?
  > Source: Discrete Random Variables - Copy.pdf
- **Homicide deaths:** In one year there were 116 homicide deaths in Richmond, Virginia. For a randomly selected day, find the probability that the number of homicide deaths is (a) 0, (b) 1, (c) 2, (d) 3, (e) 4. Then compare the calculated probabilities to these actual results: 268 days with no homicides; 79 days with 1 homicide; 17 days with 2 homicides; 1 day with 3 homicides; no days with more than 3 homicides.
  > Source: Discrete Random Variables - Copy.pdf
- **Direct parameter problem:** In a Poisson distribution, μ = 0.78. (a) What is the probability that x = 0? (b) What is the probability that x > 0?
  > Source: Discrete Random Variables - Copy.pdf
- **Switchboard (interval matching):** The mean number of wrong numbers received by a switchboard in a minute is 3. Find the probability that the switchboard receives at least two wrong numbers in the next **2 minutes**. (This is the case where μ must be rescaled to match the counting interval.)
  > Source: Discrete Random Variables - Copy.pdf
- **Russian thistles (spatial interval):** In one test plot area, the mean number of thistles per square meter was found to be 3. What's the probability that at least one thistle will appear in an area of 1 m², assuming the number of thistles follows a Poisson distribution?
  > Source: Discrete Random Variables - Copy.pdf
- **Kentucky Pick 4:** You pay $1 to select a sequence of four digits, such as 2283. If you play this game once every day, find the probability of winning exactly once in 365 days.
  > Source: Discrete Random Variables - Copy.pdf

### Binomial or Poisson? — Discrimination Problems

- A radioactive source emits particles at a rate of 2 particles per minute. What is the probability that the first particle appears sometime after three minutes but before five minutes?
  > Source: Discrete Random Variables - Copy.pdf
- A book has 600 pages and 250 typos. (a) What is the probability that the first five pages have no typos? (b) What is the probability that the first five pages have at most two typos?
  > Source: Discrete Random Variables - Copy.pdf
- On average, two tornadoes hit major U.S. metropolitan areas every year. What is the probability that more than four tornadoes occur in major U.S. metropolitan areas next year?
  > Source: Discrete Random Variables - Copy.pdf
- From past experience, airlines know that 3% of passengers don't show up for their flight. Suppose the airplane has 200 seats and the airline sells exactly 200 seats — what are the chances the airplane will be full when it takes off?
  > Source: Discrete Random Variables - Copy.pdf

## Common Misconceptions

- **Using a μ measured over a different interval than the one you're counting over.** The source flags this explicitly: if the given mean is not for the same interval, you must rescale it to that interval *before* calculating any probabilities.
  > Source: Discrete Random Variables - Copy.pdf

## Related Topics

- [The Binomial Distribution](binomial-distribution.md)
- [Random Variables and Probability Distributions](random-variables-and-distributions.md)
- [Expected Value, Variance and Standard Deviation](expected-value-variance-standard-deviation.md)
