# Conditional Probability and Bayes' Theorem

> **Main concept:** Combining Events

## Definition

Conditional probability, written 𝑃(𝐵∣𝐴) — "the probability of B given A" — captures how dependence works, and can be rearranged from the multiplication rule as:

**P(B ∣ A) = P(A ∩ B) / P(A)**
> Source: Addition and Multiplication Rules.html

Conditional probability gives you a way to update your understanding once new information is introduced.
> Source: Addition and Multiplication Rules.html

## Key Concepts

### Joint, Marginal and Conditional Probabilities

The lecture notes organise a two-stage experiment into three kinds of probability:

- **Joint** probabilities — the probability of a combined outcome, e.g. P(1H).
- **Marginal** probabilities — the probability of one component outcome on its own, e.g. P(1) or P(H). These are found by summing the joint probabilities across a row or column.
- **Conditional** probabilities — the probability of one component given the other, e.g. P(H∣1).
> Source: Probability - Copy.pdf

The relationship among the three is: **joint = marginal × conditional**, e.g. P(1H) = P(1) · P(H∣1).
> Source: Probability - Copy.pdf

### Contingency Tables

A **contingency table** lays the joint probabilities out in a grid, with the marginal probabilities along the edges (row totals and column totals) and 1 in the corner. Marginals are obtained by summing joints: for example P({H}) = P({1H}) + P({2H}) + P({3H}) + P({4H}) + P({5H}) + P({6H}).
> Source: Probability - Copy.pdf

### Testing for Independence

Independence can be checked by comparing the joint probability against the product of the marginals:

**|P(1H) − P(1)P(H)| = 0 → independence; ≠ 0 → dependence.**

This quantity could be a measure for dependence/correlation.
> Source: Probability - Copy.pdf

Equivalently, if H is independent of the outcome of the die, then **P(H∣1) = P(H∣1̄) = P(H)**.
> Source: Probability - Copy.pdf

Note also that P(1)P(H) ≠ P(1H) in the dependent case, while P(1H) can always be written either as P(1)P(H∣1) or as P(H)P(1∣H).
> Source: Probability - Copy.pdf

### Bayes' Theorem

Bayes' Theorem uses one side of the tree to get to the joint probabilities and then determines the conditionals on the other side. This way, the conditional on one side is calculated by the conditional on the other side.
> Source: Probability - Copy.pdf

For the four-sided die and coin example, the theorem is written in two forms:

**P(2∣T) = P(2T) / P(T)**

and in more detail:

**P(2∣T) = P(T∣2)·P(2) / [ P(T∣1)P(1) + P(T∣2)P(2) + P(T∣3)P(3) + P(T∣4)P(4) ]**

where the denominator is P(T1) + P(T2) + P(T3) + P(T4).
> Source: Probability - Copy.pdf

### Changing Order

The same joint distribution can be read in either direction. Reading the tree from the die first gives P(H∣die outcome); reading it from the coin first gives P(die outcome ∣ H). The joint table is unchanged — only which margin you condition on changes.
> Source: Probability - Copy.pdf

## Examples

### Dependent vs. Independent Setup

The worked experiment throughout the lecture notes: first throw a 4-sided die, then toss a *different* coin depending on the outcome of the die throw. To assign probabilities to the joint events, find a common multiple for the number of branches that end up in the joint-event space, then treat each branch as a symmetric event — giving **24 equally likely branches**.
> Source: Probability - Copy.pdf

The resulting joint probabilities are:

| | 1 | 2 | 3 | 4 | marginal |
|---|---|---|---|---|---|
| **H** | 1/8 | 1/6 | 1/12 | 1/4 | 5/8 |
| **T** | 1/8 | 1/12 | 1/6 | 0 | 3/8 |
| **marginal** | 1/4 | 1/4 | 1/4 | 1/4 | 1 |
> Source: Probability - Copy.pdf

From this table:

- P(H) = 1/8 + 1/6 + 1/12 + 1/4 = (3+4+2+6)/24 = 15/24 = **5/8**; P(T) = 1/8 + 1/12 + 1/6 + 0 = **3/8**.
  > Source: Probability - Copy.pdf
- P(H∣1) = P(H1)/P(1) = (1/8)/(1/4) = 4/8 = **1/2**.
  > Source: Probability - Copy.pdf
- P(T∣3) = P(T3)/P(3) = (1/6)/(1/4) = 4/6 = **2/3**.
  > Source: Probability - Copy.pdf
- P(1∣H) = P(1H)/P(H) = (1/8)/(5/8) = **1/5**.
  > Source: Probability - Copy.pdf
- P(2∣T) = P(2T)/P(T) = (1/12)/(3/8) = **2/9**.
  > Source: Probability - Copy.pdf
- P(4T) = P(4)·P(T∣4) = 1/4 × 0 = **0**.
  > Source: Probability - Copy.pdf

### Contingency Table for a Fair Coin and Fair Die

Every joint cell is 1/12; the die marginals are each 1/6, the coin marginals each 1/2, and the grand total is 1. Then 1/6 = 1/12 + 1/12 corresponds to P({1}) = P({1H}) + P({1T}).
> Source: Probability - Copy.pdf

### Conservative MPs Given Male

If we randomly select one local MP, what is the probability of getting a conservative, *given* that a male was selected?

| | Conservative | Liberal | NDP | total |
|---|---|---|---|---|
| Male | 46 | 39 | 11 | 96 |
| Female | 45 | 39 | 20 | 104 |
| total | 91 | 78 | 31 | 200 |

P(C∣M) = P(CM)/P(M) = (46/200)/(96/200) = 46/96 = 23/48 ≈ **0.479**.
> Source: Probability - Copy.pdf

### Alberta Tourists — Banff and Dinosaur

About 60% of Alberta tourists visit Banff National Park (B) while 45% visit Dinosaur National Park (D); 30% visit both. The joint table is:

| | B | B̄ | total |
|---|---|---|---|
| **D** | 0.30 | 0.15 | 0.45 |
| **D̄** | 0.30 | 0.25 | 0.55 |
| **total** | 0.60 | 0.40 | 1.00 |

- (a) P(D∣B) = P(DB)/P(B) = 0.30/0.60 = 1/2 = **0.50**
- (b) P(B∣D̄) = P(BD̄)/P(D̄) = 0.30/0.55 = 6/11 = **0.5̄4̄**
- (c) P(BD̄) = **0.30**
> Source: Probability - Copy.pdf

### Athletes, Stretching and Injuries

A study shows 75% of athletes did routine stretching exercises last year; 80% did not suffer any injuries in competitions; yet 15% did not engage in routine stretching **and** did suffer injuries. Let R = athletes who did routine exercises and I = athletes who suffered injuries.

| | I | Ī | total |
|---|---|---|---|
| **R** | 0.05 | 0.70 | 0.75 |
| **R̄** | 0.15 | 0.10 | 0.25 |
| **total** | 0.20 | 0.80 | 1.00 |

P(I∣R) = P(IR)/P(R) = 0.05/0.75 = 1/15 = **0.06̄**.
> Source: Probability - Copy.pdf

### Two Births Given at Least One Girl

Imagine someone has two children and you're told at least one of them is a girl. What's the probability the other is also a girl? At first glance you might say ½, since each child's gender is independent. But if you know at least one of the two children is a girl, then the only impossible case is both being boys. The remaining outcomes are:

| Case | Child 1 | Child 2 |
|---|---|---|
| A | Boy | Girl |
| B | Girl | Boy |
| C | Girl | Girl |

Each case is equally likely (¼ ÷ ¾ = ⅓ each). Only one of the three has two girls, so **P(both girls ∣ at least one girl) = ⅓**. The births themselves are independent — each child has a 0.5 chance of being a girl — but the information you're given filters the sample space in a different way.
> Source: Expected Value, Variance and Standard Deviation.html

## Worksheet Problems

These problems are posed in the worksheet screenshots without solutions. The workings below apply the definitions and formulas stated above.

### AJ's Commute — Bayes' Theorem

When coming to SAIT, AJ either takes the train or calls an Uber. Define T = {AJ takes the train}, U = {AJ takes an Uber}, L = {AJ is late}. Given:

- P(L∣T) = 0.15 — if he takes the train, he is late 15% of the time
- P(L∣U) = 0.65 — if he takes an Uber, he is late 65% of the time
- P(T) = 0.70 — he chooses the train 70% of the time, so P(U) = 1 − 0.70 = 0.30

Given that AJ is late one day, determine the probability that he had taken an Uber — that is, P(U∣L). This reverses the direction of the conditioning, which is exactly what Bayes' Theorem is for:

**P(U∣L) = P(L∣U)·P(U) / [ P(L∣T)P(T) + P(L∣U)P(U) ]**

The joint probabilities are P(L∩U) = 0.65 × 0.30 = 0.195 and P(L∩T) = 0.15 × 0.70 = 0.105, so the denominator P(L) = 0.105 + 0.195 = 0.300. Then:

P(U∣L) = 0.195 / 0.300 = **0.65**

Note that the answer, 0.65, coincides numerically with P(L∣U) here — but only because of the particular numbers chosen. The two are different quantities, and confusing them is the classic error.
> Source: Capture1.PNG (problem as posed); Bayes' Theorem applied from Probability - Copy.pdf

### Stretching and Injuries — Completing a Contingency Table

A survey of 800 athletes investigated the relationship between performing stretches and getting an injury. The table is given with entries missing:

| | Had Injury | No Injury | TOTALS |
|---|---|---|---|
| **Stretches** | ? | 295 | ? |
| **Doesn't Stretch** | 231 | ? | 450 |
| **TOTALS** | ? | ? | ? |

**Filling in the missing entries.** The grand total is 800. Since "Doesn't Stretch" totals 450, "Stretches" totals 800 − 450 = 350. Within the Stretches row, 350 − 295 = 55 had an injury. Within the Doesn't Stretch row, 450 − 231 = 219 had no injury. The column totals are then 55 + 231 = 286 injured and 295 + 219 = 514 uninjured, which check out: 286 + 514 = 800.

| | Had Injury | No Injury | TOTALS |
|---|---|---|---|
| **Stretches** | 55 | 295 | 350 |
| **Doesn't Stretch** | 231 | 219 | 450 |
| **TOTALS** | 286 | 514 | 800 |

- **(a) P(no injury)** — a marginal probability, read off the column total: 514/800 = **0.643**
- **(b) P(stretches)** — a marginal probability, read off the row total: 350/800 = **0.438**
- **(c) P(injury ∣ doesn't stretch)** — condition on the "Doesn't Stretch" row, so the denominator is that row's total: 231/450 ≈ **0.513**
- **(d) P(stretches ∣ no injury)** — condition on the "No Injury" column, so the denominator is that column's total: 295/514 ≈ **0.574**

Parts (c) and (d) illustrate that P(A∣B) ≠ P(B∣A): each conditions on a different total.
> Source: Capture3.PNG (problem and table as posed); conditional probability and contingency-table method applied from Probability - Copy.pdf; Addition and Multiplication Rules.html

*(This is a second, count-based version of the stretching-and-injuries scenario. The percentage-based version above, from Probability - Copy.pdf, uses different figures and is a separate problem.)*

### Cirrhosis Among Alcoholic and Non-Alcoholic Patients

A study of 210 patients found that of 75 alcoholic patients, 35 had cirrhosis of the liver, and of 135 non-alcoholic patients, 5 had cirrhosis. Laying this out as a contingency table:

| | Cirrhosis | No Cirrhosis | total |
|---|---|---|---|
| **Alcoholic** | 35 | 40 | 75 |
| **Non-alcoholic** | 5 | 130 | 135 |
| **total** | 40 | 170 | 210 |

- **(a) P(a non-alcoholic with cirrhosis)** — a joint probability, one cell over the grand total: 5/210 = 1/42 ≈ **0.024**
- **(b) P(a patient with cirrhosis)** — a marginal probability: 40/210 = 4/21 ≈ **0.190**
- **(c) P(an alcoholic with cirrhosis)** — a joint probability: 35/210 = 1/6 ≈ **0.167**

All three are read from the table directly. Note that (a) and (c) ask for **joint** probabilities ("an alcoholic *with* cirrhosis", out of all 210 patients), not conditional ones — P(cirrhosis ∣ alcoholic) would instead be 35/75 ≈ 0.467.
> Source: Capture10.PNG (problem as posed); joint/marginal/conditional distinction applied from Probability - Copy.pdf

## Common Misconceptions

- **𝑃(𝐴∣𝐵) is not the same as 𝑃(𝐵∣𝐴).** Read carefully which condition comes after the word "given."
  > Source: Addition and Multiplication Rules.html
- **Reading a joint probability as a conditional one.** "An alcoholic with cirrhosis" divides by the grand total (35/210); "cirrhosis given alcoholic" divides by the alcoholic row total (35/75). The wording determines the denominator.
  > Source: Capture10.PNG; Probability - Copy.pdf
- **"Given at least one girl, the other child is a girl with probability ½."** Independence of the two births does not carry over to the conditional question — conditioning removes only the Boy-Boy case, leaving three equally likely cases, so the answer is ⅓.
  > Source: Expected Value, Variance and Standard Deviation.html

## Related Topics

- [Addition and Multiplication Rules](addition-and-multiplication-rules.md)
- [Introduction to Probability](introduction-to-probability.md)
- [Expected Value, Variance and Standard Deviation](expected-value-variance-standard-deviation.md)
