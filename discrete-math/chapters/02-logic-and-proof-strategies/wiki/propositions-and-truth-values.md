# Propositions and Truth Values

## Definition
A **proposition** is a statement that is either true or false. For a particular proposition p, the truth value of p is its truth or falsity.
> Source: Introduction to Logic & Propositions.html

## Key Concepts

- **Truth Value:** Whether a proposition is true (T) or false (F).
  > Source: Introduction to Logic & Propositions.html

- **Atomic Proposition:** A simple, indivisible proposition that conveys a single idea or fact. It does not contain any logical operators (e.g., and, or, if-then) or connectives.
  > Source: Introduction to Logic & Propositions.html

- **Compound Proposition:** Formed by combining two or more atomic propositions using logical operators (connectives). Common types: Conjunction (and), Disjunction (or), Implication (if-then), Negation (not), Biconditional (if and only if).
  > Source: Introduction to Logic & Propositions.html

- **Non-Propositions:** Questions, commands, and vague expressions are not propositions because they do not have a truth value.
  > Source: Introduction to Logic & Propositions.html

- **Ambiguity in natural language:** Words like "and," "or," and "if" can be vague in everyday speech, relying on context for meaning. In mathematics and computer science, logical connectives have precise, fixed definitions that eliminate this ambiguity.
  > Source: Introduction to Logic & Propositions.html

## Examples

**Propositions:**
- "33 is a prime number." — proposition, true
- "44 is an odd number." — proposition, false
- "60 ÷ 4 = 20" — proposition, false
- "2 + 3 = 5" — proposition, true
  > Source: Introduction to Logic & Propositions.html

**Atomic proposition examples:**
- "The sky is blue."
- "She is reading a book."
- "Water boils at 100 degrees Celsius."
  > Source: Introduction to Logic & Propositions.html

**Not propositions:**
- "What time is it?" — not a proposition (question)
- "Restart your laptop." — not a proposition (command)
  > Source: Introduction to Logic & Propositions.html

**Compound proposition examples:**
- Conjunction (and): "The sky is blue and the grass is green."
- Disjunction (or): "The sky is blue or it is cloudy."
- Implication (if-then): "If it rains, then the ground will be wet."
- Negation (not): "The sky is not purple."
- Biconditional (if and only if): "You will open the door if and only if you have the key."
  > Source: Introduction to Logic & Propositions.html

**Sortable examples from practice:**
- Atomic: "The computer is on.", "7 is greater than 5.", "The number 12 is divisible by 3.", "Every student in the class owns a laptop."
- Compound: "If it rains, then the ground is wet.", "The file is saved and the program is closed.", "If the code compiles and the tests pass, then the program is correct."
- Not a Proposition: "Run around the block five times.", "Do you want coffee or tea?", "Turn off the lights when you leave the room."
  > Source: config-1759345171983.practice.json

## Common Misconceptions
- Everyday "or" can mean exclusive or inclusive depending on context, but in logic "or" (∨) is always inclusive unless explicitly stated otherwise.
  > Source: Introduction to Logic & Propositions.html

## Practice Problems

**Identifying propositions:** From the following list of sentences, select the ones that can be classified as a proposition:
- "Are you going to finish this assignment?"
- "Someone in this class is a millionaire."
- "The number 97 is a prime number."
- "Cats are smarter than dogs."
- "Everyone thinks pizza is tasty."
- "Calgary is the capital city of Alberta."
- "Let n ∈ ℤ be an arbitrary integer."
- "There exists a bird that cannot fly."
- "This sentence is false."
- "Every triangle has three sides."
  > Source: 6.PNG

**Translating to symbolic logic:** Translate each proposition into symbolic logic, defining your own predicates as necessary, using the notations ∀ and ∃ (do not determine truth/falsity):
- (a) For all integers a, there exists an integer b such that a · b is even.
- (b) There exists a real number c such that, for all real numbers d, c · d is an integer.
- (c) For all rational numbers q, if 1/q is an integer, then q has a numerator of 1.
  > Source: 7.PNG
  > Note: predicate/quantifier logic (∀, ∃, predicates) extends beyond the propositional-logic content currently compiled in this wiki; transcribed here for completeness.

**Writing negations:** Write the negation of each statement below in proper English sentences (no mathematical symbols):
- (a) For all integers a, there exists an integer b such that a · b is even.
- (b) There exists a real number c such that, for all real numbers d, c · d is an integer.
- (c) For all rational numbers q, if 1/q is an integer, then q has a numerator of 1.
- (d) For all real numbers x and y, there exists an integer z such that, if x + y = z, then x is an integer or y is an integer.
- (e) There exists an integer a such that, for all integers b, if there exist integers c, d such that a · d − b · c = 0, then a · b is even and c · d is odd.
  > Source: 12.PNG
  > Note: negating quantified (∀/∃) statements extends beyond the propositional-logic content currently compiled in this wiki; transcribed here for completeness.

## Related Topics
- [Logical Operators and Truth Tables](logical-operators-and-truth-tables.md)
- [Tautologies, Contradictions, and Equivalence](tautologies-contradictions-and-equivalence.md)
