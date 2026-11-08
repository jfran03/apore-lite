# Trigonometric (Inverse) Substitution

## Definition
Trigonometric substitution uses a suitable trigonometric identity to turn a quadratic radical into a trigonometric expression. It is an important method for integrating expressions involving powers of √(a² − x²), √(a² + x²), √(x² − a²).
> Source: MATH275-Week10-Lecture-Notes.pdf, Week of November 6 Written Notes.pdf

It is called **inverse substitution** because we replace x with an entire function in the variable θ (versus replacing a function in x by a variable u, as in ordinary substitution).
> Source: Week of November 6 Written Notes.pdf

## Key Concepts
- **The three standard substitutions (a > 0):**

  | Radical | Substitution and range | Radical after substitution |
  |---|---|---|
  | √(a² − x²) | x = a sin θ, −π/2 < θ < π/2 | a cos θ |
  | √(a² + x²) | x = a tan θ, −π/2 < θ < π/2 | a sec θ |
  | √(x² − a²) | x = a sec θ; 0 < θ < π/2 when x > a; π/2 < θ < π when x < −a | a\|tan θ\| |
  > Source: MATH275-Week10-Lecture-Notes.pdf

- **Why the ranges matter:** the indicated ranges allow us to determine the sign of the square root. The first two identities use cos θ > 0 and sec θ > 0 in the chosen ranges. In the third case the square root is always nonnegative: √(a² tan²θ) = a|tan θ|, so treat x > a and x < −a separately when necessary.
  > Source: MATH275-Week10-Lecture-Notes.pdf
- **Identities used:** 1 − sin²θ = cos²θ (sine case); tan²θ + 1 = sec²θ (tangent and secant cases).
  > Source: Week of November 6 Written Notes.pdf
- **Simplify fully in θ:** after replacing x and dx, simplify the entire integrand in θ.
  > Source: MATH275-Week10-Lecture-Notes.pdf
- **Returning to x with a reference triangle:** expressions like cos(sin⁻¹(x/4)) are simplified using a right triangle built from the substitution (for x = 4 sin θ: opposite x, hypotenuse 4, adjacent √(16 − x²)).
  > Source: Week of November 6 Written Notes.pdf
- **Definite integrals:** one may change the endpoints to angles and evaluate there; changing limits avoids back-substitution. On the chosen angle range, check the sign of each radical before simplifying it. Endpoint values outside the open ranges can be handled by continuity or, for an improper integral, by an appropriate one-sided limit.
  > Source: MATH275-Week10-Lecture-Notes.pdf
- **Check the answer:** check a proposed antiderivative by differentiation, and check the sign and size of a definite integral when possible.
  > Source: MATH275-Week10-Lecture-Notes.pdf

## Examples
See the worked examples in [Sine Substitution](sine-substitution.md), [Tangent Substitution](tangent-substitution.md) and [Secant Substitution](secant-substitution.md).

## Common Misconceptions
- **Ignoring the sign of the radical:** the square root of a square is an absolute value. For the secant substitution, √(a² tan²θ) = a|tan θ|, not a tan θ, and the cases x > a and x < −a must be handled separately.
  > Source: MATH275-Week10-Lecture-Notes.pdf, Week of November 6 Written Notes.pdf

## Related Topics
- [Sine Substitution](sine-substitution.md)
- [Tangent Substitution](tangent-substitution.md)
- [Secant Substitution](secant-substitution.md)
- [Completing the Square](completing-the-square.md)
- [Choosing an Approach](choosing-an-approach.md)
