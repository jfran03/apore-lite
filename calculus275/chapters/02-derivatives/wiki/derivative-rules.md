# Basic Derivative Rules (Laws of Derivatives)

## Definition
Suppose f and g are differentiable at x. The following laws let f' be derived from f without returning to the limit definition each time.
> Source: Week 1 Video - Tangent Lines, the Derivative and its Basic Laws.pdf

## Key Concepts
- **Constant multiple rule:** for a constant c, (cf)'(x) = c f'(x).
  > Source: Week 1 Video - Tangent Lines, the Derivative and its Basic Laws.pdf
- **Sum rule:** (f+g)'(x) = f'(x) + g'(x).
  > Source: Week 1 Video - Tangent Lines, the Derivative and its Basic Laws.pdf
- **Product rule:** (fg)'(x) = f'(x)g(x) + f(x)g'(x).
  > Source: Week 1 Video - Tangent Lines, the Derivative and its Basic Laws.pdf
- **Quotient rule:** if g(x) ≠ 0, (f/g)'(x) = [f'(x)g(x) - f(x)g'(x)] / [g(x)]².
  > Source: Week 1 Video - Tangent Lines, the Derivative and its Basic Laws.pdf
- **Chain rule:** suppose the composition g∘f is defined at x, g is differentiable at f(x), and f is differentiable at x. Then (g∘f)'(x) = g'(f(x)) · f'(x).
  > Source: Week 1 Video - Tangent Lines, the Derivative and its Basic Laws.pdf

- **Why the product rule has two terms:** starting from the definition and adding/subtracting f(a+h)g(a), [f(a+h)g(a+h) - f(a)g(a)]/h = f(a+h)·[g(a+h)-g(a)]/h + g(a)·[f(a+h)-f(a)]/h. Because differentiability implies continuity, f(a+h) → f(a). Taking limits gives (fg)'(a) = f(a)g'(a) + g(a)f'(a). The extra term is forced by the fact that both factors change.
  > Source: MATH275-Week02-Lecture-Notes.pdf
- **Nested chain rule (tracking inputs through layers):** for a nested expression, work from the outside inward, record the input at each layer, and multiply by each inner derivative. For example, if G(x) = f(x²-3) and f(1) = 2, f'(1) = -3, then at x = 2 the inner input is 2²-3 = 1, so G'(2) = f'(2²-3)·2(2) = f'(1)·4 = -12. Likewise, for H(x) = tan(πf(x)), H'(x) = sec²(πf(x))·πf'(x), so H'(1) = sec²(2π)·π(-3) = -3π (using sec²(2π) = 1).
  > Source: MATH275-Week02-Lecture-Notes.pdf

## Examples
- Quotient rule example: y = (x² - 1)/(eˣ + 1)

  y' = [2x(eˣ+1) - (x²-1)eˣ] / (eˣ+1)²
  > Source: Week 1 Video - Tangent Lines, the Derivative and its Basic Laws.pdf

- Chain rule example: y = ln(eˣ + 1)

  y' = 1/(eˣ+1) · eˣ = eˣ/(eˣ+1)
  > Source: Week 1 Video - Tangent Lines, the Derivative and its Basic Laws.pdf

- Nested exponential and trigonometric function: y = e^(-csc²x). The layers are x ↦ csc x ↦ -(csc x)² ↦ e^(-(csc x)²) (requires sin x ≠ 0). The outer derivative gives y' = e^(-csc²x) · d/dx(-csc²x), and d/dx(-csc²x) = -2csc x(-csc x cot x) = 2csc²x cot x. Therefore y' = 2csc²x cot x · e^(-csc²x).
  > Source: MATH275-Week02-Lecture-Notes.pdf

## Related Topics
- [The Derivative from First Principles](first-principle-derivative.md)
- [Exponential and Logarithmic Derivatives](exponential-logarithmic-derivatives.md)
- [Derivatives of Inverse Functions](derivative-of-inverse-functions.md)
