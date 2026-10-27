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
**Topic:** logarithmic-differentiation
**Focus Area:** derivative of ln |x|
**Question:** Show that (ln |x|)′ = 1/x for every x ≠ 0 by splitting into the cases x > 0 and x < 0.
**Answer:** ln |x| = ln x for x > 0, with derivative 1/x. For x < 0, ln |x| = ln(−x), and the chain rule gives (1/(−x))·(−1) = 1/x. So (ln |x|)′ = 1/x for any x ≠ 0. See `logarithmic-differentiation.md`.

## Q002
**Status:** active
**Type:** conceptual
**Difficulty:** introductory
**Topic:** logarithmic-differentiation
**Focus Area:** why ln |y| instead of ln y
**Question:** Why does logarithmic differentiation generally take ln |y| rather than ln y, and when may the absolute value be dropped?
**Answer:** ln y requires y > 0. Using ln |y| lets the method work on any interval where y is differentiable and never zero, since (ln |y|)′ = y′/y there. The absolute value may be dropped when the function is known to be positive, e.g. x² + 1 > 0. See `logarithmic-differentiation.md`.

## Q003
**Status:** active
**Type:** mcq
**Difficulty:** introductory
**Topic:** logarithmic-differentiation
**Focus Area:** the reliable procedure
**Question:** Which ordering matches the reliable procedure for logarithmic differentiation? (a) Differentiate; take ln |y|; check domain; multiply by y. (b) Check the domain and sign; take ln |y| or ln y; simplify with log laws valid on that domain; differentiate; multiply by y; substitute the original expression. (c) Take ln y; multiply by y; differentiate; check the sign. (d) Simplify with log laws; check the domain; differentiate; divide by y.
**Answer:** (b). See `logarithmic-differentiation.md`.

## Q004
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** logarithmic-differentiation
**Focus Area:** products and quotients of powers
**Question:** Use logarithmic differentiation to find y′ for y = (3x + 1)¹⁰ (x² − 1)⁵ / (2x − 1)¹³.
**Answer:** ln |y| = 10 ln |3x + 1| + 5 ln |x² − 1| − 13 ln |2x − 1|. Differentiating: y′/y = 30/(3x + 1) + 10x/(x² − 1) − 26/(2x − 1). So y′ = [(3x + 1)¹⁰ (x² − 1)⁵ / (2x − 1)¹³] · (30/(3x + 1) + 10x/(x² − 1) − 26/(2x − 1)). See `logarithmic-differentiation.md`.

## Q005
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** logarithmic-differentiation
**Focus Area:** quotient with several factors, domain check
**Question:** For x > 0, let y = (x + 2)³ √(x² + 4) / (x eˣ). Write ln y using log laws and find y′. On what set does your formula hold, and why?
**Answer:** ln y = 3 ln(x + 2) + ½ ln(x² + 4) − ln x − x, so y′ = y (3/(x + 2) + x/(x² + 4) − 1/x − 1). It holds on x > 0, where all the logarithms displayed are defined. See `logarithmic-differentiation.md`.

## Q006
**Status:** active
**Type:** true-false
**Difficulty:** introductory
**Topic:** logarithmic-differentiation
**Focus Area:** validity of log laws
**Question:** True or false: the laws ln(ab) = ln a + ln b and ln aʳ = r ln a hold for all nonzero real a and b.
**Answer:** False. They are stated for a > 0 and b > 0, which is why logarithmic differentiation first checks the domain and sign (and uses ln |y| when needed). See `logarithmic-differentiation.md`.

## Q007
**Status:** active
**Type:** conceptual
**Difficulty:** introductory
**Topic:** logarithmic-differentiation
**Focus Area:** idea and equivalent formulation
**Question:** Starting from y = f(x), derive y′ = y f′(x)/f(x) by logarithmic differentiation, then give the equivalent formulation using y = e^(ln f(x)). For what kinds of functions is the method used?
**Answer:** Taking ln |y| = ln |f(x)| and differentiating implicitly gives y′/y = f′(x)/f(x), so y′ = y f′(x)/f(x). Equivalently, y = e^(ln f(x)), and the chain rule gives y′ = e^(ln f(x)) · f′(x)/f(x). It is used for complicated products and powers. See `logarithmic-differentiation.md`.

## Q008
**Status:** active
**Type:** conceptual
**Difficulty:** introductory
**Topic:** variable-powers
**Focus Area:** why power and exponential rules fail
**Question:** Why can neither the derivative of xʳ nor the derivative of aˣ be used for y = xˣ (x > 0)? Find y′.
**Answer:** xˣ is neither of these forms: both base and exponent vary. Rewrite y = e^(x ln x); the chain and product rules give y′ = e^(x ln x)(ln x + x · 1/x) = xˣ(ln x + 1). Taking ln y = x ln x gives the same result. See `variable-powers.md`.

## Q009
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** variable-powers
**Focus Area:** variable base and exponent
**Question:** Find y′ for y = (x² + 1)^(sin x). Are absolute values needed?
**Answer:** No, since x² + 1 > 0. ln y = sin x ln(x² + 1), so y′/y = cos x ln(x² + 1) + sin x · 2x/(x² + 1) and y′ = (x² + 1)^(sin x)[cos x ln(x² + 1) + 2x sin x/(x² + 1)]. See `variable-powers.md`.

## Q010
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** variable-powers
**Focus Area:** checking the sign of the base
**Question:** Justify that logarithmic differentiation of y = (3 + cos x)^(x²) is valid for every real x, then find y′.
**Answer:** Since 3 + cos x ≥ 2 > 0, the base is positive for all real x. ln y = x² ln(3 + cos x), so y′ = (3 + cos x)^(x²) (2x ln(3 + cos x) − x² sin x/(3 + cos x)). See `variable-powers.md`.

## Q011
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** variable-powers
**Focus Area:** exponential exponent
**Question:** Find the derivative of y = (2 + x²)^(e^(−x)) for x ∈ ℝ.
**Answer:** The base is positive on ℝ. ln y = e^(−x) ln(2 + x²). Differentiating and multiplying by y: y′ = (2 + x²)^(e^(−x)) · e^(−x) (2x/(2 + x²) − ln(2 + x²)). See `variable-powers.md`.

## Q012
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** variable-powers
**Focus Area:** general formula and hypothesis
**Question:** State the definition of u(x)^v(x) used in the course, the hypothesis it needs, and the resulting formula for d/dx u(x)^v(x).
**Answer:** For u, v differentiable on an interval I with u(x) > 0 on I, define u^v = e^(v ln u). Then d/dx u^v = u^v (v′ ln u + v u′/u). The base-positive hypothesis is what makes this real-valued definition valid when the exponent varies continuously. See `variable-powers.md`.

## Q013
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** variable-powers
**Focus Area:** applying the general formula
**Question:** For x > 0, find the derivative of y = x^(sin x).
**Answer:** With u = x, v = sin x (u > 0): ln y = sin x ln x, so y′ = x^(sin x) (cos x ln x + sin x / x). See `variable-powers.md`.

## Q014
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** variable-powers
**Focus Area:** variable power at the edge of its domain
**Question:** For x > 0 let F(x) = x^(x²). Find F′(x). Does F extend continuously to 0, and does the extension have a right derivative at 0?
**Answer:** F′(x)/F(x) = 2x ln x + x, so F′(x) = x^(x²)(2x ln x + x). Since x² ln x → 0 as x → 0⁺, F(x) = e^(x² ln x) → 1, so F extends continuously with F(0) = 1. Right derivative: (F(x) − 1)/x = [(e^(x² ln x) − 1)/(x² ln x)] · x ln x → 1 · 0 = 0, using (eᵗ − 1)/t → 1 and x ln x → 0 (by l'Hôpital on ln x/(1/x)). So the right derivative is 0. See `variable-powers.md`.

## Q015
**Status:** active
**Type:** true-false
**Difficulty:** introductory
**Topic:** variable-powers
**Focus Area:** 0⁰ is not a definition
**Question:** True or false: the continuous extension of F(x) = x^(x²) has F(0) = 1 because 0⁰ = 1 by definition.
**Answer:** False. The value F(0) = 1 comes from a limit (x² ln x → 0, so F(x) → e⁰ = 1); 0⁰ is not used as a definition. See `variable-powers.md`.

## Q016
**Status:** active
**Type:** mcq
**Difficulty:** introductory
**Topic:** indeterminate-forms
**Focus Area:** recognizing non-indeterminate quotients
**Question:** Which of these is NOT an indeterminate form? (a) 0/0 (b) 1^∞ (c) f(x)/g(x) with f(x) → 3 and g(x) → 0⁺ (d) ∞⁰
**Answer:** (c). If f → 3 and g → 0⁺, then f/g → +∞ directly; neither required form occurs, so l'Hôpital's rule does not apply. See `indeterminate-forms.md`.

## Q017
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** indeterminate-forms
**Focus Area:** classifying forms
**Question:** Name the indeterminate form of each: (a) lim_(x→0⁺) xˣ (b) lim_(x→∞)(x − √(x² + 1)) (c) lim_(x→0⁺) x ln x (d) lim_(x→∞) x^(1/x) (e) lim_(x→∞)(1 + 1/x)ˣ
**Answer:** (a) 0⁰ (b) ∞ − ∞ (c) 0 × (−∞) (d) ∞⁰ (e) 1^∞. See `indeterminate-forms.md`.

## Q018
**Status:** active
**Type:** conceptual
**Difficulty:** introductory
**Topic:** indeterminate-forms
**Focus Area:** meaning of the notation
**Question:** What does the notation "0/0" describe when we say a limit has form 0/0? Is it a numerical value?
**Answer:** It describes the separate behavior of numerator and denominator (both tending to 0), not a numerical value. The same applies to ∞/∞. See `indeterminate-forms.md`.

## Q019
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** indeterminate-forms
**Focus Area:** decision sequence
**Question:** Describe the decision sequence for evaluating a limit that might need l'Hôpital's rule.
**Answer:** Substitute first. For a quotient, check 0/0 or ∞/∞ and the differentiability hypotheses before using l'Hôpital. For a product or difference, rewrite it as a quotient; for a positive variable power, take its logarithm. After each differentiation, recheck the form before applying the rule again. Algebra and continuity often finish sooner. See `indeterminate-forms.md`.

## Q020
**Status:** active
**Type:** true-false
**Difficulty:** introductory
**Topic:** indeterminate-forms
**Focus Area:** which forms l'Hôpital handles directly
**Question:** True or false: l'Hôpital's rule can be applied directly to any indeterminate form, including 0 · ∞ and 1^∞.
**Answer:** False. It applies directly only to the ratios 0/0 and ±∞/∞. Products and differences must be rewritten as quotients, and powers converted via logarithms first. See `indeterminate-forms.md`.

## Q021
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** lhopitals-rule
**Focus Area:** hypotheses of the theorem
**Question:** State all the hypotheses of l'Hôpital's rule (formal version) for lim_(x→a) f(x)/g(x).
**Answer:** I is an open interval with a a finite endpoint (or a = ±∞ when I is unbounded in that direction); f and g are differentiable on I; g(x) ≠ 0 and g′(x) ≠ 0 for every x ∈ I; as x → a through I, either f → 0 and g → 0, or |f| → ∞ and |g| → ∞; and lim f′/g′ = L exists in ℝ ∪ {±∞}. Then lim f/g = L. See `lhopitals-rule.md`.

## Q022
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** lhopitals-rule
**Focus Area:** basic 0/0
**Question:** Evaluate lim_(x→0) x²/tan x.
**Answer:** Form 0/0. l'Hôpital: lim 2x/sec² x = 0/1 = 0. See `lhopitals-rule.md`.

## Q023
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** lhopitals-rule
**Focus Area:** repeated ∞/∞
**Question:** Evaluate lim_(x→∞)(2x² − 1)/(3x² + x + 2) using l'Hôpital's rule, checking the form at each step.
**Answer:** ∞/∞; l'H gives 4x/(6x + 1), still ∞/∞; l'H again gives 4/6 = 2/3. See `lhopitals-rule.md`.

## Q024
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** lhopitals-rule
**Focus Area:** two applications
**Question:** Evaluate lim_(x→0)(e^(2x) − 1 − 2x)/x².
**Answer:** 0/0. After one differentiation: 2(e^(2x) − 1)/(2x), still 0/0. Second application: 4e^(2x)/2 → 2. See `lhopitals-rule.md`.

## Q025
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** lhopitals-rule
**Focus Area:** l'Hôpital followed by algebra
**Question:** Determine lim_(x→0)(ln(1 + x) − x)/x².
**Answer:** Both tend to 0; for x near 0, x ≠ 0, we have x > −1 and 2x ≠ 0. One application: (1/(1 + x) − 1)/(2x) = −1/(2(1 + x)) → −1/2. See `lhopitals-rule.md`.

## Q026
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** lhopitals-rule
**Focus Area:** growth at infinity
**Question:** Determine lim_(x→∞) ln x / √x, verifying the hypotheses you use.
**Answer:** Both → +∞; the denominator derivative 1/(2√x) is nonzero for x > 0. l'H: (1/x)/(1/(2√x)) = 2/√x → 0. See `lhopitals-rule.md`.

## Q027
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** lhopitals-rule
**Focus Area:** comparing logarithmic growth rates
**Question:** Determine lim_(x→∞) ln(1 + x²)/ln(1 + x).
**Answer:** Both → +∞, and the denominator derivative 1/(1 + x) ≠ 0 for x > 0. l'H gives [2x/(1 + x²)]/[1/(1 + x)] = 2x(1 + x)/(1 + x²) → 2. See `lhopitals-rule.md`.

## Q028
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** lhopitals-rule
**Focus Area:** third-order 0/0
**Question:** Evaluate lim_(x→0)(x − sin x)/x³.
**Answer:** 0/0. Three applications: (1 − cos x)/(3x²), then sin x/(6x), then cos x/6 → 1/6. See `lhopitals-rule.md`.

## Q029
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** lhopitals-rule
**Focus Area:** derivative quotient with no limit
**Question:** Evaluate lim_(x→0⁺) x sin(1/x), and explain why l'Hôpital's rule gives no conclusion when the expression is written as x² sin(1/x)/x.
**Answer:** Since −x ≤ x sin(1/x) ≤ x for x > 0, the squeeze theorem gives 0. Differentiating x² sin(1/x)/x gives (2x sin(1/x) − cos(1/x))/1, which has no limit as x → 0⁺. Existence of lim f′/g′ is a hypothesis, so it fails and the rule gives no conclusion, even though the original limit exists. See `lhopitals-rule.md`.

## Q030
**Status:** active
**Type:** true-false
**Difficulty:** intermediate
**Topic:** lhopitals-rule
**Focus Area:** converse misconception
**Question:** True or false: if f/g has form 0/0 at a and lim_(x→a) f′(x)/g′(x) does not exist, then lim_(x→a) f(x)/g(x) does not exist.
**Answer:** False. l'Hôpital's rule then gives no conclusion; the original limit may still exist and must be found another way (algebra, comparison, a known limit). Example: x sin(1/x) → 0 as x → 0⁺. See `lhopitals-rule.md`.

## Q031
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** lhopitals-rule
**Focus Area:** powers dominate logarithms
**Question:** For α > 0 and k ∈ ℕ, prove lim_(x→∞) x^α/(ln x)ᵏ = +∞.
**Answer:** It is enough to show the reciprocal tends to 0. (ln x)ᵏ/x^α is ∞/∞, and applying l'Hôpital's rule k times gives lim k!/(αᵏ x^α) = 0. Hence x^α/(ln x)ᵏ → +∞. See `lhopitals-rule.md`.

## Q032
**Status:** active
**Type:** conceptual
**Difficulty:** introductory
**Topic:** lhopitals-rule
**Focus Area:** intuition
**Question:** In one sentence, why does l'Hôpital's rule make sense?
**Answer:** The ratio of growth rates determines the eventual ratio of the underlying quantities. See `lhopitals-rule.md`.

## Q033
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** lhopitals-rule
**Focus Area:** two-sided limits at interior points
**Question:** The formal theorem is stated for a an endpoint of an open interval I. How do you use it for a two-sided limit at a finite interior point a?
**Answer:** Choose a left-hand interval and a right-hand interval (each with a as an endpoint) and apply the theorem separately on each side. See `lhopitals-rule.md`.

## Q034
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** products-and-differences
**Focus Area:** 0 × (−∞) to a ratio
**Question:** Evaluate lim_(x→0⁺) x ln x.
**Answer:** Form 0 × (−∞). Write as ln x/(1/x) (form −∞/∞). l'H: (1/x)/(−1/x²) = −x → 0. See `products-and-differences.md`.

## Q035
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** products-and-differences
**Focus Area:** 0 · ∞ with trig
**Question:** Evaluate lim_(x→π)(x − π) cot x.
**Answer:** Write it as (x − π)/tan x, which is 0/0. Since (tan x)′ = sec² x, l'H gives lim 1/sec² x = 1. See `products-and-differences.md`.

## Q036
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** products-and-differences
**Focus Area:** ∞ − ∞ by rationalizing
**Question:** Determine lim_(x→∞)(√(x² + 3x) − x). Is l'Hôpital's rule needed?
**Answer:** Form ∞ − ∞. Rationalize: 3x/(√(x² + 3x) + x) = 3/(√(1 + 3/x) + 1) → 3/2. The algebra settles it without l'Hôpital. See `products-and-differences.md`.

## Q037
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** products-and-differences
**Focus Area:** difference hidden in reciprocals
**Question:** Evaluate lim_(x→0)(1/sin x − 1/x).
**Answer:** Combine first: (x − sin x)/(x sin x), form 0/0. l'H twice: (1 − cos x)/(sin x + x cos x), then sin x/(2 cos x − x sin x) → 0/2 = 0. See `products-and-differences.md`.

## Q038
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** products-and-differences
**Focus Area:** choosing the quotient
**Question:** As x → 0⁺, x² ln sin x has form 0 × (−∞). It can be written as x²/(1/ln sin x) or as ln sin x/(1/x²). Which is the better choice and why?
**Answer:** ln sin x/(1/x²) (form −∞/∞). The other ratio is a valid 0/0 form, but 1/ln sin x has a bad derivative. For a product, choose the quotient that is simpler to differentiate. See `products-and-differences.md`.

## Q039
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** products-and-differences
**Focus Area:** ∞ − ∞ without l'Hôpital
**Question:** Evaluate lim_(x→∞)(x³ − x²). Does it require l'Hôpital's rule?
**Answer:** It is ∞ − ∞, but factoring gives x²(x − 1), a product of two factors tending to ∞, so the limit is ∞. No need for l'Hôpital. See `products-and-differences.md`.

## Q040
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** products-and-differences
**Focus Area:** product tending to a finite number
**Question:** Evaluate lim_(x→0⁺) x ln(1/x).
**Answer:** Form 0 · ∞. Write ln(1/x)/(1/x); both → +∞. l'H: (−1/x)/(−1/x²) = x → 0. See `products-and-differences.md`.

## Q041
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** products-and-differences
**Focus Area:** general conversions
**Question:** Give the general quotient rewrites for (a) f·g with f → 0, |g| → ∞, and (b) f − g with f, g → +∞. What must be checked afterwards?
**Answer:** (a) fg = f/(1/g) = g/(1/f). (b) f − g = (1/g − 1/f)/(1/(fg)). Afterwards, check that the resulting quotient has form 0/0 or ∞/∞ before using the rule (and for differences, combining fractions, factoring, or rationalizing may be simpler). See `products-and-differences.md`.

## Q042
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** indeterminate-powers
**Focus Area:** 1^∞ and the number e
**Question:** Show that lim_(x→∞)(1 + 1/x)ˣ = e.
**Answer:** Take the log: x ln(1 + 1/x), form ∞ × 0. Ratio: ln(1 + 1/x)/(1/x), form 0/0. l'H: [1/(1 + 1/x) · (−1/x²)]/(−1/x²) = 1/(1 + 1/x) → 1. Exponentiate: e¹ = e. One can define e as this limit. See `indeterminate-powers.md`.

## Q043
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** indeterminate-powers
**Focus Area:** ∞⁰
**Question:** Evaluate lim_(x→∞) x^(1/x).
**Answer:** ∞⁰. Limit of the log: ln x/x (∞/∞), and l'H gives (1/x)/1 → 0. Answer e⁰ = 1. See `indeterminate-powers.md`.

## Q044
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** indeterminate-powers
**Focus Area:** 0⁰ with two l'Hôpital steps
**Question:** Evaluate lim_(x→0⁺)(sin x)^(x²).
**Answer:** 0⁰. Its log is x² ln sin x (0 × (−∞)); write as ln sin x/(1/x²) (−∞/∞). l'H: (cos x/sin x)/(−2/x³) = x³ cos x/(−2 sin x) (0/0). l'H again: (3x² cos x − x³ sin x)/(−2 cos x) → 0. So the limit is e⁰ = 1. See `indeterminate-powers.md`.

## Q045
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** indeterminate-powers
**Focus Area:** 1^∞ with limit 1
**Question:** Evaluate lim_(x→∞)(1 + 4/x²)ˣ.
**Answer:** ln yₓ = x ln(1 + 4/x²) = ln(1 + 4/x²)/(1/x), form 0/0. l'H: [(−8/x³)/(1 + 4/x²)]/(−1/x²) = 8/(x(1 + 4/x²)) → 0. So the limit is e⁰ = 1. See `indeterminate-powers.md`.

## Q046
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** indeterminate-powers
**Focus Area:** refined 1^∞
**Question:** Evaluate lim_(x→0⁺)(e/(1 + x)^(1/x))^(1/x).
**Answer:** The base is positive. ln yₓ = (1 − ln(1 + x)/x)/x = (x − ln(1 + x))/x², form 0/0. One l'H: (1 − 1/(1 + x))/(2x) = 1/(2(1 + x)) → 1/2. So the limit is e^(1/2). See `indeterminate-powers.md`.

## Q047
**Status:** active
**Type:** mcq
**Difficulty:** introductory
**Topic:** indeterminate-powers
**Focus Area:** logarithmic conversion
**Question:** For lim [F(x)]^G(x), the course converts to exp(lim G(x) ln F(x)). What hypothesis on F is required? (a) F is differentiable at a (b) F(x) > 0 near the limiting input (c) F(x) → 1 (d) G(x) > 0
**Answer:** (b). F(x) > 0 is required near the limiting input. See `indeterminate-powers.md`.

## Q048
**Status:** active
**Type:** true-false
**Difficulty:** intermediate
**Topic:** indeterminate-powers
**Focus Area:** infinite limit of the logarithm
**Question:** True or false: if lim G(x) ln F(x) = −∞ (with F > 0 near a), then lim [F(x)]^G(x) = 0.
**Answer:** True. If lim G ln F = L ∈ ℝ ∪ {±∞}, the limit is e^L, with e^(−∞) = 0 and e^(+∞) = +∞. See `indeterminate-powers.md`.

## Q049
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** indeterminate-powers
**Focus Area:** nth root of n
**Question:** Evaluate lim_(n→∞) n^(1/n). What do you work with first, and why?
**Answer:** First consider the positive real variable x (l'Hôpital applies to differentiable functions): ln x/x is ∞/∞, and l'H gives 1/x → 0, so x^(1/x) = e^((ln x)/x) → 1. Restricting to positive integers gives n^(1/n) → 1. See `indeterminate-powers.md`.

## Q050
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** indeterminate-powers
**Focus Area:** 0⁰ from the right
**Question:** Determine lim_(x→0⁺)(sin x)ˣ.
**Answer:** For small x > 0, yₓ = (sin x)ˣ > 0. ln yₓ = ln(sin x)/(1/x), an ∞/∞ form (−∞ over +∞). l'H: cot x/(−1/x²) = −x² cos x/sin x → 0, using x/sin x → 1. So the limit is e⁰ = 1. See `indeterminate-powers.md`.

## Q051
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** limit-analysis
**Focus Area:** symmetric second-difference quotient
**Question:** If f is twice differentiable at a, prove lim_(h→0)[f(a + h) + f(a − h) − 2f(a)]/h² = f″(a).
**Answer:** Twice differentiability gives f(a ± h) = f(a) ± f′(a)h + ½ f″(a)h² + o(h²). Adding and subtracting 2f(a) cancels constant and linear terms: the numerator is f″(a)h² + o(h²). Dividing by h² gives f″(a). See `limit-analysis.md`.

## Q052
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** limit-analysis
**Focus Area:** recovering an unknown function
**Question:** Given lim_(x→0)(sin(6x) − x f(x))/x³ = 0, find lim_(x→0)(6 − f(x))/x².
**Answer:** Split (6 − f)/x² = (6x − sin 6x)/x³ + (sin 6x − x f)/x³. The second term → 0 by hypothesis. For the first, l'H twice: (6 − 6 cos 6x)/(3x²), then 36 sin 6x/(6x) → 36. So the limit is 36. See `limit-analysis.md`.

## Q053
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** limit-analysis
**Focus Area:** bounded function with derivative limit
**Question:** Let f be differentiable and bounded on [a, ∞), and suppose lim_(x→∞) f′(x) = A exists. Prove A = 0.
**Answer:** If A > 0, then f′(x) > A/2 for all sufficiently large x, so by the mean value theorem f eventually increases at least linearly, contradicting boundedness. If A < 0, apply the same argument to −f. Thus A = 0. See `limit-analysis.md`.

## Q054
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** limit-analysis
**Focus Area:** converse fails
**Question:** Give a differentiable f on [0, ∞) with f(x) → 0 as x → ∞ but f′(x) having no limit, and justify.
**Answer:** f(x) = sin(x²)/x for x > 0, f(0) = 0. |f(x)| ≤ 1/x so f → 0. For x > 0, f′(x) = 2 cos(x²) − sin(x²)/x²; along xₙ = √(2πn) it tends to 2, along yₙ = √((2n + 1)π) it tends to −2, so f′ has no limit at +∞. See `limit-analysis.md`.

## Q055
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** limit-analysis
**Focus Area:** first-order asymptotic ODE
**Question:** Let f be differentiable on (0, ∞), a > 0, and lim_(x→∞)(a f(x) + f′(x)) = L. What is lim f(x)? Outline the proof.
**Answer:** L/a. Put r = a f + f′ − L → 0. Multiplying by e^(ax) and integrating from a fixed X gives f(x) = e^(−a(x−X)) f(X) + ∫_X^x e^(−a(x−t))(L + r(t)) dt. The constant part is (L/a)(1 − e^(−a(x−X))) → L/a; choosing X with |r(t)| < aε for t ≥ X makes the remaining integral at most ε, and the first term → 0. See `limit-analysis.md`.

## Q056
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** limit-analysis
**Focus Area:** second-order asymptotic ODE
**Question:** If f ∈ C²((0, ∞)) and lim_(x→∞)(f + f′ + f″) = L, prove lim f = L using the first-order result.
**Answer:** Set h = f + f′. Then h + h′ = f + f′ + f″ → L, so by the first-order result with a = 1, h → L. Since f + f′ = h → L, apply the same result to f to get f → L. See `limit-analysis.md`.
