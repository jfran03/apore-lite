# Signed Area and Properties of the Definite Integral

## Definition
A definite integral counts area above the axis positively and area below it negatively. Geometric area counts both positively:
∫ₐᵇ f(x) dx = A_above − A_below,  total area = ∫ₐᵇ |f(x)| dx = A_above + A_below.
> Source: MATH275-Week08-Lecture-Notes.pdf, Week of October 23.pdf

## Key Concepts
- **Zero-width interval:** ∫ₐᵃ f(x) dx = 0 (zero area).
  > Source: Week of October 23.pdf, MATH275-Week08-Lecture-Notes.pdf
- **Additivity:** if a ≤ b ≤ c, then ∫ₐᶜ f(x) dx = ∫ₐᵇ f(x) dx + ∫ᵦᶜ f(x) dx (additive areas).
  > Source: Week of October 23.pdf, MATH275-Week08-Lecture-Notes.pdf
- **Reversing limits:** ∫ₐᵇ f(x) dx = −∫ᵦᵃ f(x) dx. This follows from the first two properties since 0 = ∫ₐᵃ f = ∫ₐᵇ f + ∫ᵦᵃ f.
  > Source: Week of October 23.pdf, MATH275-Week08-Lecture-Notes.pdf
- **Linearity:** ∫ₐᵇ [f(x) ± g(x)] dx = ∫ₐᵇ f dx ± ∫ₐᵇ g dx; ∫ₐᵇ c f(x) dx = c ∫ₐᵇ f(x) dx; in general ∫ₐᵇ (αf + βg) = α∫ₐᵇ f + β∫ₐᵇ g.
  > Source: Week of October 23.pdf, MATH275-Week08-Lecture-Notes.pdf
- **Comparison:** if f ≤ g on [a, b] with a < b, then ∫ₐᵇ f ≤ ∫ₐᵇ g. In particular, if g(x) ≥ 0 then ∫ₐᵇ g(x) dx ≥ ∫ₐᵇ 0 dx = 0. Also, m ≤ f ≤ M implies m(b − a) ≤ ∫ₐᵇ f ≤ M(b − a).
  > Source: Week of October 23.pdf, MATH275-Week08-Lecture-Notes.pdf
- **Absolute value inequality:** |∫ₐᵇ f(x) dx| ≤ ∫ₐᵇ |f(x)| dx.
  > Source: Week of October 23.pdf
- **Odd functions:** if f is odd (f(−x) = −f(x) for all x), then ∫₋ₐᵃ f(x) dx = 0: the two halves have opposite signs and cancel.
  > Source: Week of October 23.pdf, MATH275-Week08-Lecture-Notes.pdf
- **Even functions:** if f is even (f(−x) = f(x) for all x), then ∫₋ₐᵃ f(x) dx = 2∫₀ᵃ f(x) dx: the two halves are equal.
  > Source: Week of October 23.pdf, MATH275-Week08-Lecture-Notes.pdf

## Examples
- **Integral vs geometric area:** ∫₋₁³ (x − 1) dx. The graph crosses the axis at x = 1; each side is a triangle of base 2 and height 2, area 2. So ∫₋₁³ (x − 1) dx = −2 + 2 = 0, while total area = 2 + 2 = 4. Cancellation in a signed integral does not mean the geometric region has zero area.
  > Source: MATH275-Week08-Lecture-Notes.pdf
- **Symmetry, no antiderivative needed:** ∫₋₂² [t sin(t²) + √(4 − t²) − 3] dt. Since sin(t²) is even, t sin(t²) is odd, so its integral is 0. √(4 − t²) is the upper semicircle of radius 2, area 2π. The constant contributes −3(4) = −12. Total: 2π − 12.
  > Source: MATH275-Week08-Lecture-Notes.pdf
- **∫₋₄⁴ [x³/2 + x cos(x²) − √(16 − x²)] dx:** x³ is odd since (−x)³ = (−1)³x³ = −x³, so (1/2)∫₋₄⁴ x³ dx = 0. x cos(x²) is odd since (−x)cos((−x)²) = −x cos(x²), so its integral is 0. y = √(16 − x²) is the upper half of x² + y² = 16, area half of π·4², i.e. 8π. Result: −8π.
  > Source: Week of October 23.pdf

## Common Misconceptions
- A signed integral of 0 does not mean the region has zero geometric area.
  > Source: MATH275-Week08-Lecture-Notes.pdf

## Related Topics
- [The Definite Integral](definite-integral.md)
- [Reading an Accumulation Function from a Graph](accumulation-graphs.md)
