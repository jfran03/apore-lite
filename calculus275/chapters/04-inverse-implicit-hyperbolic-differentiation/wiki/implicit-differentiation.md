# Implicit Differentiation

## Definition
An equation F(x, y) = 0 may define y as a function of x locally even when solving explicitly for y is inconvenient. Differentiate both sides with respect to x, treating y = y(x); whenever a y-dependent subexpression is differentiated, apply the chain rule using dy/dx = y'.
> Source: MATH275-Week04-Lecture-Notes.pdf

If F(x, y) = 0 is some equation in x, y, we can think of y as a function of x, y = f(x). The equation becomes F(x, f(x)) = 0, which is completely in terms of x, so we can differentiate it.
> Source: Week of September 25 (Week 3) .pdf

## Key Concepts
- **Tangent lines on non-functions:** The folium of Descartes x³ + y³ = 2xy is not a function, but a tangent line can still be constructed where the curve looks like a differentiable function when zoomed in.
  > Source: Week of September 25 (Week 3) .pdf
- **Compact partial-derivative form:** d/dx F(x, y(x)) = F_x + F_y y' = 0, so wherever F_y ≠ 0, y' = −F_x / F_y.
  > Source: MATH275-Week04-Lecture-Notes.pdf
- **Typical chain-rule terms:** d/dx (y³) = 3y² y' and d/dx sin(xy) = cos(xy)(y + x y').
  > Source: MATH275-Week04-Lecture-Notes.pdf
- **Workflow:** (1) differentiate both sides with respect to x; (2) use product and chain rules before doing algebra; (3) collect all terms containing y'; (4) factor out y' and solve; (5) only then substitute the coordinates of a specified point. This keeps the chain rule visible and does not require solving the original relation for y.
  > Source: MATH275-Week04-Lecture-Notes.pdf
- **The answer depends on x and y:** the resulting expression for dy/dx will (almost) always depend on both x and y. The solved form is valid provided the coefficient being divided by is nonzero (e.g. 3y² ≠ 2x in the folium example).
  > Source: Week of September 25 (Week 3) .pdf
- **Horizontal and vertical tangent checkpoints:** if implicit differentiation gives y' = −A(x, y)/B(x, y), then A = 0 with B ≠ 0 is the checkpoint for a horizontal tangent, and B = 0 with A ≠ 0 is the checkpoint for a vertical tangent. If A = B = 0 the test is inconclusive and the point may be singular. Every candidate must also satisfy the original curve equation.
  > Source: MATH275-Week04-Lecture-Notes.pdf

## Examples
- **x² eʸ + y³ = 1 at (1, 0):** differentiating gives 2x eʸ + x² eʸ y' + 3y² y' = 0, so y' = −2x eʸ / (x² eʸ + 3y²). At (1, 0), y' = −2 and the tangent line is y = −2(x − 1).
  > Source: MATH275-Week04-Lecture-Notes.pdf
- **x² y + cos y = 2x at (0, π/2):** first check the point lies on the curve (0 + cos(π/2) = 0 = 2(0)). Differentiating gives 2xy + x² y' − sin y · y' = 2, so y' = (2 − 2xy)/(x² − sin y). At (0, π/2), y' = 2/(−1) = −2.
  > Source: MATH275-Week04-Lecture-Notes.pdf
- **y³ + x³ = 2xy (folium):** differentiating (product rule on 2xy) gives 3y² dy/dx + 3x² = 2y + 2x dy/dx, so dy/dx = (2y − 3x²)/(3y² − 2x), provided 3y² ≠ 2x. At (1, 1) the slope is (2 − 3)/(3 − 2) = −1 and the tangent line is y − 1 = −(x − 1).
  > Source: Week of September 25 (Week 3) .pdf
- **x² + 3xy − y² = 5:** differentiating gives 2x + 3(y + x y') − 2y y' = 0, so (3x − 2y) y' = −(2x + 3y) and, when 3x − 2y ≠ 0, y' = −(2x + 3y)/(3x − 2y).
  > Source: MATH275-Week04-Lecture-Notes.pdf

## Common Misconceptions
- **Substituting the point too early:** if a problem asks for the tangent slope at a point, do not substitute x = a and y = b into the original equation before differentiating. Doing so destroys the dependence of x and y and turns the relation into a numerical identity.
  > Source: MATH275-Week04-Lecture-Notes.pdf

## Related Topics
- [Derivative of an Inverse Function](inverse-function-derivative.md)
- [Choosing a Differentiation Strategy](choosing-a-differentiation-strategy.md)
