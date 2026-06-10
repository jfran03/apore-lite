# Comparing Proof Techniques

## Definition
Each proof technique has the same goal — to show that a statement is logically valid — but they differ in how they approach that goal. Comparing the techniques side by side helps identify which tool fits which problem.
> Source: Comparing Proof Techniques.html

## Key Concepts

- **Summary Table of Proof Techniques:**

  | Proof Type | Main Idea | When to Use It | Example or Connection |
  |---|---|---|---|
  | Direct Proof | Start from known facts or assumptions and use logical steps to reach the conclusion. | When the statement naturally flows from definitions and known properties. | Proving that the sum of two even numbers is even. |
  | Proof by Case | Divide the problem into separate logical possibilities (cases) and prove each one. | When a statement depends on specific conditions (e.g., even/odd, positive/negative). | Showing n² + n is even by considering whether n is even or odd. |
  | Proof by Contrapositive | Instead of proving "If p, then q," prove the logically equivalent "If not q, then not p." | When the direct proof feels awkward or requires working with negations. | Proving "If n² is even, then n is even." |
  | Proof by Contradiction | Assume the opposite of what you want to prove and show that it leads to an impossible situation. | When direct reasoning fails or when the claim itself involves a "not" statement. | Proving √2 is irrational by assuming it's rational. |
  | Proof by Counterexample | To disprove a universal claim, find one example that makes it false. | When the statement says "for all..." but you suspect it's not true for every case. | Showing that the sum of two irrational numbers is not always irrational: π + (−π) = 0. |
  | Mathematical Induction | Prove the base case, assume P(k) is true, then show P(k+1) follows. | When the statement involves natural numbers or recursive patterns. | Proving 1 + 2 + ... + n = n(n+1)/2. |
  | Strong Induction | Assume all prior cases P(1), P(2), ..., P(k) are true to prove P(k+1). | When each case depends on several earlier cases (not just the previous one). | Proving every integer greater than 1 can be factored into primes. |
  | Well-Ordering Principle | Every non-empty set of non-negative integers has a smallest element. | When reasoning about "first" or "smallest" counterexamples, often in contradiction proofs. | Proving by contradiction that all integers > 1 can be written as a product of primes. |
  > Source: Comparing Proof Techniques.html

- **Choosing a Proof Strategy:** When facing a new statement, ask:
  1. Can I get there directly from definitions? → Try a direct proof.
  2. Does it depend on different conditions (e.g., even vs. odd)? → Try a proof by case.
  3. Does it have a conditional form ("if... then...")? → Consider the contrapositive.
  4. Is it easier to assume it's false and reach a contradiction? → Use proof by contradiction.
  5. Does it claim something is true for all integers? → Use induction or strong induction.
  6. Does it talk about a smallest or first example that doesn't work? → Think well-ordering principle.
  > Source: Comparing Proof Techniques.html

- **Categorizing the Toolkit:** Direct and contrapositive proofs are logical builders. Contradiction and counterexample are error detectors. Induction and well-ordering are infinite reasoners. All proof methods share one goal: to turn belief into certainty — the art of mathematics is knowing which tool fits the problem best.
  > Source: Comparing Proof Techniques.html

## Related Topics
- [Introduction to Proofs](introduction-to-proofs.md)
- [Direct Proofs](direct-proofs.md)
- [Proof by Cases](proof-by-cases.md)
- [Proof by Contrapositive](proof-by-contrapositive.md)
- [Proof by Contradiction](proof-by-contradiction.md)
- [Proof by Counterexample](proof-by-counterexample.md)
- [Mathematical Induction](mathematical-induction.md)
- [Strong Induction](strong-induction.md)
- [The Well-Ordering Principle](well-ordering-principle.md)
