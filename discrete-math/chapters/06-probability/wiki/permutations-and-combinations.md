# Permutations and Combinations

> **Main concept:** Counting Principles

## Definition

Counting principles help you determine how many ways events can occur before applying probability. When problems involve large sets of possibilities — passwords, seating charts, datasets or random keys — it's rarely practical to list every possible outcome, so mathematics offers systematic ways to count outcomes without writing them all out. Most probability problems start with counting.
> Source: Permutations and Combinations.html

- A **permutation** is an arrangement of objects in a specific order — if you change the order, you've created a new permutation.
  > Source: Permutations and Combinations.html
- A **combination** is a selection of items from a larger group where order is irrelevant. Whether you choose A then B or B then A, the result is the same combination.
  > Source: Permutations and Combinations.html

## Key Concepts

### The Fundamental Counting Rule

Think of the counting rule as the blueprint for structured choice. When a process happens in stages, the total number of possible outcomes is the product of the choices at each stage:

**Total outcomes = n₁ × n₂ × n₃ × … × n_k**

Every choice at one step branches into all the choices at the next step, just like a tree expanding from a trunk. Each branch multiplies the number of possible outcomes.
> Source: Permutations and Combinations.html

The lecture notes give the same as the **general counting rule** n = n₁ × n₂ × … × n_k, where n = total outcomes and nᵢ = number of elements in choice i, for i = 1,…,k.
> Source: Combinatorics useful tips.pdf

### Factorials

The factorial of a number 𝑛, written 𝑛!, means the product of all positive integers from 1 up to 𝑛:

**𝑛! = 𝑛 × (𝑛−1) × (𝑛−2) × … × 3 × 2 × 1**

By definition, **0! = 1**. Factorials grow extremely quickly, which is a key reason large-scale combinatorial problems are so computationally expensive.
> Source: Permutations and Combinations.html

### The Permutation Formula

A permutation answers: *how many different ways can we arrange 𝑟 objects selected from a total of 𝑛 objects?* Written 𝑃(𝑛,𝑟) or ₙP_r:

**P(n, r) = n! / (n − r)!**

where 𝑛 is the total number of available items and 𝑟 is the number you're arranging. The denominator removes the part of 𝑛! you don't use.
> Source: Permutations and Combinations.html

### Permutations with Identical Items

If some items are the same, the total number of distinct permutations decreases, because swapping identical items doesn't create a new arrangement. When items repeat, we divide by the number of ways those identical elements could be rearranged among themselves:

**Number of unique permutations = n! / (n₁! × n₂! × n₃! × …)**

where 𝑛 = total number of items and 𝑛₁, 𝑛₂, 𝑛₃, … = counts of each group of identical items.
> Source: Permutations and Combinations.html

### The Combination Formula

The formula for combinations looks similar to permutations, but includes a division by 𝑟! to remove order-based duplicates:

**C(n, r) = ₙC_r = n! / [ r!(n − r)! ]**

The 𝑟! in the denominator corrects for all the ways you could rearrange the same group, because all those orders represent the *same selection*.
> Source: Permutations and Combinations.html

### The Five Counting Cases

The lecture notes lay out five standard cases:

- **Case 1 — choosing from n distinct objects r times *with* repetition:** n × n × … × n = **nʳ**
  > Source: Combinatorics useful tips.pdf
- **Case 2 — permuting n distinct objects (no repetitions):** n(n−1)…1 = **n!**
  > Source: Combinatorics useful tips.pdf
- **Case 3 — choosing *and* permuting r objects from n distinct objects (no repetition):** n(n−1)…(n−(r−1)) = **n! / (n−r)!** =: ₙP_r
  > Source: Combinatorics useful tips.pdf
- **Case 4 — choosing r objects from n distinct objects (no repetition, no permutation):** ₙP_r / r! = **n! / [r!(n−r)!]** =: ₙC_r (or (ⁿ_r))
  > Source: Combinatorics useful tips.pdf
- **Case 5 — partitioning n distinct objects into k partitions of sizes n₁, n₂, …, n_k** (so n₁ + n₂ + … + n_k = n, with all nᵢ > 0): **n! / (n₁! n₂! … n_k!)**. Note that ₙC_r is a partition into k = 2 partitions of size r and n−r.
  > Source: Combinatorics useful tips.pdf

### Permutation vs. Combination — Quick Comparison

| Feature | Permutation | Combination |
|---|---|---|
| Order | Matters | Doesn't Matter |
| Formula | n! / (n−r)! | n! / [r!(n−r)!] |
| Example | Ranking 3 candidates (Gold, Silver, Bronze) | Selecting 3 team members |
| 10 items, 3 chosen | ₁₀P₃ = 720 | ₁₀C₃ = 120 |
> Source: Permutations and Combinations.html

You can always tell which to use by asking: **would swapping two items create a different outcome?** If yes → permutation. If no → combination.
> Source: Permutations and Combinations.html

## Examples

### Fundamental Counting Rule

- **Passwords:** A password has five characters, each any of 92 printable keyboard symbols. 92⁵ = 6.56 × 10⁹. Each extra character multiplies the space by 92 — a 6-character password has 92⁶ possibilities, over 600 billion. This exponential growth explains why long, random passwords are dramatically stronger than short ones.
  > Source: Permutations and Combinations.html
- **Generating test data:** 3 input file types (.csv, .json, .xml) × 4 user roles (guest, user, admin, superuser) × 2 environments (Windows, Linux) = **24** unique input combinations to test.
  > Source: Permutations and Combinations.html
- **Test configurations:** A software test suite runs across 4 browsers, 3 user roles and 2 operating systems: 4 × 3 × 2 = **24** total test configurations. Each test dimension multiplies the total possibilities.
  > Source: Permutations and Combinations.html/practice/config-1763407986891.practice.json

### Simple Orderings and Factorials

- Arranging three symbols A, B, C gives ABC, ACB, BAC, BCA, CAB, CBA — **6** arrangements.
  > Source: Permutations and Combinations.html
- Arranging four symbols A, B, C, D gives **24** distinct orderings; five items gives **120**.
  > Source: Permutations and Combinations.html
- 4! = 4 × 3 × 2 × 1 = 24; 5! = 120; 6! = 720.
  > Source: Permutations and Combinations.html

### Permutations

- **Simple ordering:** From three symbols A, B, C, how many 2-symbol codes if order matters? AB, AC, BA, BC, CA, CB → 6. By formula: P(3,2) = 3!/(3−2)! = 3 × 2 = **6**.
  > Source: Permutations and Combinations.html
- **Race medals:** Eight runners; how many ways can gold, silver and bronze be awarded (no ties)? P(8,3) = 8!/(8−5)!… = 8!/5! = **336**. Change the order of any two runners and you've created a new permutation.
  > Source: Permutations and Combinations.html
- **Arranging letters:** "WATER" has 5 distinct letters, so P(5,5) = 5!/0! = **120** possible arrangements.
  > Source: Permutations and Combinations.html
- **4-digit PINs, no repeats:** 10 × 9 × 8 × 7 = **5,040** possible PINs. Each new position has one fewer option.
  > Source: Permutations and Combinations.html/practice/config-1763408059103.practice.json

### Permutations with Repeated Items

- **BALLOON:** 7 letters total; if all were unique there'd be 7! = 5,040 arrangements. Because the two L's and two O's are identical, unique arrangements = 7!/(2! × 2!) = 5,040/4 = **1,260**.
  > Source: Permutations and Combinations.html
- **Repeated digits (1123):** 4 digits total with 2 identical 1s → 4!/2! = 24/2 = **12**. Even though there are four digits, the repetition cuts the total number of unique codes in half.
  > Source: Permutations and Combinations.html
- **SUCCESS:** 7 letters with 3 S's and 2 C's → 7!/(3! × 2!) = 5,040/12 = **420** distinct arrangements, far fewer than the 5,040 you'd have if every letter were different.
  > Source: Permutations and Combinations.html

### Combinations

- **From order to selection:** Selecting 2 fruits from apple, banana, cherry — if order matters there are 6 arrangements (AB, AC, BA, BC, CA, CB), but in combinations AB and BA are the same choice, so only AB, AC, BC → **3** combinations.
  > Source: Permutations and Combinations.html
- **Choosing a committee:** 8 candidates, choose 3 for a planning committee. ₈C₃ = 8!/[3! × (8−3)!] = (8 × 7 × 6)/(3 × 2 × 1) = **56** possible committees.
  > Source: Permutations and Combinations.html
- **Lottery numbers:** Choose 5 numbers from 1 to 35, order doesn't matter. ₃₅C₅ = 35!/[5! × 30!] = **324,632** unique combinations. One ticket gives a 1-in-324,632 chance of winning. That's why lotteries feel "unfair" — the number of possible combinations grows astronomically as 𝑛 increases.
  > Source: Permutations and Combinations.html
- **Survey design:** 3 questions from a pool of 10, order doesn't matter. ₁₀C₃ = 10!/[3! × 7!] = **120** possible sets of questions.
  > Source: Permutations and Combinations.html
- **Data sampling:** 100 data records, how many unique 5-record samples? ₁₀₀C₅ = 100!/[5! × 95!] = **75,287,520** — over 75 million possible samples for just five records out of 100. Even small datasets contain an enormous number of potential subsets, which is why data scientists rely on randomised algorithms and sampling methods rather than testing every possible combination directly.
  > Source: Permutations and Combinations.html
- **Cybersecurity audit teams:** 12 analysts, select 3 for a special audit. C(12,3) = **220** unique teams.
  > Source: Permutations and Combinations.html/practice/config-1763408135740.practice.json

## Worksheet Problems

These problems are posed in the worksheet screenshot without solutions. The workings below apply the counting rules stated above. (The source numbers two separate items as "6"; they are distinguished here by name.)

### Home Alarm Codes — Repetition vs. No Repetition

A home alarm code consists of four digits, each 0 through 9, entered in the correct order. How many codes are possible if:

- **(a) Each digit can be repeated.** This is Case 1 — choosing from n distinct objects r times *with* repetition: nʳ = 10⁴ = **10,000** codes.
- **(b) No digit can be repeated.** Each position has one fewer option than the last: 10 × 9 × 8 × 7 = **5,040** codes. By the permutation formula, P(10,4) = 10!/(10−4)! = 10!/6! = 5,040.

Barring repetition cuts the code space roughly in half, which is why the "no repeated digits" habit weakens a PIN rather than strengthening it.
> Source: Capture11.PNG (problem as posed); Case 1 from Combinatorics useful tips.pdf; permutation formula from Permutations and Combinations.html

### Evaluate 6!

6! = 6 × 5 × 4 × 3 × 2 × 1 = **720**.
> Source: Capture11.PNG (problem as posed); factorial value stated in Permutations and Combinations.html

### Jumble — TAISER

How many ways can the letters T A I S E R be arranged? All six letters are distinct, so this is Case 2 — permuting n distinct objects: 6! = **720** arrangements.
> Source: Capture11.PNG (problem as posed); Case 2 from Combinatorics useful tips.pdf

### Jumble — TTIRRROGHE

Find the number of arrangements of the letters T T I R R R O G H E. There are 10 letters in total, but they are not all distinct: **T** appears twice and **R** appears three times (I, O, G, H, E appear once each). Using the formula for permutations with identical items:

**n! / (n₁! × n₂! × …) = 10! / (2! × 3!) = 3,628,800 / 12 = 302,400** arrangements.

Dividing by 2! and 3! removes the rearrangements of the identical T's and R's among themselves, which do not produce new visible words.
> Source: Capture11.PNG (problem as posed); repeated-items formula from Permutations and Combinations.html

### Lottery — Order Matters vs. Order Doesn't

In a lottery you select six numbers from 1 to 42.

- **Winning requires the correct order.** Order matters and there is no repetition, so this is a permutation — Case 3: ₄₂P₆ = 42!/(42−6)! = 42 × 41 × 40 × 39 × 38 × 37 = 3,776,965,920. Exactly one arrangement wins, so **P(win) = 1/3,776,965,920**.
- **Winning requires the right six numbers regardless of order.** Order no longer matters, so this is a combination — Case 4: ₄₂C₆ = ₄₂P₆ / 6! = 3,776,965,920 / 720 = 5,245,786. So **P(win) = 1/5,245,786**.

Dropping the order requirement improves the odds by a factor of exactly 6! = 720, because each winning set of six numbers can be drawn in 720 different orders. This is the clearest illustration of the r! in the combination formula: it collapses all the orderings of the same selection into one.
> Source: Capture11.PNG (problem as posed); Cases 3 and 4 from Combinatorics useful tips.pdf; combination formula from Permutations and Combinations.html

### Pitt Software — Was the Selection Random?

The Pitt Software Company reduced its sales staff from 32 employees to 28, claiming the four terminated employees were randomly selected. However, the four chosen were the four oldest among the original 32. Find the probability that this selection was random.

Order does not matter in choosing a group of four to terminate, so the number of possible groups is a combination:

**₃₂C₄ = 32! / [4!(32−4)!] = (32 × 31 × 30 × 29) / (4 × 3 × 2 × 1) = 863,040 / 24 = 35,960**

Exactly one of those 35,960 groups consists of the four oldest employees, so **P = 1/35,960 ≈ 0.0000278**.

A probability this small means that if the selection really were random, this outcome would almost never occur — which is evidence against the company's claim.
> Source: Capture11.PNG (problem as posed); combination formula from Permutations and Combinations.html; Case 4 from Combinatorics useful tips.pdf

## Common Misconceptions

- **"Independent choices should be added."** For the 4 browsers × 3 roles × 2 operating systems problem, these are independent choices, not alternatives — multiply them, don't add them.
  > Source: Permutations and Combinations.html/practice/config-1763407986891.practice.json
- **Forgetting to divide out repeated letters.** Treating TTIRRROGHE as ten distinct letters gives 10! = 3,628,800, twelve times too many. Identical letters must be divided out by 2! × 3!.
  > Source: Capture11.PNG; Permutations and Combinations.html
- **Using permutations when order doesn't matter.** If the same three people form one team no matter who's picked first, use combinations, not permutations.
  > Source: Permutations and Combinations.html/practice/config-1763408135740.practice.json

## Related Topics

- [Addition and Multiplication Rules](addition-and-multiplication-rules.md)
- [Introduction to Probability](introduction-to-probability.md)
- [The Binomial Distribution](binomial-distribution.md)
