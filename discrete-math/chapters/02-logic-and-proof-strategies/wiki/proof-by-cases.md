# Proof by Cases

## Definition
Sometimes a statement can't be proven with a single chain of reasoning: it depends on different situations that must each be considered separately. A proof by cases divides a problem into distinct, logical cases and proves the statement in each case. Once all cases are shown to be true, the entire statement is proven. A proof by cases shows that a statement (p₁ ∨ p₂ ∨ ... ∨ pₙ) → q is true by proving q under each possible case pᵢ.
> Source: Proofs by Cases.html

## Key Concepts

- **General Process:**
  1. Identify all possible cases that cover every situation.
  2. Prove that the conclusion holds in each case.
  3. Conclude that the statement is true in general.
  Once all cases are true, the entire statement is true.
  > Source: Proofs by Cases.html

- **When to Use:** This method is especially useful when a statement's truth depends on whether certain conditions hold, for example, whether a number is positive or negative, or whether a user has a certain level of access. Whenever a statement depends on conditions like "if even/odd" or "if positive/negative," it's a good sign that a proof by cases approach might be the best path forward.
  > Source: Proofs by Cases.html

## Examples

- **n² + n is even:** Theorem: For any integer n, n² + n is even. Proof: There are two possible cases for an integer n: it's either even or odd.
  - Case 1: n is even. Let n = 2k for some integer k. Then n² + n = (2k)² + 2k = 4k² + 2k = 2(2k² + k), which is even.
  - Case 2: n is odd. Let n = 2k + 1 for some integer k. Then n² + n = (2k+1)² + (2k+1) = 4k² + 6k + 2 = 2(2k² + 3k + 1), which is even.
  Since the statement holds in both cases, n² + n is even for all integers n. ∎
  > Source: Proofs by Cases.html

- **n² ≥ n:** Theorem: If n is an integer, then n² ≥ n. Proof: Consider three possible cases: n ≥ 1, n = 0, n ≤ 1.
  - Case 1: n ≥ 1. Multiplying both sides of n ≥ 1 by n (a positive number) preserves the inequality: n·n ≥ n·1 ⇒ n² ≥ n.
  - Case 2: n = 0. Then n² = 0, so n² = n and the inequality holds.
  - Case 3: n ≤ 1 (n negative). n² is positive (a negative times a negative is positive), while n itself is negative, so n² ≥ n.
  Because the inequality n² ≥ n holds in all cases, if n is an integer, then n² ≥ n. ∎
  > Source: Proofs by Cases.html

- **The product of three consecutive integers is divisible by 6:** Theorem: The product of three consecutive integers is divisible by 6. Proof: Let the integers be n, n+1 and n+2.
  - Case 1: n is divisible by 3. Then n(n+1)(n+2) includes a factor of 3. Among any three consecutive numbers, one is even, so the product is divisible by 2 and 3 → divisible by 6.
  - Case 2: n leaves remainder 1 when divided by 3. Then n+2 is divisible by 3. Again, one number is even, so the product is divisible by 6.
  - Case 3: n leaves remainder 2 when divided by 3. Then n+1 is divisible by 3, and one of the three is even.
  Since the statement holds in all three cases, the product of three consecutive integers is divisible by 6. ∎
  > Source: Proofs by Cases.html

## Related Topics
- [Introduction to Proofs](introduction-to-proofs.md)
- [Direct Proofs](direct-proofs.md)
- [Comparing Proof Techniques](comparing-proof-techniques.md)
