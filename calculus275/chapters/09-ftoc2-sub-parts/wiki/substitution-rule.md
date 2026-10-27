# Integration by Substitution (Indefinite)

## Definition
**The substitution rule:** For continuous f and continuously differentiable g, write u = g(x) and du = g′(x) dx. Then

∫ f(g(x)) g′(x) dx = ∫ f(u) du = F(g(x)) + C,

where F′ = f. It reverses the chain rule: if F′ = f, then d/dx F(g(x)) = f(g(x)) g′(x).
> Source: MATH275-Week09-Lecture-Notes.pdf

Handwritten version ("inverting the chain rule"): the family of antiderivatives of h(x) = f′(g(x)) g′(x) is ∫ h(x) dx = f(g(x)) + C by the chain rule. Letting u = g(x), du/dx = g′(x), so ∫ f′(g(x)) g′(x) dx = ∫ f′(u)·(du/dx) dx = ∫ f′(u) du = f(u) + C = f(g(x)) + C.
> Source: Week of October 30.pdf

## Key Concepts
- **Choosing u:** Choose an inner expression whose derivative appears elsewhere in the integrand. When integrating something that looks like the derivative of a composition, we often need to "guess" what g(x) should be.
  > Source: MATH275-Week09-Lecture-Notes.pdf, Week of October 30.pdf
- **Replace everything:** Replace the entire integrand and differential by expressions in u; return to x in the final indefinite integral. All factors must be rewritten in u before integrating.
  > Source: MATH275-Week09-Lecture-Notes.pdf
- **Constant factors:** if du differs from the available factor by a constant, solve for it (e.g. du/4 = x³ dx, or −du = eᵗ dt).
  > Source: Week of October 30.pdf
- **Verify by differentiating:** differentiate the answer to confirm.
  > Source: Week of October 30.pdf

## Examples
- ∫ x³ cos(x⁴) dx: x³ is almost the derivative of x⁴. Guess u = x⁴, du/dx = 4x³, so du/4 = x³ dx. Then the integral is (1/4)∫ cos u du = (1/4) sin u + C = (1/4) sin(x⁴) + C.
  > Source: Week of October 30.pdf
- ∫ eᵗ √(1 − eᵗ) dt: guess u = 1 − eᵗ, du/dt = −eᵗ, so −du = eᵗ dt. Then −∫ u^(1/2) du = −u^(3/2)/(3/2) + C = −(2/3)(1 − eᵗ)^(3/2) + C.
  > Source: Week of October 30.pdf
- ∫ x(2x² + 5)⁴ dx: u = 2x² + 5, du = 4x dx, so the integral is (1/4)∫ u⁴ du = (2x² + 5)⁵/20 + C.
  > Source: MATH275-Week09-Lecture-Notes.pdf
- ∫ (6x − 1)/(3x² − x + 4) dx: u = 3x² − x + 4, du = (6x − 1) dx, so ∫ du/u = ln(3x² − x + 4) + C. The logarithm is defined for every real x because 3x² − x + 4 = 3(x − 1/6)² + 47/12 > 0.
  > Source: MATH275-Week09-Lecture-Notes.pdf
- ∫ x⁵ √(1 + x²) dx (rewrite a remaining power of x): u = 1 + x², du = 2x dx, and x⁴ = (u − 1)². Then (1/2)∫ (u − 1)² u^(1/2) du = (1/2)∫ (u^(5/2) − 2u^(3/2) + u^(1/2)) du = (1 + x²)^(7/2)/7 − 2(1 + x²)^(5/2)/5 + (1 + x²)^(3/2)/3 + C. The original power x⁵ supplies both x dx and x⁴.
  > Source: MATH275-Week09-Lecture-Notes.pdf

## Common Misconceptions
- **Integrating with mixed variables:** all factors must be rewritten in u before integration, including leftover powers of x (see the x⁵√(1 + x²) example).
  > Source: MATH275-Week09-Lecture-Notes.pdf

## Related Topics
- [Substitution in Definite Integrals](definite-substitution.md)
- [Choosing a Useful Substitution](choosing-substitutions.md)
- [Combining Methods & Integral-Defined Functions](combining-methods.md)
