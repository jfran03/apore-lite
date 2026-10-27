# Curve Sketching Procedure

## Definition
Procedure for curve sketching: (i) find the domain of f; (ii) plot intercepts; (iii) find asymptotes, both vertical and horizontal; (iv) compute f′(x) to find critical/singular points, intervals of increase/decrease and local extrema; (v) compute f″(x) to find intervals of concavity and inflection points.
> Source: Week of October 9 (Week 5).pdf

Record the domain, intercepts, and symmetry; compute limits at domain boundaries and at infinity; locate critical and singular points and classify extrema from f′; determine concavity from f″; then draw the branches consistently with all of this information.
> Source: MATH275-Week06-Lecture-Notes.pdf

## Key Concepts
- **Horizontal asymptotes:** compute limits at ±∞.
  > Source: Week of October 9 (Week 5).pdf
- **Vertical asymptotes:** determine where one- or two-sided limits are ±∞. Determine the sign of each one-sided infinite limit (e.g. by the sign of "8/0⁺" vs "8/0⁻").
  > Source: Week of October 9 (Week 5).pdf
- **Direction of approach to a horizontal asymptote:** check whether f(x) is above or below the asymptote for large |x| (e.g. f(x) > 1 for large x means y = 1 is approached from above).
  > Source: Week of October 9 (Week 5).pdf, MATH275-Week06-Lecture-Notes.pdf
- **Symmetry:** record whether the function is even (or odd) as part of the sketch.
  > Source: MATH275-Week06-Lecture-Notes.pdf
- **Absolute extrema on unbounded branches:** unbounded branches exclude absolute extrema.
  > Source: MATH275-Week06-Lecture-Notes.pdf

## Examples
- **f(x) = (x² + 4)/(x² − 4):**
  (i) dom(f) = {x | x ≠ ±2} = (−∞, −2) ∪ (−2, 2) ∪ (2, ∞).
  (ii) y-intercept (0, f(0)) = (0, −1). No x-intercepts, since x² + 4 = 0 has no solutions.
  (iii) lim_{x→±∞} f(x) = 1, so y = 1 is a horizontal asymptote; f(x) > 1 for large x, so it is approached from above. Vertical asymptotes x = ±2 with lim_{x→−2⁻} f = ∞, lim_{x→−2⁺} f = −∞, lim_{x→2⁻} f = −∞, lim_{x→2⁺} f = ∞.
  (iv) f′(x) = −16x/(x² − 4)². Increasing on (−∞, −2) and (−2, 0), decreasing on (0, 2) and (2, ∞); local max at x = 0.
  (v) f″(x) = (48x² + 64)/(x² − 4)³. Concave up on (−∞, −2) and (2, ∞), concave down on (−2, 2). No inflection points.
  > Source: Week of October 9 (Week 5).pdf
- **f(x) = (x² + 1)/(x² − 4):** domain ℝ \ {−2, 2}. The function is even. Its only intercept is (0, −1/4), since the numerator is always positive. f(x) = 1 + 5/(x² − 4) → 1 as x → ±∞, so y = 1 is a horizontal asymptote approached from above at both ends. Vertical asymptotes x = ±2 with f → +∞ as x → −2⁻, −∞ as x → −2⁺, −∞ as x → 2⁻, +∞ as x → 2⁺. f′(x) = −10x/(x² − 4)², f″(x) = 10(3x² + 4)/(x² − 4)³. Signs on (−∞, −2), (−2, 0), (0, 2), (2, ∞): f′ is +, +, −, −; f″ is +, −, −, +. So f increases on (−∞, −2) and (−2, 0) and decreases on (0, 2) and (2, ∞). The only critical point is 0, a strict local max at (0, −1/4). No singular points (±2 are outside the domain). Concave up on (−∞, −2) and (2, ∞), down on (−2, 2). No inflection points, since the only concavity changes occur where f is undefined. The unbounded branches exclude absolute extrema.
  > Source: MATH275-Week06-Lecture-Notes.pdf
- **g(x) = xe^{−x}** and **p(x) = x³ − 6x² + 9x** are also fully analysed (extrema, concavity, asymptotes/end behaviour); see [Concavity and the Second Derivative Test](concavity-and-second-derivative-test.md) and [Monotonicity and the First Derivative Test](monotonicity-and-first-derivative-test.md).
  > Source: MATH275-Week06-Lecture-Notes.pdf

## Common Misconceptions
- **Inflection points at asymptotes:** concavity may change across a vertical asymptote, but there is no inflection point there because f is undefined.
  > Source: MATH275-Week06-Lecture-Notes.pdf, Week of October 9 (Week 5).pdf

## Related Topics
- [Extreme Values, Critical and Singular Points](extreme-values.md)
- [Monotonicity and the First Derivative Test](monotonicity-and-first-derivative-test.md)
- [Concavity and the Second Derivative Test](concavity-and-second-derivative-test.md)
