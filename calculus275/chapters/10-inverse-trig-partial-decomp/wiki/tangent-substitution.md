# Tangent Substitution

## Definition
For √(a² + x²) (or powers of a² + x²), substitute x = a tan θ with −π/2 < θ < π/2. Then dx = a sec²θ dθ and √(a² + x²) = a sec θ, using tan²θ + 1 = sec²θ and sec θ > 0 on the chosen range.
> Source: MATH275-Week10-Lecture-Notes.pdf, Week of November 6 Written Notes.pdf

## Key Concepts
- **Back-substitution:** θ = tan⁻¹(x/a). A reference triangle (opposite x, adjacent a, hypotenuse √(a² + x²)) gives sin θ and cos θ in terms of x.
  > Source: Week of November 6 Written Notes.pdf
- **Double-angle back-substitution:** when x = tan θ, sin(2θ) = 2 tan θ/(1 + tan²θ) = 2x/(1 + x²). Equivalently, (1/4) sin 2θ = (1/2) sin θ cos θ can be read off the triangle.
  > Source: MATH275-Week10-Lecture-Notes.pdf, Week of November 6 Written Notes.pdf
- **Power-reduction identities used after substitution:** cos²θ = (1 + cos 2θ)/2 and sin²θ = (1 − cos 2θ)/2.
  > Source: Week of November 6 Written Notes.pdf, MATH275-Week10-Lecture-Notes.pdf
- **Changing limits:** in a definite integral, convert the x-limits to θ-limits and evaluate in θ.
  > Source: MATH275-Week10-Lecture-Notes.pdf

## Examples
- **∫ dx/(1 + x²)²:** let x = tan θ, so 1 + x² = sec²θ and dx = sec²θ dθ. Then ∫ sec²θ/(sec²θ)² dθ = ∫ cos²θ dθ = (1/2)∫ (1 + cos 2θ) dθ = θ/2 + (1/4) sin(2θ) + C = (1/2) tan⁻¹x + (1/2) sin θ cos θ + C. From the triangle, sin θ = x/√(1 + x²) and cos θ = 1/√(1 + x²), giving (1/2)[tan⁻¹x + x/(1 + x²)] + C.
  > Source: Week of November 6 Written Notes.pdf, MATH275-Week10-Lecture-Notes.pdf
- **∫₀^√3 dx/(1 + x²)^{3/2}:** set x = tan θ, −π/2 < θ < π/2. Since sec θ > 0, dx = sec²θ dθ and (1 + x²)^{3/2} = sec³θ. The limits x = 0 and x = √3 give θ = 0 and θ = π/3, so the integral is ∫₀^{π/3} cos θ dθ = [sin θ]₀^{π/3} = √3/2.
  > Source: MATH275-Week10-Lecture-Notes.pdf
- **∫₀² x²/(x² + 4)² dx:** set x = 2 tan θ, 0 ≤ θ ≤ π/4. Then dx = 2 sec²θ dθ and x² + 4 = 4 sec²θ. The endpoints become 0 and π/4, so the integral is (1/2)∫₀^{π/4} sin²θ dθ. Using sin²θ = (1 − cos 2θ)/2 gives [θ/4 − sin(2θ)/8]₀^{π/4} = π/16 − 1/8. The value is positive, as expected from the integrand.
  > Source: MATH275-Week10-Lecture-Notes.pdf
- **∫ dx/((x + 2)² + 4):** put u = (x + 2)/2, so dx = 2 du and (x + 2)² + 4 = 4(u² + 1). The integral is (1/2)∫ du/(1 + u²) = (1/2) arctan u + C = (1/2) arctan((x + 2)/2) + C.
  > Source: MATH275-Week10-Lecture-Notes.pdf

## Related Topics
- [Trigonometric (Inverse) Substitution](trig-substitution.md)
- [Irreducible Quadratic Factors](irreducible-quadratic-factors.md)
- [Completing the Square](completing-the-square.md)
