# Overestimates and Underestimates

## Definition
An underestimate means L_a(x) < f(x); an overestimate means L_a(x) > f(x). Concavity, not
whether the function is increasing or decreasing, determines the tangent's position.
> Source: MATH275-Week03-Lecture-Notes.pdf

| Shape between a and x | Tangent-line position | Consequence |
|---|---|---|
| Concave up, f'' > 0 | L_a(x) lies below f(x) | underestimate |
| Concave down, f'' < 0 | L_a(x) lies above f(x) | overestimate |
> Source: MATH275-Week03-Lecture-Notes.pdf

## Key Concepts
- **The sign condition must hold on the whole interval.** These sign conditions must hold
  throughout the interval between a and the input being approximated.
  > Source: MATH275-Week03-Lecture-Notes.pdf
- **Exact agreement at the base point.** At x = a, the tangent line and the function agree exactly.
  > Source: MATH275-Week03-Lecture-Notes.pdf
- **The rule works on either side of a.** Concave-up graphs bend above their tangent lines, while
  concave-down graphs bend below them.
  > Source: MATH275-Week03-Lecture-Notes.pdf
- **Connection to Taylor's theorem.** Since (x − a)² > 0, the identity
  f(x) − L_a(x) = f''(ξ)(x − a)²/2 also explains the concavity test.
  > Source: MATH275-Week03-Lecture-Notes.pdf

## Examples
- **Reciprocal example.** For f(x) = 1/x, f''(x) = 2/x³ > 0 on (0, ∞). Therefore 0.245 is an
  underestimate of 1/4.08.
  > Source: MATH275-Week03-Lecture-Notes.pdf
- **Arctangent example.** f''(x) = −2x/(1 + x²)² < 0 for x > 0, so π/4 + 0.02 is an overestimate
  of arctan(1.04).
  > Source: MATH275-Week03-Lecture-Notes.pdf
- **Exponential example.** For f(x) = e^x with a = 0, L_0(x) = 1 + x and e^(−0.03) ≈ 0.97.
  Because f''(x) = e^x > 0, the graph is concave up and 0.97 is an underestimate, even though
  the target input lies to the left of a.
  > Source: MATH275-Week03-Lecture-Notes.pdf
- **Logarithm example.** For f(x) = ln x on [1, 1.04], f''(t) = −1/t² < 0, so the estimate 0.04
  is an overestimate of ln(1.04).
  > Source: MATH275-Week03-Lecture-Notes.pdf

## Common Misconceptions
- **Using increasing/decreasing instead of concavity.** Concavity, not whether the function is
  increasing or decreasing, determines the tangent's position.
  > Source: MATH275-Week03-Lecture-Notes.pdf
- **Assuming the target must lie to the right of a.** The rule works on either side of a; the
  exponential example has its target input to the left of a and is still an underestimate.
  > Source: MATH275-Week03-Lecture-Notes.pdf
- **Applying the test when concavity changes.** If concavity changes, this test alone does not
  determine whether the approximation is an overestimate or an underestimate.
  > Source: MATH275-Week03-Lecture-Notes.pdf

## Related Topics
- [Linear Approximation](linear-approximation.md)
- [Taylor's Remainder Bound](taylors-remainder-bound.md)
