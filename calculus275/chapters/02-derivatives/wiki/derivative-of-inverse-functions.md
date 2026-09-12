# Derivatives of Inverse Functions

## Definition
Suppose f is differentiable and strictly monotone (strictly increasing or strictly decreasing) on an open interval I. Then it has an inverse g = f⁻¹ on its image f(I). If a ∈ I, b = f(a), and f'(a) ≠ 0, then g is differentiable at b and

(f⁻¹)'(b) = 1/f'(a) = 1/f'(f⁻¹(b))
> Source: MATH275-Week02-Lecture-Notes.pdf

Here f⁻¹ means the inverse function, not 1/f. The inverse reverses inputs and outputs: f(a) = b means g(b) = a.
> Source: MATH275-Week02-Lecture-Notes.pdf

## Key Concepts
- **Where the formula comes from:** once differentiability of g is guaranteed by the theorem, the chain rule applied to f(g(y)) = y gives f'(g(b))g'(b) = 1, i.e. f'(a)g'(b) = 1, at y = b.
  > Source: MATH275-Week02-Lecture-Notes.pdf
- **Hypotheses matter:** we need an inverse on the chosen interval and a nonzero denominator. If f'(a) = 0, the formula does not apply — we do not divide by zero.
  > Source: MATH275-Week02-Lecture-Notes.pdf

## Examples
- Using inverse data without solving for the inverse: let f(x) = x³ + x. Both x³ and x are strictly increasing, so f is strictly increasing and has an inverse g = f⁻¹ on its range. To find g'(2), first find the original input: f(1) = 2, so g(2) = 1. Since f'(x) = 3x² + 1, f'(1) = 4 ≠ 0, so g'(2) = 1/f'(1) = 1/4. There is no need to find a formula for g.
  > Source: MATH275-Week02-Lecture-Notes.pdf
- Derivative of arctan: on (-π/2, π/2), tan is differentiable and strictly increasing with range ℝ; its inverse is arctan. If y = tan x, then x = arctan y and sec²x = 1 + tan²x = 1 + y². Therefore d/dy arctan y = 1/sec²x = 1/(1+y²). Renaming the input variable gives (arctan x)' = 1/(1+x²) for every real x.
  > Source: MATH275-Week02-Lecture-Notes.pdf

## Related Topics
- [Basic Derivative Rules](derivative-rules.md)
- [The Derivative from First Principles](first-principle-derivative.md)
