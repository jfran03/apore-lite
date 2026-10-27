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
**Topic:** antiderivatives
**Focus Area:** definition of antiderivative
**Question:** State the definition of an antiderivative of f on an interval I. How do you verify that a proposed antiderivative is correct?
**Answer:** F is an antiderivative of f on I if F′(x) = f(x) for every x ∈ I. Since integration reverses differentiation, verify by differentiating the answer and checking you recover f. See `antiderivatives.md`.

## Q002
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** antiderivatives
**Focus Area:** why the + C describes all antiderivatives
**Question:** Suppose F and G are both antiderivatives of f on an interval I. Prove that F − G is constant on I, and state what this says about the set of all antiderivatives of f. Which theorem is used, and why does the hypothesis "on an interval" matter?
**Answer:** (F − G)′(x) = F′(x) − G′(x) = f(x) − f(x) = 0 for all x ∈ I. A consequence of the Mean Value Theorem is that a function with zero derivative on an interval is constant, so F − G is constant. Hence if F is any antiderivative of f, the set of all antiderivatives is {F(x) + C | C ∈ ℝ}, written ∫ f(x) dx = F(x) + C. The MVT consequence is applied on an interval I, which is why the definition specifies one. See `antiderivatives.md`.

## Q003
**Status:** active
**Type:** true-false
**Difficulty:** introductory
**Topic:** antiderivatives
**Focus Area:** non-uniqueness of antiderivatives
**Question:** True or false: F(x) = (1/3)x³ + 12 and G(x) = (1/3)x³ − 2 are both antiderivatives of f(x) = x².
**Answer:** True. Both have derivative x². Antiderivatives are not unique: if F is an antiderivative of f, so is F + C for any constant C. See `antiderivatives.md`.

## Q004
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** antiderivatives
**Focus Area:** reverse power rule and linearity
**Question:** Find ∫ (x^(−3/2) + 3e^x) dx.
**Answer:** By linearity, ∫ x^(−3/2) dx + 3∫ e^x dx = x^(−1/2)/(−1/2) + 3e^x + C = −2x^(−1/2) + 3e^x + C. See `antiderivatives.md`.

## Q005
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** antiderivatives
**Focus Area:** rewrite before integrating
**Question:** For x > 0, find ∫ (6√x − 4/x + 5e^x) dx and verify your answer.
**Answer:** Rewrite as ∫ (6x^(1/2) − 4x^(−1) + 5e^x) dx = 6·x^(3/2)/(3/2) − 4 ln x + 5e^x + C = 4x^(3/2) − 4 ln x + 5e^x + C (one constant for the whole sum). Differentiating gives 6√x − 4/x + 5e^x. See `antiderivatives.md`.

## Q006
**Status:** active
**Type:** mcq
**Difficulty:** introductory
**Topic:** antiderivatives
**Focus Area:** basic antiderivative formulas
**Question:** Which is an antiderivative of sec x tan x? (a) tan x (b) sec x (c) sec² x (d) −cos x
**Answer:** (b) sec x. From the basic formula table: sec² x has antiderivative tan x, and sec x tan x has antiderivative sec x. See `antiderivatives.md`.

## Q007
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** antiderivatives
**Focus Area:** scaled inverse tangent
**Question:** Find ∫ dx/(9 + 4x²), and verify the coefficient by differentiation.
**Answer:** d/dx arctan(2x/3) = (2/3)/(1 + 4x²/9) = (2/3)/((9 + 4x²)/9) = 6/(9 + 4x²). So ∫ dx/(9 + 4x²) = (1/6) arctan(2x/3) + C on ℝ. See `antiderivatives.md`.

## Q008
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** antiderivatives
**Focus Area:** scaled inverse sine and domain
**Question:** Find ∫ dx/√(25 − 9x²). On what interval is your answer valid? Verify by differentiation.
**Answer:** On −5/3 < x < 5/3: d/dx arcsin(3x/5) = (3/5)/√(1 − 9x²/25) = (3/5)/(√(25 − 9x²)/5) = 3/√(25 − 9x²). So the family is (1/3) arcsin(3x/5) + C on (−5/3, 5/3). See `antiderivatives.md`.

## Q009
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** antiderivatives
**Focus Area:** reverse chain rule with linear inner function
**Question:** If F′ = f, what is ∫ f(kx + b) dx for constants k ≠ 0 and b? Why does the factor 1/k appear, and when does this shortcut apply?
**Answer:** ∫ f(kx + b) dx = (1/k) F(kx + b) + C. Differentiating F(kx + b) introduces a factor k (chain rule), so 1/k cancels it. The recognition works only when the inner derivative is constant; more general substitution is developed separately. See `antiderivatives.md`.

## Q010
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** antiderivatives
**Focus Area:** initial conditions, position from acceleration
**Question:** A particle has acceleration a(t) = 6t − 4 for t ≥ 0, with v(0) = 3 and s(0) = 2. Find v(t) and s(t).
**Answer:** v(t) = ∫ (6t − 4) dt = 3t² − 4t + C₁; v(0) = 3 gives C₁ = 3. s(t) = ∫ (3t² − 4t + 3) dt = t³ − 2t² + 3t + C₂; s(0) = 2 gives C₂ = 2. So v(t) = 3t² − 4t + 3, s(t) = t³ − 2t² + 3t + 2. Check: s″(t) = 6t − 4. See `antiderivatives.md`.

## Q011
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** riemann-sums
**Focus Area:** partition and Riemann sum setup
**Question:** When [a, b] is divided into n equal pieces, give the formulas for Δx and the partition points xᵢ, and write the general Riemann sum.
**Answer:** Δx = (b − a)/n (total width over number of rectangles), xᵢ = a + iΔx for i = 0, …, n. Choosing xᵢ* ∈ [xᵢ₋₁, xᵢ], the Riemann sum is Σᵢ₌₁ⁿ f(xᵢ*) Δx. See `riemann-sums.md`.

## Q012
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** riemann-sums
**Focus Area:** computing lower and upper sums
**Question:** For f(x) = 2x + 1 on [0, 2], compute L(f, 4) and U(f, 4). What do they tell you about the area, and how does this compare with the exact geometric area?
**Answer:** Δx = 1/2, points 0, 1/2, 1, 3/2, 2. f is increasing, so minima are at left endpoints and maxima at right endpoints: L(f, 4) = (1/2)(1 + 2 + 3 + 4) = 5, U(f, 4) = (1/2)(2 + 3 + 4 + 5) = 7. The area lies between 5 and 7. The region is a trapezoid with sides 1 and 5 and width 2, exact area 6, consistent with the bounds. See `riemann-sums.md`.

## Q013
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** riemann-sums
**Focus Area:** interior extrema in lower/upper sums
**Question:** Let f(x) = (x − 1)² on [0, 2] with partition 0, 3/2, 2. Find the lower sum L and upper sum U. Is the right-endpoint sum equal to U? Explain.
**Answer:** On [0, 3/2], min is f(1) = 0 and max is f(0) = 1. On [3/2, 2], f increases from 1/4 to 1. L = (3/2)(0) + (1/2)(1/4) = 1/8; U = (3/2)(1) + (1/2)(1) = 2. Right-endpoint sum = (3/2)(1/4) + (1/2)(1) = 7/8 ≠ U. The first subinterval contains the interior minimum x = 1, and f is not monotone there, so endpoints do not give the extrema. See `riemann-sums.md`.

## Q014
**Status:** active
**Type:** true-false
**Difficulty:** intermediate
**Topic:** riemann-sums
**Focus Area:** endpoint choice vs upper sum
**Question:** True or false: for any continuous function, the right-endpoint Riemann sum equals the upper sum U(f, n).
**Answer:** False. Right endpoints give maxima only for increasing f. For decreasing f the roles reverse, and for a nonmonotone function interior extrema must be checked on each subinterval. See `riemann-sums.md`.

## Q015
**Status:** active
**Type:** mcq
**Difficulty:** introductory
**Topic:** riemann-sums
**Focus Area:** where minima occur for monotone f
**Question:** If f is decreasing on [a, b], the lower sum L(f, n) uses f evaluated at: (a) left endpoints (b) right endpoints (c) midpoints (d) wherever f′ = 0
**Answer:** (b) right endpoints. For increasing f, minima occur at left endpoints; for decreasing f the roles reverse, so minima are at right endpoints. See `riemann-sums.md`.

## Q016
**Status:** active
**Type:** conceptual
**Difficulty:** introductory
**Topic:** definite-integral
**Focus Area:** definition of Riemann integrable
**Question:** What does it mean for f to be Riemann integrable on [a, b], and how is ∫ₐᵇ f(x) dx defined?
**Answer:** f is Riemann integrable on [a, b] if lim_{n→∞} L(f, n) and lim_{n→∞} U(f, n) both exist and agree. The common value is written ∫ₐᵇ f(x) dx and called the definite integral of f on [a, b]; when it exists it is interpreted as the area in question (a signed area). See `definite-integral.md`.

## Q017
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** definite-integral
**Focus Area:** evaluating ∫₀¹ x dx from lower sums
**Question:** Use lower Riemann sums to compute ∫₀¹ x dx. Identify ℓᵢ, compute L(f, n) in closed form, and take the limit.
**Answer:** Δx = 1/n. f(x) = x is increasing so it is smallest at left endpoints: ℓᵢ = (i − 1)/n. L(f, n) = Σᵢ₌₁ⁿ ((i − 1)/n)(1/n) = (1/n²)[0 + 1 + ⋯ + (n − 1)] = (1/n²)·(n − 1)n/2 = (1/2)(n − 1)n/n² → 1/2. Similarly U(f, n) = (1/2)(n + 1)n/n² → 1/2. The limits agree, so ∫₀¹ x dx = 1/2. See `definite-integral.md`.

## Q018
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** definite-integral
**Focus Area:** telescoping U − L and evaluating from the definition
**Question:** For f(x) = x² + 1 on [1, 3] with Δx = 2/n, you are given U(f, n) = 32/3 + 8/n + 4/(3n²). Use the fact that f is increasing to find U(f, n) − L(f, n), then find L(f, n) and ∫₁³ (x² + 1) dx.
**Answer:** Since f is increasing, U uses right endpoints and L uses left endpoints, so the difference telescopes: U − L = (2/n) Σ (f(xᵢ) − f(xᵢ₋₁)) = (2/n)(f(3) − f(1)) = (2/n)(10 − 2) = 16/n. So L(f, n) = 32/3 − 8/n + 4/(3n²). Both tend to 32/3, so ∫₁³ (x² + 1) dx = 32/3. See `definite-integral.md`.

## Q019
**Status:** active
**Type:** true-false
**Difficulty:** introductory
**Topic:** definite-integral
**Focus Area:** dummy variable
**Question:** True or false: ∫ₐᵇ f(x) dx = ∫ₐᵇ f(t) dt.
**Answer:** True. x is a dummy variable; replacing it by t does not change the value. See `definite-integral.md`.

## Q020
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** integral-properties
**Focus Area:** signed integral vs geometric area
**Question:** Use geometry to find ∫₋₁³ (x − 1) dx and the total area between y = x − 1 and the x-axis on [−1, 3].
**Answer:** The graph crosses the axis at x = 1; each side is a triangle with base 2 and height 2, area 2. ∫₋₁³ (x − 1) dx = −2 + 2 = 0, while total area = ∫ |x − 1| dx = 2 + 2 = 4. See `integral-properties.md`.

## Q021
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** integral-properties
**Focus Area:** symmetry and geometry
**Question:** Evaluate ∫₋₂² [t sin(t²) + √(4 − t²) − 3] dt without finding an antiderivative. Justify each piece.
**Answer:** sin(t²) is even, so t sin(t²) is odd and integrates to 0 on [−2, 2]. √(4 − t²) is the upper semicircle of radius 2, area 2π. The constant term gives −3(4) = −12. Total: 2π − 12. See `integral-properties.md`.

## Q022
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** integral-properties
**Focus Area:** odd function check and semicircle
**Question:** Compute ∫₋₄⁴ [x³/2 + x cos(x²) − √(16 − x²)] dx, verifying any oddness claims algebraically.
**Answer:** (−x)³ = −x³, so x³ is odd and (1/2)∫₋₄⁴ x³ dx = 0. (−x)cos((−x)²) = −x cos(x²), so x cos(x²) is odd and integrates to 0. y = √(16 − x²) is the upper half of x² + y² = 16, area (1/2)π·4² = 8π. Result: 0 + 0 − 8π = −8π. See `integral-properties.md`.

## Q023
**Status:** active
**Type:** mcq
**Difficulty:** introductory
**Topic:** integral-properties
**Focus Area:** reversing limits
**Question:** The property ∫ₐᵇ f(x) dx = −∫ᵦᵃ f(x) dx follows from which two properties? (a) linearity and comparison (b) ∫ₐᵃ f = 0 and additivity (c) the even/odd symmetry rules (d) the absolute value inequality and comparison
**Answer:** (b). 0 = ∫ₐᵃ f = ∫ₐᵇ f + ∫ᵦᵃ f, so ∫ₐᵇ f = −∫ᵦᵃ f. See `integral-properties.md`.

## Q024
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** integral-properties
**Focus Area:** comparison bounds m(b − a) ≤ ∫ f ≤ M(b − a)
**Question:** Suppose f is continuous and 1 ≤ f(x) ≤ 3 for all x in [2, 5]. What bounds can you give for ∫₂⁵ f(x) dx, and which property justifies them?
**Answer:** By the comparison property, m ≤ f ≤ M implies m(b − a) ≤ ∫ₐᵇ f ≤ M(b − a). Here 1·3 ≤ ∫₂⁵ f ≤ 3·3, so 3 ≤ ∫₂⁵ f(x) dx ≤ 9. See `integral-properties.md`.

## Q025
**Status:** active
**Type:** true-false
**Difficulty:** intermediate
**Topic:** integral-properties
**Focus Area:** cancellation in signed area
**Question:** True or false: if ∫ₐᵇ f(x) dx = 0, then the region between the graph of f and the x-axis on [a, b] has zero area.
**Answer:** False. The definite integral is a signed area (A_above − A_below); cancellation does not mean the geometric region has zero area. Example: ∫₋₁³ (x − 1) dx = 0 but the total area is 4. See `integral-properties.md`.

## Q026
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** ftc-part-1
**Focus Area:** statement of FTC Part I
**Question:** State FTC Part I precisely: its hypothesis, the function it defines, and all of its conclusions (including the value at the left endpoint).
**Answer:** If f is continuous on [a, b], then A(x) = ∫ₐˣ f(t) dt is continuous on [a, b], differentiable on (a, b), and A′(x) = f(x). In particular A is an antiderivative of f and A(a) = 0. See `ftc-part-1.md`.

## Q027
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** ftc-part-1
**Focus Area:** direct application of FTC I
**Question:** Find dy/dx for y = ∫₃ˣ cos(t²) dt. Do you need to evaluate the integral?
**Answer:** No. cos(t²) is continuous, so FTC I directly gives dy/dx = cos(x²). See `ftc-part-1.md`.

## Q028
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** ftc-part-1
**Focus Area:** second derivative and value of accumulation function
**Question:** Let A(x) = ∫₁ˣ cos(t³) dt. Find A′(x), A″(x), and A(1), checking the hypothesis of FTC I.
**Answer:** cos(t³) is continuous on ℝ, so FTC I gives A′(x) = cos(x³). By the chain rule, A″(x) = −3x² sin(x³). A(1) = 0 because the limits coincide. No elementary antiderivative of cos(t³) is needed. See `ftc-part-1.md`.

## Q029
**Status:** active
**Type:** mcq
**Difficulty:** intermediate
**Topic:** ftc-part-1
**Focus Area:** three different operations
**Question:** What is d/dx ∫₀² e^(t²) dt? (a) e^(x²) (b) e^4 − 1 (c) 0 (d) e^(x²) + C
**Answer:** (c) 0. With fixed limits, ∫₀² e^(t²) dt is a constant, so its derivative with respect to x is 0. FTC I applies only when the variable is in a limit, as in d/dx ∫ₐˣ f(t) dt = f(x), and that answer has no + C. See `ftc-part-1.md`.

## Q030
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** ftc-part-1
**Focus Area:** why FTC I holds
**Question:** Explain why A′(x) = f(x) for A(x) = ∫ₐˣ f(t) dt with f continuous. Express the difference quotient as an integral and bound its distance from f(x). Where is continuity used?
**Answer:** By additivity, (A(x + h) − A(x))/h = (1/h)∫ₓˣ⁺ʰ f(t) dt, the average value of f on the interval Iₕ between x and x + h. Then |(1/h)∫ₓˣ⁺ʰ f(t) dt − f(x)| = |(1/h)∫ₓˣ⁺ʰ (f(t) − f(x)) dt| ≤ (1/|h|)∫_{Iₕ} |f(t) − f(x)| dt ≤ max_{t∈Iₕ} |f(t) − f(x)|, which tends to 0 as h → 0 by continuity of f at x. So the difference quotient tends to f(x). Intuitively, for small h the area ∫ₓˣ⁺ʰ f is close to a rectangle of base h and height f(x). See `ftc-part-1.md`.

## Q031
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** variable-limits
**Focus Area:** composite upper limit
**Question:** Find G′(x) for G(x) = ∫₂^(x³) e^t sec(t) dt, explaining the role of FTC I and the chain rule.
**Answer:** Let F(x) = ∫₂ˣ e^t sec(t) dt; FTC I gives F′(x) = e^x sec x. Since G(x) = F(x³), the chain rule gives G′(x) = F′(x³)·(x³)′ = e^(x³) sec(x³)·3x². See `variable-limits.md`.

## Q032
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** variable-limits
**Focus Area:** two moving endpoints
**Question:** Find B′(x) if B(x) = ∫ from (1 − x²) to (e^x) of √(1 + t⁶) dt. State the hypotheses you check.
**Answer:** The integrand is continuous on ℝ and both limits are differentiable. d/dx ∫_{u(x)}^{v(x)} f(t) dt = f(v(x))v′(x) − f(u(x))u′(x). Upper: √(1 + e^(6x))·e^x. Lower: √(1 + (1 − x²)⁶)·(−2x), subtracted. B′(x) = e^x √(1 + e^(6x)) + 2x √(1 + (1 − x²)⁶). The plus sign comes from subtracting −2x. See `variable-limits.md`.

## Q033
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** variable-limits
**Focus Area:** moving lower limit and second derivative
**Question:** For x > 0, let C(x) = ∫ from (ln x) to 2 of e^(t²) dt. Find C′(x) and C″(x).
**Answer:** Reverse the limits: C(x) = −∫₂^(ln x) e^(t²) dt. FTC I and the chain rule give C′(x) = −e^((ln x)²)·(1/x) = −e^((ln x)²)/x. Differentiate −x⁻¹ e^((ln x)²) with the product and chain rules: C″(x) = x⁻² e^((ln x)²) − x⁻¹ e^((ln x)²)·(2 ln x)/x = (e^((ln x)²)/x²)(1 − 2 ln x). See `variable-limits.md`.

## Q034
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** accumulation-graphs
**Focus Area:** reading A from the graph of f
**Question:** For continuous f and A(x) = ∫꜀ˣ f(t) dt, what does the graph of f tell you about where A increases/decreases, its critical points, and its concavity? Is a zero of f enough to give A a local extremum?
**Answer:** Since A′ = f: A increases where f > 0 and decreases where f < 0. Interior zeros of f are critical points of A, but a zero alone is not enough for a local extremum; f must change sign. Where f is differentiable, A″ = f′, so increasing f gives concave-up A and decreasing f gives concave-down A. See `accumulation-graphs.md`.

## Q035
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** accumulation-graphs
**Focus Area:** absolute extrema of an accumulation function
**Question:** f is continuous and linear between the vertices (−3, 0), (−1, 2), (1, −2), (3, 0), (5, 2). Let A(x) = ∫₋₁ˣ f(t) dt on [−3, 5]. Find the intervals where A increases/decreases and the absolute extrema of A.
**Answer:** A′ = f, and f = 0 at x = 0 and x = 3, so A increases on (−3, 0) and (3, 5) and decreases on (0, 3). Values: A(−3) = −∫₋₃⁻¹ f = −(1/2)(2)(2) = −2; A(0) = (1/2)(1)(2) = 1; A(3) = 1 − 1 − 2 = −2 (negative triangles of area 1 and 2); A(5) = −2 + 2 = 0. Absolute max A(0) = 1; absolute min −2, attained at x = −3 and x = 3. Endpoints must be checked for absolute extrema. See `accumulation-graphs.md`.

## Q036
**Status:** active
**Type:** true-false
**Difficulty:** advanced
**Topic:** accumulation-graphs
**Focus Area:** concavity and corners
**Question:** In the setup where f is linear between (−3, 0), (−1, 2), (1, −2), (3, 0), (5, 2) and A(x) = ∫₋₁ˣ f(t) dt: true or false, A is not differentiable at x = −1 and x = 1 because f has corners there, so these cannot be inflection points of A.
**Answer:** False. f is continuous, so A′ = f exists everywhere, including at the corners. f increases on (−3, −1) and (1, 5) and decreases on (−1, 1), so A is concave up on (−3, −1) and (1, 5) and concave down on (−1, 1); x = −1 and x = 1 are inflection points of A. See `accumulation-graphs.md`.
