# Secant Substitution

## Definition
For √(x² − a²), substitute x = a sec θ, with 0 < θ < π/2 when x > a and π/2 < θ < π when x < −a. Then dx = a sec θ tan θ dθ and √(x² − a²) = √(a² tan²θ) = a|tan θ|.
> Source: MATH275-Week10-Lecture-Notes.pdf, Week of November 6 Written Notes.pdf

The written notes describe this substitution as "rare".
> Source: Week of November 6 Written Notes.pdf

## Key Concepts
- **Two cases for the sign:** |tan θ| = tan θ when x > a (0 < θ < π/2), and |tan θ| = −tan θ when x < −a (π/2 < θ < π). Treat the two intervals separately.
  > Source: MATH275-Week10-Lecture-Notes.pdf, Week of November 6 Written Notes.pdf
- **Finding the θ-range:** from a/x = cos θ, θ = cos⁻¹(a/x). This puts θ in [0, π/2) when x ≥ a and in (π/2, π] when x ≤ −a. (The written notes use non-strict inequalities such as x ≥ 2; the lecture notes use the open ranges x > a and x < −a.)
  > Source: Week of November 6 Written Notes.pdf, MATH275-Week10-Lecture-Notes.pdf
- **Independent constants:** the antiderivatives on x > a and on x < −a may carry different, independent constants (C₊ and C₋).
  > Source: MATH275-Week10-Lecture-Notes.pdf

## Examples
- **∫ dx/√(x² − 4):** let x = 2 sec θ, so dx = 2 sec θ tan θ dθ and √(x² − 4) = 2|tan θ|. Then ∫ 2 sec θ tan θ dθ/(2|tan θ|) equals ∫ sec θ dθ for x ≥ 2 and −∫ sec θ dθ for x ≤ −2, that is, ln|sec θ + tan θ| + C or −ln|sec θ + tan θ| + C. With sec θ = x/2, tan θ = √(x² − 4)/2 for x ≥ 2 and tan θ = −√(x² − 4)/2 for x ≤ −2:
  - x ≥ 2: ln|x/2 + √(x² − 4)/2| + C
  - x ≤ −2: −ln|x/2 − √(x² − 4)/2| + C
  > Source: Week of November 6 Written Notes.pdf
- **∫ dx/(x²√(x² − 9)) on x > 3 and x < −3:** let x = 3 sec θ, so dx = 3 sec θ tan θ dθ and √(x² − 9) = 3|tan θ|.
  - If x > 3, choose 0 < θ < π/2. Then |tan θ| = tan θ and the integrand becomes (1/9) cos θ dθ, giving (1/9) sin θ + C₊ = √(x² − 9)/(9x) + C₊.
  - If x < −3, choose π/2 < θ < π. Then |tan θ| = −tan θ and the integrand becomes −(1/9) cos θ dθ. As tan θ < 0 and cos θ = 3/x, tan θ = −√(x² − 9)/3 and sin θ = tan θ cos θ = −√(x² − 9)/x, giving −(1/9) sin θ + C₋ = √(x² − 9)/(9x) + C₋.
  - The formula has the same shape on both components; C₊ and C₋ are independent. Differentiation confirms the result on either interval.
  > Source: MATH275-Week10-Lecture-Notes.pdf

## Common Misconceptions
- **Writing √(x² − a²) = a tan θ without the absolute value:** for x < −a, tan θ < 0, so the radical equals −a tan θ. Dropping the sign gives the wrong antiderivative on that interval.
  > Source: MATH275-Week10-Lecture-Notes.pdf, Week of November 6 Written Notes.pdf

## Related Topics
- [Trigonometric (Inverse) Substitution](trig-substitution.md)
