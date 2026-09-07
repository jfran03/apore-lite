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
