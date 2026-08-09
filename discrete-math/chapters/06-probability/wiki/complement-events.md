# Complement Events and the Birthday Problem

> **Main concept:** Foundations of Probability

## Definition

The complement of an event 𝐴, written as 𝐴ᶜ (or sometimes 𝐴′), represents all the outcomes in the sample space that are **not** part of 𝐴:

**𝐴ᶜ = 𝑆 − 𝐴**, where 𝑆 is the sample space.
> Source: Introduction to Probability.html

For every event A, the complementary event Ā indicates the event of A **not** happening. In other words, it is the set of all simple events not contained in A.
> Source: Probability - Copy.pdf

## Key Concepts

### The Complement Rule

The probabilities of an event and its complement always add up to 1:

**P(A) + P(Aᶜ) = 1**, or equivalently **P(Aᶜ) = 1 − P(A)**
> Source: Introduction to Probability.html; Probability - Copy.pdf

This makes sense because between an event and its complement, every possible outcome is covered. Something either happens or it doesn't. There's no overlap or gap.
> Source: Introduction to Probability.html

Since the probability of all events — which is the sum of probabilities of all simple events — is 1, it follows that P(A) + P(Ā) = 1.
> Source: Probability - Copy.pdf

### Why Complements Are Useful

- **They often make problems easier.** For example, it's easier to find the probability of *not* rolling a 6 (5/6) than of rolling anything else.
  > Source: Introduction to Probability.html
- **They reduce errors in reasoning.** Thinking in terms of both an event and its complement forces you to consider the entire sample space.
  > Source: Introduction to Probability.html
- **They're common in programming and logic.** In Boolean terms, the complement of a condition is its negation: the event that the condition evaluates to false.
  > Source: Introduction to Probability.html

## Examples

- **Even vs. odd die roll:** Let 𝐴 = "roll is even" on a fair six-sided die. Sample space 𝑆 = {1,2,3,4,5,6}; event 𝐴 = {2,4,6}; complement 𝐴ᶜ = {1,3,5}. Each outcome is equally likely, so P(A) = 0.5 and P(𝐴ᶜ) = 0.5, and 0.5 + 0.5 = 1. Read this as: the die roll must be either even or odd — there's no other possibility.
  > Source: Introduction to Probability.html
- **Complement on a die (lecture version):** P({3, 4, 5, 6}) = 4/6 = 1 − 2/6 = 1 − P({1, 2}).
  > Source: Probability - Copy.pdf
- **Security system:** A security system correctly blocks a malicious login attempt 97% of the time; the probability that a malicious attempt slips through is the complement of that.
  > Source: Introduction to Probability.html

## The Birthday Problem

The Birthday Problem is one of the most surprising results in probability and a classic demonstration of why complements are so useful. The question: **how big would a group of people have to be for the probability that at least two people share a birthday** to exceed 50%? Most people guess you'd need a huge group, maybe 100 people. In reality, you only need **23 people**.
> Source: Introduction to Probability.html

### Step 1 — Define the Event and Its Complement

Let event 𝐴 = "at least two people share a birthday." Its complement 𝐴ᶜ = "no two people share a birthday." It's almost impossible to count all the ways people can share birthdays, but it's easy to count the ways they don't. So we find 𝑃(𝐴ᶜ) first and then use the complement rule: **𝑃(𝐴) = 1 − 𝑃(𝐴ᶜ)**.
> Source: Introduction to Probability.html

### Step 2 — Use the Multiplication Rule

Assume 365 possible birthdays (ignoring leap years), each equally likely. If there's 1 person, their birthday can be any of 365 days. If there are 2 people, the first can have any birthday and the second must have a different one. That logic continues as each new person joins:

**P(𝐴ᶜ) = (365/365) × (364/365) × … × ((365 − n + 1)/365)**, where 𝑛 is the number of people.

Each term represents the probability that a new person's birthday doesn't match any previous one. This applies the multiplication rule for **dependent** events: each person's probability depends on how many unique birthdays remain.
> Source: Introduction to Probability.html

### Step 3 — Compute for 23 People

For 𝑛 = 23: P(𝐴ᶜ) = (365/365) × (364/365) × (363/365) × … × (343/365) ≈ 0.493.

Then 𝑃(𝐴) = 1 − 0.493 = **0.507**. With just 23 people, there's about a 50.7% chance that two share a birthday.
> Source: Introduction to Probability.html

### Why the Complement Matters Here

Calculating "at least two share a birthday" directly would mean adding probabilities for one match, two matches, three matches, and so on — nearly impossible by hand. But the complement, "no shared birthdays," follows a simple pattern of sequential restrictions. This example highlights why complement reasoning is so powerful: it often turns a messy counting problem into one clean calculation.
> Source: Introduction to Probability.html

## Common Misconceptions

- **"You'd need about 100 people for a shared birthday to be likely."** In a small group, shared birthdays are already more likely than not — 23 people is enough to pass 50%. That's the counter-intuitive part.
  > Source: Introduction to Probability.html

## Related Topics

- [Introduction to Probability](introduction-to-probability.md)
- [Addition and Multiplication Rules](addition-and-multiplication-rules.md)
