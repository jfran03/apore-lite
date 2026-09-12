# Differentiability and Continuity

## Definition
A function f is differentiable at x = a if f'(a) exists. f is differentiable on an interval I if f'(x) exists for all x in I (using one-sided limits at endpoints, if necessary).
> Source: Week 1 Video - Tangent Lines, the Derivative and its Basic Laws.pdf

## Key Concepts
- **Differentiability implies continuity:** if f is differentiable at x = a, then f is continuous at x = a. The converse does not hold.
  > Source: Week 1 Video - Tangent Lines, the Derivative and its Basic Laws.pdf
- **Proof sketch that differentiability implies continuity:** if f'(a) exists as a finite number, then for h ≠ 0, f(a+h) - f(a) = h · [f(a+h)-f(a)]/h → 0 · f'(a) = 0. Hence f(a+h) → f(a).
  > Source: MATH275-Week02-Lecture-Notes.pdf
- **One-sided derivatives:** f'_-(a) = lim_{h→0-} [f(a+h)-f(a)]/h and f'_+(a) = lim_{h→0+} [f(a+h)-f(a)]/h. At an interior point, f'(a) exists exactly when both one-sided derivatives exist as finite numbers and are equal. At an endpoint of an interval, we can instead ask for the one-sided derivative from within the domain; this is not a two-sided derivative.
  > Source: MATH275-Week02-Lecture-Notes.pdf

## Common Misconceptions
- Continuity does not imply differentiability. The example given is f(x) = |x|, which is continuous everywhere but not differentiable at x = 0.
  > Source: Week 1 Video - Tangent Lines, the Derivative and its Basic Laws.pdf
- For f(x) = |x| at 0, the one-sided derivatives are f'_-(0) = -1 and f'_+(0) = 1: the graph is continuous but has a corner, since the one-sided derivatives are finite but unequal.
  > Source: MATH275-Week02-Lecture-Notes.pdf

## Related Topics
- [The Derivative from First Principles](first-principle-derivative.md)
- [Nondifferentiability: Corners, Cusps, and Vertical Tangents](nondifferentiability.md)
