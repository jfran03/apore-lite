# Addition and Multiplication Rules

> **Main concept:** Combining Events

## Definition

The Addition Rule handles "or" situations (one event, the other, or both). The Multiplication Rule handles "and" situations (both events occur together). In probability, the word "or" is always **inclusive**, meaning either event could happen, or both could occur at the same time.
> Source: Addition and Multiplication Rules.html

| Rule | Use for | Formula | What It Tells You |
|---|---|---|---|
| Addition ("or") | Either event A or event B (or both) occurs | P(A∪B) = P(A) + P(B) − P(A∩B) | Adds probabilities while avoiding double-counting overlap. Simplifies to P(A)+P(B) if events are mutually exclusive. |
| Multiplication ("and") | Both event A and event B occur | P(A∩B) = P(A)×P(B) if independent, or P(A)×P(B∣A) if dependent | Multiplies probabilities to find the chance that events happen together. Adjusts for dependence using conditional probability. |
> Source: Addition and Multiplication Rules.html

## Key Concepts

### The Addition Rule

If you simply add the probabilities of two events, you may count the overlap twice — once in each event. The addition rule corrects for that double-counting:

**P(A∪B) = P(A) + P(B) − P(A∩B)**

where 𝐴 ∪ 𝐵 means "A or B or both", 𝐴 ∩ 𝐵 means "A and B" (the overlap), and subtracting 𝑃(𝐴∩𝐵) removes that double-counted overlap.
> Source: Addition and Multiplication Rules.html

### Mutually Exclusive Events

If two events cannot occur together (for example, rolling both a 2 and a 3 on the same single die), they are **mutually exclusive**, and their overlap probability is zero. In that case the rule simplifies to:

**P(A∪B) = P(A) + P(B)**
> Source: Addition and Multiplication Rules.html

The lecture notes state the same rule for **disjoint** events: P(A or B) = P(A) + P(B), and more generally P(A or B or … or Z) = P(A) + P(B) + … + P(Z). More generally, P(A or B) = P(A) + P(B) − P(overlap of A & B); when A and B are not disjoint, P(overlap) ≠ 0.
> Source: Probability - Copy.pdf

### From Set Sizes to Probabilities

Where |𝒰| = n is the size of the sample space, |A∪B| = |A| + |B| − |A∩B|. Dividing through by n gives P(A∪B) = |A∪B|/n, P(A) = |A|/n, P(B) = |B|/n, P(A∩B) = |A∩B|/n — so P(A∪B) = P(A) + P(B) − P(A∩B).
> Source: Combinatorics useful tips.pdf

### Inclusion–Exclusion for Three or More Sets

For three sets:

**|A∪B∪C| = |A| + |B| + |C| − |A∩B| − |A∩C| − |B∩C| + |A∩B∩C|**

and correspondingly

**P(A∪B∪C) = P(A) + P(B) + P(C) − P(A∩B) − P(A∩C) − P(B∩C) + P(A∩B∩C)**
> Source: Combinatorics useful tips.pdf

For four sets:

**|A∪B∪C∪D| = |A| + |B| + |C| + |D| − |A∩B| − |A∩C| − |A∩D| − |B∩C| − |B∩D| − |C∩D| + |A∩B∩C| + |A∩B∩D| + |A∩C∩D| + |B∩C∩D| − |A∩B∩C∩D|**
> Source: Combinatorics useful tips.pdf

The same pattern continues: **+** individuals, **−** pairs, **+** triples, **−** quadruples, and so on.
> Source: Combinatorics useful tips.pdf

### The Multiplication Rule

When you see the word "and" in probability, think of two conditions that must both be satisfied. Because both events must occur, these probabilities are usually smaller than for individual events. The general form is:

**P(A ∩ B) = P(A) × P(B ∣ A)**

where 𝑃(𝐴) is the probability that event A occurs and 𝑃(𝐵∣𝐴) is the probability that event B occurs *given* that A has already occurred.
> Source: Addition and Multiplication Rules.html

If the outcome of A changes the likelihood of B, the events are **dependent**. If A has no effect on B, they are **independent** and the formula simplifies.
> Source: Addition and Multiplication Rules.html

The lecture notes phrase it as: when two (or more) **independent** events happen in sequence, one after the other, the probability of the compound event is the product of the probabilities of each event in the sequence — P(A and B) = P(A) · P(B), or P(A and B and … Z) = P(A) P(B) … P(Z), assuming independence.
> Source: Probability - Copy.pdf

### Case 1 — Independent Events

Two events are independent if the outcome of one has no influence on the other. Mathematically **P(B ∣ A) = P(B)**, and the formula reduces to:

**P(A ∩ B) = P(A) × P(B)**
> Source: Addition and Multiplication Rules.html

### Case 2 — Dependent Events

Two events are dependent when the outcome of one changes the probability of the other. You see this anytime outcomes are drawn **without replacement**, or when one event filters the set of possibilities for the next. In these cases you must adjust the second probability to reflect what has already happened.
> Source: Addition and Multiplication Rules.html

### Case 3 — Conditional Probability and Dependence

The expression 𝑃(𝐵∣𝐴), "the probability of B given A," captures how dependence works. It can be rearranged as:

**P(B ∣ A) = P(A ∩ B) / P(A)**

This form is especially useful when you know the joint probability and want to find how one event depends on another.
> Source: Addition and Multiplication Rules.html

## Examples

- **Numbers divisible by 2 or 5:** Pick a random integer from 1 to 10. 𝑇 = "divisible by 2" → {2,4,6,8,10}, so P(T) = 5/10 = 0.5. 𝑅 = "divisible by 5" → {5,10}, so P(R) = 2/10 = 0.2. Only 10 is divisible by both, so P(T∩R) = 1/10 = 0.1. Then P(T∪R) = 0.5 + 0.2 − 0.1 = **0.6** — a 60 % chance the number is divisible by 2 or 5 (or both).
  > Source: Addition and Multiplication Rules.html
- **Tech vs retail (mutually exclusive):** In a class of 40, 17 want tech and 13 want retail, and no one selected both. P(Tech or Retail) = 17/40 + 13/40 = 30/40 = **0.75**.
  > Source: Addition and Multiplication Rules.html
- **Tech vs retail (overlapping):** Repeat the survey allowing both: 24 prefer tech, 19 prefer retail, 6 chose both. P(Tech or Retail) = 24/40 + 19/40 − 6/40 = 37/40 = **0.925**. When overlap is allowed the total increases, but not as much as simple addition would suggest, because we must subtract the shared portion.
  > Source: Addition and Multiplication Rules.html
- **Hearts or queens:** In a standard deck, A = "card is a heart" and B = "card is a queen". P(A) = 13/52 = 0.25, P(B) = 4/52 = 0.0769, P(A∩B) = 1/52 = 0.0192. So P(A∪B) = 0.25 + 0.0769 − 0.0192 = 0.3077 ≈ **0.308**.
  > Source: Addition and Multiplication Rules.html/practice/config-1763079267429.practice.json
- **Multiples of 2, 3 or 4 (inclusion–exclusion):** Pick a number at random from 1 to 30. With 𝒰 = {1,…,30}, |A| = ⌊30/2⌋ = 15, |B| = ⌊30/3⌋ = 10, |C| = ⌊30/4⌋ = ⌊7.5⌋ = 7. Intersections use the least common multiple: |A∩B| = ⌊30/lcm(2,3)⌋ = ⌊30/6⌋ = 5, |A∩C| = ⌊30/lcm(2,4)⌋ = ⌊30/4⌋ = 7, |B∩C| = ⌊30/lcm(3,4)⌋ = ⌊30/12⌋ = 2, |A∩B∩C| = ⌊30/lcm(2,3,4)⌋ = 2. So |A∪B∪C| = 15 + 10 + 7 − 5 − 7 − 2 + 2 = 20 and P(A∪B∪C) = 20/30 = 0.6̄. (Here ⌊x⌋ = floor(x), round down to the nearest integer.)
  > Source: Combinatorics useful tips.pdf
- **Coin and die (independent):** Event C = "coin shows heads" → 𝑃(𝐶) = 0.5; event D = "die shows a 4" → 𝑃(𝐷) = 1/6 ≈ 0.1667. These are independent, so P(C ∩ D) = 1/2 × 1/6 = 1/12 ≈ **0.0833** — about an 8.3 % chance of getting both.
  > Source: Addition and Multiplication Rules.html
- **Heads and a 5:** Flip a fair coin and roll a fair six-sided die. The coin and die are independent, so P = 0.5 × 1/6 = **0.0833**.
  > Source: Addition and Multiplication Rules.html/practice/config-1763079457118.practice.json
- **Marbles without replacement (dependent):** A jar has 3 red and 2 blue marbles (5 total). Draw one, don't put it back, draw again. A = "first is red" → P(A) = 3/5. After one red is gone, 4 marbles remain (2 red, 2 blue), so B = "second is blue given first was red" → P(B∣A) = 2/4 = 0.5. Then P(A ∩ B) = 3/5 × 1/2 = 3/10 = **0.30**. The second event's probability changes because the jar's contents change.
  > Source: Addition and Multiplication Rules.html
- **Two blue socks:** A drawer has 5 red and 3 blue socks; pull one, then a second without replacing. P(first blue) = 3/8; after removing one blue, P(second blue ∣ first blue) = 2/7. So 3/8 × 2/7 = 3/28 = **0.107**.
  > Source: Addition and Multiplication Rules.html/practice/config-1763079028892.practice.json
- **Two aces from a deck:** From a standard 52-card deck (no replacement), E = "first card is an ace" → 𝑃(𝐸) = 4/52 = 1/13; F = "second card is an ace, given the first was an ace" → 𝑃(𝐹∣𝐸) = 3/51 = 1/17. P(E ∩ F) = 1/13 × 1/17 = 1/221 ≈ **0.00452** — less than half a percent.
  > Source: Addition and Multiplication Rules.html
- **Compound events multiply too:** P({1 or 2 or 3} and {H}) = P({1 or 2 or 3}) × P({H}) = 3/6 × 1/2 = 3/12 = 1/4.
  > Source: Probability - Copy.pdf
- **Adding disjoint die faces:** P({1 or 2}) = 1/6 + 1/6 = 2/6 = 1/3. P({1 or 2 or 3}) = 3/6 = 1/2. P({1 or 2 or 3 or 4}) = 4/6 = 2/3, which also equals 2/6 + 3/6 − 1/6.
  > Source: Probability - Copy.pdf

## The Monty Hall Problem

The Monty Hall problem is a famous puzzle from the TV game show *Let's Make a Deal*. **The setup:** you're on a game show with three doors — behind one is a car (the prize), behind the other two are goats. You pick one door. The host, Monty Hall, who knows what's behind each door, opens one of the other two doors, always revealing a goat. Then he gives you a choice: **stay** with your original door, or **switch** to the remaining closed door.
> Source: Addition and Multiplication Rules.html

Most people think it doesn't matter: "two doors left, 50–50 chance." But that's wrong.
> Source: Addition and Multiplication Rules.html

- **Step 1 — Before Monty opens a door:** P(car behind chosen door) = 1/3, and P(car behind other doors) = 2/3.
  > Source: Addition and Multiplication Rules.html
- **Step 2 — After Monty opens a door:** Monty always opens a door with a goat, and this action *depends* on your first choice. He gives you information: one of the losing doors is now gone. If your first choice was the car (1/3 chance), switching makes you lose. If your first choice was a goat (2/3 chance), switching makes you win, because the only other unopened door must have the car.
  > Source: Addition and Multiplication Rules.html
- **Step 3 — Conditional reasoning:** P(win if you switch) = P(initially picked goat) = 2/3. P(win if you stay) = P(initially picked car) = 1/3. **Switching doubles your chances of winning.**
  > Source: Addition and Multiplication Rules.html

## Common Misconceptions

- **Confusing "or" with "and."** "Or" → addition rule. "And" → multiplication rule. Mixing them is the most common student error.
  > Source: Addition and Multiplication Rules.html
- **Assuming independence too quickly.** Always ask whether one event changes the sample space of the other. In "without replacement" cases, events are dependent.
  > Source: Addition and Multiplication Rules.html
- **Ignoring overlap.** When two events can both happen, subtract 𝑃(𝐴∩𝐵) once. Use a Venn diagram to visualise shared regions.
  > Source: Addition and Multiplication Rules.html
- **Switching conditional directions.** 𝑃(𝐴∣𝐵) is *not* the same as 𝑃(𝐵∣𝐴). Read carefully which condition comes after the word "given."
  > Source: Addition and Multiplication Rules.html
- **Relying on intuition.** Intuition often fails in probability, as the Monty Hall Problem shows.
  > Source: Addition and Multiplication Rules.html
- **Treating a without-replacement draw as independent.** For the two-blue-socks problem, 0.125 comes from assuming independence and 0.214 from multiplying 3/7 × 2/7 as if replacement occurred — both are wrong because the first sock is not replaced.
  > Source: Addition and Multiplication Rules.html/practice/config-1763079028892.practice.json

## Related Topics

- [Introduction to Probability](introduction-to-probability.md)
- [Complement Events and the Birthday Problem](complement-events.md)
- [Conditional Probability and Bayes' Theorem](conditional-probability-and-bayes.md)
- [Permutations and Combinations](permutations-and-combinations.md)
