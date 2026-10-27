# Concavity, Inflection Points, and the Second Derivative Test

## Definition
**Secant-line definition.** A function is concave upward on an interval when, between any two points on its graph, the graph lies on or below the secant segment joining those points. It is concave downward when the graph lies on or above every such segment. For a differentiable function, these conditions correspond to f′ being nondecreasing and nonincreasing, respectively.
> Source: MATH275-Week06-Lecture-Notes.pdf

**Tangent-line definition.** Suppose f is differentiable on an interval I (so f is also continuous). (i) f is concave up on I if f lies above its tangent lines on I. (ii) f is concave down on I if f lies below its tangent lines on I.
> Source: Week of October 9 (Week 5).pdf

**Inflection point.** An inflection point (c, f(c)) is a point where f is continuous and the concavity changes across c (concave up on one side of c and concave down on the other).
> Source: MATH275-Week06-Lecture-Notes.pdf, Week of October 9 (Week 5).pdf

## Key Concepts
- **Concavity describes slopes, not values:** concavity describes how the slopes change, not whether the function values increase or decrease.
  > Source: MATH275-Week06-Lecture-Notes.pdf
- **Concavity and the second derivative:** suppose f is twice differentiable on an interval I. If f″ > 0 on I, f is concave up on I (acceleration). If f″ < 0 on I, f is concave down on I (deceleration). If f″(c) = 0 or f″(c) does not exist, f *may* have an inflection point at x = c.
  > Source: Week of October 9 (Week 5).pdf, MATH275-Week06-Lecture-Notes.pdf
- **A zero of f″ is not enough:** a zero of f″ at one point does not by itself determine concavity or imply an inflection point. Check zeros of f″ and points where f″ is undefined, then verify the change in concavity.
  > Source: MATH275-Week06-Lecture-Notes.pdf
- **Split at vertical asymptotes:** still subdivide by vertical asymptotes for concavity testing; f may have different concavities on either side of a vertical asymptote. A point where f is not defined cannot be an inflection point even if concavity changes across it.
  > Source: Week of October 9 (Week 5).pdf
- **Second derivative test:** if f is twice differentiable near c and f′(c) = 0, then f″(c) > 0 implies a strict local minimum and f″(c) < 0 implies a strict local maximum. If f″(c) = 0, the test gives no conclusion.
  > Source: MATH275-Week06-Lecture-Notes.pdf, Week of October 9 (Week 5).pdf
- **Why f″(c) = 0 is inconclusive:** at c = 0, each of x⁴, −x⁴ and x³ has first and second derivatives equal to zero. Yet x⁴ has a strict local min, −x⁴ a strict local max, and x³ neither. When the test is inconclusive, examine the signs of f′ on either side instead.
  > Source: MATH275-Week06-Lecture-Notes.pdf

## Examples
- **p(x) = x³ − 6x² + 9x:** p″(x) = 6x − 12. Concave down on (−∞, 2), up on (2, ∞), inflection point (2, 2).
  > Source: MATH275-Week06-Lecture-Notes.pdf
- **u(x) = x⁴ (not an inflection point):** u″(x) = 12x² > 0 on both sides of 0, so the graph is concave up on both sides and (0, 0) is not an inflection point even though u″(0) = 0.
  > Source: MATH275-Week06-Lecture-Notes.pdf
- **v(x) = x|x| (inflection point without f″):** v is continuous at 0, v(x) = −x² for x < 0 and x² for x > 0, so v″ = −2 for x < 0 and 2 for x > 0. Thus (0, 0) is an inflection point. v′(0) = lim_{h→0}|h| = 0, but v″(0) does not exist since v′(x) = 2|x| has unequal one-sided derivatives at 0.
  > Source: MATH275-Week06-Lecture-Notes.pdf
- **g(x) = xe^{−x}:** g′(x) = e^{−x}(1 − x), g″(x) = e^{−x}(x − 2). g increases on (−∞, 1) and decreases on (1, ∞), giving an absolute maximum at (1, e^{−1}); no local minimum. Concave down on (−∞, 2), up on (2, ∞), inflection point (2, 2e^{−2}). As x → +∞, l'Hôpital's rule gives x/eˣ → 0, so y = 0 is a horizontal asymptote approached from above. As x → −∞, xe^{−x} → −∞, so there is no absolute minimum.
  > Source: MATH275-Week06-Lecture-Notes.pdf
- **q(x) = x⁴ − 4x² (exit check):** q′(x) = 4x(x² − 2), q″(x) = 12x² − 8. Critical points −√2, 0, √2. q″(0) = −8 < 0, so (0, 0) is a strict local max. q″(±√2) = 16 > 0, so (±√2, −4) are strict local minima; they are also absolute minima because q(x) = (x² − 2)² − 4 ≥ −4. No absolute maximum since q → +∞ as |x| → ∞. q″ < 0 for |x| < √(2/3) and > 0 for |x| > √(2/3), so the inflection points are (±√(2/3), −20/9).
  > Source: MATH275-Week06-Lecture-Notes.pdf
- **f(x) = (x² + 4)/(x² − 4):** f′(x) = −16x/(x² − 4)², f″(x) = (48x² + 64)/(x² − 4)³. f″(x) ≠ 0 since 48x² + 64 > 0, and f″ exists on the domain of f. Sign chart split at ±2: f″ > 0 on (−∞, −2), < 0 on (−2, 2), > 0 on (2, ∞). So f is concave up on (−∞, −2) and (2, ∞), concave down on (−2, 2), with no inflection points.
  > Source: Week of October 9 (Week 5).pdf

## Common Misconceptions
- **"f″(c) = 0 means inflection point":** false; x⁴ has u″(0) = 0 but no inflection point.
  > Source: MATH275-Week06-Lecture-Notes.pdf
- **"f″(c) = 0 at a critical point means no extremum":** false; the second derivative test is simply inconclusive there (x⁴, −x⁴, x³).
  > Source: MATH275-Week06-Lecture-Notes.pdf
- **Counting asymptotes as inflection points:** a concavity change across a vertical asymptote is not an inflection point, since f is not defined there.
  > Source: Week of October 9 (Week 5).pdf, MATH275-Week06-Lecture-Notes.pdf

## Related Topics
- [Monotonicity and the First Derivative Test](monotonicity-and-first-derivative-test.md)
- [Curve Sketching Procedure](curve-sketching.md)
