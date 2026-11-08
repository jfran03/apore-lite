# Partial Fraction Decomposition: Setup

## Definition
Partial fraction decomposition is used for breaking down any function of the form p(x)/q(x), where p and q are polynomials with deg(p) < deg(q), into pieces that are easy to integrate.
> Source: Week of November 6 Written Notes.pdf

For a rational function N(x)/D(x): first divide if deg N ≥ deg D. Then factor D over the real numbers into linear factors and irreducible quadratics.
> Source: MATH275-Week10-Lecture-Notes.pdf

## Key Concepts
- **The target pieces (or whole powers of these):**
  - (i) ∫ 1/(ax + b) dx = (1/a) ln|ax + b| + C
  - (ii) ∫ x/(x² + a²) dx = (1/2) ln(a² + x²) + C
  - (iii) ∫ x/(x² − a²) dx = (1/2) ln|x² − a²| + C
  - (iv) ∫ 1/(x² + a²) dx = (1/a) tan⁻¹(x/a) + C
  > Source: Week of November 6 Written Notes.pdf
- **Irreducible quadratic:** a quadratic q(x) is irreducible over ℝ if its discriminant is negative (a quadratic factor "without roots", e.g. x² + 1).
  > Source: MATH275-Week10-Lecture-Notes.pdf, Week of November 6 Written Notes.pdf
- **Form of the decomposition:** for every distinct factor, include a term for each power up to its multiplicity:

  | Factor in the denominator | Terms to include |
  |---|---|
  | (x − r)^m | P₁/(x − r) + P₂/(x − r)² + ⋯ + P_m/(x − r)^m |
  | q(x)^n, q irreducible quadratic | (Q₁x + R₁)/q(x) + ⋯ + (Q_n x + R_n)/q(x)^n |

  Use a linear numerator over each quadratic power.
  > Source: MATH275-Week10-Lecture-Notes.pdf
- **Counting coefficients:** the number of unknown coefficients equals the degree of the denominator (e.g. a degree 6 denominator means 6 coefficients; a degree 7 denominator means 7).
  > Source: Week of November 6 Written Notes.pdf
- **Solving for coefficients:** clear denominators (multiply both sides by the full denominator), then determine coefficients by convenient substitutions, coefficient comparison, or both. Substituting n distinct values of x gives n equations in n unknowns; try the roots first, then "sub in something easy" for the remaining values.
  > Source: MATH275-Week10-Lecture-Notes.pdf, Week of November 6 Written Notes.pdf
- **Factor completely over ℝ first:** a factor such as x⁴ − 16 should be factored further over ℝ before choosing the decomposition.
  > Source: MATH275-Week10-Lecture-Notes.pdf
- **Divide first when improper:** if the numerator's degree is at least the denominator's, divide first.
  > Source: MATH275-Week10-Lecture-Notes.pdf

## Examples
- **Divide before decomposing, ∫ (2x² + 1)/(x² + 1) dx:** numerator and denominator have equal degree. Division gives (2x² + 1)/(x² + 1) = 2 − 1/(x² + 1), so the integral is 2x − arctan x + C. Differentiating gives 2 − 1/(1 + x²), the original integrand.
  > Source: MATH275-Week10-Lecture-Notes.pdf
- **Factoring a quartic over ℝ:** x⁴ + 4 = (x² + 2)² − (2x)² = (x² − 2x + 2)(x² + 2x + 2), a difference of squares; both quadratic factors are irreducible over ℝ. (See [Choosing an Approach](choosing-an-approach.md) for the full integral.)
  > Source: MATH275-Week10-Lecture-Notes.pdf

## Common Misconceptions
- **Decomposing an improper fraction directly:** when deg N ≥ deg D, divide first.
  > Source: MATH275-Week10-Lecture-Notes.pdf
- **Stopping the factorization early:** factor the denominator fully over ℝ (e.g. x(x² − 4) = x(x − 2)(x + 2); x⁴ − 16 must be factored further) before writing the decomposition.
  > Source: MATH275-Week10-Lecture-Notes.pdf, Week of November 6 Written Notes.pdf

## Related Topics
- [Linear Factors (Distinct and Repeated)](linear-factors.md)
- [Irreducible Quadratic Factors](irreducible-quadratic-factors.md)
- [Choosing an Approach](choosing-an-approach.md)
