# The Area Problem and Riemann Sums

## Definition
**The area problem:** given a continuous function f on [a, b], what is the area contained between the graph of y = f(x) and the x-axis? This is an approximation problem. Idea: estimate the area using shapes whose areas are easy to compute (rectangles), then refine the approximation using smaller shapes.
> Source: Week of October 23.pdf, MATH275-Week08-Lecture-Notes.pdf

Divide [a, b] into n equal pieces:
Δx = (b − a)/n (total width / number of rectangles), xᵢ = a + iΔx (i = 0, …, n).
Choosing a sample point xᵢ* ∈ [xᵢ₋₁, xᵢ], the corresponding **Riemann sum** is Σᵢ₌₁ⁿ f(xᵢ*) Δx.
> Source: MATH275-Week08-Lecture-Notes.pdf, Week of October 23.pdf

## Key Concepts
- **Lower Riemann sum:** L(f, n) = Σᵢ₌₁ⁿ f(ℓᵢ) Δx, where ℓᵢ is where f(x) is minimal on the i-th subinterval. Equivalently L(f, n) = Σ mᵢ Δx with mᵢ the minimum of f on [xᵢ₋₁, xᵢ]. Rectangles have base equal to each subinterval and height equal to the smallest value attained by f on it.
  > Source: Week of October 23.pdf, MATH275-Week08-Lecture-Notes.pdf
- **Upper Riemann sum:** U(f, n) = Σᵢ₌₁ⁿ f(uᵢ) Δx, where uᵢ is where f(x) is maximal on the i-th subinterval. Equivalently U(f, n) = Σ Mᵢ Δx with Mᵢ the maximum of f on [xᵢ₋₁, xᵢ].
  > Source: Week of October 23.pdf, MATH275-Week08-Lecture-Notes.pdf
- **Bounds:** L(f, n) ≤ the true area ≤ U(f, n).
  > Source: Week of October 23.pdf
- **Where the min/max occur:** for increasing f, minima occur at left endpoints and maxima at right endpoints. For decreasing f, the roles reverse. For a nonmonotone function, also check interior extrema on each subinterval. Left-endpoint rectangles for an increasing function lie below the graph.
  > Source: MATH275-Week08-Lecture-Notes.pdf, Week of October 23.pdf

## Examples
- **Four rectangles:** f(x) = 2x + 1 on [0, 2], n = 4. Δx = 1/2; partition points 0, 1/2, 1, 3/2, 2. f is increasing, so L(f, 4) = (1/2)(1 + 2 + 3 + 4) = 5 and U(f, 4) = (1/2)(2 + 3 + 4 + 5) = 7. The area lies between 5 and 7. The region is a trapezoid with parallel sides 1 and 5 and width 2, exact area (1/2)(1 + 5)(2) = 6, consistent with the bounds.
  > Source: MATH275-Week08-Lecture-Notes.pdf
- **Endpoints do not always give upper sums:** f(x) = (x − 1)² on [0, 2] with partition 0, 3/2, 2. On [0, 3/2] the minimum is f(1) = 0 and the maximum is f(0) = 1; on [3/2, 2], f increases from 1/4 to 1. So L = (3/2)(0) + (1/2)(1/4) = 1/8 and U = (3/2)(1) + (1/2)(1) = 2. The right-endpoint sum is (3/2)(1/4) + (1/2)(1) = 7/8, which is not U. The first subinterval contains the interior minimum x = 1; neither endpoint gives its minimum.
  > Source: MATH275-Week08-Lecture-Notes.pdf
- **Lower sums for f(x) = x³/10** on [−2, 3] were shown for n = 9, 16, 25, 100: as n grows, the rectangles fill the region more closely. The rectangles below the x-axis (on [−2, 0]) contribute negatively.
  > Source: Week of October 23.pdf

## Common Misconceptions
- The right-endpoint sum is not automatically the upper sum (and the left-endpoint sum is not automatically the lower sum) when f is not monotone on a subinterval.
  > Source: MATH275-Week08-Lecture-Notes.pdf

## Related Topics
- [The Definite Integral](definite-integral.md)
- [Signed Area and Integral Properties](integral-properties.md)
