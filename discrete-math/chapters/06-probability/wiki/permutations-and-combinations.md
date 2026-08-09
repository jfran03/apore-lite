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

## Common Misconceptions

- **"Independent choices should be added."** For the 4 browsers × 3 roles × 2 operating systems problem, these are independent choices, not alternatives — multiply them, don't add them.
  > Source: Permutations and Combinations.html/practice/config-1763407986891.practice.json
- **Using permutations when order doesn't matter.** If the same three people form one team no matter who's picked first, use combinations, not permutations.
  > Source: Permutations and Combinations.html/practice/config-1763408135740.practice.json

## Related Topics

- [Addition and Multiplication Rules](addition-and-multiplication-rules.md)
- [Introduction to Probability](introduction-to-probability.md)
- [The Binomial Distribution](binomial-distribution.md)
