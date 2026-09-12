# Nondifferentiability: Corners, Cusps, and Vertical Tangents

## Definition
Continuity is necessary but not sufficient for differentiability. At a suspicious point, first check continuity and then compare the one-sided difference quotients. "Slopes" here means the difference quotients based at 0, not derivatives at nearby points.
> Source: MATH275-Week02-Lecture-Notes.pdf

## Key Concepts
- **Discontinuity:** a jump function is not continuous at 0, so it cannot be differentiable there.
  > Source: MATH275-Week02-Lecture-Notes.pdf
- **Corner:** modeled by f(x) = |x|. The one-sided derivatives are finite but unequal (left: -1, right: 1).
  > Source: MATH275-Week02-Lecture-Notes.pdf
- **Cusp:** modeled by f(x) = |x|^(2/3). The one-sided slopes are infinite with opposite signs: left slope → -∞, right slope → +∞. The quotient is |h|^(2/3)/h = -|h|^(-1/3) → -∞ as h→0⁻ and |h|^(-1/3) → +∞ as h→0⁺.
  > Source: MATH275-Week02-Lecture-Notes.pdf
- **Vertical tangent:** modeled by f(x) = ∛x. Both one-sided slopes → +∞ (matching infinite slopes), since the difference quotient at 0 is h^(-2/3), and h^(2/3) = (∛h)² > 0 for either sign of h ≠ 0. The function is continuous at 0, but f'(0) does not exist as a finite real number.
  > Source: MATH275-Week02-Lecture-Notes.pdf
- **Distinguishing cusp from vertical tangent:** the cusp has opposite-signed infinite one-sided slopes, while the vertical tangent has matching infinite one-sided slopes. Reflections can reverse the signs; the distinction is opposite versus matching infinite slopes.
  > Source: MATH275-Week02-Lecture-Notes.pdf

## Examples
- Differentiable despite an absolute value: q(x) = x|x|, which equals x² for x ≥ 0 and -x² for x < 0. Neither open-interval formula alone establishes the derivative at the junction; using the definition, q'(0) = lim_{h→0} (h|h| - 0)/h = lim_{h→0} |h| = 0. Thus q is differentiable everywhere, with q'(x) = 2|x| (including x = 0), despite containing an absolute value.
  > Source: MATH275-Week02-Lecture-Notes.pdf
- Continuous at two junctions, differentiable at only one: for the piecewise function p(x) = x² (x ≤ 1), 2x-1 (1 < x ≤ 2), (x-2)²+3 (x > 2), checking continuity first shows p is continuous at both x=1 and x=2. At x=1, the one-sided derivatives both equal 2, so p'(1) = 2. At x=2, the one-sided derivatives are 2 (left) and 0 (right), which disagree, so p'(2) does not exist. When each branch is a polynomial whose formula value at the junction agrees with the actual function value, the branch may be differentiated directly and evaluated at the junction as a shortcut — justified by the matching junction values and differentiability of the branch formulas there, not by continuity alone.
  > Source: MATH275-Week02-Lecture-Notes.pdf
- Differentiable does not mean continuously differentiable: for F(x) = x²sin(1/x) (x ≠ 0), F(0) = 0, the squeeze theorem gives F'(0) = lim_{h→0} h sin(1/h) = 0. For x ≠ 0, F'(x) = 2x sin(1/x) - cos(1/x). Along x_n = 1/(2πn), F'(x_n) = -1; along y_n = 1/((2n+1)π), F'(y_n) = 1. Since a limit would need to agree along both sequences, lim_{x→0} F'(x) does not exist, even though F'(0) = 0. So F is differentiable everywhere but not continuously differentiable.
  > Source: MATH275-Week02-Lecture-Notes.pdf

## Related Topics
- [Differentiability and Continuity](differentiability-and-continuity.md)
- [The Derivative from First Principles](first-principle-derivative.md)
