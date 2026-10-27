# The Definite Integral

## Definition
f is **Riemann integrable on [a, b]** if lim_{n→∞} L(f, n) = lim_{n→∞} U(f, n) (i.e. both limits exist and agree). The common value is written ∫ₐᵇ f(x) dx and called the **definite integral of f on [a, b]**. When this value exists, it is interpreted as the area in question.
> Source: Week of October 23.pdf

For continuous f on [a, b], the lower and upper sums approach the same limit, and this common limit is the definite integral:
∫ₐᵇ f(x) dx = lim_{n→∞} Σᵢ₌₁ⁿ f(xᵢ*) (b − a)/n.
> Source: MATH275-Week08-Lecture-Notes.pdf

## Key Concepts
- **Independence of sample points:** the limit is independent of the sample points xᵢ*.
  > Source: MATH275-Week08-Lecture-Notes.pdf
- **Dummy variable:** the symbol x in ∫ₐᵇ f(x) dx is a dummy variable; replacing it by t does not change the value.
  > Source: MATH275-Week08-Lecture-Notes.pdf
- **Signed area:** the process interprets area below the x-axis as contributing negatively to the total. The Riemann integral is called a *signed* area for this reason.
  > Source: Week of October 23.pdf
- **Summation formulas used:** Σᵢ₌₁ⁿ i = n(n + 1)/2 (the "old formula" attributed to Gauss), and Σᵢ₌₁ⁿ i² = n(n + 1)(2n + 1)/6.
  > Source: Week of October 23.pdf, MATH275-Week08-Lecture-Notes.pdf
- **Telescoping difference for increasing f:** with equal widths, U(f, n) − L(f, n) = Δx Σ (f(xᵢ) − f(xᵢ₋₁)) = Δx (f(b) − f(a)).
  > Source: MATH275-Week08-Lecture-Notes.pdf

## Examples
- **∫₀¹ x dx from Riemann sums:** subdivide [0, 1] into intervals of width Δx = 1/n: [0, 1/n], [1/n, 2/n], …, [(n−1)/n, 1]. For the lower sum, f(x) = x is smallest at the left-hand endpoint, so ℓᵢ = (i − 1)/n. Then L(f, n) = Σ ((i − 1)/n)(1/n) = (1/n²)[0 + 1 + ⋯ + (n − 1)] = (1/n²)·(n − 1)n/2 = (1/2)(n − 1)n/n² → 1/2. Similarly U(f, n) = (1/2)(n + 1)n/n² → 1/2. The limits agree, so ∫₀¹ x dx = 1/2, matching the triangle area.
  > Source: Week of October 23.pdf
- **∫₁³ (x² + 1) dx from the definition:** f is increasing on [1, 3]. With Δx = 2/n and right endpoints xᵢ = 1 + 2i/n,
  U(f, n) = (2/n) Σ [(1 + 2i/n)² + 1] = (2/n) Σ (2 + 4i/n + 4i²/n²) = 4 + (8/n²)·n(n + 1)/2 + (8/n³)·n(n + 1)(2n + 1)/6 = 32/3 + 8/n + 4/(3n²).
  Left endpoints give the lower sum; the difference telescopes: U − L = (2/n)(f(3) − f(1)) = 16/n. So L(f, n) = 32/3 − 8/n + 4/(3n²). Both tend to 32/3, so ∫₁³ (x² + 1) dx = 32/3.
  > Source: MATH275-Week08-Lecture-Notes.pdf

## Related Topics
- [Riemann Sums](riemann-sums.md)
- [Signed Area and Integral Properties](integral-properties.md)
- [FTC Part I](ftc-part-1.md)
