# Irreducible Quadratic Factors

## Definition
**Type II (distinct irreducible quadratic terms):** if q(x) has quadratic factors without roots (e.g. x² + 1), written q₁(x), …, q_k(x) and distinct, then there are constants A₁, B₁, A₂, B₂, … so that
p(x)/q(x) = (Type I and Ia terms) + (A₁x + B₁)/q₁(x) + (A₂x + B₂)/q₂(x) + ⋯ + (A_k x + B_k)/q_k(x).
> Source: Week of November 6 Written Notes.pdf

**Type IIa (repeated irreducible factors):** if q(x) has a factor q₁(x)^k with q₁ an irreducible quadratic, the decomposition contains the terms
(A₁x + B₁)/q₁(x) + (A₂x + B₂)/q₁(x)² + ⋯ + (A_k x + B_k)/q₁(x)^k.
> Source: Week of November 6 Written Notes.pdf, MATH275-Week10-Lecture-Notes.pdf

## Key Concepts
- **Linear numerator over each quadratic power:** a repeated irreducible quadratic requires a linear numerator at each power.
  > Source: MATH275-Week10-Lecture-Notes.pdf
- **Integrating (Qx + R)/q(x):** write the numerator as λq′(x) + μ. The derivative term integrates to a logarithm, and completing the square reduces the constant term to an arctangent integral. These terms "are done with substitution or inverse tan substitution or both."
  > Source: MATH275-Week10-Lecture-Notes.pdf, Week of November 6 Written Notes.pdf
- **Repeated quadratics may need another method:** after decomposition, a repeated quadratic may require a trigonometric substitution or integration by parts.
  > Source: MATH275-Week10-Lecture-Notes.pdf

## Examples
- **Form only, ∫ (x³ + 2x + 1)/(x(x − 1)²(x² + 2x + 4)(x² + 4)) dx:** x and (x − 1)² are the Type I / Ia part, x² + 2x + 4 and x² + 4 are Type II factors. Degree 7 means 7 coefficients: A₁/x + A₂/(x − 1) + A₃/(x − 1)² + (B₁x + C₁)/(x² + 2x + 4) + (B₂x + C₂)/(x² + 4). (The notes do not solve for these.)
  > Source: Week of November 6 Written Notes.pdf
  - *Source note:* the written notes write the fourth denominator as x² + 2x + 9 in the decomposition line, but the original denominator contains x² + 2x + 4; the matching factor is x² + 2x + 4.
- **Form only, repeated quadratic:** (4x² + 3x − 2)/((x − 1)²(x − 4)²(x² + 1)³) = A₁/(x − 1) + A₂/(x − 1)² + B₁/(x − 4) + B₂/(x − 4)² + (C₁x + D₁)/(x² + 1) + (C₂x + D₂)/(x² + 1)² + (C₃x + D₃)/(x² + 1)³.
  > Source: Week of November 6 Written Notes.pdf
  - *Source note:* in the handwritten denominator the factor (x − 4)² is hard to read and resembles (x − 9)²; the decomposition terms on the same line show (x − 4), which is used here.
- **Form only, several quadratics:** 2/((x² + 1)(x² + 2x + 6)²(x² + 2)²) = (A₁x + B₁)/(x² + 1) + (A₂x + B₂)/(x² + 2x + 6) + (A₃x + B₃)/(x² + 2x + 6)² + (A₄x + B₄)/(x² + 2) + (A₅x + B₅)/(x² + 2)².
  > Source: Week of November 6 Written Notes.pdf
- **∫ (2x² + 3x + 6)/((x + 2)(x² + 4)) dx:** the decomposition is P/(x + 2) + (Qx + R)/(x² + 4). Clearing denominators: 2x² + 3x + 6 = P(x² + 4) + (Qx + R)(x + 2). At x = −2, 8 = 8P, P = 1. Comparing x² coefficients: 2 = P + Q, Q = 1; constants: 6 = 4P + 2R, R = 1. The x coefficient also agrees: 3 = 2Q + R. The integral is ∫ dx/(x + 2) + ∫ x dx/(x² + 4) + ∫ dx/(x² + 4) = ln|x + 2| + (1/2) ln(x² + 4) + (1/2) arctan(x/2) + C.
  > Source: MATH275-Week10-Lecture-Notes.pdf
- **∫ (x² + 2)/(x² + 1)² dx:** separate the two powers: (x² + 2)/(x² + 1)² = 1/(x² + 1) + 1/(x² + 1)². For the second integral put x = tan θ, −π/2 < θ < π/2: ∫ dx/(x² + 1)² = ∫ cos²θ dθ = θ/2 + sin(2θ)/4 + C. Since θ = arctan x and sin(2θ) = 2x/(1 + x²), adding the first term gives (3/2) arctan x + x/(2(1 + x²)) + C.
  > Source: MATH275-Week10-Lecture-Notes.pdf
- **∫ x/(x² + 2x + 4) dx:** worked in [Completing the Square](completing-the-square.md).
  > Source: Week of November 6 Written Notes.pdf

## Common Misconceptions
- **Constant numerator over a quadratic:** over an irreducible quadratic (or each power of one) the numerator must be linear, Qx + R, not just a constant.
  > Source: MATH275-Week10-Lecture-Notes.pdf

## Related Topics
- [Partial Fraction Decomposition: Setup](partial-fractions-setup.md)
- [Completing the Square](completing-the-square.md)
- [Tangent Substitution](tangent-substitution.md)
- [Linear Factors (Distinct and Repeated)](linear-factors.md)
