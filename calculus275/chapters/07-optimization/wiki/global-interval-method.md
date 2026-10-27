# Global Interval Method

## Definition
**Global Interval Method:** Used on intervals like (a, b), (a, b], [a, b), (−∞, b), (−∞, b], (a, ∞), [a, ∞) when f has **only one critical/singular value**.

If f has a local max in this case, it must be the global max. There may be no global min, or it could occur at an endpoint (if there is one). The analogous statement for the global min holds as well.
> Source: Week of October 16.pdf

## Key Concepts
- **When to use it:** the interval is not closed and bounded (open, half-open, or infinite), so the closed interval method does not apply. The method requires that f has exactly one critical/singular value on the interval.
  > Source: Week of October 16.pdf
- **Single local extremum ⇒ global extremum:** with only one critical/singular value, a local min there is the global min (and a local max there is the global max).
  > Source: Week of October 16.pdf
- **The other extremum may not exist:** on a non-closed interval, the opposite global extremum may fail to exist, e.g. when f(x) → ∞ toward an excluded endpoint.
  > Source: Week of October 16.pdf
- **Classifying the single point:** use the first derivative test (sign chart of f'(x) with test values on each side) to decide whether the point is a local min or local max.
  > Source: Week of October 16.pdf

## Examples
- **Graph on [a, b) (correction from lecture):** a single local min at a critical point, hence the global min. There is **no** max since lim_{x→b⁻} f(x) = ∞.
  > Source: Week of October 16.pdf
- **Graph on (a, b):** minimum at a singular point (a corner) and no maximum; the graph rises toward vertical asymptotes at both a and b.
  > Source: Week of October 16.pdf
- **Find the max/min (if they exist) for f(x) = 4x² + 1/x on (0, ∞).**
  - Note lim_{x→0⁺} f(x) = ∞ and lim_{x→∞} f(x) = ∞.
  - f'(x) = 8x − 1/x², which exists on (0, ∞).
  - f'(x) = 0 ⇔ 8x = 1/x² ⇔ x³ = 1/8 ⇔ x = 1/2, the only critical point.
  - Sign of f'(x): try x = 1/4: f'(1/4) = 2 − 16 = −14 < 0; try x = 10: positive. So f decreases then increases.
  - By the first derivative test there is a local min at x = 1/2. By the global interval method, f(1/2) is also the global min. (There is no global max.)
  > Source: Week of October 16.pdf

## Related Topics
- [Closed Interval Method](closed-interval-method.md)
- [Constrained Optimization](constrained-optimization.md)
