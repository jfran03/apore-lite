# Proof by Contrapositive

## Definition
In many proofs, it's easier to show that the contrapositive of a statement is true rather than proving the statement directly. When you prove the contrapositive of an implication, you're showing the same logical truth, just from a different direction. The original statement and its contrapositive are logically equivalent, which means that if one is true, the other must also be true.
> Source: Proof by Contrapositive.html

## Key Concepts

- **Related Forms of a Conditional Statement (p ⇒ q):** Given "If p, then q":
  | Form | Description | Symbolic Form | Example (if it rains, the ground is wet) |
  |------|-------------|----------------|---------------------------------------------|
  | Original | The starting statement | p ⇒ q | If it rains, the ground gets wet. |
  | Converse | Switch p and q | q ⇒ p | If the ground gets wet, it rains. |
  | Inverse | Negate both p and q | ¬p ⇒ ¬q | If it doesn't rain, the ground doesn't get wet. |
  | Contrapositive | Switch and negate p and q | ¬q ⇒ ¬p | If the ground isn't wet, it didn't rain. |
  Among these, the original statement and its contrapositive always have the same truth value. When the direct path "p ⇒ q" is complicated or abstract, proving the contrapositive can simplify your reasoning.
  > Source: Proof by Contrapositive.html

- **Steps for a Proof by Contrapositive:**
  1. Rewrite the original statement as its contrapositive — identify the hypothesis (p) and conclusion (q), then write p ⇒ q as ¬q ⇒ ¬p.
  2. Work through the contrapositive logically — start by assuming the negation of the conclusion (¬q), and use definitions, algebraic manipulation or known theorems to reason step-by-step toward the negation of the hypothesis (¬p), being explicit about each step.
  3. Conclude that the original statement is true because its contrapositive is true — because a statement and its contrapositive are logically equivalent, once you've proven ¬q ⇒ ¬p, you've automatically proven p ⇒ q.
  > Source: Proof by Contrapositive.html

- **Key Insight:** A proof by contrapositive is not a new kind of logic — it's a reframing that makes complex proofs more accessible. Sometimes, turning a statement "inside out" is the most direct route to understanding why it's true. It is especially useful when starting with the original assumption (p) is complicated or abstract, or when the negation of the conclusion (¬q) gives you something easier to analyze.
  > Source: Proof by Contrapositive.html

## Examples

- **If n² is even, then n is even:** Contrapositive: If n is not even (n is odd), then n² is not even (n² is odd). Proof: Assume n is odd. Then n = 2k + 1 for some integer k. n² = (2k+1)² = 4k² + 4k + 1 = 4(k² + k) + 1. This is one more than a multiple of 2, which means n² is odd. Since n² is odd whenever n is odd, the contrapositive holds. Therefore, the original statement "If n² is even, then n is even" is true. ∎
  > Source: Proof by Contrapositive.html

- **If |x| + |y| ≠ |x + y|, then xy < 0:** Contrapositive: If xy > 0 [i.e., xy ≥ 0], then |x| + |y| = |x + y|. Proof: Assume xy ≥ 0. This means x and y have the same sign: either both nonnegative or both nonpositive.
  - Case 1: x ≥ 0 and y ≥ 0. Then |x| + |y| = x + y by the definition of absolute value. Also, |x + y| = x + y, because x ≥ 0 and y ≥ 0 implies x + y ≥ 0. So |x| + |y| = |x + y|.
  - Case 2: x ≤ 0 and y ≤ 0. Then |x| + |y| = (−x) + (−y), again by the definition of absolute value. And |x + y| = −(x + y) = (−x) + (−y), because x ≤ 0 and y ≤ 0 implies x + y ≤ 0. Therefore |x| + |y| = |x + y|.
  Therefore, when xy ≥ 0, |x| + |y| = |x + y|. By contraposition, we conclude that if |x| + |y| ≠ |x + y|, then xy < 0. ∎
  > Source: Proof by Contrapositive.html

## Common Misconceptions

- In Example 1, "odd" numbers have a clear algebraic form that makes the pattern obvious; in Example 2, reasoning about the same sign of x and y is much simpler than handling all possible absolute value combinations directly — both examples start by flipping and negating the statement, allowing the proof to rely on simpler reasoning.
  > Source: Proof by Contrapositive.html

## Practice Problems

**Prove by contrapositive:**
1. If n is an integer such that 3n + 2 is odd, then n is odd.
2. If n² is an even integer then n is an even integer.
3. If x and y are both integers, such that xy is even and x + y is even, then both x and y are even.
4. Let r be a number. If 5r is not rational then r is not rational.
5. If p is a prime number greater than 2, then p² is odd.
  > Source: 15.PNG

## Related Topics
- [Introduction to Proofs](introduction-to-proofs.md)
- [Direct Proofs](direct-proofs.md)
- [Proof by Contradiction](proof-by-contradiction.md)
- [Comparing Proof Techniques](comparing-proof-techniques.md)
