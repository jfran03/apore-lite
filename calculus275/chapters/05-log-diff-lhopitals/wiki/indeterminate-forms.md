# Indeterminate Forms

## Definition
An indeterminate form is a limit of one of the forms: 0/0; 0⁰; ∞ − ∞; ∞/∞ (and −∞/∞, ∞/−∞, −∞/−∞); 0 × ∞ (and 0 × (−∞)); ∞⁰; 1^∞.
> Source: Week of October 2 (Week 4).pdf

The notation 0/0 describes the separate behavior of numerator and denominator, not a numerical value. The same applies to ∞/∞.
> Source: MATH275-Week05-Lecture-Notes.pdf

## Key Concepts
- **Catalogue of forms with examples:**
  - 0/0: lim_(x→0) sin x / x
  - 0⁰: lim_(x→0⁺) xˣ
  - ∞ − ∞: lim_(x→∞) (x − √(x² + 1))
  - ∞/∞: lim_(x→∞) x2ˣ/(3ˣ + 1)
  - 0 × ∞: lim_(x→0⁺) x ln x
  - ∞⁰: lim_(x→∞) x^(1/x)
  - 1^∞: lim_(x→∞) (1 + 1/x)ˣ
  > Source: Week of October 2 (Week 4).pdf
- **Only ratios go directly into l'Hôpital:** l'Hôpital's rule allows us to take limits found in the indeterminate ratios 0/0 and ±∞/∞. Other forms must first be rewritten (products and differences as quotients; powers via logarithms).
  > Source: Week of October 2 (Week 4).pdf, MATH275-Week05-Lecture-Notes.pdf
- **A finite quotient is not an indeterminate form:** if f(x) → 3 and g(x) → 0⁺, then f(x)/g(x) → +∞ directly. L'Hôpital's rule does not apply because neither required form occurs.
  > Source: MATH275-Week05-Lecture-Notes.pdf
- **Decision sequence:** Substitute first. For a quotient, check 0/0 or ∞/∞ and the differentiability hypotheses before using l'Hôpital. For a product or difference, rewrite it; for a positive variable power, take its logarithm. After each differentiation, recheck the form before applying the rule again. Algebra and continuity often finish the calculation sooner.
  > Source: MATH275-Week05-Lecture-Notes.pdf

## Common Misconceptions
- **Treating 0/0 as a number:** 0/0 and ∞/∞ are descriptions of how numerator and denominator behave separately, not numerical values.
  > Source: MATH275-Week05-Lecture-Notes.pdf
- **Applying l'Hôpital to a non-indeterminate quotient:** a quotient like (→3)/(→0⁺) goes directly to +∞; l'Hôpital's rule does not apply.
  > Source: MATH275-Week05-Lecture-Notes.pdf

## Related Topics
- [L'Hôpital's Rule](lhopitals-rule.md)
- [Products and Differences (0·∞, ∞−∞)](products-and-differences.md)
- [Indeterminate Powers](indeterminate-powers.md)
