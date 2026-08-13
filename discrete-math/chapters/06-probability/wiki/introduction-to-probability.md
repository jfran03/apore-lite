# Introduction to Probability

> **Main concept:** Foundations of Probability

## Definition

Probability is the branch of mathematics that gives us a language and toolkit to reason about uncertainty — questions like "Will it rain tomorrow? Will a server fail? Will a user click on a particular link?"
> Source: Introduction to Probability.html

The probability of an "event" is a real number between 0 and 1. The larger the number (i.e. the closer to 1), the more "likely" the event is to happen in a given circumstance.
> Source: Probability - Copy.pdf

Probability provides the model and the language to analyze the likelihood of various outcomes, events and results of measurements. The main aim of statistics is to make general conclusions about an entire population, based on the limited data gathered from a sample; the price to pay is a lack of certainty, so instead we need to determine the likelihood or "probability" of such conclusions.
> Source: Probability - Copy.pdf

## Key Concepts

### Core Terms

- **Experiment:** a process you carry out that leads to one or more outcomes (for example: rolling a die, choosing a support-ticket at random).
  > Source: Introduction to Probability.html
- **Outcome:** a single result of the experiment (for example: rolling a 4, choosing a billing ticket).
  > Source: Introduction to Probability.html
- **Sample space (𝑆):** the set of all possible outcomes of the experiment (for example: {1,2,3,4,5,6} for a fair six-sided die).
  > Source: Introduction to Probability.html
- **Event:** a subset of the sample space with one or more outcomes that we focus on (for example: "rolling an even number" = {2,4,6}).
  > Source: Introduction to Probability.html

Using consistent language makes it easier to build on more advanced rules without confusion.
> Source: Introduction to Probability.html

### Range of Probability

No matter the experiment, the probability of any event always lies between 0 and 1 inclusive:

**0 ⩽ P(A) ⩽ 1**

- 𝑃(𝐴) = 0 means the event cannot happen (impossible event).
- 𝑃(𝐴) = 1 means the event is certain (sure event).
- A value between 0 and 1 shows how likely the event is (closer to 1 = more likely).
> Source: Introduction to Probability.html

### The Classical Probability Formula

When each outcome in the sample space is equally likely, the probability of an event 𝐴 is:

**P(A) = (number of favourable outcomes for A) / (total number of outcomes in S)**
> Source: Introduction to Probability.html

### Three Interpretations of Probability

The lecture notes present three options for how probabilities get assigned:

- **Option 1 — The frequency interpretation:** the ratio of favourable outcomes (for the event) over total outcomes approaches the probability of the event, written m/n → P(A). **Problem:** the ratio only gets more *"likely"* to approach the fixed probability as n increases indefinitely.
  > Source: Probability - Copy.pdf
- **Option 2 — The subjective interpretation:** probability, or "credence," as a measure of subjective certainty or ignorance. Start with total ignorance (e.g. 50:50 for a coin) and update with each piece of evidence/observation. **Problem:** independence of events is not well-defined in this interpretation; additionally, rejection of theories is not a gradual process. Example: the paradox of black ravens.
  > Source: Probability - Copy.pdf
- **Option 3 — The objective/classical interpretation (based on symmetry):** the starting point is symmetry. For 𝑛 physically identical simple events, indistinguishable except for arbitrary labels, we assign to each simple event the probability **P = 1/n**.
  > Source: Probability - Copy.pdf

### Theoretical vs. Experimental Probability

Probability can be understood in two main ways: **theoretical probability** (based on reasoning) and **experimental probability** (based on observation or data). Both describe how likely an event is, but they differ in how the probability is found.
> Source: Introduction to Probability.html

- **Theoretical probability** assumes all outcomes are equally likely and is calculated using the classical formula. You don't need to actually perform the experiment, you just need to reason it out.
  > Source: Introduction to Probability.html
- **Experimental probability** comes from real or simulated trials. Instead of theory, you collect data and calculate how often an event occurs:

  **P(A) = (number of times A occurs) / (total number of trials)**
  > Source: Introduction to Probability.html
- **The Law of Large Numbers:** the more times you repeat the experiment, the closer the experimental probability should get to the theoretical value.
  > Source: Introduction to Probability.html

Theoretical probability is ideal for pure reasoning, like computing the odds in card games or algorithm outcomes. Experimental probability is used when you have data, such as system logs, sensor readings or randomised simulations.
> Source: Introduction to Probability.html

### Sample Spaces and Tables

The sample space lists all possible outcomes of an experiment. When multiple random actions occur together, it's useful to organise the sample space in a table. A sample space table (or outcome grid) works best when each random event can be shown along one axis; each cell represents one possible combined outcome.
> Source: Introduction to Probability.html

### Coarse Graining

To start with and work with **unequal** probabilities, we bundle events under the same label (which brings resolution down), so we can have different probabilities for different labels.
> Source: Probability - Copy.pdf

### Simple vs. Compound Events

Probabilities are first assigned to **simple events**, then combined to determine the probability of **compound events**.
> Source: Probability - Copy.pdf

## Examples

- **Die roll (classical formula):** You roll a fair six-sided die. Let 𝐴 = "roll is a 4". Favourable outcomes = {4} → 1. Total outcomes = 6. So 𝑃(𝐴) = 1/6 ≈ 0.1667.
  > Source: Introduction to Probability.html
- **Customer-support calls:** 100 calls arrive and each is equally likely to be selected. 10 of today's calls were billing-related. Let 𝐵 = "selected call is billing". 𝑃(𝐵) = 10/100 = 0.10.
  > Source: Introduction to Probability.html
- **Impossible and sure events:** On a fair six-sided die, "roll a 7" has no favourable outcomes, so 𝑃 = 0/6 = 0. "Roll something from 1 to 6" has six favourable outcomes out of six, so 𝑃 = 6/6 = 1.
  > Source: Introduction to Probability.html
- **Support-call vocabulary:** Pick a support-call at random from all the calls made this morning. *Experiment*: selecting a random call. *Sample space*: all the calls made this morning. *Outcome*: e.g. "this call was about billing". *Event*: "call is about billing or returns".
  > Source: Introduction to Probability.html
- **Two dice sample-space table:** Roll two fair six-sided dice and add the numbers on the upper faces. Each die has outcomes {1,…,6}, so together there are 6 × 6 = 36 equally likely outcomes. For event 𝐴 = "the total of both dice is 3", only (1, 2) and (2, 1) produce a total of 3, so 𝑃(𝐴) = 2/36 = 1/18 ≈ 0.0556 — you can expect a total of 3 only about 5.6 % of the time.
  > Source: Introduction to Probability.html
- **Experimental probability:** You roll a fair die 60 times and get an even number 28 times. 𝑃(even) = 28/60 = 0.467. This is close to the theoretical 0.5, and if you rolled many more times the difference would likely shrink.
  > Source: Introduction to Probability.html
- **Symmetry — fair coin:** a uniform mass distribution with 2 sides that have identical shape, so P(H) = P(T) = 1/2. The space of events is 𝑀 = {H, T}.
  > Source: Probability - Copy.pdf
- **Symmetry — fair die:** a uniform mass distribution with 6 sides of a symmetric cube, all identical, so each face has probability 1/6. (All fair dice are regular polyhedra.)
  > Source: Probability - Copy.pdf
- **Coarse graining an unfair coin:** Consider a coin twice as heavy on the head side. We can simulate that with a *three*-sided coin, all equally weighted, labelling two sides H and one side T. Then P(H) = 1/3 + 1/3 = 2/3 and P(T) = 1/3.
  > Source: Probability - Copy.pdf
- **Birthday-date probabilities:** For a randomly selected person (ignoring leap years): (a) P(birthday is October 18) = 1/365; (b) P(birthday is in October) = 31/365; (c) P(born on a day of the week ending with the letter "y") = 7/7 = 1, because all seven days of the week end in "y".
  > Source: Probability - Copy.pdf; Capture4.PNG
  >
  > *(Capture4.PNG restates this as worksheet exercise 1(a)–(c) with no solution given; the worked values above come from Probability - Copy.pdf.)*
- **The Sleeping Beauty problem** is given as an example of the subtleties and difficulties in assigning probabilities: depending on how the question is framed, P(T | sleeping beauty wakes up) is either 1/2 or 1/3.
  > Source: Probability - Copy.pdf

## The History of Probability

Probability theory started with questions about games and chance, but quickly expanded to science, business and engineering.
> Source: Introduction to Probability.html

- **Early Curiosity about Chance (Pre-1500s):** Games of chance were common long before formal mathematics existed, but people relied on intuition rather than systematic analysis. There was no agreed way to measure luck or predict outcomes.
  > Source: Introduction to Probability.html
- **Gerolamo Cardano (1501–1576):** an Italian mathematician and physician, the first to treat probability as a mathematical concept. In the unpublished *Liber de Ludo Aleae* (Book on Games of Chance) he defined probability as the ratio of favourable outcomes to total equally likely outcomes — a foundational idea still used today.
  > Source: Introduction to Probability.html
- **Pascal and Fermat (1600s):** Blaise Pascal and Pierre de Fermat exchanged letters on gambling problems, particularly how to divide winnings if a game stopped early. Their reasoning marked the start of formal probability theory.
  > Source: Introduction to Probability.html
- **Laplace (1700s–1800s):** Pierre-Simon Laplace extended probability beyond gambling to science, politics and population studies, framing it as a universal tool for reasoning under uncertainty and connecting it to statistics.
  > Source: Introduction to Probability.html
- **From Games to Computers (Today):** probability underpins machine learning, cryptography, computer networks and reliability modelling.
  > Source: Introduction to Probability.html

## Common Misconceptions

- **"After 7 heads in 20 flips, the coin must be biased / due for tails."** The Knowledge Check on this page raises the case of flipping a fair coin 20 times and getting 7 heads. The page's own framing is that experimental probability approaches the theoretical value only as the number of trials grows — the Law of Large Numbers — so a short run departing from 0.5 is expected.
  > Source: Introduction to Probability.html

## Related Topics

- [Complement Events and the Birthday Problem](complement-events.md)
- [Addition and Multiplication Rules](addition-and-multiplication-rules.md)
- [Conditional Probability and Bayes' Theorem](conditional-probability-and-bayes.md)
- [Random Variables and Probability Distributions](random-variables-and-distributions.md)
