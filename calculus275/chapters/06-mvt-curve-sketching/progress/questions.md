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
**Topic:** extreme-values
**Focus Area:** critical vs singular points
**Question:** Define a critical point and a singular point of f. What must be true of c in both definitions?
**Answer:** A critical point is an interior domain point c where f′(c) = 0. A singular point is an interior domain point c where f′(c) does not exist (e.g. a discontinuity, a cusp, or a vertical tangent at c). In both, c must be an interior point of the domain. See `extreme-values.md`.

## Q002
**Status:** active
**Type:** true-false
**Difficulty:** introductory
**Topic:** extreme-values
**Focus Area:** critical point need not be an extremum
**Question:** True or false: if f′(c) = 0 at an interior point c, then f has a local maximum or local minimum at c.
**Answer:** False. f(x) = x³ has f′(0) = 0, but f(x) < f(0) for x < 0 and f(x) > f(0) for x > 0, so 0 is neither a local max nor a local min. See `extreme-values.md`.

## Q003
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** extreme-values
**Focus Area:** closed interval method with a singular point
**Question:** Find the absolute maximum and minimum of f(x) = x^{2/3} − x on [−1, 8], where x^{2/3} = (∛x)². Justify that x = 0 is a singular point.
**Answer:** f is continuous on [−1, 8]. For x ≠ 0, f′(x) = 2/(3∛x) − 1 = 0 ⟺ x = 8/27 (critical point). At 0, (f(h) − f(0))/h = 1/∛h − 1 → −∞ as h → 0⁻ and +∞ as h → 0⁺, so f′(0) does not exist: 0 is singular. Candidates: f(−1) = 2, f(0) = 0, f(8/27) = 4/27, f(8) = −4. Absolute max 2 at x = −1; absolute min −4 at x = 8. See `extreme-values.md`.

## Q004
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** extreme-values
**Focus Area:** why the closed interval method works
**Question:** Explain why, for a continuous f on [a, b], it suffices to compare f at the endpoints and at critical and singular points in (a, b) to find its absolute extrema.
**Answer:** The Extreme Value Theorem guarantees absolute extrema exist. Any interior absolute extremum is also a local extremum, so by Fermat's theorem its derivative is zero if it exists. Hence an interior extremum must be a critical or singular point; the only other possibilities are the endpoints. These are candidates, not guaranteed extrema, so their values must be compared. See `extreme-values.md`.

## Q005
**Status:** active
**Type:** mcq
**Difficulty:** introductory
**Topic:** extreme-values
**Focus Area:** converse of the local extrema theorem
**Question:** For f(x) = ∛x, which statement about x = 0 is correct? (A) critical point and local min (B) singular point and local max (C) singular point but not a local extremum (D) not in the domain
**Answer:** (C). f(x) = ∛x has a singular point at x = 0 but no local extremum there. This shows the converse of "all local extrema occur at critical or singular points" does not hold. See `extreme-values.md`.

## Q006
**Status:** active
**Type:** true-false
**Difficulty:** introductory
**Topic:** extreme-values
**Focus Area:** endpoint convention
**Question:** True or false: in this course, the endpoint a of a domain [a, b] can be a local maximum of f.
**Answer:** False. By convention, local extrema are not allowed to occur at endpoints. Endpoints can still be global (absolute) extrema. See `extreme-values.md`.

## Q007
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** extreme-values
**Focus Area:** points outside the domain
**Question:** For f(x) = (x² + 4)/(x² − 4), f′(x) = −16x/(x² − 4)² appears undefined at x = ±2. Are x = ±2 singular points? Explain.
**Answer:** No. Singular points must be interior points of the domain, and x = ±2 are not in the domain of f, so they cannot be called singular points. f has vertical asymptotes there instead. The only critical point is x = 0. See `extreme-values.md` and `monotonicity-and-first-derivative-test.md`.

## Q008
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** rolle-and-mean-value-theorem
**Focus Area:** statement of the MVT
**Question:** State the Mean Value Theorem, including its hypotheses, and describe its geometric meaning.
**Answer:** If f is continuous on [a, b] and differentiable on (a, b), then there is at least one c ∈ (a, b) with f′(c) = (f(b) − f(a))/(b − a). Geometrically, some tangent line has the same slope as the secant line joining (a, f(a)) and (b, f(b)): instantaneous rate of change equals average rate of change somewhere in (a, b). See `rolle-and-mean-value-theorem.md`.

## Q009
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** rolle-and-mean-value-theorem
**Focus Area:** finding the MVT point
**Question:** Verify the MVT hypotheses for f(x) = √x on [1, 9] and find every c guaranteed by the theorem.
**Answer:** f is continuous on [1, 9] and differentiable on (1, 9). Secant slope = (3 − 1)/(9 − 1) = 1/4. Solve 1/(2√c) = 1/4 to get c = 4, which lies in (1, 9) and is the only solution. See `rolle-and-mean-value-theorem.md`.

## Q010
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** rolle-and-mean-value-theorem
**Focus Area:** multiple MVT points
**Question:** Find all c for which the conclusion of the MVT holds for f(x) = x³ − x on [−2, 3].
**Answer:** Secant slope = (f(3) − f(−2))/(3 − (−2)) = (24 − (−6))/5 = 30/5 = 6. f′(x) = 3x² − 1, so 3c² − 1 = 6 ⟺ c² = 7/3, giving c = ±√(7/3). Both lie in (−2, 3), so there are two such c (the MVT guarantees at least one, not exactly one). See `rolle-and-mean-value-theorem.md`.

## Q011
**Status:** active
**Type:** mcq
**Difficulty:** intermediate
**Topic:** rolle-and-mean-value-theorem
**Focus Area:** hypothesis failure
**Question:** For f(x) = |x| on [−1, 1], no c ∈ (−1, 1) has f′(c) equal to the secant slope. Why does this not contradict the MVT? (A) f is not continuous on [−1, 1] (B) f is not differentiable on (−1, 1) (C) f(−1) ≠ f(1) (D) the secant slope is undefined
**Answer:** (B). The secant slope is 0, but f′ is −1 or 1 wherever it exists. The MVT does not apply because differentiability fails at 0 ∈ (−1, 1). See `rolle-and-mean-value-theorem.md`.

## Q012
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** rolle-and-mean-value-theorem
**Focus Area:** proof of the MVT
**Question:** Prove the Mean Value Theorem from Rolle's theorem. What auxiliary function do you use and why?
**Answer:** Let m = (f(b) − f(a))/(b − a) and h(x) = f(x) − f(a) − m(x − a). This subtracts the secant line y = f(a) + m(x − a) from f, making both endpoint heights zero. h is continuous on [a, b], differentiable on (a, b), and h(a) = h(b) = 0. Rolle's theorem gives c ∈ (a, b) with h′(c) = f′(c) − m = 0, i.e. f′(c) = m. See `rolle-and-mean-value-theorem.md`.

## Q013
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** rolle-and-mean-value-theorem
**Focus Area:** proof of Rolle's theorem
**Question:** Prove Rolle's theorem using the Extreme Value Theorem and Fermat's theorem.
**Answer:** By the EVT, f attains a maximum and a minimum on [a, b]. If f is constant, every interior point has f′ = 0. Otherwise some value differs from the common endpoint value f(a) = f(b), so a maximum or a minimum occurs at an interior point c. Since f is differentiable there, Fermat's theorem gives f′(c) = 0. See `rolle-and-mean-value-theorem.md`.

## Q014
**Status:** active
**Type:** true-false
**Difficulty:** introductory
**Topic:** rolle-and-mean-value-theorem
**Focus Area:** uniqueness of c
**Question:** True or false: the MVT guarantees exactly one c ∈ (a, b) with f′(c) = (f(b) − f(a))/(b − a).
**Answer:** False. It guarantees at least one such c. For a linear function every c ∈ (a, b) works, and x³ − x on [−2, 3] has two values, ±√(7/3). See `rolle-and-mean-value-theorem.md`.

## Q015
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** consequences-of-mvt
**Focus Area:** derivative bound gives an error bound
**Question:** Use the MVT to show that 0 < √4.04 − 2 ≤ 0.01.
**Answer:** For x, y ≥ 4, the derivative of √t, namely 1/(2√t), is at most 1/4 between them. The MVT gives |√y − √x| ≤ (1/4)|y − x|. With x = 4, y = 4.04: √4.04 − 2 ≤ (1/4)(0.04) = 0.01, and it is positive since √t is increasing. See `consequences-of-mvt.md`.

## Q016
**Status:** active
**Type:** true-false
**Difficulty:** intermediate
**Topic:** consequences-of-mvt
**Focus Area:** interval condition
**Question:** True or false: since f(x) = 1/x has f′(x) < 0 everywhere on its domain, f is decreasing on its domain.
**Answer:** False. The monotonicity conclusion holds separately on (−∞, 0) and (0, ∞), not on the disconnected domain: −1 < 1 but f(−1) = −1 < f(1) = 1. The MVT cannot compare these values because f is undefined at 0 ∈ [−1, 1]. See `consequences-of-mvt.md`.

## Q017
**Status:** active
**Type:** true-false
**Difficulty:** introductory
**Topic:** consequences-of-mvt
**Focus Area:** converse of the monotonicity test
**Question:** True or false: if f is strictly increasing on ℝ and differentiable, then f′(x) > 0 for every x.
**Answer:** False. f(x) = x³ is strictly increasing on ℝ, yet f′(0) = 0. A zero derivative alone does not show a function stops increasing or has a local extremum. See `consequences-of-mvt.md`.

## Q018
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** consequences-of-mvt
**Focus Area:** inequality from an unknown MVT point
**Question:** Prove that x/(1 + x²) < arctan x < x for every x > 0.
**Answer:** arctan t is continuous on [0, x] and differentiable on (0, x). The MVT gives c ∈ (0, x) with arctan x − arctan 0 = x/(1 + c²). Since 0 < c < x, 1/(1 + x²) < 1/(1 + c²) < 1. Multiplying by x > 0 gives x/(1 + x²) < arctan x < x. See `consequences-of-mvt.md`.

## Q019
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** consequences-of-mvt
**Focus Area:** bounding a logarithm by monotonicity
**Question:** Prove that x − x²/2 < ln(1 + x) < x for every x > 0.
**Answer:** Let F(x) = x − ln(1 + x) for x ≥ 0: F(0) = 0 and F′(x) = x/(1 + x) > 0 for x > 0, so the MVT on [0, x] gives F(x) > F(0) = 0, the upper bound. Let G(x) = ln(1 + x) − x + x²/2: G(0) = 0 and G′(x) = 1/(1 + x) − 1 + x = x²/(1 + x) > 0 for x > 0, so G(x) > 0, the lower bound. See `consequences-of-mvt.md`.

## Q020
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** consequences-of-mvt
**Focus Area:** repeated Rolle's theorem bounds roots
**Question:** Let A, B, C ∈ ℝ. Prove that eˣ − Ax² − Bx − C = 0 has at most three distinct real roots.
**Answer:** Let F(x) = eˣ − Ax² − Bx − C and suppose four distinct roots r₁ < r₂ < r₃ < r₄. F is smooth, so Rolle on each [rᵢ, rᵢ₊₁] gives three distinct zeros s₁ < s₂ < s₃ of F′. Rolle on F′ over [s₁, s₂], [s₂, s₃] gives two zeros t₁ < t₂ of F″. Rolle once more gives a zero of F‴ in (t₁, t₂), contradicting F‴(x) = eˣ > 0. See `consequences-of-mvt.md`.

## Q021
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** consequences-of-mvt
**Focus Area:** limit of differences via the MVT
**Question:** Evaluate lim_{x→+∞} x²[ln(arctan(x + 1)) − ln(arctan x)] using the MVT.
**Answer:** Let H(t) = ln(arctan t), H′(t) = 1/[(1 + t²) arctan t]. The MVT on [x, x + 1] gives cₓ ∈ (x, x + 1) with x²[H(x + 1) − H(x)] = (x²/(1 + cₓ²))(1/arctan cₓ). Since 1 < cₓ/x < 1 + 1/x, cₓ/x → 1 and cₓ → +∞, so x²/(1 + cₓ²) = 1/[x⁻² + (cₓ/x)²] → 1 and arctan cₓ → π/2. The limit is 2/π. See `consequences-of-mvt.md`.

## Q022
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** consequences-of-mvt
**Focus Area:** zero derivative implies constant
**Question:** Suppose f and g are continuous on an interval I and f′ = g′ throughout its interior. What can you conclude, and which MVT consequence justifies it?
**Answer:** f and g differ by a constant on I. Apply the consequence "f′ = 0 on the interior of I implies f constant on I" to f − g. The hypothesis that I is an interval matters (compare 1/x on a disconnected domain). See `consequences-of-mvt.md`.

## Q023
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** monotonicity-and-first-derivative-test
**Focus Area:** sign chart from factorization
**Question:** Find the intervals on which f(x) = x³ − x is strictly increasing and strictly decreasing.
**Answer:** f′(x) = 3x² − 1 = 3(x − 1/√3)(x + 1/√3). Test points: f′(−10) > 0, f′(0) = −1 < 0, f′(10) > 0. f is strictly increasing on (−∞, −1/√3) and (1/√3, ∞), strictly decreasing on (−1/√3, 1/√3). See `monotonicity-and-first-derivative-test.md`.

## Q024
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** monotonicity-and-first-derivative-test
**Focus Area:** classifying extrema with a sign chart
**Question:** For p(x) = x³ − 6x² + 9x, find the intervals of increase/decrease, all local extrema, and state whether they are absolute on ℝ.
**Answer:** p(x) = x(x − 3)², p′(x) = 3(x − 1)(x − 3). p′ is + on (−∞, 1), − on (1, 3), + on (3, ∞). So p increases on (−∞, 1) and (3, ∞), decreases on (1, 3); strict local max (1, 4), strict local min (3, 0). Neither is absolute on ℝ because p → −∞ as x → −∞ and p → +∞ as x → +∞. See `monotonicity-and-first-derivative-test.md`.

## Q025
**Status:** active
**Type:** mcq
**Difficulty:** intermediate
**Topic:** monotonicity-and-first-derivative-test
**Focus Area:** reading a graph of f′
**Question:** On an interval, f′ > 0 and f′ is decreasing. Which describes f? (A) decreasing, concave up (B) increasing, concave down (C) increasing, concave up (D) decreasing, concave down
**Answer:** (B). f′ > 0 means f is increasing; f′ decreasing means f is concave downward. f increases while its slopes get smaller. See `monotonicity-and-first-derivative-test.md`.

## Q026
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** monotonicity-and-first-derivative-test
**Focus Area:** limits of the graph of f′
**Question:** Given only the graph of f′, which features of f can you determine, and what can you not determine? Why?
**Answer:** From the height (sign) of f′: where f increases or decreases. From whether f′ rises or falls: concavity of f. From zeros of f′ with a sign change: local max (+ to −) or local min (− to +). You cannot determine the height f(c), because adding a constant to f leaves f′ unchanged. A zero of f′ without a sign change need not be an extremum. See `monotonicity-and-first-derivative-test.md`.

## Q027
**Status:** active
**Type:** true-false
**Difficulty:** intermediate
**Topic:** monotonicity-and-first-derivative-test
**Focus Area:** first derivative test at singular points
**Question:** True or false: the first derivative test can only be applied at points c where f′(c) = 0.
**Answer:** False. It requires f continuous at the interior point c and differentiable immediately to either side; it also applies when f′(c) does not exist (singular points, e.g. a corner or cusp). See `monotonicity-and-first-derivative-test.md`.

## Q028
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** concavity-and-second-derivative-test
**Focus Area:** second derivative test
**Question:** State the second derivative test, including what happens when f″(c) = 0.
**Answer:** If f is twice differentiable near c and f′(c) = 0, then f″(c) > 0 implies a strict local minimum and f″(c) < 0 implies a strict local maximum. If f″(c) = 0 the test gives no conclusion; examine the sign of f′ on either side instead. See `concavity-and-second-derivative-test.md`.

## Q029
**Status:** active
**Type:** mcq
**Difficulty:** intermediate
**Topic:** concavity-and-second-derivative-test
**Focus Area:** why f″(c) = 0 is inconclusive
**Question:** x⁴, −x⁴ and x³ all have f′(0) = f″(0) = 0. Which correctly classifies x = 0 for each, in that order? (A) all have no extremum (B) min, max, neither (C) min, min, neither (D) inflection, inflection, inflection
**Answer:** (B). x⁴ has a strict local min, −x⁴ a strict local max, and x³ neither, which is why f″(c) = 0 makes the second derivative test inconclusive. See `concavity-and-second-derivative-test.md`.

## Q030
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** concavity-and-second-derivative-test
**Focus Area:** inflection point without a second derivative
**Question:** Show that (0, 0) is an inflection point of v(x) = x|x| even though v″(0) does not exist. Contrast with u(x) = x⁴.
**Answer:** v is continuous at 0; v(x) = −x² for x < 0 and x² for x > 0, so v″ = −2 for x < 0 and 2 for x > 0: concavity changes, so (0, 0) is an inflection point. v′(0) = lim_{h→0}|h| = 0, but v′(x) = 2|x| has unequal one-sided derivatives at 0, so v″(0) does not exist. By contrast u″(x) = 12x² > 0 on both sides of 0, so (0, 0) is not an inflection point of x⁴ despite u″(0) = 0. See `concavity-and-second-derivative-test.md`.

## Q031
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** concavity-and-second-derivative-test
**Focus Area:** exponential curve analysis
**Question:** For g(x) = xe^{−x}, find all local extrema, intervals of concavity, inflection points, and the horizontal asymptote as x → +∞.
**Answer:** g′(x) = e^{−x}(1 − x), g″(x) = e^{−x}(x − 2). g increases on (−∞, 1), decreases on (1, ∞): absolute max at (1, e^{−1}), no local min. Concave down on (−∞, 2), up on (2, ∞), inflection point (2, 2e^{−2}). By l'Hôpital's rule, x/eˣ → 0 as x → +∞, so y = 0 is a horizontal asymptote approached from above. As x → −∞, g → −∞, so no absolute minimum. See `concavity-and-second-derivative-test.md`.

## Q032
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** concavity-and-second-derivative-test
**Focus Area:** critical and inflection points of a quartic
**Question:** For q(x) = x⁴ − 4x², find all critical points, classify the local extrema, and find all inflection points.
**Answer:** q′(x) = 4x(x² − 2), q″(x) = 12x² − 8. Critical points −√2, 0, √2. q″(0) = −8 < 0: strict local max (0, 0). q″(±√2) = 16 > 0: strict local minima (±√2, −4), also absolute minima since q(x) = (x² − 2)² − 4 ≥ −4. No absolute max. q″ < 0 for |x| < √(2/3), > 0 for |x| > √(2/3), so inflection points are (±√(2/3), −20/9). See `concavity-and-second-derivative-test.md`.

## Q033
**Status:** active
**Type:** true-false
**Difficulty:** introductory
**Topic:** concavity-and-second-derivative-test
**Focus Area:** f″ = 0 vs inflection
**Question:** True or false: if f″(c) = 0, then (c, f(c)) is an inflection point.
**Answer:** False. f″(c) = 0 or f″(c) undefined only means f may have an inflection point there; you must verify that f is continuous at c and concavity actually changes across c. Example: x⁴ has f″(0) = 0 but is concave up on both sides. See `concavity-and-second-derivative-test.md`.

## Q034
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** curve-sketching
**Focus Area:** curve sketching procedure
**Question:** List the steps of the curve sketching procedure.
**Answer:** (i) Find the domain (and note symmetry); (ii) find/plot intercepts; (iii) find vertical and horizontal asymptotes (limits at domain boundaries and at ±∞); (iv) compute f′ to find critical/singular points, intervals of increase/decrease, and local extrema; (v) compute f″ to find intervals of concavity and inflection points; then draw the branches consistently with all of this. See `curve-sketching.md`.

## Q035
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** curve-sketching
**Focus Area:** rational function with disconnected domain
**Question:** For f(x) = (x² + 1)/(x² − 4), find the domain, symmetry, intercepts, asymptotes (with one-sided behaviour), monotonicity, local extrema, concavity, and inflection points. You are given f′(x) = −10x/(x² − 4)² and f″(x) = 10(3x² + 4)/(x² − 4)³.
**Answer:** Domain ℝ \ {−2, 2}; even. Only intercept (0, −1/4). f = 1 + 5/(x² − 4) → 1, so y = 1 is a horizontal asymptote approached from above. Vertical asymptotes x = ±2: f → +∞ (x → −2⁻), −∞ (−2⁺), −∞ (2⁻), +∞ (2⁺). Increasing on (−∞, −2), (−2, 0); decreasing on (0, 2), (2, ∞). Only critical point 0: strict local max (0, −1/4); no singular points. Concave up on (−∞, −2), (2, ∞), down on (−2, 2). No inflection points (concavity changes only where f is undefined). No absolute extrema (unbounded branches). See `curve-sketching.md`.

## Q036
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** curve-sketching
**Focus Area:** asymptotes and intercepts
**Question:** For f(x) = (x² + 4)/(x² − 4), find the intercepts, the horizontal asymptote, and the four one-sided limits at the vertical asymptotes.
**Answer:** y-intercept (0, −1); no x-intercepts since x² + 4 = 0 has no solutions. lim_{x→±∞} f(x) = 1, so y = 1 is a horizontal asymptote (approached from above since f > 1 for large x). lim_{x→−2⁻} f = ∞, lim_{x→−2⁺} f = −∞, lim_{x→2⁻} f = −∞, lim_{x→2⁺} f = ∞ (numerator → 8, denominator → 0 with the appropriate sign). See `curve-sketching.md`.

## Q037
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** curve-sketching
**Focus Area:** concavity changes across asymptotes
**Question:** For f(x) = (x² + 4)/(x² − 4), f″(x) = (48x² + 64)/(x² − 4)³ changes sign at x = ±2. Does f have inflection points? Why must the concavity sign chart still be split at x = ±2?
**Answer:** No inflection points. f″ is never zero (48x² + 64 > 0) and exists on the whole domain; the sign changes happen only at x = ±2, which are not in the domain, so they cannot be inflection points. The chart must still be split at the vertical asymptotes because f can have different concavities on either side: concave up on (−∞, −2) and (2, ∞), concave down on (−2, 2). See `concavity-and-second-derivative-test.md` and `curve-sketching.md`.
