# Closed Interval Method

## Definition
**Fundamental fact about continuous functions:** If f is continuous on the interval [a, b], then f must achieve a global (absolute) max/min on that interval.
> Source: Week of October 16.pdf

**Closed Interval Method:** If f is continuous on [a, b], then f achieves its global maxima and minima at points within the list:
1. Critical points
2. Singular points
3. Endpoints x = a, b

Critical points and singular points are the points that coincide with local extrema.
> Source: Week of October 16.pdf

## Key Concepts
- **Hypotheses:** the method requires f to be continuous on a *closed* interval [a, b]. This is what guarantees a global max and min exist.
  > Source: Week of October 16.pdf
- **Procedure:** (1) Find the critical/singular points. (2) Evaluate f at these and also at a, b. (3) The largest (smallest) value from this list is/are the maxima (resp. minima).
  > Source: Week of October 16.pdf
- **Critical values vs. singular values:** critical values are where f'(x) = 0; singular values are where f'(x) does not exist (DNE). Only those lying in [a, b] are kept as candidates.
  > Source: Week of October 16.pdf
- **Where global extrema can occur (illustrated cases on [a, b]):**
  - Minimum at a critical point, max at an endpoint.
  - Max at a singular point (a sharp corner), min at an endpoint.
  - A constant function: every point is the max/min.
  - An increasing function: both global extrema occur at endpoints.
  > Source: Week of October 16.pdf

## Examples
- **Find the global max/min of f(x) = ∛(x³ − 3x²) on [−5, 5].**
  - By the chain rule, f'(x) = (1/3)(x³ − 3x²)^(−2/3) · (3x² − 6x) = (3x² − 6x) / [3(x³ − 3x²)^(2/3)] = x(x − 2) / [(x²)^(2/3)(x − 3)^(2/3)] = (x − 2) / [x^(1/3)(x − 3)^(2/3)].
  - Critical values: f'(x) = 0 ⇔ x = 2. Singular values: f'(x) DNE ⇔ x = 0, 3. All lie in [−5, 5].
  - Evaluate: f(0) = 0; f(2) = ∛(8 − 12) = ∛(−4); f(3) = ∛(27 − 27) = 0; f(−5) = ∛(−125 − 75) = ∛(−200) (**min**); f(5) = ∛(125 − 75) = ∛50 (**max**).
  - Both global extrema occur at endpoints.
  > Source: Week of October 16.pdf

## Common Misconceptions
- Endpoints must be evaluated too: in the worked example, neither the critical point nor the singular points gave the global extrema; both came from the endpoints x = −5 and x = 5.
  > Source: Week of October 16.pdf

## Related Topics
- [Global Interval Method](global-interval-method.md)
- [Constrained Optimization](constrained-optimization.md)
