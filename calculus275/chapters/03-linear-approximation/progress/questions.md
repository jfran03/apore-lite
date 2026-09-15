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
**Topic:** linear-approximation
**Focus Area:** the linearization formula
**Question:** If f is differentiable at a, write the formula for the tangent line L_a(x), and state what the approximation f(x) ≈ L_a(x) requires.
**Answer:** L_a(x) = f(a) + f'(a)(x − a). The approximation f(x) ≈ L_a(x) holds for x close to a. See `linear-approximation.md`.

## Q002
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** linear-approximation
**Focus Area:** why linear approximation works
**Question:** Explain, from the definition of the derivative, why f(x) − f(a) ≈ f'(a)(x − a) for x near a.
**Answer:** The derivative definition says that [f(x) − f(a)]/(x − a) approaches f'(a) as x → a. Thus for nearby inputs the actual change f(x) − f(a) is approximately f'(a)(x − a). See `linear-approximation.md`.

## Q003
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** linear-approximation
**Focus Area:** reading the formula
**Question:** In L_a(x) = f(a) + f'(a)(x − a), identify the roles of a, x, and x − a, and say which part estimates the change in output.
**Answer:** a is the fixed base input, x is the target input, and x − a is the signed input change. The term f'(a)(x − a) estimates the change in output; adding f(a) estimates the new value. The subscript in L_a records the chosen base input. See `linear-approximation.md`.

## Q004
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** linear-approximation
**Focus Area:** approximating arctan(1.04)
**Question:** Approximate arctan(1.04) by linearizing f(x) = arctan x at a = 1. Show the linearization and the resulting estimate.
**Answer:** a = 1 is convenient because tan(π/4) = 1, so arctan(1) = π/4. With f(1) = π/4, f'(x) = 1/(1 + x²) and f'(1) = 1/2, the input change is 0.04 and the estimated output change is (1/2)(0.04) = 0.02. So L_1(x) = π/4 + (1/2)(x − 1) and arctan(1.04) ≈ π/4 + 0.02. See `linear-approximation.md`.

## Q005
**Status:** active
**Type:** true-false
**Difficulty:** introductory
**Topic:** linear-approximation
**Focus Area:** radians in trigonometric linearizations
**Question:** True or false: when linearizing a trigonometric function, the input may be left in degrees.
**Answer:** False. All trigonometric derivative formulas, and therefore their linear approximations, use radians. See `linear-approximation.md`. In the sec(46°) example the angle is first converted: 46° = 46π/180 rad.

## Q006
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** linear-approximation
**Focus Area:** estimating a fourth root
**Question:** Estimate the fourth root of 15.98 by linear approximation. State the function, the base point, and the resulting estimate.
**Answer:** Use f(x) = x^(1/4) with a = 16, since f(16) = 2. Then f'(x) = (1/4)x^(−3/4) = 1/(4(x^(1/4))³), so f'(16) = 1/(4·2³) = 1/32. Hence f(15.98) ≈ f(16) + f'(16)(15.98 − 16) = 2 + (1/32)(−0.02) = 2 − 2/3200 = 2 − 1/1600. See `linear-approximation.md`.

## Q007
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** linear-approximation
**Focus Area:** estimating sec(46°)
**Question:** Estimate sec(46°) using linear approximation. Include the unit conversion, the base point, and the final expression.
**Answer:** Since 180° = π rad, 1° = π/180 rad, so 46° = 46π/180 rad. Use f(x) = sec x with a = π/4: f(π/4) = sec(π/4) = 1/cos(π/4) = √2, and f'(x) = sec(x)tan(x), so f'(π/4) = √2 · 1 = √2. Then sec(46π/180) ≈ √2 + √2(46π/180 − π/4) = √2 + √2(π/180). See `linear-approximation.md`.

## Q008
**Status:** active
**Type:** mcq
**Difficulty:** intermediate
**Topic:** linear-approximation
**Focus Area:** local validity of the tangent-line model
**Question:** Which statement best describes the range over which L_a(x) is guaranteed accurate? (A) For every x in the domain of f. (B) Only locally — differentiability alone gives only a local guarantee. (C) For every x where f is increasing. (D) For every x where f'' exists.
**Answer:** (B). The formula L_a(x) may be evaluated for any x, but differentiability alone gives only a local guarantee of accuracy. A large |x − a|, a rapidly changing slope, or a singularity between a and x can make the approximation poor, and one should check that f(x) is defined at the target input. See `linear-approximation.md`.

## Q009
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** best-linear-approximation
**Focus Area:** the minimization that singles out the tangent line
**Question:** Among all lines through (a, f(a)) with slope m, which slope makes the line the best linear approximation to f near a, and what quantity is being minimized?
**Answer:** The quantity minimized is D := |f(x) − f(a) − m(x − a)|, the distance between y = f(x) and the line y − f(a) = m(x − a) near x = a. The Key Fact is that m = f'(a) is the unique value that minimizes D, so the tangent line L is the best linear approximation to f at x = a. See `best-linear-approximation.md`.

## Q010
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** best-linear-approximation
**Focus Area:** the two properties determining the tangent line
**Question:** State the two properties that determine the tangent line to f at x = a.
**Answer:** (i) It contains the point (a, f(a)); (ii) the rate of change of y = f(x) with respect to x at x = a is the slope of this line. See `best-linear-approximation.md` and `linear-approximation.md`.

## Q011
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** choosing-the-expansion-point
**Focus Area:** the two conditions on a
**Question:** What two conditions should a useful expansion point a satisfy?
**Answer:** a should be close to the input of interest, and both f(a) and f'(a) should be easy to compute. See `choosing-the-expansion-point.md`.

## Q012
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** choosing-the-expansion-point
**Focus Area:** closeness is not sufficient
**Question:** To estimate 1/4.08, why is a = 4 preferred over a = 4.1 even though 4.1 is closer to 4.08?
**Answer:** Closeness alone is not enough if it leaves the same difficult calculation inside f(a) or f'(a). Choosing a = 4.1 would be closer, but it would not simplify the starting value. With a = 4, f(x) = x^(−1) gives f(4) = 1/4 and f'(4) = −1/16, both easy. See `choosing-the-expansion-point.md`.

## Q013
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** choosing-the-expansion-point
**Focus Area:** estimating 1/4.08
**Question:** Use a linear approximation to estimate 1/4.08.
**Answer:** Choose a = 4 for f(x) = 1/x. Rewrite f(x) = x^(−1), so f'(x) = −x^(−2). Then f(4) = 1/4, f'(4) = −1/16, and the input change is 0.08. So L_4(x) = 1/4 − (1/16)(x − 4), giving 1/4.08 ≈ 1/4 − 0.08/16 = 0.245. See `choosing-the-expansion-point.md`.

## Q014
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** choosing-the-expansion-point
**Focus Area:** when the method is worth using
**Question:** When does a differential or linear approximation fail to offer much practical benefit?
**Answer:** The method is valuable when f(x) and f'(x) are simple at the chosen base point while the nearby exact value is difficult. If the differential still contains a value that is just as hard to compute as the original expression, the approximation may offer little practical benefit. See `choosing-the-expansion-point.md` and `applied-differential-problems.md`.

## Q015
**Status:** active
**Type:** mcq
**Difficulty:** introductory
**Topic:** overestimates-and-underestimates
**Focus Area:** concavity determines the direction of error
**Question:** If f'' > 0 throughout the interval between a and x, the tangent-line approximation L_a(x) is: (A) an overestimate; (B) an underestimate; (C) exact; (D) undetermined without knowing whether f is increasing.
**Answer:** (B) an underestimate. Concave up (f'' > 0) means L_a(x) lies below f(x). Concavity, not whether the function is increasing or decreasing, determines the tangent's position. See `overestimates-and-underestimates.md`.

## Q016
**Status:** active
**Type:** true-false
**Difficulty:** intermediate
**Topic:** overestimates-and-underestimates
**Focus Area:** the sign condition must hold on the whole interval
**Question:** True or false: it is enough to check the sign of f'' at the base point a to decide whether the approximation is an overestimate or an underestimate.
**Answer:** False. The sign conditions must hold throughout the interval between a and the input being approximated. If concavity changes, this test alone does not determine whether the approximation is an overestimate or an underestimate. See `overestimates-and-underestimates.md`.

## Q017
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** overestimates-and-underestimates
**Focus Area:** applying the concavity test
**Question:** For the estimate 1/4.08 ≈ 0.245 obtained from f(x) = 1/x at a = 4, decide whether the estimate is an overestimate or an underestimate, and justify it.
**Answer:** f''(x) = 2/x³ > 0 on (0, ∞), so f is concave up there and the tangent line lies below the curve. Therefore 0.245 is an underestimate of 1/4.08. See `overestimates-and-underestimates.md`.

## Q018
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** overestimates-and-underestimates
**Focus Area:** the rule holds on both sides of a
**Question:** Using f(x) = e^x linearized at a = 0, approximate e^(−0.03) and decide whether it is an overestimate or an underestimate. Why does the target input lying to the left of a not change the conclusion?
**Answer:** Since f(0) = f'(0) = 1, L_0(x) = 1 + x. The signed input change is −0.03 − 0 = −0.03, so e^(−0.03) ≈ 1 − 0.03 = 0.97. Because f''(x) = e^x > 0, the graph is concave up and 0.97 is an underestimate, even though the target input lies to the left of a — the rule works on either side of a, since concave-up graphs bend above their tangent lines. See `overestimates-and-underestimates.md`.

## Q019
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** differentials-and-exact-changes
**Focus Area:** Δy versus dy
**Question:** Write the definitions of Δy and dy, and state which one is exact and which is the approximation.
**Answer:** Δy = f(x + Δx) − f(x) is the exact change in y given Δx; with dx = Δx, dy = f'(x)dx is the change along the tangent line. The equation defining dy is exact; only the replacement of the curve's change Δy by dy is approximate, giving Δy ≈ dy = f'(x)Δx for small Δx. See `differentials-and-exact-changes.md`.

## Q020
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** differentials-and-exact-changes
**Focus Area:** differentials and linear approximation are one statement
**Question:** Show that the differential approximation is the same statement as linear approximation.
**Answer:** Apply linear approximation at the current input x to the new input x + Δx: f(x + Δx) ≈ f(x) + f'(x)Δx. After subtracting f(x), this becomes Δy ≈ f'(x)Δx = dy. See `differentials-and-exact-changes.md`.

## Q021
**Status:** active
**Type:** true-false
**Difficulty:** introductory
**Topic:** differentials-and-exact-changes
**Focus Area:** the nature of dx
**Question:** True or false: dx is an unknown quantity that must be solved for, and it is always positive.
**Answer:** False. dx is the chosen input change, not an additional unknown and not necessarily positive. Always compute a signed change as new minus old. See `differentials-and-exact-changes.md`.

## Q022
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** differentials-and-exact-changes
**Focus Area:** estimating a change with differentials
**Question:** Let S(t) = 80/(t + 4). Estimate the change in S when t increases from 6 to 6.05, and then give the approximate new value of S.
**Answer:** The old input is t = 6, so dt = 0.05. Using S(t) = 80(t + 4)^(−1), S'(t) = −80/(t + 4)², so S'(6) = −0.8. Then ΔS ≈ dS = (−0.8)(0.05) = −0.04; the sign says the output decreases. This is a change, not the new output: S(6) = 8, so S(6.05) ≈ 8 − 0.04 = 7.96. The exact change is 80/10.05 − 8 = −8/201 ≈ −0.03980. See `differentials-and-exact-changes.md`.

## Q023
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** differentials-and-exact-changes
**Focus Area:** geometric meaning of dy
**Question:** Describe dy and Δy geometrically on a graph of y = f(x) with its tangent line at x.
**Answer:** Since dy/dx is the slope of the tangent (rise/run), dy is the "rise" of the tangent line over the "run" dx. Δy is the rise along the curve from f(x) to f(x + Δx), while dy is the rise along the tangent line over the same Δx = dx. Because the tangent line is the best linear approximation to f near x, dy ≈ Δy, and this approximation improves for smaller Δx. See `differentials-and-exact-changes.md`.

## Q024
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** relative-change-and-percentage-error
**Focus Area:** relative and percentage change
**Question:** Write the formulas for relative change and percentage change in terms of dy and y, and state the condition on y.
**Answer:** relative change = Δy/y ≈ dy/y, and percentage change ≈ 100(dy/y) %. Here y = f(x) ≠ 0 is the original output. The ratios have no units because numerator and denominator have the same units. See `relative-change-and-percentage-error.md`.

## Q025
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** relative-change-and-percentage-error
**Focus Area:** the power-law relative differential
**Question:** For a power law y = Cx^n with C ≠ 0 and x > 0, derive dy/y and state what the exponent does to the relative change.
**Answer:** dy = Cnx^(n−1)dx, so dy/y = Cnx^(n−1)dx/(Cx^n) = nx^(−1)dx = n(dx/x). The constant C cancels and x^(n−1)/x^n = x^(−1). Thus the exponent multiplies the approximate relative change, and a negative exponent reverses its sign. See `relative-change-and-percentage-error.md`.

## Q026
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** relative-change-and-percentage-error
**Focus Area:** propagation of measurement error
**Question:** The resistance of a cylindrical wire of fixed length is R(r) = K/r² with K > 0 constant. If the measured radius is 1.5% too large, estimate the resulting percentage error in the computed resistance.
**Answer:** With R = Kr^(−2), dR/R = −2(dr/r). Here dr/r = 1.5/100 = 0.015, not 1.5, and the measured radius is r + dr = 1.015r. Then ΔR/R ≈ dR/R = −2(0.015) = −0.03, and 100(−0.03) = −3, so the computed resistance is approximately 3% too small. Its unsigned relative error is estimated by |ΔR|/R ≈ 0.03. This is a first-order estimate, not a rigorous maximum-error bound. See `relative-change-and-percentage-error.md`.

## Q027
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** relative-change-and-percentage-error
**Focus Area:** relative error in surface area of a cube
**Question:** A cubic box is constructed. If the error in the length measurement is at most 1%, estimate the resulting error in the surface area.
**Answer:** The surface area is A = 6ℓ², so A'(ℓ) = 12ℓ. Then ΔA/A ≈ dA/A = A'(ℓ)dℓ/A = 12ℓ dℓ/(6ℓ²) = 2(dℓ/ℓ). Given dℓ/ℓ = ±0.01, ΔA/A ≈ ±0.02, i.e. a 2% range. See `relative-change-and-percentage-error.md`.

## Q028
**Status:** active
**Type:** mcq
**Difficulty:** intermediate
**Topic:** relative-change-and-percentage-error
**Focus Area:** what a percentage change divides by
**Question:** A percentage change is computed by dividing by which quantity? (A) The change itself. (B) The original output. (C) The input change. (D) The derivative at the base point.
**Answer:** (B) the original output. A percentage change divides by the original output, not by the change. For a positive original output, a negative percentage change means a decrease. See `relative-change-and-percentage-error.md`.

## Q029
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** taylors-remainder-bound
**Focus Area:** statement of the bound
**Question:** State Taylor's remainder bound for linear approximation, including its hypotheses.
**Answer:** Suppose f is twice differentiable on an open interval containing the closed segment joining a and x, and |f''(t)| ≤ M for every t in that closed segment. Then |f(x) − L_a(x)| ≤ (M/2)|x − a|². See `taylors-remainder-bound.md`.

## Q030
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** taylors-remainder-bound
**Focus Area:** derivation of the bound
**Question:** Where does the bound (M/2)|x − a|² come from, and why is M needed at all?
**Answer:** Taylor's theorem states that, when x ≠ a, f(x) − L_a(x) = f''(ξ)(x − a)²/2 for some point ξ strictly between a and x. We usually do not know ξ, so we bound |f''| on the entire segment; taking absolute values and using |f''(ξ)| ≤ M gives the bound. Since (x − a)² > 0, this identity also explains the concavity test. See `taylors-remainder-bound.md`.

## Q031
**Status:** active
**Type:** true-false
**Difficulty:** intermediate
**Topic:** taylors-remainder-bound
**Focus Area:** halving the displacement
**Question:** True or false: halving |x − a| reduces the error bound by a factor of four, provided the same M is valid.
**Answer:** True. The factor |x − a|² explains why halving the input displacement reduces this error bound by a factor of four, provided the same M is valid. See `taylors-remainder-bound.md`.

## Q032
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** taylors-remainder-bound
**Focus Area:** certifying an approximation to a logarithm
**Question:** Use L_1(x) to approximate ln(1.04), give a rigorous error bound, and state the resulting certified interval.
**Answer:** For f(x) = ln x, f'(x) = 1/x, so f(1) = 0 and f'(1) = 1, giving L_1(x) = x − 1 and ln(1.04) ≈ 0.04. On [1, 1.04], f''(t) = −1/t² < 0, so 0.04 is an overestimate; and t ≥ 1 implies t² ≥ 1, hence |f''(t)| = 1/t² ≤ 1, so M = 1 is valid. Then |ln(1.04) − 0.04| ≤ (1/2)(0.04)² = 0.0008, and combining with the overestimate gives 0.0392 ≤ ln(1.04) ≤ 0.04. See `taylors-remainder-bound.md`.

## Q033
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** taylors-remainder-bound
**Focus Area:** choosing M correctly
**Question:** A student takes M = |f''(a)| without further comment. Under what condition is this legitimate, and must M be the smallest possible bound?
**Answer:** Use |f''(a)| for M only after showing that it bounds |f''| throughout the segment joining a and x — the bound must cover the whole interval. Any valid upper bound works; it need not be the smallest possible one. To choose M, write the interval with its smaller endpoint first, compute f'', and find a nonnegative number bounding |f''(t)| everywhere on that interval. See `taylors-remainder-bound.md`.

## Q034
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** applied-differential-problems
**Focus Area:** the modelling workflow
**Question:** List the steps of the modelling workflow for applied differential problems.
**Answer:** (1) define the input and output, with units; (2) write the function relating them; (3) identify the current input and the small input change; (4) compute dy = f'(x)dx; (5) interpret the sign and units, then decide whether an absolute or percentage change is asked. See `applied-differential-problems.md`.

## Q035
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** applied-differential-problems
**Focus Area:** a geometric change with a constraint
**Question:** A taut, straight cable has a fixed vertical rise of 3 m and horizontal span x m, so its length is ℓ(x) = √(x² + 9). When the span is 4 m it increases by 0.02 m while the rise stays fixed. Estimate the increase in cable length, in centimetres.
**Answer:** Here x = 4 and dx = 0.02 m. ℓ'(x) = (1/2)(x² + 9)^(−1/2)(2x) = x/√(x² + 9), so ℓ'(4) = 4/5. Hence Δℓ ≈ dℓ = (4/5)(0.02) = 0.016 m, which is 1.6 cm. The original length is ℓ(4) = 5 m, so the new length is approximately 5.016 m. See `applied-differential-problems.md`.

## Q036
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** applied-differential-problems
**Focus Area:** approximate change in volume of a sphere
**Question:** Determine the approximate increase in volume if the radius of a sphere is increased from 50 m to 51 m.
**Answer:** Here r = 50 m and Δr = 1 m, with V(r) = (4/3)πr³. Then ΔV ≈ dV = V'(r)Δr = 4πr²Δr = 4π(50)²·1 = 10000π m³. See `applied-differential-problems.md`.
