# Monotonicity and the First Derivative Test

## Definition
**First derivative test.** Suppose f is continuous at an interior point c and differentiable immediately to either side.
- f′ changes from + to − at c: a strict local maximum occurs at c.
- f′ changes from − to + at c: a strict local minimum occurs at c.
- Same strict sign on both sides: no local extremum occurs at c.

The test also applies when f′(c) does not exist.
> Source: MATH275-Week06-Lecture-Notes.pdf

Suppose f is continuous on an interval I and has a singular or critical point at x = c. (i) If f′(x) > 0 to the left of c and f′(x) < 0 to the right, f has a local maximum at x = c. (ii) If f′(x) < 0 to the left and f′(x) > 0 to the right, f has a local minimum at x = c.
> Source: Week of October 9 (Week 5).pdf

## Key Concepts
- **Building a sign chart:** split the domain at critical points, singular points, and points excluded from the domain. Determine the sign of f′ on each resulting interval.
  > Source: MATH275-Week06-Lecture-Notes.pdf
- **Test points:** use a number line for the sign of f′(x), taking a test point in each subinterval to determine the sign. A sign test at one point represents the whole interval only after verifying that the derivative cannot change sign there, for example from its factorization.
  > Source: Week of October 9 (Week 5).pdf, MATH275-Week06-Lecture-Notes.pdf
- **Approach to finding local extrema:** (1) find all critical/singular values; (2) use the first derivative test to classify them.
  > Source: Week of October 9 (Week 5).pdf
- **Works at singular points too:** a local max or min can occur at a singular point (a corner/cusp), as well as at a critical point (smooth peak or valley).
  > Source: Week of October 9 (Week 5).pdf
- **Reading a graph of f′:** keep the height of f′ separate from whether f′ is rising or falling.
  - Where f′ is above the axis (f′ > 0), f is increasing; below the axis (f′ < 0), f is decreasing.
  - Where f′ is increasing, f is concave upward; where f′ is decreasing, f is concave downward. A positive but decreasing f′ means f is increasing while its slopes get smaller.
  - A zero of f′ locates a critical point of f. + to − gives a local max, − to + gives a local min. A zero without a sign change need not give an extremum.
  - The graph of f′ alone does not determine the height f(c): adding a constant to f leaves f′ unchanged.
  > Source: MATH275-Week06-Lecture-Notes.pdf

## Examples
- **f(x) = x³ − x:** f′(x) = 3x² − 1 = 3(x − 1/√3)(x + 1/√3). Test points: f′(−10) > 0, f′(0) = −1 < 0, f′(10) > 0. So f is strictly increasing on (−∞, −1/√3) and on (1/√3, ∞), and strictly decreasing on (−1/√3, 1/√3).
  > Source: Week of October 9 (Week 5).pdf
- **p(x) = x³ − 6x² + 9x:** factor p(x) = x(x − 3)² and p′(x) = 3(x − 1)(x − 3). Signs of p′: + on (−∞, 1), − on (1, 3), + on (3, ∞). So (1, 4) is a strict local maximum and (3, 0) a strict local minimum. Intercepts (0, 0) and (3, 0); the graph crosses the axis at 0 and touches it at 3. The cubic leading term gives p → −∞ as x → −∞ and p → +∞ as x → +∞, so neither local extremum is absolute on ℝ.
  > Source: MATH275-Week06-Lecture-Notes.pdf
- **f(x) = (x² + 4)/(x² − 4):** by the quotient rule f′(x) = [2x(x² − 4) − (x² + 4)2x]/(x² − 4)² = −16x/(x² − 4)². f′(x) = 0 only at x = 0, the only critical point. f′ appears undefined at x = ±2, but these are not in the domain, so they are not singular points (there are vertical asymptotes there). The sign chart (split at −2, 0, 2) shows f increasing on (−∞, −2) and (−2, 0), decreasing on (0, 2) and (2, ∞). The first derivative test gives a local max at x = 0.
  > Source: Week of October 9 (Week 5).pdf
- **Quick check:** if f′ > 0 and f′ is decreasing on an interval, is f decreasing? No. It is increasing and concave downward.
  > Source: MATH275-Week06-Lecture-Notes.pdf

## Common Misconceptions
- **Confusing the height of f′ with its slope:** f′ > 0 tells you f increases; f′ increasing tells you f is concave up. These are different facts.
  > Source: MATH275-Week06-Lecture-Notes.pdf
- **Assuming every zero of f′ is an extremum:** a zero without a sign change need not give an extremum.
  > Source: MATH275-Week06-Lecture-Notes.pdf
- **Forgetting to split at points excluded from the domain:** sign charts must also be split at points not in the domain, e.g. x = ±2 for (x² + 4)/(x² − 4).
  > Source: MATH275-Week06-Lecture-Notes.pdf, Week of October 9 (Week 5).pdf

## Related Topics
- [Consequences and Applications of the MVT](consequences-of-mvt.md)
- [Extreme Values, Critical and Singular Points](extreme-values.md)
- [Concavity and the Second Derivative Test](concavity-and-second-derivative-test.md)
- [Curve Sketching Procedure](curve-sketching.md)
