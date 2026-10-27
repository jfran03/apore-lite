# Rolle's Theorem and the Mean Value Theorem

## Definition
**Rolle's theorem.** Let a < b. If f is continuous on [a, b], differentiable on (a, b), and f(a) = f(b), then some c ∈ (a, b) satisfies f′(c) = 0.
> Source: MATH275-Week06-Lecture-Notes.pdf

**Mean Value Theorem (MVT).** If f is continuous on [a, b] and differentiable on (a, b), then there is at least one c ∈ (a, b) with
f′(c) = (f(b) − f(a))/(b − a).
> Source: MATH275-Week06-Lecture-Notes.pdf, Week of October 9 (Week 5).pdf

## Key Concepts
- **Intuitive idea:** if we travel 100 km in 1 hour, we achieve the average rate of change (100 km/hr) at least once during the trip, provided our path of travel is a differentiable function.
  > Source: Week of October 9 (Week 5).pdf
- **Geometric meaning:** the average rate of change on [a, b] is (f(b) − f(a))/(b − a), the slope of the secant line. f′(x) is the slope of the tangent at x. The MVT says some tangent line has the same slope as the secant line joining the endpoints, i.e. instantaneous rate of change = average rate of change somewhere in (a, b).
  > Source: MATH275-Week06-Lecture-Notes.pdf, Week of October 9 (Week 5).pdf
- **At least one, not exactly one:** the theorem guarantees at least one such c, not necessarily exactly one. For a linear function, every c ∈ (a, b) works.
  > Source: MATH275-Week06-Lecture-Notes.pdf
- **Proof of Rolle's theorem:** the EVT supplies a maximum and a minimum. If f is constant, every interior point works. Otherwise some value differs from the common endpoint value, so a maximum or a minimum occurs at an interior point. Fermat's theorem gives a zero derivative there.
  > Source: MATH275-Week06-Lecture-Notes.pdf
- **Proof of the MVT:** put m = (f(b) − f(a))/(b − a) and h(x) = f(x) − f(a) − m(x − a). This subtracts the secant line y = f(a) + m(x − a) from the graph of f, making both endpoint heights zero. h is continuous on [a, b], differentiable on (a, b), and h(a) = h(b) = 0. Rolle's theorem gives h′(c) = f′(c) − m = 0.
  > Source: MATH275-Week06-Lecture-Notes.pdf
- **Checking hypotheses:** before applying the MVT, verify continuity on the closed interval [a, b] and differentiability on the open interval (a, b), and check that any c found lies in (a, b).
  > Source: MATH275-Week06-Lecture-Notes.pdf

## Examples
- **f(x) = √x on [1, 9]:** f is continuous on [1, 9] and differentiable on (1, 9). The secant slope is (3 − 1)/(9 − 1) = 1/4. Then 1/(2√c) = 1/4 ⟺ c = 4, which lies in (1, 9) and is the only solution.
  > Source: MATH275-Week06-Lecture-Notes.pdf
- **f(x) = x³ − x on [−2, 3]:** the secant slope is (f(3) − f(−2))/(3 − (−2)) = ((27 − 3) − (−8 + 2))/5 = 30/5 = 6. With f′(x) = 3x² − 1, solving 3c² − 1 = 6 gives 3c² = 7, so c = ±√(7/3). There are two values of c.
  > Source: Week of October 9 (Week 5).pdf
- **Hypothesis check with |x| on [−1, 1]:** the secant slope is 0, but the derivative is −1 or 1 wherever it exists. The MVT cannot be applied because differentiability fails at 0.
  > Source: MATH275-Week06-Lecture-Notes.pdf

## Common Misconceptions
- **Assuming c is unique:** the MVT guarantees at least one c; x³ − x on [−2, 3] has two.
  > Source: MATH275-Week06-Lecture-Notes.pdf, Week of October 9 (Week 5).pdf
- **Ignoring the differentiability hypothesis:** |x| on [−1, 1] has no point with derivative equal to the secant slope 0, because it is not differentiable at 0.
  > Source: MATH275-Week06-Lecture-Notes.pdf

## Related Topics
- [Consequences and Applications of the MVT](consequences-of-mvt.md)
- [Extreme Values, Critical and Singular Points](extreme-values.md)
