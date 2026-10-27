# Question Bank

> Generated from `wiki/` during the compile step. Extended on wrong-answer targeting and graduation.
> Do not edit manually — all changes are made by Claude during compile and session flows.

---

<!-- Question format (do not delete this comment):

## Q{NNN}
**Status:** active | retired
**Type:** mcq | short-answer | conceptual | true-false
**Difficulty:** introductory | intermediate | advanced
**Topic:** {topic-slug}
**Focus Area:** {specific concept or sub-topic}
**Question:** {question text}
**Answer:** {model answer — sourced from wiki only}

-->

## Q001
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** ftoc-part-2
**Focus Area:** statement and hypotheses of FTC Part II
**Question:** State FTC Part II precisely, including all hypotheses on f and F.
**Answer:** If f is continuous on [a, b] and F′ = f on (a, b), with F continuous on [a, b], then ∫ₐᵇ f(x) dx = F(b) − F(a) = [F(x)]ₐᵇ. See `ftoc-part-2.md`.

## Q002
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** ftoc-part-2
**Focus Area:** evaluating with an antiderivative
**Question:** Evaluate ∫₁² x^(−3/2) dx.
**Answer:** An antiderivative is −2x^(−1/2). So [−2x^(−1/2)]₁² = −2/√2 + 2 = 2 − √2. See `ftoc-part-2.md`.

## Q003
**Status:** active
**Type:** true-false
**Difficulty:** introductory
**Topic:** ftoc-part-2
**Focus Area:** arbitrary constant cancels
**Question:** True or false: when evaluating ∫ₐᵇ f(x) dx with FTC Part II, the answer depends on which antiderivative F you choose.
**Answer:** False. Any antiderivative works because the arbitrary constant cancels: (F(b) + C) − (F(a) + C) = F(b) − F(a). See `ftoc-part-2.md`.

## Q004
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** ftoc-part-2
**Focus Area:** proof of Part II from Part I
**Question:** Prove FTC Part II from FTC Part I. Name the theorem you use to conclude that a function is constant.
**Answer:** Let A(x) = ∫ₐˣ f(t) dt. By Part I, A′ = f, so (F − A)′ = 0 on (a, b). By the Mean Value Theorem, F − A is constant. By continuity and A(a) = 0, the constant is F(a). Evaluating at b gives A(b) = F(b) − F(a), i.e. ∫ₐᵇ f = F(b) − F(a). See `ftoc-part-2.md`.

## Q005
**Status:** active
**Type:** mcq
**Difficulty:** intermediate
**Topic:** ftoc-part-2
**Focus Area:** checking the interval before applying FTC
**Question:** A student writes ∫₋₁¹ (1/x) dx = [ln |x|]₋₁¹ = 0. Which statement is correct? (A) The answer is correct because 1/x is odd. (B) The answer is correct because ln |1| = ln |−1|. (C) The computation is invalid because 1/x is undefined at 0 and not continuous on [−1, 1]. (D) The computation is invalid because ln |x| is not an antiderivative of 1/x.
**Answer:** (C). The integrand is undefined at 0 and is not continuous on the interval, so FTC does not apply; such integrals require a separate definition and analysis. See `ftoc-part-2.md`.

## Q006
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** ftoc-part-2
**Focus Area:** displacement / Riemann sum motivation
**Question:** Let p be position and v = p′. Explain how the Mean Value Theorem and upper/lower Riemann sums together show p(b) − p(a) = ∫ₐᵇ v(t) dt.
**Answer:** Split [a, b] into n pieces of width Δt. By the MVT, on each [tᵢ, tᵢ₊₁] there is cᵢ with p(tᵢ₊₁) − p(tᵢ) = v(cᵢ)Δt. Telescoping, p(b) − p(a) = Σ v(cᵢ)Δt. Since v(lᵢ) ≤ v(cᵢ) ≤ v(uᵢ) (smallest/largest values on each piece), L(v, n) ≤ p(b) − p(a) ≤ U(v, n). As n → ∞, both bounds tend to ∫ₐᵇ v(t) dt, so p(b) − p(a) equals it. See `ftoc-part-2.md`.

## Q007
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** ftoc-part-2
**Focus Area:** net change vs total distance
**Question:** For a velocity v(t) on [a, b], what do ∫ₐᵇ v(t) dt and ∫ₐᵇ |v(t)| dt represent, and how is the second one computed?
**Answer:** ∫ₐᵇ v(t) dt is displacement (net change of position). ∫ₐᵇ |v(t)| dt is total distance, computed by splitting the interval at changes of sign of v. See `ftoc-part-2.md`.

## Q008
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** substitution-rule
**Focus Area:** recognizing inner function and derivative
**Question:** Find ∫ x³ cos(x⁴) dx.
**Answer:** u = x⁴, du = 4x³ dx, so x³ dx = du/4. The integral is (1/4)∫ cos u du = (1/4) sin(x⁴) + C. See `substitution-rule.md`.

## Q009
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** substitution-rule
**Focus Area:** negative constant in du
**Question:** Find ∫ eᵗ √(1 − eᵗ) dt.
**Answer:** u = 1 − eᵗ, du = −eᵗ dt, so eᵗ dt = −du. Then −∫ u^(1/2) du = −(2/3)u^(3/2) + C = −(2/3)(1 − eᵗ)^(3/2) + C. See `substitution-rule.md`.

## Q010
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** substitution-rule
**Focus Area:** absolute value in logarithm
**Question:** ∫ (6x − 1)/(3x² − x + 4) dx = ln(3x² − x + 4) + C, written without absolute value bars. Justify why that is acceptable.
**Answer:** With u = 3x² − x + 4, du = (6x − 1) dx, the integral is ∫ du/u. Since 3x² − x + 4 = 3(x − 1/6)² + 47/12 > 0 for all real x, the logarithm is defined everywhere and no absolute value is needed. See `substitution-rule.md`.

## Q011
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** substitution-rule
**Focus Area:** rewriting a leftover power of x in u
**Question:** Find ∫ x⁵ √(1 + x²) dx.
**Answer:** u = 1 + x², du = 2x dx, x⁴ = (u − 1)². The integral is (1/2)∫ (u − 1)² u^(1/2) du = (1/2)∫ (u^(5/2) − 2u^(3/2) + u^(1/2)) du = (1 + x²)^(7/2)/7 − 2(1 + x²)^(5/2)/5 + (1 + x²)^(3/2)/3 + C. The power x⁵ supplies both x dx and x⁴. See `substitution-rule.md`.

## Q012
**Status:** active
**Type:** mcq
**Difficulty:** intermediate
**Topic:** definite-substitution
**Focus Area:** consistent variable and limits
**Question:** After substituting u = g(x) in a definite integral and finding an antiderivative in u, which is NOT a valid way to finish? (A) Use the transformed limits g(a), g(b) in the u-antiderivative. (B) Substitute back to x and use the original limits a, b. (C) Use the original limits a, b in the u-antiderivative. (D) Change limits before integrating and never return to x.
**Answer:** (C). Do not apply x-limits to an antiderivative still written in u. See `definite-substitution.md`.

## Q013
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** definite-substitution
**Focus Area:** changing endpoints, tan θ
**Question:** Evaluate ∫_{π/6}^{π/4} tan θ dθ by changing the endpoints, and state the antiderivative of tan θ this gives.
**Answer:** u = cos θ, du = −sin θ dθ; endpoints become √3/2 (at π/6) and 1/√2 (at π/4). So −∫_{√3/2}^{1/√2} du/u = ∫_{1/√2}^{√3/2} du/u = ln(√3/2) − ln(1/√2) = ln √(3/2) = (1/2) ln(3/2). It also gives ∫ tan θ dθ = −ln |cos θ| + C = ln |sec θ| + C. See `definite-substitution.md`.

## Q014
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** definite-substitution
**Focus Area:** decreasing substitution, reversed limits
**Question:** Evaluate ∫₀^{π/4} sin(2x)/(2 + cos(2x)) dx, and check the sign of your answer.
**Answer:** u = 2 + cos(2x), du = −2 sin(2x) dx; x = 0 ⇒ u = 3, x = π/4 ⇒ u = 2. So −(1/2)∫₃² du/u = (1/2)∫₂³ du/u = (1/2) ln(3/2). It is positive, agreeing with the sign of the integrand. See `definite-substitution.md`.

## Q015
**Status:** active
**Type:** true-false
**Difficulty:** advanced
**Topic:** definite-substitution
**Focus Area:** one-to-one not required
**Question:** True or false: the definite substitution formula ∫ₐᵇ f(g(x))g′(x) dx = ∫_{g(a)}^{g(b)} f(u) du requires g to be one-to-one on [a, b]. Use ∫₋₁¹ 2x e^(x²) dx to illustrate.
**Answer:** False. The proof (choose F′ = f and apply FTC II to F(g(x))) does not need it. With u = x², both endpoints map to 1, giving ∫₁¹ eᵘ du = 0, which matches e¹ − e¹ = 0 from (e^(x²))′ = 2x e^(x²). From −1 to 0, u goes 1 → 0, then back 0 → 1; the two oriented integrals cancel, and the factor 2x records the change of direction. See `definite-substitution.md`.

## Q016
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** choosing-substitutions
**Focus Area:** odd power of cosine
**Question:** Find ∫ sin⁴x cos³x dx. Which factor do you save, and what identity do you use?
**Answer:** Save one cos x dx and write cos³x = (1 − sin²x) cos x using cos²x = 1 − sin²x. With u = sin x, ∫ u⁴(1 − u²) du = sin⁵x/5 − sin⁷x/7 + C. See `choosing-substitutions.md`.

## Q017
**Status:** active
**Type:** conceptual
**Difficulty:** introductory
**Topic:** choosing-substitutions
**Focus Area:** strategy for sinᵐx cosⁿx
**Question:** For ∫ sinᵐx cosⁿx dx, what strategy does each case suggest: odd power of sine, odd power of cosine, both powers even?
**Answer:** Odd power of cosine: save cos x dx, u = sin x, rewrite with cos²x = 1 − sin²x. Odd power of sine: save sin x dx, u = cos x, rewrite with sin²x = 1 − cos²x. Even powers: may require the half-angle identities sin²x = (1 − cos 2x)/2 and cos²x = (1 + cos 2x)/2. See `choosing-substitutions.md`.

## Q018
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** choosing-substitutions
**Focus Area:** exponential substitution u = eˣ
**Question:** Find ∫ e^(3x)/(1 + e^(2x)) dx. Why is u = 1 + e^(2x) a poor choice here?
**Answer:** With u = 1 + e^(2x), the leftover eˣ = √(u − 1), giving √(u − 1)/(2u) du, which still needs more techniques. Instead u = eˣ, du = eˣ dx: e^(3x) dx = u² du, so ∫ u²/(1 + u²) du = ∫ (1 − 1/(1 + u²)) du = u − tan⁻¹u + C = eˣ − tan⁻¹(eˣ) + C. See `choosing-substitutions.md`.

## Q019
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** choosing-substitutions
**Focus Area:** divide before integrating
**Question:** Find ∫ e^(4x)/(4 + e^(2x)) dx.
**Answer:** u = e^(2x), du = 2e^(2x) dx, e^(4x) dx = (1/2)u du. Then (1/2)∫ u/(u + 4) du = (1/2)∫ (1 − 4/(u + 4)) du = (1/2)(u − 4 ln(u + 4)) + C = (1/2)e^(2x) − 2 ln(4 + e^(2x)) + C. See `choosing-substitutions.md`.

## Q020
**Status:** active
**Type:** conceptual
**Difficulty:** introductory
**Topic:** integration-by-parts
**Focus Area:** derivation and choosing U
**Question:** Derive ∫ U dV = UV − ∫ V dU from the product rule, and state how U and dV should be chosen.
**Answer:** (fg)′ = f′g + fg′, so fg = ∫ f′g dx + ∫ fg′ dx. With U = f, V = g, dU = f′ dx, dV = g′ dx: UV = ∫ V dU + ∫ U dV, so ∫ U dV = UV − ∫ V dU. Choose U so differentiation simplifies it, and dV so V can be found; ∫ V dU should be easier. See `integration-by-parts.md`.

## Q021
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** integration-by-parts
**Focus Area:** single function as product with 1
**Question:** Find ∫ ln x dx.
**Answer:** Write it as 1·ln x: U = ln x, dV = dx, dU = dx/x, V = x. Then x ln x − ∫ x·(1/x) dx = x ln x − x + C. See `integration-by-parts.md`.

## Q022
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** integration-by-parts
**Focus Area:** inverse trig, parts then substitution
**Question:** Find ∫ tan⁻¹x dx.
**Answer:** U = tan⁻¹x, dV = dx, dU = dx/(1 + x²), V = x. Then x tan⁻¹x − ∫ x/(1 + x²) dx; substitute u = 1 + x², du/2 = x dx: x tan⁻¹x − (1/2) ln(1 + x²) + C. See `integration-by-parts.md`.

## Q023
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** integration-by-parts
**Focus Area:** polynomial times trig
**Question:** Find ∫ x cos(3x) dx.
**Answer:** U = x, dV = cos(3x) dx, dU = dx, V = (1/3) sin(3x). Then x sin(3x)/3 − (1/3)∫ sin(3x) dx = x sin(3x)/3 + cos(3x)/9 + C. See `integration-by-parts.md`.

## Q024
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** integration-by-parts
**Focus Area:** definite integration by parts
**Question:** Evaluate ∫₁ᵉ x² ln x dx. Where is it easy to lose a term?
**Answer:** U = ln x, dV = x² dx, dU = dx/x, V = x³/3. [x³ ln x/3]₁ᵉ − (1/3)∫₁ᵉ x² dx = e³/3 − [x³/9]₁ᵉ = (2e³ + 1)/9. The boundary term at 1 is zero, but the second integral still contributes 1/9 from the lower endpoint. See `integration-by-parts.md`.

## Q025
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** integration-by-parts
**Focus Area:** definite integration by parts
**Question:** Evaluate ∫ₑ^{e²} x ln x dx.
**Answer:** U = ln x, dV = x dx, dU = dx/x, V = x²/2. (1/2)x² ln x |ₑ^{e²} − (1/2)∫ₑ^{e²} x dx = e⁴ − (1/2)e² − (1/4)e⁴ + (1/4)e² = (3/4)e⁴ − (1/4)e². See `integration-by-parts.md`.

## Q026
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** repeated-cyclic-parts
**Focus Area:** reducing the power of a logarithm
**Question:** Find ∫ x (ln x)² dx for x > 0.
**Answer:** U = (ln x)², dV = x dx: (x²/2)(ln x)² − ∫ x ln x dx. Then U = ln x, dV = x dx: ∫ x ln x dx = (x²/2) ln x − x²/4. Combined: (x²/2)(ln x)² − (x²/2) ln x + x²/4 + C. See `repeated-cyclic-parts.md`.

## Q027
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** repeated-cyclic-parts
**Focus Area:** cyclic integral, exponential times trig
**Question:** Find ∫ e^(2x) sin(3x) dx.
**Answer:** Let I = ∫ e^(2x) sin(3x) dx, J = ∫ e^(2x) cos(3x) dx, integrating the exponential each time: I = (1/2)e^(2x) sin(3x) − (3/2)J, J = (1/2)e^(2x) cos(3x) + (3/2)I. So I = (1/2)e^(2x) sin(3x) − (3/4)e^(2x) cos(3x) − (9/4)I, giving (13/4)I = (1/2)e^(2x) sin(3x) − (3/4)e^(2x) cos(3x), and I = (e^(2x)/13)(2 sin(3x) − 3 cos(3x)) + C. See `repeated-cyclic-parts.md`.

## Q028
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** repeated-cyclic-parts
**Focus Area:** definite cyclic integral
**Question:** Evaluate ∫₁ᵉ sin(ln x) dx.
**Answer:** U = sin(ln x), dV = dx: x sin(ln x)|₁ᵉ − ∫₁ᵉ cos(ln x) dx. Again with U = cos(ln x): = e sin 1 − [x cos(ln x)|₁ᵉ + ∫₁ᵉ sin(ln x) dx] = e sin 1 − e cos 1 + 1 − ∫₁ᵉ sin(ln x) dx. Adding the integral to both sides and dividing by 2: (1/2)[e sin 1 − e cos 1 + 1]. See `repeated-cyclic-parts.md`.

## Q029
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** repeated-cyclic-parts
**Focus Area:** repeated vs cyclic outcome
**Question:** A second application of integration by parts can lead to two different outcomes. What are they, and what do you do in each case?
**Answer:** It can simplify the remaining integral further (keep going until it is elementary), or it can bring back the original integral (collect the original integral on one side and solve for it). See `repeated-cyclic-parts.md`.

## Q030
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** repeated-cyclic-parts
**Focus Area:** csc³x via parts and identity
**Question:** On an interval with no zero of sin x, find ∫ csc³x dx. First establish ∫ csc x dx by differentiating csc x − cot x.
**Answer:** (csc x − cot x)′ = −csc x cot x + csc²x = csc x (csc x − cot x), so ∫ csc x dx = ln |csc x − cot x| + C. For I = ∫ csc³x dx, U = csc x, dV = csc²x dx, dU = −csc x cot x dx, V = −cot x: I = −csc x cot x − ∫ csc x cot²x dx = −csc x cot x − ∫ csc x (csc²x − 1) dx = −csc x cot x − I + ln |csc x − cot x|. So I = −(1/2) csc x cot x + (1/2) ln |csc x − cot x| + C. See `repeated-cyclic-parts.md`.

## Q031
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** combining-methods
**Focus Area:** substitute first, then parts
**Question:** Evaluate ∫₀^{√(ln 2)} x³ e^(x²) dx.
**Answer:** u = x², du = 2x dx, x³ dx = (1/2)u du, limits 0 and ln 2: (1/2)∫₀^{ln 2} u eᵘ du. By parts (U = u, dV = eᵘ du): (1/2)[(u − 1)eᵘ]₀^{ln 2} = (1/2)[2(ln 2 − 1) + 1] = ln 2 − 1/2. See `combining-methods.md`.

## Q032
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** combining-methods
**Focus Area:** accumulation functions in answers
**Question:** Let S(x) = ∫₀ˣ cos(t²) dt. (a) Find S′(x) and S(0). (b) For x ≥ 1, express H(x) = ∫₁^{x²} (cos t/√t) dt in terms of S. (c) Express K(x) = ∫₀ˣ S(t) dt in terms of S and elementary functions.
**Answer:** (a) By FTC Part I, S′(x) = cos(x²); S(0) = 0. (b) t = u², u ≥ 1, dt = 2u du, √t = u, upper limit u = x: H(x) = 2∫₁ˣ cos(u²) du = 2(S(x) − S(1)). (c) Parts with U = S(t), dV = dt: K(x) = [tS(t)]₀ˣ − ∫₀ˣ t cos(t²) dt = xS(x) − (1/2) sin(x²). See `combining-methods.md`.
