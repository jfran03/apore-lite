# Hyperbolic Functions

## Definition
The hyperbolic functions are built from exponentials:
sinh x = (eˣ − e⁻ˣ)/2, cosh x = (eˣ + e⁻ˣ)/2, tanh x = sinh x / cosh x, sech x = 1/cosh x, csch x = 1/sinh x, coth x = cosh x / sinh x.
> Source: MATH275-Week04-Lecture-Notes.pdf, Week of September 25 (Week 3) .pdf

## Key Concepts
- **Domains and ranges:** dom(cosh) = ℝ, ran(cosh) = [1, ∞); dom(sinh) = ℝ, ran(sinh) = ℝ; dom(tanh) = ℝ, ran(tanh) = (−1, 1).
  > Source: Week of September 25 (Week 3) .pdf
- **Identities parallel trigonometric ones with a sign change:** cosh² x − sinh² x = 1, 1 − tanh² x = sech² x, coth² x − csch² x = 1 (x ≠ 0). Also sinh(−x) = −sinh x and cosh(−x) = cosh x.
  > Source: MATH275-Week04-Lecture-Notes.pdf
- **Shape facts:** sinh is odd and strictly increasing; cosh is even with minimum value 1 at x = 0; tanh is odd, strictly increasing, with range (−1, 1) and horizontal asymptotes y = ±1; sech is even with range (0, 1].
  > Source: MATH275-Week04-Lecture-Notes.pdf
- **Why "hyperbolic":** (X, Y) = (cosh t, sinh t) satisfies X² − Y² = 1, so sinh and cosh play for the unit hyperbola the role that sine and cosine play for the unit circle.
  > Source: MATH275-Week04-Lecture-Notes.pdf
- **Derivatives:** (sinh x)' = cosh x, (cosh x)' = sinh x, (tanh x)' = sech² x, (sech x)' = −sech x tanh x, (coth x)' = −csch² x, (csch x)' = −csch x coth x. csch and coth, hence their derivative formulas, require x ≠ 0.
  > Source: MATH275-Week04-Lecture-Notes.pdf, Week of September 25 (Week 3) .pdf
- **Derivation:** the formulas follow directly from the exponential definitions with the product and quotient rules. E.g. (sinh x)' = (eˣ − (−e⁻ˣ))/2 = cosh x.
  > Source: MATH275-Week04-Lecture-Notes.pdf, Week of September 25 (Week 3) .pdf
- **Use like trig derivatives:** apply the hyperbolic derivative formulas exactly as trig derivative formulas, while keeping the different identities straight.
  > Source: MATH275-Week04-Lecture-Notes.pdf

## Examples
- **Verify the identity:** cosh² x − sinh² x = [(eˣ + e⁻ˣ)² − (eˣ − e⁻ˣ)²]/4 = 1.
  > Source: MATH275-Week04-Lecture-Notes.pdf
- **r(x) = sech x tanh² x:** by the product and chain rules, r'(x) = −sech x tanh³ x + 2 sech³ x tanh x. Using tanh(ln 2) = 3/5 and sech(ln 2) = 4/5, r'(ln 2) = −(4/5)(3/5)³ + 2(4/5)³(3/5) = 276/625.
  > Source: MATH275-Week04-Lecture-Notes.pdf
- **s(x) = cosh(2x) − 3 sinh(x²):** identify each inner derivative first (2x → 2; x² → 2x). Then s'(x) = 2 sinh(2x) − 6x cosh(x²).
  > Source: MATH275-Week04-Lecture-Notes.pdf
- **y = tanh(x³):** with u = x³, u' = 3x², y' = 3x² sech²(x³).
  > Source: MATH275-Week04-Lecture-Notes.pdf

## Common Misconceptions
- **Notation:** sinh⁻¹ x is commonly used for arsinh x, not for csch x. Context and parentheses matter.
  > Source: MATH275-Week04-Lecture-Notes.pdf

## Related Topics
- [Inverse Hyperbolic Functions](inverse-hyperbolic-functions.md)
- [Inverse Trigonometric Derivatives](inverse-trig-derivatives.md)
