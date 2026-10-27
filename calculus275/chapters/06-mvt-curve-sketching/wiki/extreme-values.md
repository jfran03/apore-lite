# Extreme Values, Critical and Singular Points

## Definition
A function f has an absolute maximum at c in its domain D if f(x) ≤ f(c) for every x ∈ D. A local maximum requires this inequality only sufficiently close to an interior point c. Reverse the inequality for minima. An extremum's location is c; its value is f(c).
> Source: MATH275-Week06-Lecture-Notes.pdf

Let f be a function with domain D. (i) f has a global/absolute maximum f(c) if f(c) ≥ f(x) for all x ∈ D. (ii) f has a global/absolute minimum f(c) if f(c) ≤ f(x) for all x ∈ D. (iii) f has a local maximum (resp. local minimum) f(c) if there is an open interval I in D so that f(c) ≥ f(x) (resp. f(c) ≤ f(x)) for all x ∈ I.
> Source: Week of October 9 (Week 5).pdf

## Key Concepts
- **Endpoint convention:** in this course, endpoints are not local extrema. Global (absolute) extrema at endpoints are allowed.
  > Source: MATH275-Week06-Lecture-Notes.pdf, Week of October 9 (Week 5).pdf
- **Critical point:** an interior domain point c where f′(c) = 0.
  > Source: MATH275-Week06-Lecture-Notes.pdf, Week of October 9 (Week 5).pdf
- **Singular point:** an interior domain point c where f′(c) does not exist. This happens, for example, when f is not continuous at c, f has a cusp at c, or f has a point of infinite tangency (vertical tangent) at c.
  > Source: MATH275-Week06-Lecture-Notes.pdf, Week of October 9 (Week 5).pdf
- **Points outside the domain are not singular points:** if f′ appears to be undefined at a point that is not in the domain of f (e.g. x = ±2 for (x² + 4)/(x² − 4)), it cannot be called a singular point. There may be a vertical asymptote there instead.
  > Source: Week of October 9 (Week 5).pdf
- **Extreme Value Theorem (EVT):** a continuous function on a closed bounded interval [a, b] attains an absolute maximum and an absolute minimum.
  > Source: MATH275-Week06-Lecture-Notes.pdf
- **Fermat's theorem:** if c is an interior local extremum and f′(c) exists, then f′(c) = 0.
  > Source: MATH275-Week06-Lecture-Notes.pdf
- **Local extrema occur only at critical or singular points:** if f has a local max/min at x = c, then either f′(c) = 0 or f′(c) does not exist.
  > Source: Week of October 9 (Week 5).pdf
- **Unbounded functions may have no global max:** a function with lim_{x→b⁻} f(x) = ∞ is unbounded above and has no global maximum.
  > Source: Week of October 9 (Week 5).pdf
- **Closed interval method:** to find absolute extrema of a continuous function on [a, b], evaluate f at all critical and singular points in (a, b) and at both endpoints, then compare the values.
  > Source: MATH275-Week06-Lecture-Notes.pdf
- **Why the closed interval method works:** the EVT guarantees absolute extrema exist. Any interior absolute extremum is also a local extremum, so Fermat's theorem says its derivative must be zero if it exists. Thus an interior extremum must be a critical or singular point; the remaining possibilities are the endpoints. These are candidates, not guaranteed extrema.
  > Source: MATH275-Week06-Lecture-Notes.pdf
- **EVT hypotheses are sufficient, not necessary:** they guarantee existence, but a function may have absolute extrema even when those hypotheses fail.
  > Source: MATH275-Week06-Lecture-Notes.pdf

## Examples
- **f(x) = x³ (critical point, no extremum):** f′(0) = 0, but f(x) < f(0) for x < 0 and f(x) > f(0) for x > 0. Thus 0 is neither a local maximum nor a local minimum.
  > Source: MATH275-Week06-Lecture-Notes.pdf
- **f(x) = |x| (extremum at a singular point):** |x| has an absolute minimum at 0, where its derivative does not exist.
  > Source: MATH275-Week06-Lecture-Notes.pdf
- **f(x) = ∛x (singular point, no extremum):** f has a singular point at x = 0 but no local extremum there. This shows the converse of "local extrema occur at critical or singular points" does not hold.
  > Source: Week of October 9 (Week 5).pdf
- **f(x) = x^{2/3} − x on [−1, 8], where x^{2/3} = (∛x)²:** f is continuous on [−1, 8]. For x ≠ 0, f′(x) = 2/(3∛x) − 1, and f′(x) = 0 ⟺ x = 8/27, the only critical point. At 0 the difference quotient (f(h) − f(0))/h = 1/∛h − 1 tends to −∞ as h → 0⁻ and to +∞ as h → 0⁺, so f′(0) does not exist and 0 is a singular point. Candidate values: f(−1) = 2, f(0) = 0, f(8/27) = 4/27, f(8) = −4. The absolute maximum is 2 at x = −1; the absolute minimum is −4 at x = 8.
  > Source: MATH275-Week06-Lecture-Notes.pdf
- **Graph on [a, b] with labelled points:** the left endpoint a is not a local min (by convention); an interior peak is a local max; an interior valley is both a local and global min; the right endpoint b, the highest point, is a global but not local max.
  > Source: Week of October 9 (Week 5).pdf

## Common Misconceptions
- **A critical point need not be an extremum:** f(x) = x³ has f′(0) = 0 but no extremum at 0.
  > Source: MATH275-Week06-Lecture-Notes.pdf
- **Candidates are not guaranteed extrema:** critical points, singular points, and endpoints are only candidates; their values must be compared.
  > Source: MATH275-Week06-Lecture-Notes.pdf
- **Calling points outside the domain singular:** x = ±2 for (x² + 4)/(x² − 4) are not in the domain, so they are not singular points.
  > Source: Week of October 9 (Week 5).pdf

## Related Topics
- [Rolle's Theorem and the Mean Value Theorem](rolle-and-mean-value-theorem.md)
- [Monotonicity and the First Derivative Test](monotonicity-and-first-derivative-test.md)
- [Concavity and the Second Derivative Test](concavity-and-second-derivative-test.md)
