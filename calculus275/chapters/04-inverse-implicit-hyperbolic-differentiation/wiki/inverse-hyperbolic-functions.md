# Inverse Hyperbolic Functions

## Definition
The inverse hyperbolic functions are obtained from one-to-one branches. sinh: ℝ → ℝ, cosh: [0, ∞) → [1, ∞) and tanh: ℝ → (−1, 1) are one-to-one, with inverses arsinh x, arcosh x, artanh x (also written sinh⁻¹, cosh⁻¹, tanh⁻¹).
> Source: MATH275-Week04-Lecture-Notes.pdf, Week of September 25 (Week 3) .pdf

## Key Concepts
- **Restriction of cosh is essential:** cosh is even, so y = arcosh x always means the nonnegative solution of cosh y = x. The range (−1, 1) of tanh determines the domain of artanh.
  > Source: MATH275-Week04-Lecture-Notes.pdf
- **Logarithmic forms:** arsinh x = ln(x + √(x² + 1)) for x ∈ ℝ; arcosh x = ln(x + √(x² − 1)) for x ≥ 1; artanh x = ½ ln((1 + x)/(1 − x)) for |x| < 1. For artanh the logarithm is real on |x| < 1 because both 1 + x and 1 − x are positive there.
  > Source: MATH275-Week04-Lecture-Notes.pdf, Week of September 25 (Week 3) .pdf
- **Derivatives:**
  - d/dx arsinh x = 1/√(1 + x²), x ∈ ℝ
  - d/dx arcosh x = 1/√(x² − 1), x > 1
  - d/dx artanh x = 1/(1 − x²), |x| < 1
  > Source: MATH275-Week04-Lecture-Notes.pdf, Week of September 25 (Week 3) .pdf
- **Endpoint behavior:** arcosh 1 = 0, but its derivative is not finite at the endpoint x = 1.
  > Source: MATH275-Week04-Lecture-Notes.pdf
- **Remaining inverse hyperbolic functions (course definitions):** arccsch x = arsinh(1/x) (x ≠ 0); arcsech x = arcosh(1/x) (0 < x ≤ 1); arccoth x = artanh(1/x) (|x| > 1). Their derivatives: d/dx arccsch x = −1/(|x|√(1 + x²)) (x ≠ 0); d/dx arcsech x = −1/(x√(1 − x²)) (0 < x < 1); d/dx arccoth x = 1/(1 − x²) (|x| > 1). These follow from the same inverse-function rule used for inverse trig functions.
  > Source: MATH275-Week04-Lecture-Notes.pdf, Week of September 25 (Week 3) .pdf
- **Method for inverting a hyperbolic function:** set x = sinh y and solve for y; rewrite with exponentials and treat eʸ as the variable.
  > Source: MATH275-Week04-Lecture-Notes.pdf, Week of September 25 (Week 3) .pdf

## Examples
- **Deriving arsinh:** let y = arsinh x, so x = (eʸ − e⁻ʸ)/2. Multiplying by 2eʸ gives e²ʸ − 2x eʸ − 1 = 0, a quadratic in eʸ. The quadratic formula gives eʸ = x ± √(x² + 1). Because eʸ > 0, the "+" branch is required, so y = ln(x + √(x² + 1)).
  > Source: MATH275-Week04-Lecture-Notes.pdf, Week of September 25 (Week 3) .pdf
- **Derivative of the log form:** differentiating ln(x + √(x² + 1)) by the chain rule and putting the numerator over a common denominator gives 1/√(x² + 1) for any x.
  > Source: Week of September 25 (Week 3) .pdf
- **q(x) = arcosh(2x − 1):** the function requires 2x − 1 ≥ 1, so its domain is x ≥ 1. Using (arcosh u)' = u'/√(u² − 1), q'(x) = 2/√((2x − 1)² − 1) = 1/√(x(x − 1)). The function is defined at x = 1, but the derivative is finite only for x > 1.
  > Source: MATH275-Week04-Lecture-Notes.pdf
- **y = arsinh(4x):** with u = 4x, u' = 4, y' = 4/√(1 + 16x²).
  > Source: MATH275-Week04-Lecture-Notes.pdf

## Common Misconceptions
- **Notation:** sinh⁻¹ x is commonly used for arsinh x, not for csch x.
  > Source: MATH275-Week04-Lecture-Notes.pdf

## Related Topics
- [Hyperbolic Functions](hyperbolic-functions.md)
- [Derivative of an Inverse Function](inverse-function-derivative.md)
- [Inverse Trigonometric Derivatives](inverse-trig-derivatives.md)
