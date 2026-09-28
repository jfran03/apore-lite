# Derivative of an Inverse Function

## Definition
A function f is invertible if there is a function g so that g(f(x)) = x for all x in dom f and f(g(y)) = y for all y in ran f. We call g the inverse of f and write g = f⁻¹ (this is not the function 1/f).
> Source: Week of September 25 (Week 3) .pdf

## Key Concepts
- **Domain and range swap:** dom(f⁻¹) = ran(f) and ran(f⁻¹) = dom(f).
  > Source: Week of September 25 (Week 3) .pdf
- **Graph:** the graph of f⁻¹ is the graph of f reflected over y = x.
  > Source: Week of September 25 (Week 3) .pdf
- **Invertibility criterion:** f is invertible if and only if f is one-to-one (f passes the horizontal line test).
  > Source: Week of September 25 (Week 3) .pdf
- **Inverse Function Theorem:** suppose f is differentiable on an open interval I with f'(x) ≠ 0 on I. Then f⁻¹ is also differentiable on f(I) and (f⁻¹)'(f(x)) = 1/f'(x) for all x in I. Replacing f(x) with x (so x becomes f⁻¹(x)) gives (f⁻¹)'(x) = 1 / f'(f⁻¹(x)) for any x in ran(f).
  > Source: Week of September 25 (Week 3) .pdf
- **Lecture-notes version (hypotheses):** if f is differentiable and one-to-one on an interval with f'(t) ≠ 0 at the corresponding point t = f⁻¹(x), then (f⁻¹)'(x) = 1/f'(f⁻¹(x)) where the inverse is defined and the denominator is nonzero. At a corresponding pair f(a) = b, (f⁻¹)'(b) = 1/f'(a).
  > Source: MATH275-Week04-Lecture-Notes.pdf
- **Derivation:** since f(f⁻¹(x)) = x, the chain rule gives f'(f⁻¹(x)) (f⁻¹)'(x) = 1. (Equivalently, y = f⁻¹(x) can be written f(y) = x; differentiating implicitly gives f'(y) dy/dx = 1, so dy/dx = 1/f'(y).)
  > Source: MATH275-Week04-Lecture-Notes.pdf, Week of September 25 (Week 3) .pdf
- **Geometric meaning:** the slope of the tangent line to f⁻¹ at f(a) is the reciprocal of the slope of the tangent line to f at a. A tangent with slope m ≠ 0 reflects to one with slope 1/m.
  > Source: Week of September 25 (Week 3) .pdf, MATH275-Week04-Lecture-Notes.pdf
- **When f'(a) = 0:** the reciprocal formula does not apply; the inverse may still exist but can have a vertical tangent. For f(x) = x³, which is one-to-one, f⁻¹(x) = ∛x has a vertical tangent at the origin.
  > Source: MATH275-Week04-Lecture-Notes.pdf

## Examples
- **f(x) = x⁵ + 2x + 1, find (f⁻¹)'(4):** f'(x) = 5x⁴ + 2 > 0, so f is strictly increasing. Since f(1) = 4, f⁻¹(4) = 1, and f'(1) = 7. Hence (f⁻¹)'(4) = 1/7, with no explicit formula for f⁻¹ needed.
  > Source: MATH275-Week04-Lecture-Notes.pdf
- **f(x) = x⁵ + 3x, find (f⁻¹)'(4):** f'(x) = 5x⁴ + 3 ≥ 3 > 0, so f is always strictly increasing, passes the horizontal line test, and is invertible. f⁻¹(4) is the solution of x⁵ + 3x = 4, which can have only one solution; x = 1 works. So (f⁻¹)'(4) = 1/f'(1) = 1/(5 + 3) = 1/8.
  > Source: Week of September 25 (Week 3) .pdf
- **Exit check:** if f(2) = −1 and f'(2) = 5, then f⁻¹(−1) = 2 and (f⁻¹)'(−1) = 1/f'(2) = 1/5.
  > Source: MATH275-Week04-Lecture-Notes.pdf

## Common Misconceptions
- **Inverse is not reciprocal:** f⁻¹ means the inverse function, not 1/f. For example sin⁻¹ x = arcsin x, while 1/sin x = csc x.
  > Source: MATH275-Week04-Lecture-Notes.pdf
- **Corresponding inputs:** (f⁻¹)'(b) = 1/f'(a) uses corresponding inputs f(a) = b; it is not the reciprocal of f'(b) in general.
  > Source: MATH275-Week04-Lecture-Notes.pdf

## Related Topics
- [Implicit Differentiation](implicit-differentiation.md)
- [Inverse Trigonometric Derivatives](inverse-trig-derivatives.md)
- [Inverse Hyperbolic Functions](inverse-hyperbolic-functions.md)
