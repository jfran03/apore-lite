# Best Linear Approximation

## Definition
Among all lines through (a, f(a)), the tangent line is the one that best approximates f near
x = a. Consider any line passing through (a, f(a)) with slope m, given by y − f(a) = m(x − a).
We wish to minimize the distance between y = f(x) and this line **near** x = a:

    D := | f(x) − f(a) − m(x − a) |
> Source: Week 2 Video - Linear Approximation and Differentials .pdf

## Key Concepts
- **Key Fact:** m = f'(a) is the unique value that minimizes D.
  > Source: Week 2 Video - Linear Approximation and Differentials .pdf
- **Meaning:** The tangent line L is the best linear approximation to f at x = a.
  > Source: Week 2 Video - Linear Approximation and Differentials .pdf
- **Other lines through the same point are worse:** a different line through (a, f(a)) with a
  different slope opens a large gap between the line and the curve near a, while the tangent
  line's gap stays small.
  > Source: Week 2 Video - Linear Approximation and Differentials .pdf
- **This is what justifies the differential approximation:** because the tangent line is the
  best linear approximation to f near x, dy ≈ Δy.
  > Source: Week 2 Video - Linear Approximation and Differentials .pdf

## Related Topics
- [Linear Approximation](linear-approximation.md)
- [Differentials and Exact Changes](differentials-and-exact-changes.md)
