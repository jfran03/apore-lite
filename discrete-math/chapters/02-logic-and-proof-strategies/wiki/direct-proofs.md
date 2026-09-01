# Direct Proofs

## Definition
A direct proof of a conditional statement p → q is constructed by assuming that p (the hypothesis) is true, applying logical reasoning, definitions and previously known results, and concluding that q (the conclusion) must also be true. We begin at what we know and move forward logically until we reach what we want to prove. This method leaves no gaps, ensuring that the case "p true and q false" never occurs.
> Source: Direct Proofs.html

## Key Concepts

- **General Structure of a Direct Proof:**
  1. Start with what's given — restate the assumption (p) clearly and precisely, and translate it into a usable form (definitions, known properties or symbolic logic).
  2. Apply logical steps — use previously proven results, definitions, or algebraic manipulation to move toward the conclusion, justifying each step.
  3. Arrive at what you want to show (q) — rewrite the target conclusion if needed and connect it back to the reasoning.
  4. Conclude with clarity — finish with a short sentence confirming that the conclusion follows directly from the assumption, often ending with the proof symbol (∎).
  > Source: Direct Proofs.html

- **Even and Odd Definitions:** An integer n is even if there exists an integer k such that n = 2k. An integer n is odd if there exists an integer k such that n = 2k + 1. Every integer is either even or odd, but never both. Even 0 is an even integer, because it can be written as 2 × 0 = 0.
  > Source: Direct Proofs.html

## Examples

- **Direct Proof in Logic:** Theorem: If p and q are true, then p ∧ q is true. Proof: Assume p and q are both true. By the definition of conjunction, p ∧ q is true exactly when both components are true. Therefore, p ∧ q is true. ∎
  > Source: Direct Proofs.html

- **Direct Proof in Sets:** Theorem: If A ⊆ B and B ⊆ C, then A ⊆ C. Proof: Assume x ∈ A. Since A ⊆ B, x ∈ B. Since B ⊆ C, x ∈ C. Thus, every element of A is in C, so A ⊆ C. ∎
  > Source: Direct Proofs.html

- **Direct Proof in Real-World Reasoning:** Theorem: If a file is encrypted and stored on a secure server, then it is not publicly accessible. Proof: Assume the file is encrypted and stored on a secure server. By definition, a secure server restricts public access, and encryption ensures the contents cannot be read without authorization. Therefore, the file is not publicly accessible. ∎
  > Source: Direct Proofs.html

- **The Sum of Two Even Numbers Is Even:** Theorem: If two numbers are even, then their sum is even. Proof: Let the two even numbers be 2a and 2b, where a and b are integers. Their sum is 2a + 2b = 2(a + b). Since a+b is an integer, the sum can be expressed as 2k for some integer k = a+b. Therefore, the sum of two even numbers is even. ∎
  > Source: Direct Proofs.html

- **The Product of Two Odd Numbers Is Odd:** Theorem: If two numbers are odd, then their product is odd. Proof: Let the two odd numbers be 2a+1 and 2b+1, where a and b are integers. Their product is (2a+1)(2b+1) = 4ab + 2a + 2b + 1 = 2(2ab + a + b) + 1. Since 2ab+a+b is an integer, the product is of the form 2k+1, which is odd. ∎
  > Source: Direct Proofs.html

- **The Sum of Two Consecutive Integers Is Odd:** Theorem: The sum of two consecutive integers is always odd. Proof: Let the two consecutive integers be n and n+1. Then n + (n+1) = 2n + 1. Since 2n+1 has the form 2k+1 for integer k=n, the sum is odd. ∎
  > Source: Direct Proofs.html

## Practice Problems

**Prove directly:**
1. If n is an even integer then 7n + 4 is an even integer.
2. If n is an even integer then n² is an even integer.
3. If n is an even integer then 5n + 3n³ is even.
4. If m is an even integer and n is an odd integer then m + n is an odd integer.
5. If m is an even integer and n is an odd integer then mn is an even integer.
6. The sum of two consecutive integers is odd.
7. If a, b and c are integers such that a | b and a | c then a | b + c.
8. If a, b and c are integers such that a | b and b | c then a | c.
9. The sum of two rational numbers is rational.
10. If p is a prime number greater than 2, then p² is odd.
  > Source: 13.PNG

## Related Topics
- [Introduction to Proofs](introduction-to-proofs.md)
- [Proof by Cases](proof-by-cases.md)
- [Proof by Contrapositive](proof-by-contrapositive.md)
- [Comparing Proof Techniques](comparing-proof-techniques.md)
