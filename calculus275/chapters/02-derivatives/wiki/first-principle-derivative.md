# The Derivative from First Principles

## Definition
The average rate of change of a function between x = a and x = a+h is given by the difference quotient [f(a+h) - f(a)] / h. The limit of this quantity as h → 0 is called the derivative of f at x = a:

F'(a) = lim_{h→0} [f(a+h) - f(a)] / h
> Source: Week 1 Video - Tangent Lines, the Derivative and its Basic Laws.pdf

Other common notations for the derivative: F'(x), y'(x), dy/dx.
> Source: Week 1 Video - Tangent Lines, the Derivative and its Basic Laws.pdf

Replacing a with x gives the derivative as a function:

F'(x) = lim_{h→0} [f(x+h) - f(x)] / h
> Source: Week 1 Video - Tangent Lines, the Derivative and its Basic Laws.pdf

## Key Concepts
- **Tangent line via the derivative:** the derivative F'(a) gives the slope of the tangent line to y = f(x) at x = a. The tangent line equation is y - f(a) = F'(a)(x - a).
  > Source: Week 1 Video - Tangent Lines, the Derivative and its Basic Laws.pdf

- **Local linear approximation:** when f'(a) exists, the tangent line is not only a geometric object but a first-order local model: for small h, f(a+h) ≈ f(a) + f'(a)h. For example, for f(x) = x² at a = 1, f(1) = 1 and f'(1) = 2, so (1+h)² ≈ 1 + 2h. Since (1+h)² = 1 + 2h + h², the approximation omits the small quadratic term h². At h = 0.01, the approximation gives 1.02, while the exact value is 1.0201.
  > Source: MATH275-Week02-Lecture-Notes.pdf

## Examples
- First-principles derivative of a cube root: for f(x) = ∛x, compute f'(1) using the difference-of-cubes identity A³ - B³ = (A-B)(A²+AB+B²) with A = ∛(1+h), B = 1:

  f'(1) = lim_{h→0} [∛(1+h) - 1] / h = lim_{h→0} h / [h(∛(1+h)² + ∛(1+h) + 1)] = lim_{h→0} 1 / [∛(1+h)² + ∛(1+h) + 1] = 1/3
  > Source: MATH275-Week02-Lecture-Notes.pdf

- Computing the tangent line for f(x) = √x at x = 9:

  F'(x) = lim_{h→0} [√(x+h) - √x] / h

  Multiplying by the conjugate:

  F'(x) = lim_{h→0} [(√(x+h) - √x)(√(x+h) + √x)] / [h(√(x+h) + √x)]
        = lim_{h→0} h / [h(√(x+h) + √x)]
        = lim_{h→0} 1 / [√(x+h) + √x]
        = 1 / (2√x)

  At x = 9, F'(9) = 1/6, and the tangent line is:

  y - 3 = (1/6)(x - 9)  →  y = (1/6)x + 3/2
  > Source: Week 1 Video - Tangent Lines, the Derivative and its Basic Laws.pdf

## Related Topics
- [Differentiability and Continuity](differentiability-and-continuity.md)
- [Basic Derivative Rules](derivative-rules.md)
- [Tangent-Line Problems](tangent-line-problems.md)
