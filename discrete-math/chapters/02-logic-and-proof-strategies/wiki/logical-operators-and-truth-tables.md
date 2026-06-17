# Logical Operators and Truth Tables

## Definition
A **truth table** is a tool that shows all the possible truth values of a proposition or combination of propositions, and the resulting truth value of the compound statement. The columns list the input truth values (e.g., for p, q); the final column shows the result for the operator being studied.
> Source: Logical Operators & Truth Tables.html

## Key Concepts

- **Negation (¬, "not"):** Let p be a proposition. The negation of p, denoted ¬p (or p̅), is the statement "It is not the case that p." The truth value of ¬p is the opposite of the truth value of p.
  > Source: Logical Operators & Truth Tables.html

- **Conjunction (∧, "and"):** Let p and q be two propositions. The conjunction p ∧ q is the proposition "p and q." It is true when both p and q are true, and false otherwise.
  > Source: Logical Operators & Truth Tables.html

- **Disjunction (∨, "or"):** Let p and q be two propositions. The disjunction p ∨ q is the proposition "p or q." It is false only when both p and q are false, and true otherwise. In mathematics and logic, "or" is inclusive: both may be true.
  > Source: Logical Operators & Truth Tables.html

- **Implication (⟹, "if/then"):** Let p and q be propositions. The conditional statement p ⟹ q is the proposition "if p, then q." It is false only when p is true and q is false; in all other cases, it is true.
  > Source: Logical Operators & Truth Tables.html

- **Biconditional (⟺, "if and only if"):** Let p and q be propositions. The biconditional p ⟺ q is the proposition "p if and only if q." It is true when p and q have the same truth value, and false otherwise.
  > Source: Logical Operators & Truth Tables.html

- **Exclusive Or (⊕, XOR):** Let p and q be propositions. The exclusive or p ⊕ q is true when exactly one of p or q is true, and false otherwise.
  > Source: Logical Operators & Truth Tables.html

## Truth Tables

**Negation:**

| p | ¬p |
|---|-----|
| T | F |
| F | T |
> Source: Logical Operators & Truth Tables.html

**Conjunction:**

| p | q | p ∧ q |
|---|---|--------|
| T | T | T |
| T | F | F |
| F | T | F |
| F | F | F |
> Source: Logical Operators & Truth Tables.html

**Disjunction:**

| p | q | p ∨ q |
|---|---|--------|
| T | T | T |
| T | F | T |
| F | T | T |
| F | F | F |
> Source: Logical Operators & Truth Tables.html

**Implication:**

| p | q | p ⟹ q |
|---|---|---------|
| T | T | T |
| T | F | F |
| F | T | T |
| F | F | T |
> Source: Logical Operators & Truth Tables.html

**Biconditional:**

| p | q | p ⟺ q |
|---|---|---------|
| T | T | T |
| T | F | F |
| F | T | F |
| F | F | T |
> Source: Logical Operators & Truth Tables.html

**Exclusive Or:**

| p | q | p ⊕ q |
|---|---|--------|
| T | T | F |
| T | F | T |
| F | T | T |
| F | F | F |
> Source: Logical Operators & Truth Tables.html

## Examples

- Negation: p = "It is raining." (True) → ¬p = "It is not raining." (False)
  > Source: Logical Operators & Truth Tables.html
- Conjunction: p = "The computer is on." q = "The printer is working." → p ∧ q = "The computer is on and the printer is working."
  > Source: Logical Operators & Truth Tables.html
- Disjunction: p = "The computer is on." q = "The printer is working." → p ∨ q = "The computer is on or the printer is working."
  > Source: Logical Operators & Truth Tables.html
- Implication: p = "It rains." q = "The ground is wet." → p ⟹ q = "If it rains, then the ground is wet."
  > Source: Logical Operators & Truth Tables.html
- Biconditional: p = "You study." q = "You pass the test." → p ⟺ q = "You will pass the test if and only if you study."
  > Source: Logical Operators & Truth Tables.html
- XOR: p = "The cake is chocolate." q = "The cake is vanilla." → p ⊕ q = "The cake is either chocolate or vanilla (but not both)."
  > Source: Logical Operators & Truth Tables.html

## Practice Problems

**Finding the truth values that make a statement false (MCQ):** Consider the logical statement
[ ((P ⊕ S) ⇒ ¬R) ∨ (S ⇒ (Q ∧ ¬P)) ] ∨ [ (P ∧ (R ∨ ¬S)) ∧ (S ∨ (¬Q ∨ ¬P)) ].
Which of the following combinations of truth values would result in this statement being false?
- (a) P → True, Q → True, R → False, S → True
- (b) P → True, Q → False, R → True, S → False
- (c) P → False, Q → False, R → True, S → True
- (d) P → False, Q → True, R → True, S → False
  > Source: 10.PNG

## Related Topics
- [Propositions and Truth Values](propositions-and-truth-values.md)
- [Tautologies, Contradictions, and Equivalence](tautologies-contradictions-and-equivalence.md)
