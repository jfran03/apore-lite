# Derivatives of Trigonometric Functions

## Definition
The derivation relies on two limits expected from geometry:

(i) lim_{θ→0} sin(θ)/θ = 1
(ii) lim_{θ→0} [cos(θ) - 1]/θ = 0
> Source: Week 1 Video - Tangent Lines, the Derivative and its Basic Laws.pdf

## Key Concepts
- **Derivative of sin x:** using the angle-addition formula and the two limits above,

  F'(x) = lim_{h→0} [sin(x+h) - sin(x)] / h
        = lim_{h→0} sin(x)[cos(h)-1]/h + cos(x)[sin(h)/h]
        = sin(x)·0 + cos(x)·1 = cos(x)

  So (sin x)' = cos x.
  > Source: Week 1 Video - Tangent Lines, the Derivative and its Basic Laws.pdf

- **Derivative of the other trig functions:** using a similar analog, the remaining basic trig derivatives are:
  - (tan x)' = sec²x
  - (cot x)' = -csc²x
  - (sec x)' = sec x tan x
  - (csc x)' = -csc x cot x
  > Source: Week 1 Video - Tangent Lines, the Derivative and its Basic Laws.pdf

## Related Topics
- [The Derivative from First Principles](first-principle-derivative.md)
- [Basic Derivative Rules](derivative-rules.md)
