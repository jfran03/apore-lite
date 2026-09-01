# Tautologies, Contradictions, and Equivalence

## Definition
When working with logic, some statements are always true (tautologies), some are sometimes true (satisfiable), and some are never true (contradictions/unsatisfiable). Understanding these three categories helps reason precisely about whether an argument is valid or flawed.
> Source: Tautologies, Contradictions, and Equivalence.html

## Key Concepts

- **Tautology:** A proposition that is always true, no matter what truth values its components take. Identified by building its truth table and observing that every row evaluates to True.
  > Source: Tautologies, Contradictions, and Equivalence.html

- **Satisfiable Proposition:** A proposition that is true under at least one assignment of truth values.
  > Source: Tautologies, Contradictions, and Equivalence.html

- **Unsatisfiable Proposition (Contradiction):** A proposition that is never true. Its truth table contains only "false."
  > Source: Tautologies, Contradictions, and Equivalence.html

- **Logical Equivalence:** Two propositions p and q are logically equivalent if they have identical truth values in every possible case. Written as p ≡ q. Equivalently, p and q are logically equivalent if the biconditional p ⟺ q is a tautology.
  > Source: Tautologies, Contradictions, and Equivalence.html

## Examples

**Tautologies:**

- **Law of the Excluded Middle:** p ∨ ¬p — every proposition is either true or false; there is no "in-between." Always evaluates to True.

  | p | ¬p | p ∨ ¬p |
  |---|-----|---------|
  | T | F | T |
  | F | T | T |
  > Source: Tautologies, Contradictions, and Equivalence.html

- **Modus Ponens:** (p ∧ (p ⟹ q)) ⟹ q — if p is true and p implies q, then q must also be true. Every row in its truth table is T.

  | p | q | p ⟹ q | p ∧ (p ⟹ q) | (p ∧ (p ⟹ q)) ⟹ q |
  |---|---|--------|-------------|---------------------|
  | T | T | T | T | T |
  | T | F | F | F | T |
  | F | T | T | F | T |
  | F | F | T | F | T |
  > Source: Tautologies, Contradictions, and Equivalence.html

**Satisfiable vs. Contradiction:**

| Type | Example | Description |
|------|---------|-------------|
| Satisfiable | p ∧ q | True when both p and q are true |
| Contradiction | p ∧ ¬p | Can never be true; p and ¬p can't both hold |
> Source: Tautologies, Contradictions, and Equivalence.html

**Logical Equivalence example:** ¬(p ∧ q) and (p ∧ q) ⟹ ¬q are logically equivalent — their truth table columns are identical.

| p | q | (p ∧ q) ⟹ ¬q | ¬(p ∧ q) |
|---|---|--------------|----------|
| T | T | F | F |
| T | F | T | T |
| F | T | T | T |
| F | F | T | T |
> Source: Tautologies, Contradictions, and Equivalence.html

## Common Logical Equivalences

| Name | Expression | Meaning |
|------|-----------|---------|
| Double Negation | p ≡ ¬¬p | Removing two negations doesn't change truth |
| Implication Rewrite | p ⟹ q ≡ ¬p ∨ q | Every implication can be written as an "or" statement |
| De Morgan's Laws | ¬(p ∧ q) ≡ ¬p ∨ ¬q | Negation distributes through ∧/∨ and flips them |
|  | ¬(p ∨ q) ≡ ¬p ∧ ¬q |  |
| Commutative | p ∨ q ≡ q ∨ p | Order doesn't matter for ∨ or ∧ |
|  | p ∧ q ≡ q ∧ p |  |
> Source: Tautologies, Contradictions, and Equivalence.html

## Practice Problems

**Tautology and equivalence via truth tables:** Consider the compound statements
A := (P ⇒ Q) ∨ (Q ⇒ R) ∨ (R ⇒ P)    and    B := P ∨ Q ∨ R.
- (a) Determine if statement A is a tautology by constructing a truth table.
- (b) Determine if A ⟺ B. If so, provide reasoning as to why. If not, provide a sample of truth values for the individual propositions P, Q, R that cause the logical equivalence to fail.
  > Source: 8.PNG

**Proving logical equivalence using the equivalence axioms:** Prove the following logical equivalence using the logical equivalence axioms (state the name of the axiom(s) used in each step):
( (P ⇒ Q) ∨ ¬R ) ⇒ ( P ∧ ¬(Q ⇒ R) )    ⟺    P ∧ (Q ⊕ R).
  > Source: 9.PNG
  > Note: a full step-by-step derivation requires equivalence laws (e.g., distribution, absorption) beyond the subset listed under "Common Logical Equivalences" above; transcribed here for completeness.

## Related Topics
- [Propositions and Truth Values](propositions-and-truth-values.md)
- [Logical Operators and Truth Tables](logical-operators-and-truth-tables.md)
