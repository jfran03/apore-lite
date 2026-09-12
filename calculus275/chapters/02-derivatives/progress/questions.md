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
**Type:** conceptual
**Difficulty:** introductory
**Topic:** first-principle-derivative
**Focus Area:** definition of the derivative
**Question:** State the limit definition of the derivative F'(a), and name two alternative notations for the derivative.
**Answer:** F'(a) = lim_{h→0} [f(a+h) - f(a)] / h. Alternative notations include F'(x), y'(x), and dy/dx. (see `first-principle-derivative.md`)

## Q002
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** first-principle-derivative
**Focus Area:** computing a derivative from first principles
**Question:** Using the limit definition, find F'(x) for f(x) = √x.
**Answer:** F'(x) = lim_{h→0} [√(x+h) - √x]/h. Multiplying by the conjugate gives lim_{h→0} 1/[√(x+h)+√x] = 1/(2√x). (see `first-principle-derivative.md`)

## Q003
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** first-principle-derivative
**Focus Area:** tangent line equation
**Question:** Find the equation of the tangent line to f(x) = √x at x = 9.
**Answer:** F'(9) = 1/6 and f(9) = 3, so the tangent line is y - 3 = (1/6)(x-9), i.e. y = (1/6)x + 3/2. (see `first-principle-derivative.md`)

## Q004
**Status:** active
**Type:** true-false
**Difficulty:** introductory
**Topic:** differentiability-and-continuity
**Focus Area:** differentiability implies continuity
**Question:** True or false: if a function is differentiable at x = a, it must be continuous at x = a.
**Answer:** True. Differentiability at a point implies continuity at that point. (see `differentiability-and-continuity.md`)

## Q005
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** differentiability-and-continuity
**Focus Area:** continuity does not imply differentiability
**Question:** Give an example of a function that is continuous everywhere but not differentiable at a point, and identify where it fails to be differentiable.
**Answer:** f(x) = |x| is continuous everywhere but not differentiable at x = 0. (see `differentiability-and-continuity.md`)

## Q006
**Status:** active
**Type:** mcq
**Difficulty:** introductory
**Topic:** derivative-rules
**Focus Area:** constant multiple and sum rules
**Question:** If f and g are differentiable at x and c is a constant, which of the following is correct? (a) (cf)'(x) = f'(x)  (b) (cf)'(x) = c f'(x)  (c) (f+g)'(x) = f'(x)·g'(x)  (d) (f+g)'(x) = f'(x) - g'(x)
**Answer:** (b) (cf)'(x) = c f'(x). Also note the sum rule: (f+g)'(x) = f'(x) + g'(x). (see `derivative-rules.md`)

## Q007
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** derivative-rules
**Focus Area:** product rule
**Question:** State the product rule for (fg)'(x).
**Answer:** (fg)'(x) = f'(x)g(x) + f(x)g'(x). (see `derivative-rules.md`)

## Q008
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** derivative-rules
**Focus Area:** quotient rule application
**Question:** Using the quotient rule, find y' for y = (x² - 1)/(eˣ + 1).
**Answer:** y' = [2x(eˣ+1) - (x²-1)eˣ] / (eˣ+1)². (see `derivative-rules.md`)

## Q009
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** derivative-rules
**Focus Area:** chain rule
**Question:** State the chain rule for the derivative of a composition g∘f at x, including the conditions required for it to apply.
**Answer:** If g∘f is defined at x, g is differentiable at f(x), and f is differentiable at x, then (g∘f)'(x) = g'(f(x)) · f'(x). (see `derivative-rules.md`)

## Q010
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** derivative-rules
**Focus Area:** chain rule application
**Question:** Using the chain rule, find y' for y = ln(eˣ + 1).
**Answer:** y' = 1/(eˣ+1) · eˣ = eˣ/(eˣ+1). (see `derivative-rules.md`)

## Q011
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** exponential-logarithmic-derivatives
**Focus Area:** derivative of a^x
**Question:** What is the derivative of f(x) = aˣ for a > 0, a ≠ 1?
**Answer:** (aˣ)' = ln(a) · aˣ. (see `exponential-logarithmic-derivatives.md`)

## Q012
**Status:** active
**Type:** mcq
**Difficulty:** introductory
**Topic:** exponential-logarithmic-derivatives
**Focus Area:** derivative of e^x
**Question:** What is (eˣ)'? (a) eˣ  (b) x·eˣ⁻¹  (c) ln(x)·eˣ  (d) eˣ⁻¹
**Answer:** (a) eˣ, since ln(e) = 1 in the general rule (aˣ)' = ln(a)·aˣ. (see `exponential-logarithmic-derivatives.md`)

## Q013
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** exponential-logarithmic-derivatives
**Focus Area:** derivative of ln x
**Question:** What is the derivative of ln(x)? What about the general log_a(x)?
**Answer:** (ln x)' = 1/x. In general, (log_a x)' = 1/(x ln a). (see `exponential-logarithmic-derivatives.md`)

## Q014
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** trig-derivatives
**Focus Area:** derivation of (sin x)'
**Question:** Using the limit definition and the identities lim_{θ→0} sin(θ)/θ = 1 and lim_{θ→0} [cos(θ)-1]/θ = 0, derive that (sin x)' = cos x.
**Answer:** F'(x) = lim_{h→0} [sin(x+h)-sin(x)]/h = lim_{h→0} sin(x)[cos(h)-1]/h + cos(x)[sin(h)/h] = sin(x)·0 + cos(x)·1 = cos(x). (see `trig-derivatives.md`)

## Q015
**Status:** active
**Type:** mcq
**Difficulty:** introductory
**Topic:** trig-derivatives
**Focus Area:** basic trig derivatives
**Question:** Which of the following is correct? (a) (tan x)' = sec²x  (b) (tan x)' = -sec²x  (c) (sec x)' = -sec x tan x  (d) (csc x)' = csc x cot x
**Answer:** (a) (tan x)' = sec²x. Also: (cot x)' = -csc²x, (sec x)' = sec x tan x, (csc x)' = -csc x cot x. (see `trig-derivatives.md`)

## Q016
**Status:** active
**Type:** mcq
**Difficulty:** introductory
**Topic:** derivative-rules
**Focus Area:** chain rule conditions — where each function must be differentiable
**Question:** The chain rule for (g∘f)'(x) requires g to be differentiable at which point? (a) x  (b) f(x)  (c) g(x)  (d) f'(x)
**Answer:** (b) f(x). The rule states that g must be differentiable at f(x), while f must be differentiable at x. (see `derivative-rules.md`)

## Q017
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** derivative-rules
**Focus Area:** chain rule conditions applied to concrete values
**Question:** Suppose f is differentiable at x = 2 with f(2) = 5, and g is differentiable at x = 5, and g∘f is defined at x = 2. Does the chain rule apply at x = 2, and if so what is (g∘f)'(2)?
**Answer:** Yes — all three conditions hold: g∘f is defined at 2, g is differentiable at f(2) = 5, and f is differentiable at 2. Therefore (g∘f)'(2) = g'(f(2))·f'(2) = g'(5)·f'(2). (see `derivative-rules.md`)

## Q018
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** derivative-rules
**Focus Area:** quotient rule — pairing each derivative with the correct factor
**Question:** Applying the quotient rule to y = (x² - 1)/(eˣ + 1), a student writes the numerator as (2x)(x² - 1) - (x² - 1)eˣ. Identify the error and give the correct numerator.
**Answer:** The first term must be f'(x)·g(x), i.e. the derivative of the numerator times the *denominator*: (2x)(eˣ+1), not (2x)(x²-1). The correct numerator is 2x(eˣ+1) - (x²-1)eˣ. (see `derivative-rules.md`)

## Q019
**Status:** active
**Type:** mcq
**Difficulty:** introductory
**Topic:** derivative-rules
**Focus Area:** quotient rule statement and sign order
**Question:** For g(x) ≠ 0, the numerator of (f/g)'(x) is: (a) f'(x)g(x) + f(x)g'(x)  (b) f'(x)g(x) - f(x)g'(x)  (c) f(x)g'(x) - f'(x)g(x)  (d) f'(x)g'(x)
**Answer:** (b) f'(x)g(x) - f(x)g'(x), all over [g(x)]². (see `derivative-rules.md`)

## Q020
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** trig-derivatives
**Focus Area:** the four derived trig derivatives, with signs
**Question:** State the derivatives of tan x, cot x, sec x, and csc x. Pay attention to which ones carry a negative sign.
**Answer:** (tan x)' = sec²x, (cot x)' = -csc²x, (sec x)' = sec x tan x, (csc x)' = -csc x cot x. (see `trig-derivatives.md`)

## Q021
**Status:** active
**Type:** mcq
**Difficulty:** introductory
**Topic:** trig-derivatives
**Focus Area:** sign pattern among trig derivatives
**Question:** Among tan, cot, sec, and csc, which derivatives carry a negative sign? (a) tan and sec  (b) cot and csc  (c) sec and csc  (d) none of them
**Answer:** (b) cot and csc: (cot x)' = -csc²x and (csc x)' = -csc x cot x, while (tan x)' = sec²x and (sec x)' = sec x tan x are both positive. (see `trig-derivatives.md`)

## Q022
**Status:** active
**Type:** conceptual
**Difficulty:** introductory
**Topic:** first-principle-derivative
**Focus Area:** local linear approximation
**Question:** What does it mean for the tangent line to be a "first-order local model" of f near x = a? Illustrate with f(x) = x² at a = 1 and h = 0.01.
**Answer:** For small h, f(a+h) ≈ f(a) + f'(a)h. For f(x) = x² at a = 1, f(1) = 1 and f'(1) = 2, so (1+h)² ≈ 1 + 2h; this omits the small quadratic term h². At h = 0.01, the approximation gives 1.02 while the exact value is 1.0201. (see `first-principle-derivative.md`)

## Q023
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** first-principle-derivative
**Focus Area:** first-principles derivative of a cube root
**Question:** Using the limit definition and the difference-of-cubes identity A³-B³ = (A-B)(A²+AB+B²), find f'(1) for f(x) = ∛x.
**Answer:** With A = ∛(1+h), B = 1: f'(1) = lim_{h→0} [∛(1+h) - 1]/h = lim_{h→0} 1/[∛(1+h)² + ∛(1+h) + 1] = 1/3. (see `first-principle-derivative.md`)

## Q024
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** differentiability-and-continuity
**Focus Area:** one-sided derivatives
**Question:** Define f'_-(a) and f'_+(a), and state the condition under which f'(a) exists at an interior point a.
**Answer:** f'_-(a) = lim_{h→0-} [f(a+h)-f(a)]/h and f'_+(a) = lim_{h→0+} [f(a+h)-f(a)]/h. At an interior point, f'(a) exists exactly when both one-sided derivatives exist as finite numbers and are equal. (see `differentiability-and-continuity.md`)

## Q025
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** differentiability-and-continuity
**Focus Area:** proof that differentiability implies continuity
**Question:** Prove that if f'(a) exists as a finite number, then f is continuous at a.
**Answer:** For h ≠ 0, f(a+h) - f(a) = h · [f(a+h)-f(a)]/h. As h → 0, the right side → 0 · f'(a) = 0, so f(a+h) → f(a), which is continuity at a. (see `differentiability-and-continuity.md`)

## Q026
**Status:** active
**Type:** true-false
**Difficulty:** introductory
**Topic:** differentiability-and-continuity
**Focus Area:** endpoint one-sided derivatives
**Question:** True or false: at an endpoint of an interval, the one-sided derivative from within the domain counts as a full two-sided derivative.
**Answer:** False. At an endpoint we can only ask for the one-sided derivative from within the domain; this is not a two-sided derivative. (see `differentiability-and-continuity.md`)

## Q027
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** derivative-rules
**Focus Area:** proof of the product rule
**Question:** Starting from the limit definition, explain why the product rule (fg)'(a) produces two terms rather than one.
**Answer:** Adding and subtracting f(a+h)g(a): [f(a+h)g(a+h)-f(a)g(a)]/h = f(a+h)·[g(a+h)-g(a)]/h + g(a)·[f(a+h)-f(a)]/h. Since differentiability implies continuity, f(a+h)→f(a), so taking limits gives (fg)'(a) = f(a)g'(a) + g(a)f'(a) — two terms because both factors change. (see `derivative-rules.md`)

## Q028
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** derivative-rules
**Focus Area:** nested chain rule, tracking inputs of an unknown function
**Question:** Suppose f(1) = 2 and f'(1) = -3. If G(x) = f(x²-3) and H(x) = tan(πf(x)), find G'(2) and H'(1).
**Answer:** G'(2) = f'(2²-3)·2(2) = f'(1)·4 = -12. H'(x) = sec²(πf(x))·πf'(x), so H'(1) = sec²(2π)·π(-3) = -3π (since sec²(2π) = 1). (see `derivative-rules.md`)

## Q029
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** derivative-rules
**Focus Area:** nested exponential/trig chain rule
**Question:** Find y' for y = e^(-csc²x).
**Answer:** The layers are x ↦ csc x ↦ -(csc x)² ↦ e^(-(csc x)²). d/dx(-csc²x) = -2csc x(-csc x cot x) = 2csc²x cot x, so y' = 2csc²x cot x · e^(-csc²x). (see `derivative-rules.md`)

## Q030
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** derivative-of-inverse-functions
**Focus Area:** inverse function derivative formula and its hypotheses
**Question:** State the formula for (f⁻¹)'(b), and explain the hypotheses under which it is valid.
**Answer:** (f⁻¹)'(b) = 1/f'(a) = 1/f'(f⁻¹(b)), where b = f(a). It requires f to be differentiable and strictly monotone on an open interval containing a, and f'(a) ≠ 0 — the formula does not apply if f'(a) = 0. (see `derivative-of-inverse-functions.md`)

## Q031
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** derivative-of-inverse-functions
**Focus Area:** applying the inverse derivative formula without solving for the inverse
**Question:** Let f(x) = x³ + x, which has an inverse g = f⁻¹. Find g'(2) without finding a formula for g.
**Answer:** f(1) = 2, so g(2) = 1. f'(x) = 3x² + 1, so f'(1) = 4 ≠ 0, and g'(2) = 1/f'(1) = 1/4. (see `derivative-of-inverse-functions.md`)

## Q032
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** derivative-of-inverse-functions
**Focus Area:** deriving the arctan derivative
**Question:** Using the inverse function derivative rule, derive (arctan x)' = 1/(1+x²).
**Answer:** On (-π/2, π/2), tan is differentiable and strictly increasing with inverse arctan. If y = tan x, then sec²x = 1+tan²x = 1+y². So d/dy arctan y = 1/sec²x = 1/(1+y²); renaming the variable gives (arctan x)' = 1/(1+x²). (see `derivative-of-inverse-functions.md`)

## Q033
**Status:** active
**Type:** mcq
**Difficulty:** introductory
**Topic:** nondifferentiability
**Focus Area:** distinguishing corner, cusp, and vertical tangent
**Question:** At a point where the one-sided difference quotients are both +∞ (matching infinite slopes), the graph has a: (a) corner  (b) cusp  (c) vertical tangent  (d) jump discontinuity
**Answer:** (c) vertical tangent, modeled by f(x) = ∛x. A corner has finite unequal one-sided slopes (e.g. |x|); a cusp has opposite-signed infinite slopes (e.g. |x|^(2/3)). (see `nondifferentiability.md`)

## Q034
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** nondifferentiability
**Focus Area:** differentiability despite an absolute value
**Question:** Show that q(x) = x|x| is differentiable at x = 0, and give q'(x).
**Answer:** q(x) = x² for x≥0 and -x² for x<0. At 0, using the definition, q'(0) = lim_{h→0} (h|h|-0)/h = lim_{h→0} |h| = 0. So q is differentiable everywhere with q'(x) = 2|x|. (see `nondifferentiability.md`)

## Q035
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** nondifferentiability
**Focus Area:** checking differentiability at a piecewise junction
**Question:** For p(x) = x² (x≤1), 2x-1 (1<x≤2), (x-2)²+3 (x>2), determine whether p is differentiable at x=1 and at x=2.
**Answer:** p is continuous at both junctions. At x=1, both one-sided derivatives equal 2, so p'(1)=2 exists. At x=2, the one-sided derivatives are 2 (left) and 0 (right), which disagree, so p'(2) does not exist. (see `nondifferentiability.md`)

## Q036
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** nondifferentiability
**Focus Area:** differentiable but not continuously differentiable
**Question:** For F(x) = x²sin(1/x) (x≠0), F(0)=0, show F'(0) exists but F' is not continuous at 0.
**Answer:** By the squeeze theorem, F'(0) = lim_{h→0} h sin(1/h) = 0. For x≠0, F'(x) = 2x sin(1/x) - cos(1/x). Along x_n = 1/(2πn), F'(x_n) = -1; along y_n = 1/((2n+1)π), F'(y_n) = 1. Since the limit would need to agree along both sequences, lim_{x→0} F'(x) does not exist, so F is differentiable everywhere but not continuously differentiable. (see `nondifferentiability.md`)

## Q037
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** tangent-line-problems
**Focus Area:** tangent parallel to a given line
**Question:** Find all points on g(x) = x³ - 3x whose tangent line is parallel to y = 9x - 4.
**Answer:** Need g'(x) = 9: 3x²-3 = 9 gives x = ±2. Since g(2)=2 and g(-2)=-2, the points are (2,2) and (-2,-2). (see `tangent-line-problems.md`)

## Q038
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** tangent-line-problems
**Focus Area:** tangent perpendicular to a given line
**Question:** Find every point on f(x) = 2x³ - 4x where the tangent is perpendicular to y = -½x + 3.
**Answer:** The required tangent slope is the negative reciprocal of -½, which is 2. Since f'(x) = 6x²-4 = 2, x = ±1, giving points (1,-2) and (-1,2). (see `tangent-line-problems.md`)

## Q039
**Status:** active
**Type:** mcq
**Difficulty:** intermediate
**Topic:** derivative-rules
**Focus Area:** chain rule conditions — where g must be differentiable (targeted follow-up to Q017)
**Question:** Suppose h(x) = g(f(x)). For the chain rule to apply at x = a, which of the following must be true? (a) g must be differentiable at a  (b) g must be differentiable at f(a)  (c) g must be differentiable at g(a)  (d) g must be continuous at a, but need not be differentiable anywhere
**Answer:** (b) g must be differentiable at f(a). The chain rule requires g to be differentiable at f(x), and f to be differentiable at x. (see `derivative-rules.md`)

## Q040
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** derivative-rules
**Focus Area:** chain rule conditions — failure case when g fails at f(x) (targeted follow-up to Q017)
**Question:** Suppose f is differentiable at x = 3 with f(3) = 7, and g is differentiable at x = 3 but NOT at x = 7. Does the chain rule guarantee that (g∘f)'(3) exists? Explain.
**Answer:** No. The chain rule requires g to be differentiable at f(3) = 7, not at x = 3. Since g is not differentiable at 7, this condition fails, so the chain rule cannot guarantee (g∘f)'(3) exists. (see `derivative-rules.md`)

## Q041
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** first-principle-derivative
**Focus Area:** local linear approximation (targeted follow-up to Q022)
**Question:** Using the local linear approximation formula f(a+h) ≈ f(a) + f'(a)h, and given that for f(x) = ∛x, f(1) = 1 and f'(1) = 1/3, estimate f(1.03). Is this an exact value or an approximation, and why?
**Answer:** f(1.03) ≈ f(1) + f'(1)(0.03) = 1 + (1/3)(0.03) = 1.01. This is an approximation, not exact — the tangent line is only a first-order local model and omits higher-order terms in h, analogous to how (1+h)² ≈ 1+2h omits h². (see `first-principle-derivative.md`)

## Q042
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** differentiability-and-continuity
**Focus Area:** finite vs infinite one-sided derivatives (targeted follow-up to Q024)
**Question:** For f(x) = ∛x at a = 0, both one-sided difference quotients approach +∞. Do f'_-(0) and f'_+(0) "exist" in the sense required for f'(0) to exist? Explain using the definition of one-sided derivatives.
**Answer:** No. Although the one-sided quotients agree in direction (+∞), a derivative must exist as a finite number — "equals +∞" means the limit diverges rather than settling on a real number. Since f'_-(0) and f'_+(0) do not exist as finite numbers, f'(0) does not exist, even though the one-sided behavior "matches." (see `differentiability-and-continuity.md`, `nondifferentiability.md`)

## Q043
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** differentiability-and-continuity
**Focus Area:** endpoint one-sided derivatives (targeted follow-up to Q026)
**Question:** Suppose f is defined on [0, 5]. At x = 0, only f'_+(0) can be computed from within the domain. If f'_+(0) exists and equals 3, can we say f'(0) = 3? Explain.
**Answer:** No. At an endpoint we can only ask for the one-sided derivative from within the domain — this is not a two-sided derivative. Even though f'_+(0) = 3 exists, f'(0) as a two-sided derivative is not defined here since there's no domain to the left of 0 to compute f'_-(0). (see `differentiability-and-continuity.md`)

## Q044
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** first-principle-derivative
**Focus Area:** first-order local model, meaning of terms (targeted follow-up to Q041)
**Question:** In the local linear approximation f(a+h) ≈ f(a) + f'(a)h, why is this called a "first-order" model, and why does the wiki call it "local" rather than a global description of f?
**Answer:** It is "first-order" because it only keeps the term with h to the first power (f'(a)h), omitting higher-order terms like h². It is "local" because the approximation is only reliable for small h near a — as h grows, the omitted higher-order terms (e.g. h² in the (1+h)² example) grow and the approximation degrades. (see `first-principle-derivative.md`)

## Q045
**Status:** active
**Type:** mcq
**Difficulty:** introductory
**Topic:** exponential-logarithmic-derivatives
**Focus Area:** reading prime notation for derivatives (targeted follow-up to Q012)
**Question:** (log_a x)' means: (a) log_a x multiplied by x  (b) the derivative of log_a x  (c) log_a(x) raised to a power  (d) log_a of x'
**Answer:** (b) the derivative of log_a x. The prime symbol (') denotes differentiation, not multiplication or exponentiation — (log_a x)' = 1/(x ln a). (see `exponential-logarithmic-derivatives.md`)

## Q046
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** derivative-of-inverse-functions
**Focus Area:** locating a = f⁻¹(b) before applying the formula (targeted follow-up to Q031)
**Question:** Let f(x) = x⁵ + 2x, which is strictly increasing and has an inverse g = f⁻¹. Find g'(3) by first identifying the input a with f(a) = 3.
**Answer:** f(1) = 1⁵ + 2(1) = 3, so a = 1 and g(3) = 1. f'(x) = 5x⁴ + 2, so f'(1) = 7 ≠ 0. Therefore g'(3) = 1/f'(1) = 1/7. (see `derivative-of-inverse-functions.md`)

## Q047
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** tangent-line-problems
**Focus Area:** tangent parallel to a given line, different function (targeted follow-up to Q037)
**Question:** Find all points on h(x) = x³ - 12x whose tangent line is parallel to y = 15x + 1.
**Answer:** Need h'(x) = 15: 3x² - 12 = 15 gives 3x² = 27, x² = 9, x = ±3. Since h(3) = 27-36 = -9 and h(-3) = -27+36 = 9, the points are (3,-9) and (-3,9). (see `tangent-line-problems.md`)
