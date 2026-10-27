# Variable Powers

## Definition
Let u and v be differentiable on an interval I, and suppose u(x) > 0 on I. Define u(x)^v(x) = e^(v(x) ln u(x)). Thus

d/dx u(x)^v(x) = u(x)^v(x) · ( v′(x) ln u(x) + v(x) u′(x)/u(x) ).

The base-positive hypothesis is what makes this real-valued definition valid when the exponent varies continuously.
> Source: MATH275-Week05-Lecture-Notes.pdf

## Key Concepts
- **Neither power rule nor exponential rule applies:** for y = xˣ (x > 0), you cannot use the derivative of xʳ nor of aˣ, since it is neither of these. Instead rewrite y = e^(ln(xˣ)) = e^(x ln x) and use the chain rule, or take ln y = ln xˣ; both differentiate y to the same thing.
  > Source: Week of October 2 (Week 4).pdf
- **Check the sign of the base first:** logarithmic differentiation of a variable power requires the base to be positive on the interval considered. For example, since 3 + cos x ≥ 2, logarithmic differentiation of (3 + cos x)^(x²) is valid for every real x; and 2 + x² is positive on all of ℝ.
  > Source: MATH275-Week05-Lecture-Notes.pdf
- **0⁰ is not used as a definition:** at the edge of the domain of a variable power, a value such as F(0) = 1 for F(x) = x^(x²) comes from a limit, not from defining 0⁰.
  > Source: MATH275-Week05-Lecture-Notes.pdf

## Examples
- **y = xˣ, x > 0:** y = e^(x ln x), so y′ = e^(x ln x) · (x ln x)′ = e^(x ln x)(1·ln x + x·1/x) (product rule) = xˣ (ln x + 1).
  > Source: Week of October 2 (Week 4).pdf
- **y = (x² + 1)^(sin x):** no need for |·| since x² + 1 > 0. ln y = sin x · ln(x² + 1). Implicit differentiation: y′/y = cos x ln(x² + 1) + sin x · 2x/(x² + 1), so y′ = (x² + 1)^(sin x) [cos x ln(x² + 1) + sin x · 2x/(x² + 1)].
  > Source: Week of October 2 (Week 4).pdf
- **An exponential exponent, y = (2 + x²)^(e^(−x)), x ∈ ℝ:** the base is positive on ℝ. ln y = e^(−x) ln(2 + x²). Differentiate and multiply by y: y′ = (2 + x²)^(e^(−x)) · e^(−x) (2x/(2 + x²) − ln(2 + x²)).
  > Source: MATH275-Week05-Lecture-Notes.pdf
- **y = (3 + cos x)^(x²):** since 3 + cos x ≥ 2, the method is valid for every real x: y′ = (3 + cos x)^(x²) (2x ln(3 + cos x) − x² sin x/(3 + cos x)).
  > Source: MATH275-Week05-Lecture-Notes.pdf
- **A variable power at the edge of its domain, F(x) = x^(x²), x > 0:** logarithmic differentiation gives F′(x)/F(x) = 2x ln x + x, so F′(x) = x^(x²)(2x ln x + x). Since x² ln x → 0 as x → 0⁺, F has a continuous extension F(0) = 1. This extension also has a right derivative at 0: (F(x) − F(0))/x = [(e^(x² ln x) − 1)/(x² ln x)] · x ln x → 1 · 0 = 0. Here (eᵗ − 1)/t → 1 and x ln x → 0; the latter follows by writing ln x/(1/x) and applying l'Hôpital's rule.
  > Source: MATH275-Week05-Lecture-Notes.pdf

## Related Topics
- [Logarithmic Differentiation](logarithmic-differentiation.md)
- [Indeterminate Powers](indeterminate-powers.md)
- [Products and Differences (0·∞, ∞−∞)](products-and-differences.md)
