# Introduction to Proofs

## Definition
A proof of a proposition is a convincing argument that demonstrates the proposition is true. A proof is a valid logical argument built from axioms (statements assumed to be true), premises or hypotheses (conditions given in the theorem), and previously proven theorems or definitions (trusted building blocks). Using these, we apply rules of inference step-by-step until we reach the desired conclusion.
> Source: Introduction to Proofs.html

## Key Concepts

- **Proof as Writing:** Like a persuasive essay or a clear argument in code comments, a proof must be structured and written for an audience that expects logical precision and clarity. Good proofs are clear (every step follows logically from the last), complete (no gaps that require "intuition"), and convincing (the reader understands why the statement is true, not just that it is).
  > Source: Introduction to Proofs.html

- **Theorem:** A statement that has been rigorously proven true. Usually an important or central result.
  > Source: Introduction to Proofs.html

- **Proposition:** A statement that can be proven true, but is typically less significant than a theorem.
  > Source: Introduction to Proofs.html

- **Lemma:** A "helping theorem" — a smaller result proved mainly to help prove a larger one.
  > Source: Introduction to Proofs.html

- **Corollary:** A statement that follows directly from a theorem that's already been proven.
  > Source: Introduction to Proofs.html

- **Conjecture:** A statement believed to be true based on evidence or intuition, but not yet proven. Once proven, a conjecture becomes a theorem.
  > Source: Introduction to Proofs.html

- **Why Computer Scientists Care About Proofs:** Proofs ensure that an algorithm or system will always behave as expected under all conditions — they guarantee correctness by showing that results hold in every possible situation, not just in testing scenarios. Proofs help replace assumptions and testing with logical certainty, and provide a way to formally verify security, correctness and termination in programs. They underpin areas like formal verification, compiler correctness, and security protocols. Proofs are not only used in pure mathematics, and they do not rely on guessing — they eliminate uncertainty through formal reasoning.
  > Source: config-1759771574388.practice.json, Introduction to Proofs.html

- **Types of Proof Techniques:** Four main strategies for constructing proofs are introduced:
  - Direct Proof: Show that a statement follows logically from given facts or premises.
  - Proof by Cases: Divide a problem into distinct cases and show that the claim holds in each one.
  - Proof by Contrapositive: Instead of proving "if p then q," prove the logically equivalent "if not q then not p."
  - Proof by Contradiction: Assume the opposite of what you want to prove, then show that this leads to a contradiction.
  > Source: Introduction to Proofs.html

## Examples

- **From Conjecture to Theorem:** For centuries, mathematicians conjectured that there were infinitely many prime numbers. In 300 BCE, Euclid proved it by contradiction, transforming that conjecture into one of the first great theorems in history.
  > Source: Introduction to Proofs.html

- **History of Proof:** Ancient Greeks, especially Euclid, built the first formal system of proofs in *Elements* (circa 300 BCE), with a structure of definitions, axioms and theorems still used today. In the 20th century, logicians like Bertrand Russell and Kurt Gödel showed that formal systems have both power and limits — Gödel's Incompleteness Theorem proved that not every true statement can be proven within a system. In computer science, proofs evolved into automated reasoning and formal verification, where proof assistants check logical steps for correctness.
  > Source: Introduction to Proofs.html

## Practice Problems

**Determine which statements are true (no proof required):** Determine which of the following mathematical statements are True:
- |−20.26| = −20
- For all a, b ∈ ℤ, if a | b, then a | 2b.
- For all n ∈ {0, 1, 2, 3, 4, 5, 6}, n | 360.
- For all x, y ∈ ℝ, if ⌊x⌋ = |y|, then x = y.
- The number 57 is not a composite number.
- For all a, b ∈ ℤ, if 5 | a + b, then 5 | a or 5 | b.
- There exists n ∈ ℚ such that, for all m ∈ ℚ, n · m ∈ ℤ.
- For all m, n ∈ ℤ, if m + n is odd, then m + 2n is even.
- For all n ∈ ℝ, there exists m ∈ ℝ such that ⌊n⌋ + ⌈m⌉ = 1.
- For all x, y ∈ ℝ, if x + y is irrational, then x and y are irrational.
  > Source: 11.PNG

**Determine True/False and write a complete proof for each:**
- (a) For all integers a, b, c, d, if a | b and c | d, then a + b | c + d.
- (b) For all integers m, there exists an integer n such that 3 | m + n.
- (c) For all real numbers x, y, ⌊x · y⌋ = ⌊x⌋ · ⌊y⌋.
- (d) For all real numbers x, y, if x · y is rational, then x is rational or y is rational.
- (e) For all integers m, n, if m and n are odd, then m² + n² is even.
  > Source: 18.PNG
  > Note: several of these involve floor/ceiling and quantifier reasoning beyond the proof-technique content currently compiled in this wiki; transcribed here for completeness.

## Related Topics
- [Direct Proofs](direct-proofs.md)
- [Proof by Cases](proof-by-cases.md)
- [Proof by Contrapositive](proof-by-contrapositive.md)
- [Proof by Contradiction](proof-by-contradiction.md)
- [Comparing Proof Techniques](comparing-proof-techniques.md)
