# Strong Induction

## Definition
Strong induction is a variation of mathematical induction that allows us to use all previous cases up to k to prove the next case k+1. To prove a statement P(n) is true for all positive integers n, we complete two steps: Basis Step — verify that P(1) (or the first relevant case) is true; Inductive Step — assume P(1), P(2), ..., P(k) are all true for some k ≥ 1, and under this assumption show that P(k+1) is also true. Symbolically, the inductive step has the form [P(1) ∧ P(2) ∧ ... ∧ P(k)] → P(k+1). If both steps hold, then P(n) is true for all n ≥ 1.
> Source: Strong Induction.html

## Key Concepts

- **How It Differs from Regular Induction:** Regular induction assumes just one prior case P(k). Strong induction assumes all prior cases P(1), P(2), ..., P(k). This extra information can make it possible to prove statements that depend on multiple previous values, such as prime factorizations, recurrence relations, and tiling, counting or algorithm problems.
  > Source: Strong Induction.html

- **Alternate Names:** Strong induction is sometimes called the Second Principle of Mathematical Induction or Complete Induction. The term "complete" doesn't mean that ordinary induction is "incomplete" — both methods are logically equivalent. The difference is simply how much we assume in the inductive step.
  > Source: Strong Induction.html

- **Staircase Analogy:** In ordinary induction, each step only depends on the previous one. In strong induction, each step can depend on any or all earlier steps. So even if P(k+1) depends on P(k−1), P(k−2), or P(2), we're covered, because we assume they're all true.
  > Source: Strong Induction.html

## Examples

- **Every integer greater than 1 can be written as a product of primes:** A prime number is an integer greater than 1 whose only factors are 1 and itself.
  - Define P(n): "n can be written as a product of primes."
  - Basis step: For n = 2, 2 is prime, so it can be written as the product of one prime (itself). P(2) is true.
  - Inductive hypothesis: Assume P(j) is true for all integers j with 2 ≤ j ≤ k — every integer between 2 and k can be written as a product of primes.
  - Inductive step: Show P(k+1) is true. There are two cases:
    - Case 1: k+1 is prime. Then k+1 can be written as a product of one prime, itself.
    - Case 2: k+1 is composite. Then k+1 = a · b where both a and b are greater than 1 and smaller than k+1. By the inductive hypothesis, a and b can each be written as products of primes: a = p₁ × p₂ × ... × pₘ and b = q₁ × q₂ × ... × qₙ. Then k+1 = a · b = (p₁ × ... × pₘ) · (q₁ × ... × qₙ), which is also a product of primes.
  - Conclusion: By strong induction, every integer n > 1 can be written as a product of primes. ∎
  > Source: Strong Induction.html

- **3ⁿ − 1 is divisible by 2 for all n ≥ 1:**
  - Define P(n): "3ⁿ − 1 is divisible by 2."
  - Basis step: For n = 1, 3¹ − 1 = 2, which is divisible by 2. P(1) is true.
  - Inductive hypothesis: Assume P(j) is true for all integers j with 1 ≤ j ≤ k — 3ʲ − 1 is divisible by 2 for all such j.
  - Inductive step: Show P(k+1) is true, i.e., 3^(k+1) − 1 is divisible by 2. 3^(k+1) − 1 = 3 · 3ᵏ − 1 = 3 · 3ᵏ − 1 + 3 − 3 = 3 · 3ᵏ − 3 + 3 − 1 = 3 · 3ᵏ − 3 + 2 = 3(3ᵏ − 1) + 2. By the inductive hypothesis, 3ᵏ − 1 is divisible by 2, so 3(3ᵏ − 1) is also divisible by 2, and 2 is obviously divisible by 2. Adding these gives a number divisible by 2.
  - Conclusion: By strong induction, 3ⁿ − 1 is divisible by 2 for all n ≥ 1. ∎
  > Source: Strong Induction.html

## Related Topics
- [Mathematical Induction](mathematical-induction.md)
- [The Well-Ordering Principle](well-ordering-principle.md)
- [Comparing Proof Techniques](comparing-proof-techniques.md)
