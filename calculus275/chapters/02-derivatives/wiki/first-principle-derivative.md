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

## Examples
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
