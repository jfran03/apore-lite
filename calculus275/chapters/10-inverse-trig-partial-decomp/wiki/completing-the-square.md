# Completing the Square

## Definition
Complete the square before choosing a substitution: a quadratic is rewritten as (x + h)² + k, so that a shift u = x + h exposes a standard form such as a² − u² or u² + a².
> Source: MATH275-Week10-Lecture-Notes.pdf, Week of November 6 Written Notes.pdf

## Key Concepts
- **Examples of the form:** x² + 4x + 8 = (x + 2)² + 4; 9 − (x − 1)² already has the form a² − u²; x² + 2x + 4 = (x + 1)² − 1 + 4 = (x + 1)² + 3.
  > Source: MATH275-Week10-Lecture-Notes.pdf, Week of November 6 Written Notes.pdf
- **Splitting the numerator:** a numerator can often be split into a multiple of the derivative of the quadratic plus a constant. The derivative part is handled by a logarithmic derivative or a u-substitution; the constant part leads to an arctangent or arcsine integral.
  > Source: MATH275-Week10-Lecture-Notes.pdf

## Examples
- **∫ (2x + 5)/√(9 − (x − 1)²) dx on −2 < x < 4:** put u = x − 1, so 2x + 5 = 2u + 7 and du = dx. The integral is 2∫ u du/√(9 − u²) + 7∫ du/√(9 − u²). For the first, v = 9 − u² and dv = −2u du give −∫ v^(−1/2) dv = −2√(9 − u²) + C₁. For the second, u = 3 sin θ gives ∫ dθ = arcsin(u/3) + C₂. Combining (C = C₁ + 7C₂): −2√(9 − (x − 1)²) + 7 arcsin((x − 1)/3) + C. Differentiation gives 2(x − 1)/√(9 − (x − 1)²) + 7/√(9 − (x − 1)²), the original integrand.
  > Source: MATH275-Week10-Lecture-Notes.pdf
- **∫ (3x + 7)/(x² + 4x + 8) dx:** write 3x + 7 = (3/2)(2x + 4) + 1. Since x² + 4x + 8 = (x + 2)² + 4, the integral is (3/2)∫ (2x + 4)/(x² + 4x + 8) dx + ∫ dx/((x + 2)² + 4). The first term uses the logarithmic derivative; in the second put u = (x + 2)/2. Result: (3/2) ln(x² + 4x + 8) + (1/2) arctan((x + 2)/2) + C. The quadratic is positive on ℝ.
  > Source: MATH275-Week10-Lecture-Notes.pdf
- **∫ x/(x² + 2x + 4) dx:** complete the square to (x + 1)² + 3 and let u = x + 1, du = dx, so x = u − 1. The integral is ∫ u/(u² + 3) du − ∫ 1/(u² + 3) du = (1/2) ln(u² + 3) − (1/√3) tan⁻¹(u/√3) + C = (1/2) ln((x + 1)² + 3) − (1/√3) tan⁻¹((x + 1)/√3) + C.
  > Source: Week of November 6 Written Notes.pdf
  - *Source note:* partway through this computation the written notes slip from u² + 3 to u² − 3. The version above follows the standard forms stated on the same notes: ∫ x/(x² + a²) dx = (1/2) ln(a² + x²) + C and ∫ 1/(x² + a²) dx = (1/a) tan⁻¹(x/a) + C.

## Related Topics
- [Sine Substitution](sine-substitution.md)
- [Tangent Substitution](tangent-substitution.md)
- [Irreducible Quadratic Factors](irreducible-quadratic-factors.md)
