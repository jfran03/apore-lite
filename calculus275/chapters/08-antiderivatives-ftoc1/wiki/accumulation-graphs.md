# Reading an Accumulation Function from a Graph

## Definition
For continuous f and A(x) = ∫꜀ˣ f(t) dt, FTC Part I turns a graph of f into derivative information about A (since A′ = f).
> Source: MATH275-Week08-Lecture-Notes.pdf

## Key Concepts
- **Monotonicity:** A increases where f > 0 and decreases where f < 0.
  > Source: MATH275-Week08-Lecture-Notes.pdf
- **Critical points:** interior zeros of f are critical points of A. A sign change determines whether A has a local extremum; a zero alone is not enough.
  > Source: MATH275-Week08-Lecture-Notes.pdf
- **Concavity:** where f is differentiable, A″ = f′. Thus increasing f gives concave-up A, and decreasing f gives concave-down A.
  > Source: MATH275-Week08-Lecture-Notes.pdf
- **Values of A from signed areas:** A(x) is the signed area from c to x; for x < c, reverse the limits (A(x) = −∫ₓᶜ f).
  > Source: MATH275-Week08-Lecture-Notes.pdf
- **Endpoint convention:** endpoints are not classified as local extrema, but they must still be checked when finding absolute extrema.
  > Source: MATH275-Week08-Lecture-Notes.pdf

## Examples
- **Piecewise-linear f:** f is continuous and linear between the vertices (−3, 0), (−1, 2), (1, −2), (3, 0), (5, 2). A(x) = ∫₋₁ˣ f(t) dt on [−3, 5].
  - Since A′ = f, A increases on (−3, 0) and (3, 5) and decreases on (0, 3). f(x) = 0 at x = 0 and x = 3, the interior critical points.
  - Values: A(−3) = −∫₋₃⁻¹ f = −(1/2)(2)(2) = −2; A(0) = (1/2)(1)(2) = 1; from 0 to 3 two negative triangles of areas 1 and 2 give A(3) = 1 − 1 − 2 = −2; the positive triangle from 3 to 5 adds 2, so A(5) = 0.

    | x | −3 | 0 | 3 | 5 |
    |---|----|---|---|---|
    | A(x) | −2 | 1 | −2 | 0 |
  - Absolute maximum A(0) = 1; absolute minimum −2, attained at x = −3 and x = 3.
  - f increases on (−3, −1) and (1, 5) and decreases on (−1, 1), so A is concave up on (−3, −1) and (1, 5), concave down on (−1, 1). Inflection points at x = −1 and x = 1. Although f has corners there, it is continuous, so A′ exists there.
  > Source: MATH275-Week08-Lecture-Notes.pdf

## Common Misconceptions
- A zero of f alone does not guarantee a local extremum of A; f must change sign.
  > Source: MATH275-Week08-Lecture-Notes.pdf
- Corners in f do not prevent A from being differentiable there, because f is continuous.
  > Source: MATH275-Week08-Lecture-Notes.pdf

## Related Topics
- [FTC Part I](ftc-part-1.md)
- [Signed Area and Integral Properties](integral-properties.md)
