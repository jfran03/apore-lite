# Logarithmic Differentiation

## Definition
For a positive differentiable function y, the chain rule gives (ln y)′ = y′/y. Taking a logarithm converts a product into a sum and a power into a product. More generally, on an interval where y is differentiable and never zero, use ln |y|: (ln |y|)′ = y′/y.
> Source: MATH275-Week05-Lecture-Notes.pdf

Idea of logarithmic differentiation: from y = f(x), take ln |y| = ln |f(x)|, then implicitly differentiate both sides to get y′/y = f′(x)/f(x), so y′ = y f′(x)/f(x).
> Source: Week of October 2 (Week 4).pdf

## Key Concepts
- **Logarithm laws used:** ln(ab) = ln a + ln b and ln aʳ = r ln a, valid for a > 0 and b > 0.
  > Source: Week of October 2 (Week 4).pdf
- **Derivative of ln |x|:** writing ln |x| = ln x for x > 0 and ln(−x) for x < 0, the chain rule gives y′ = 1/x for x > 0 and (1/(−x))·(−1) = 1/x for x < 0. So (ln |x|)′ = 1/x for any x ≠ 0.
  > Source: Week of October 2 (Week 4).pdf
- **Why absolute values:** taking ln |y| (rather than ln y) lets the method work on an interval where y is differentiable and never zero, even if y is negative there. When the function is known to be positive (e.g. x² + 1 > 0), there is no need for absolute values.
  > Source: MATH275-Week05-Lecture-Notes.pdf, Week of October 2 (Week 4).pdf
- **A reliable procedure:** (1) check the domain and sign; (2) take ln |y| or ln y; (3) simplify using logarithm laws valid on that domain; (4) differentiate; (5) multiply by y; (6) substitute the original expression.
  > Source: MATH275-Week05-Lecture-Notes.pdf
- **Equivalent formulation:** y = f(x) = e^(ln f(x)), so by the chain rule y′ = e^(ln f(x)) · f′(x)/f(x).
  > Source: Week of October 2 (Week 4).pdf
- **When to use it:** for complicated products and powers.
  > Source: Week of October 2 (Week 4).pdf

## Examples
- **A quotient with several factors (x > 0):** y = (x + 2)³ √(x² + 4) / (x eˣ). Then ln y = 3 ln(x + 2) + ½ ln(x² + 4) − ln x − x, and y′ = y (3/(x + 2) + x/(x² + 4) − 1/x − 1). The formula holds on x > 0, where all logarithms displayed are defined.
  > Source: MATH275-Week05-Lecture-Notes.pdf
- **y = (3x + 1)¹⁰ (x² − 1)⁵ / (2x − 1)¹³:** by log laws, ln |y| = 10 ln |3x + 1| + 5 ln |x² − 1| − 13 ln |2x − 1|. Implicit differentiation gives y′/y = 10·3/(3x + 1) + 5·2x/(x² − 1) − 13·2/(2x − 1). Solving for y′ in terms of x: y′ = [(3x + 1)¹⁰ (x² − 1)⁵ / (2x − 1)¹³] · (30/(3x + 1) + 10x/(x² − 1) − 26/(2x − 1)), where the bracketed factor is y.
  > Source: Week of October 2 (Week 4).pdf

## Related Topics
- [Variable Powers](variable-powers.md)
- [Indeterminate Powers](indeterminate-powers.md)
