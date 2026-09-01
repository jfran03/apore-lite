# Mathematical Induction

## Definition
To prove a statement P(n) is true for all integers n ≥ k, we use mathematical induction: (1) Base Case — show P(k) is true; (2) Inductive Step — assume P(n) is true for some arbitrary integer n (the inductive hypothesis), and prove P(n+1) is true. If both steps hold, we conclude that P(n) is true for all n ≥ k. ∎
> Source: Introduction to Induction.html

## Key Concepts

- **The Big Idea:** Mathematical induction is like dominoes falling or climbing a ladder. If you can knock over the first domino (show the statement is true for the first case), and show that each domino knocks over the next (if it's true for one case, it must be true for the next), then all the dominoes fall, meaning the statement is true for every integer that follows.
  > Source: Introduction to Induction.html

- **The Ladder Analogy:** Think of induction like climbing an infinite ladder. The first rung represents the base case — you show you can step onto it (the statement works for the first number). The rule for moving up is the inductive step — you show that if you can stand on one rung, you can climb to the next. Once both are true, you can reach any rung on the ladder by stepping up one at a time. If the first step holds, and each step leads to the next, then every step can be reached.
  > Source: Introduction to Induction.html

- **Chain of Implications:** Induction relies on a simple chain of logical implications: P(k) ⇒ P(k+1) ⇒ P(k+2) ⇒ ... By proving the first case and the link between each case, you create an infinite chain of truth.
  > Source: Introduction to Induction.html

- **Why It Matters in Computer Science:** This reasoning underlies many ideas in computer science including recursive algorithms, loop invariants and proofs about program correctness.
  > Source: Introduction to Induction.html

## Examples

- **Sum of the First n Positive Integers:** Statement: 1 + 2 + 3 + ... + n = n(n+1)/2.
  - Base case: For n = 1, the sum is 1·(1+1)/2 = 1.
  - Inductive step: If the formula holds for n, then it also holds for n+1.
  If both are true, the statement holds for all positive integers, forever.
  > Source: Introduction to Induction.html

## Common Misconceptions

- The base case is essential — without verifying the first case, the chain of implications P(k) ⇒ P(k+1) ⇒ ... has nothing to start from, even if the inductive step is valid.
  > Source: Introduction to Induction.html

## Practice Problems

**Prove by induction:** (If the range is not specified, first identify the range where the relation is false, exclude those values and begin the induction in the remaining set.)
1. 2ⁿ > n + 4.
2. 1 + ... + n = n(n+1)/2 for all natural numbers.
3. 6ⁿ − 1 is divisible by 5.
4. The set of all n-bit strings has exactly 2ⁿ elements.
5. The power set of a set with n elements has 2ⁿ elements.
6. Every positive integer is a product of prime numbers.
7. For all natural numbers n: 1/2! + 2/3! + 3/4! + ... + n/(n+1)! = 1 − 1/(n+1)!.
  > Source: 17.PNG

**Prove the following using induction:** For all integers n ≥ 1, 5ⁿ − 3ⁿ is even.
  > Source: 20.PNG

## Related Topics
- [Strong Induction](strong-induction.md)
- [The Well-Ordering Principle](well-ordering-principle.md)
- [Comparing Proof Techniques](comparing-proof-techniques.md)
