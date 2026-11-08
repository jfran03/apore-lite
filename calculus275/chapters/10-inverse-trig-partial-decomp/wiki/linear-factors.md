# Linear Factors (Distinct and Repeated)

## Definition
**Type I (distinct linear factors):** if q(x) = A(x − x₁)(x − x₂)⋯(x − xₙ) with distinct linear factors, then there are constants C₁, C₂, …, Cₙ so that
p(x)/q(x) = C₁/(x − x₁) + C₂/(x − x₂) + ⋯ + Cₙ/(x − xₙ).
> Source: Week of November 6 Written Notes.pdf

**Type Ia (repeated linear factors):** if deg(p) < k, then there are coefficients A₁, …, A_k so that
p(x)/(x − a)^k = A₁/(x − a) + A₂/(x − a)² + ⋯ + A_k/(x − a)^k.
This can be mixed with other Type I terms.
> Source: Week of November 6 Written Notes.pdf

## Key Concepts
- **Keep every power:** a repeated factor (x − r)³ requires terms with denominators (x − r), (x − r)² and (x − r)³.
  > Source: MATH275-Week10-Lecture-Notes.pdf
- **Finding coefficients for a repeated factor:** evaluating at its root often finds the coefficient of the highest power; a second root and one other convenient value can determine the rest.
  > Source: MATH275-Week10-Lecture-Notes.pdf, Week of November 6 Written Notes.pdf
- **Mixed example of the form:** (3x⁴ − 2x)/((x − 1)(x − 2)²(x − 3)³) = A/(x − 1) + B₁/(x − 2) + B₂/(x − 2)² + C₁/(x − 3) + C₂/(x − 3)² + C₃/(x − 3)³. Degree 6 means 6 coefficients.
  > Source: Week of November 6 Written Notes.pdf
- **Integrating the pieces:** ∫ C/(x − r) dx = C ln|x − r| + C′, and terms with (x − r)², e.g. ∫ C/(x + 2)² dx = −C/(x + 2) + const.
  > Source: Week of November 6 Written Notes.pdf, MATH275-Week10-Lecture-Notes.pdf
- **Domain of the result:** the identity and antiderivative hold on each interval on which the integrand is defined; the constants may differ on the separate components (e.g. of ℝ \ {−1, 3}).
  > Source: MATH275-Week10-Lecture-Notes.pdf

## Examples
- **∫ (5x + 1)/((x − 1)(x + 2)) dx:** write (5x + 1)/((x − 1)(x + 2)) = P/(x − 1) + Q/(x + 2). Clearing denominators: 5x + 1 = P(x + 2) + Q(x − 1). At x = 1, P = 2; at x = −2, Q = 3. Hence the integral is 2 ln|x − 1| + 3 ln|x + 2| + C.
  > Source: MATH275-Week10-Lecture-Notes.pdf
- **∫ (x² + 2x + 3)/(x(x² − 4)) dx:** factor x(x² − 4) = x(x − 2)(x + 2), so (x² + 2x + 3)/(x(x − 2)(x + 2)) = C₁/x + C₂/(x − 2) + C₃/(x + 2). Multiplying by x(x − 2)(x + 2): x² + 2x + 3 = C₁(x − 2)(x + 2) + C₂x(x + 2) + C₃x(x − 2). Try the roots: x = 0 gives 3 = −4C₁, C₁ = −3/4; x = 2 gives 11 = 8C₂, C₂ = 11/8; x = −2 gives 3 = 8C₃, C₃ = 3/8. Result: −(3/4) ln|x| + (11/8) ln|x − 2| + (3/8) ln|x + 2| + C.
  > Source: Week of November 6 Written Notes.pdf
- **∫ (3x² − 1)/(x³ + 4x² + 4x) dx:** factor x³ + 4x² + 4x = x(x² + 4x + 4) = x(x + 2)². Decompose as A/x + B/(x + 2) + C/(x + 2)², which integrates to A ln|x| + B ln|x + 2| − C/(x + 2) + const. Equation: 3x² − 1 = A(x + 2)² + Bx(x + 2) + Cx. Roots: x = 0 gives −1 = 4A, A = −1/4; x = −2 gives 11 = −2C, C = −11/2. Something easy for the third value: x = 1 gives 2 = 9A + 3B + C = −9/4 + 3B − 11/2, so B = 13/4. Substituting these values: −(1/4) ln|x| + (13/4) ln|x + 2| + 11/(2(x + 2)) + const.
  > Source: Week of November 6 Written Notes.pdf
- **∫ (x² − 6x + 25)/((x + 1)(x − 3)²) dx:** set the integrand equal to P/(x + 1) + Q/(x − 3) + R/(x − 3)². Clearing denominators: x² − 6x + 25 = P(x − 3)² + Q(x + 1)(x − 3) + R(x + 1). x = −1 gives 32 = 16P, P = 2; x = 3 gives 16 = 4R, R = 4; x = 0 gives 25 = 9P − 3Q + R, Q = −1. Integrating: 2 ln|x + 1| − ln|x − 3| − 4/(x − 3) + C. The constants may differ on the components of ℝ \ {−1, 3}.
  > Source: MATH275-Week10-Lecture-Notes.pdf

## Common Misconceptions
- **Omitting lower powers of a repeated factor:** (x − 3)² needs both Q/(x − 3) and R/(x − 3)², not just R/(x − 3)².
  > Source: MATH275-Week10-Lecture-Notes.pdf

## Related Topics
- [Partial Fraction Decomposition: Setup](partial-fractions-setup.md)
- [Irreducible Quadratic Factors](irreducible-quadratic-factors.md)
