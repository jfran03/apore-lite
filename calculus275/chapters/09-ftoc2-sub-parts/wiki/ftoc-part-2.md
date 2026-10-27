# The Fundamental Theorem of Calculus, Part II

## Definition
**FTC Part II:** If f is continuous on [a, b] and F′ = f on (a, b), with F continuous on [a, b], then

∫ₐᵇ f(x) dx = F(b) − F(a) = [F(x)]ₐᵇ.

> Source: MATH275-Week09-Lecture-Notes.pdf

Handwritten statement: "If F is an antiderivative for f then F(b) − F(a) = ∫ₐᵇ f(x) dx."
> Source: Week of October 30.pdf

## Key Concepts
- **Bracket notation:** [F(x)]ₐᵇ (also written F(x) |ₓ₌ₐᵇ, "evaluate between x = a and x = b") means the value at the upper endpoint minus the value at the lower endpoint.
  > Source: MATH275-Week09-Lecture-Notes.pdf, Week of October 30.pdf
- **Any antiderivative works:** an arbitrary constant cancels: (F(b) + C) − (F(a) + C) = F(b) − F(a).
  > Source: MATH275-Week09-Lecture-Notes.pdf
- **Relationship to Part I:** FTC Part I (previous week) showed that the accumulation function A(x) = ∫ₐˣ f(t) dt satisfies A′ = f when f is continuous. Part II evaluates a definite integral using any antiderivative.
  > Source: MATH275-Week09-Lecture-Notes.pdf
- **Proof from Part I:** Let A(x) = ∫ₐˣ f(t) dt. Then (F − A)′ = 0 on (a, b), so the Mean Value Theorem implies F − A is constant. By continuity and A(a) = 0, this constant is F(a). Evaluating at b gives A(b) = F(b) − F(a).
  > Source: MATH275-Week09-Lecture-Notes.pdf
- **Motivating argument (displacement via Riemann sums):** Let p(t) be the position of a particle and v(t) = p′(t) its velocity. Total displacement on [a, b] is p(b) − p(a). Divide [a, b] into n equal pieces of width Δt = (b − a)/n with t₀ = a, tₙ = b. By the Mean Value Theorem, on each [tᵢ, tᵢ₊₁] there is cᵢ ∈ (tᵢ, tᵢ₊₁) with v(cᵢ) = p′(cᵢ) = (p(tᵢ₊₁) − p(tᵢ))/Δt (the average rate of change). So the displacement on [tᵢ, tᵢ₊₁] is v(cᵢ)Δt, which "looks like the area of a rectangle." Telescoping, p(b) − p(a) = v(cₙ₋₁)Δt + ⋯ + v(c₀)Δt, a sum of areas of rectangles. Comparing with upper and lower Riemann sums, v(lᵢ) ≤ v(cᵢ) ≤ v(uᵢ), where lᵢ and uᵢ are the times where v is smallest and largest on [tᵢ, tᵢ₊₁]. So L(v, n) ≤ p(b) − p(a) ≤ U(v, n). As n → ∞, Δt → 0 so lᵢ, cᵢ, uᵢ get squeezed together, both bounds tend to ∫ₐᵇ v(t) dt, and p(b) − p(a) = ∫ₐᵇ v(t) dt.
  > Source: Week of October 30.pdf
- **Net change:** If Q′ = q and q is continuous, then ∫ₐᵇ q(t) dt = Q(b) − Q(a). For velocity this gives displacement.
  > Source: MATH275-Week09-Lecture-Notes.pdf
- **Total distance:** Total distance is ∫ₐᵇ |v(t)| dt, found by splitting at changes of sign of v.
  > Source: MATH275-Week09-Lecture-Notes.pdf

## Examples
- ∫₀² (3x² − 4x + 2) dx: an antiderivative is F(x) = x³ − 2x² + 2x, so the integral is [x³ − 2x² + 2x]₀² = (8 − 8 + 4) − 0 = 4. Lesson: evaluate the whole antiderivative at each endpoint.
  > Source: MATH275-Week09-Lecture-Notes.pdf
- ∫₁² x^(−3/2) dx = [x^(−3/2+1)/(−3/2+1)]₁² = [−2x^(−1/2)]₁² = −2·2^(−1/2) − (−2·1^(−1/2)) = −2/√2 + 2 = 2 − √2.
  > Source: Week of October 30.pdf
- ∫_{π/4}^{π/2} cot θ csc θ dθ: recall (csc θ)′ = −csc θ cot θ, so the integral is [−csc θ]_{π/4}^{π/2} = −1/sin(π/2) + 1/sin(π/4) = −1 + √2.
  > Source: Week of October 30.pdf

## Common Misconceptions
- **Applying FTC across a discontinuity:** The expression [ln |x|]₋₁¹ = 0 does not evaluate ∫₋₁¹ (1/x) dx. The integrand is undefined at 0 and is not continuous on the interval. Integrals with such singularities require a separate definition and analysis. Check the interval before applying FTC.
  > Source: MATH275-Week09-Lecture-Notes.pdf

## Related Topics
- [Substitution in Definite Integrals](definite-substitution.md)
- [Integration by Parts](integration-by-parts.md)
- [Combining Methods & Integral-Defined Functions](combining-methods.md)
