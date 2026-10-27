# Substitution in Definite Integrals

## Definition
For continuous f on an interval containing g([a, b]) and continuously differentiable g on [a, b],

∫ₐᵇ f(g(x)) g′(x) dx = ∫_{g(a)}^{g(b)} f(u) du.

To verify the formula, choose F′ = f and apply FTC Part II to F(g(x)). This proof does not require g to be one-to-one.
> Source: MATH275-Week09-Lecture-Notes.pdf

## Key Concepts
- **Keep the variable and limits consistent:** If you change the integration variable to u, change both limits to values of u. Alternatively, find an antiderivative, substitute back to x, and use the original x-limits. Do not apply x-limits to an antiderivative still written in u.
  > Source: MATH275-Week09-Lecture-Notes.pdf
- **Before or after:** take care of the endpoints either before or after the integration is done. If the endpoints are changed before integrating, you never need to return to the original variable.
  > Source: Week of October 30.pdf
- **Decreasing substitutions:** both the negative sign in du and the order of the transformed endpoints must be retained.
  > Source: MATH275-Week09-Lecture-Notes.pdf

## Examples
- ∫_{π/6}^{π/4} tan θ dθ = ∫ (sin θ / cos θ) dθ. Let u = cos θ, du = −sin θ dθ. Change the endpoints: u(π/4) = cos(π/4) = 1/√2, u(π/6) = cos(π/6) = √3/2. Then the integral is −∫_{√3/2}^{1/√2} du/u = ∫_{1/√2}^{√3/2} du/u = [ln |u|]_{1/√2}^{√3/2} = ln(√3/2) − ln(1/√2) = ln(√3·√2/2) = ln √(3/2) = (1/2) ln(3/2). There is no need to return to θ.
  > Source: Week of October 30.pdf
- **By-product:** the same substitution gives ∫ tan θ dθ = −ln |cos θ| + C = ln |sec θ| + C.
  > Source: Week of October 30.pdf
- ∫₀^{π/4} sin(2x)/(2 + cos(2x)) dx (decreasing substitution, reversed limits): u = 2 + cos(2x), du = −2 sin(2x) dx. x = 0 ⇒ u = 3; x = π/4 ⇒ u = 2. So the integral is −(1/2)∫₃² du/u = (1/2)∫₂³ du/u = (1/2) ln(3/2). The positive answer agrees with the sign of the integrand.
  > Source: MATH275-Week09-Lecture-Notes.pdf
- ∫₋₁¹ 2x e^(x²) dx with u = x² (equal transformed endpoints): du = 2x dx and both endpoints map to 1, so the integral is ∫₁¹ eᵘ du = 0. Equivalently (e^(x²))′ = 2x e^(x²), so FTC gives e¹ − e¹ = 0. Although x² is not one-to-one on [−1, 1], this is valid: from x = −1 to 0, u travels from 1 to 0; from 0 to 1 it travels back from 0 to 1. The two oriented integrals cancel. The factor 2x records this change of direction.
  > Source: MATH275-Week09-Lecture-Notes.pdf

## Common Misconceptions
- **Plugging x-limits into a u-antiderivative:** not allowed; either convert both limits to u or convert back to x first.
  > Source: MATH275-Week09-Lecture-Notes.pdf
- **Thinking g must be one-to-one:** the definite substitution formula's proof (FTC II applied to F(g(x))) does not require it.
  > Source: MATH275-Week09-Lecture-Notes.pdf

## Related Topics
- [The Fundamental Theorem of Calculus, Part II](ftoc-part-2.md)
- [Integration by Substitution (Indefinite)](substitution-rule.md)
