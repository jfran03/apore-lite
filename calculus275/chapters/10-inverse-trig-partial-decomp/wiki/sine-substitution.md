# Sine Substitution

## Definition
For √(a² − x²), substitute x = a sin θ with −π/2 < θ < π/2. Then dx = a cos θ dθ and √(a² − x²) = a cos θ, using 1 − sin²θ = cos²θ and cos θ > 0 on the chosen range.
> Source: MATH275-Week10-Lecture-Notes.pdf, Week of November 6 Written Notes.pdf

## Key Concepts
- **Why cos θ ≥ 0:** √(16 − 16 sin²θ) = √(16 cos²θ) = 4 cos θ provided cos θ ≥ 0. Since −4 ≤ x ≤ 4, it must be the case that θ ∈ [−π/2, π/2], and so cos θ ≥ 0.
  > Source: Week of November 6 Written Notes.pdf
- **Back-substitution:** from x/a = sin θ, θ = sin⁻¹(x/a). Expressions such as cos(sin⁻¹(x/a)) are simplified with a reference triangle (opposite x, hypotenuse a, adjacent √(a² − x²)).
  > Source: Week of November 6 Written Notes.pdf
- **Basic arcsine result:** with u = 3 sin θ, ∫ du/√(9 − u²) = ∫ dθ = arcsin(u/3) + C.
  > Source: MATH275-Week10-Lecture-Notes.pdf

## Examples
- **∫ (x + 1)/√(16 − x²) dx:** let x = 4 sin θ, so √(16 − x²) = 4 cos θ and dx = 4 cos θ dθ. The integral becomes ∫ (4 sin θ + 1) dθ = −4 cos θ + θ + C = −4 cos(sin⁻¹(x/4)) + sin⁻¹(x/4) + C. Using the triangle, cos θ = √(16 − x²)/4, so the result is −√(16 − x²) + sin⁻¹(x/4) + C.
  > Source: Week of November 6 Written Notes.pdf
- **∫ √(9 − x²)/x dx on 0 < x < 3:** let x = 3 sin θ with 0 < θ < π/2. Then dx = 3 cos θ dθ and √(9 − x²) = 3 cos θ, so the integral is 3∫ cos²θ/sin θ dθ = 3∫ (csc θ − sin θ) dθ. Since (csc θ − cot θ)′ = csc θ(csc θ − cot θ), this equals 3 ln|csc θ − cot θ| + 3 cos θ + C. With cos θ = √(9 − x²)/3 and csc θ − cot θ = (3 − √(9 − x²))/x, the result is √(9 − x²) + 3 ln((3 − √(9 − x²))/x) + C. The logarithm's argument is positive on the stated interval.
  > Source: MATH275-Week10-Lecture-Notes.pdf

## Common Misconceptions
- **Forgetting to replace dx:** dx must also be replaced (dx = a cos θ dθ). In ∫ (x + 1)/√(16 − x²) dx, the factor 4 cos θ from dx cancels the 4 cos θ from the radical.
  > Source: Week of November 6 Written Notes.pdf

## Related Topics
- [Trigonometric (Inverse) Substitution](trig-substitution.md)
- [Completing the Square](completing-the-square.md)
