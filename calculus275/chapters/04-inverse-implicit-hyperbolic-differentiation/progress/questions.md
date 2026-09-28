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
**Topic:** inverse-function-derivative
**Focus Area:** inverse derivative formula
**Question:** State the formula for (f⁻¹)'(b) when f(a) = b, and the conditions under which it applies.
**Answer:** (f⁻¹)'(b) = 1/f'(a), where f(a) = b (equivalently (f⁻¹)'(x) = 1/f'(f⁻¹(x))). It applies when f is differentiable and one-to-one on an interval and f'(a) ≠ 0 at the corresponding point a = f⁻¹(b). See `inverse-function-derivative.md`.

## Q002
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** inverse-function-derivative
**Focus Area:** computing (f⁻¹)' without the inverse
**Question:** Let f(x) = x⁵ + 2x + 1. Find (f⁻¹)'(4) without finding a formula for f⁻¹.
**Answer:** f'(x) = 5x⁴ + 2 > 0, so f is strictly increasing (one-to-one). Since f(1) = 4, f⁻¹(4) = 1, and f'(1) = 7. Hence (f⁻¹)'(4) = 1/7. See `inverse-function-derivative.md`.

## Q003
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** inverse-function-derivative
**Focus Area:** invertibility and (f⁻¹)'
**Question:** Show that f(x) = x⁵ + 3x is invertible and find (f⁻¹)'(4).
**Answer:** f'(x) = 5x⁴ + 3 ≥ 3 > 0, so f is always strictly increasing, passes the horizontal line test, and is invertible. f⁻¹(4) is the solution of x⁵ + 3x = 4, which can have only one solution; x = 1 works. So (f⁻¹)'(4) = 1/f'(1) = 1/8. See `inverse-function-derivative.md`.

## Q004
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** inverse-function-derivative
**Focus Area:** failure when f'(a) = 0
**Question:** f(x) = x³ is one-to-one, yet the reciprocal formula for (f⁻¹)' cannot be used at the origin. Explain why, and describe what happens to f⁻¹ there.
**Answer:** At a = 0, f'(0) = 0, so the reciprocal formula 1/f'(a) does not apply (the denominator is zero). The inverse f⁻¹(x) = ∛x still exists but has a vertical tangent at the origin. See `inverse-function-derivative.md`.

## Q005
**Status:** active
**Type:** true-false
**Difficulty:** introductory
**Topic:** inverse-function-derivative
**Focus Area:** inverse vs. reciprocal
**Question:** True or false: f⁻¹(x) means the same thing as 1/f(x).
**Answer:** False. f⁻¹ is the inverse function, not 1/f. For example sin⁻¹ x = arcsin x, while 1/sin x = csc x. See `inverse-function-derivative.md`.

## Q006
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** inverse-function-derivative
**Focus Area:** corresponding inputs
**Question:** If f(2) = −1 and f'(2) = 5, what is (f⁻¹)'(−1)?
**Answer:** Since f(2) = −1, f⁻¹(−1) = 2, so (f⁻¹)'(−1) = 1/f'(2) = 1/5. See `inverse-function-derivative.md`.

## Q007
**Status:** active
**Type:** mcq
**Difficulty:** introductory
**Topic:** inverse-function-derivative
**Focus Area:** geometric meaning
**Question:** A tangent line to the graph of f at (a, f(a)) has slope m ≠ 0. What is the slope of the tangent line to the graph of f⁻¹ at (f(a), a)? (A) m  (B) −m  (C) 1/m  (D) −1/m
**Answer:** (C) 1/m. The graph of f⁻¹ is the reflection of the graph of f over y = x, and a tangent of slope m ≠ 0 reflects to one of reciprocal slope 1/m. See `inverse-function-derivative.md`.

## Q008
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** inverse-function-derivative
**Focus Area:** Inverse Function Theorem hypotheses
**Question:** State the Inverse Function Theorem as given in the course, including what is concluded about the domain on which f⁻¹ is differentiable.
**Answer:** Suppose f is differentiable on an open interval I with f'(x) ≠ 0 on I. Then f⁻¹ is also differentiable on f(I) and (f⁻¹)'(f(x)) = 1/f'(x) for all x in I; equivalently (f⁻¹)'(x) = 1/f'(f⁻¹(x)) for any x in ran(f). See `inverse-function-derivative.md`.

## Q009
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** inverse-function-derivative
**Focus Area:** deriving the inverse formula
**Question:** Use implicit differentiation (or the chain rule) to derive the formula for (f⁻¹)'(x).
**Answer:** Write y = f⁻¹(x) as f(y) = x. Differentiating both sides with respect to x gives f'(y)·dy/dx = 1, so dy/dx = 1/f'(y), i.e. (f⁻¹)'(x) = 1/f'(f⁻¹(x)). Equivalently, differentiate f(f⁻¹(x)) = x by the chain rule: f'(f⁻¹(x))(f⁻¹)'(x) = 1. See `inverse-function-derivative.md`.

## Q010
**Status:** active
**Type:** conceptual
**Difficulty:** introductory
**Topic:** inverse-function-derivative
**Focus Area:** domain and range of an inverse
**Question:** How are dom(f⁻¹) and ran(f⁻¹) related to f, and what condition on f guarantees f⁻¹ exists?
**Answer:** dom(f⁻¹) = ran(f) and ran(f⁻¹) = dom(f). f is invertible if and only if f is one-to-one (passes the horizontal line test). See `inverse-function-derivative.md`.

## Q011
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** implicit-differentiation
**Focus Area:** chain rule on y-terms
**Question:** Compute d/dx (y³) and d/dx sin(xy), treating y as a function of x.
**Answer:** d/dx (y³) = 3y² y'. d/dx sin(xy) = cos(xy)(y + x y') (chain rule on the outer sine, product rule on xy). See `implicit-differentiation.md`.

## Q012
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** implicit-differentiation
**Focus Area:** partial-derivative form
**Question:** If F(x, y) = 0 defines y implicitly as a function of x, what is y' in terms of partial derivatives of F, and when is this valid?
**Answer:** y' = −F_x/F_y, valid wherever F_y ≠ 0 (from d/dx F(x, y(x)) = F_x + F_y y' = 0). See `implicit-differentiation.md`.

## Q013
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** implicit-differentiation
**Focus Area:** five-step workflow
**Question:** List the workflow for implicit differentiation.
**Answer:** (1) Differentiate both sides with respect to x. (2) Use product and chain rules before doing algebra. (3) Collect all terms containing y'. (4) Factor out y' and solve. (5) Only then substitute the coordinates of a specified point. See `implicit-differentiation.md`.

## Q014
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** implicit-differentiation
**Focus Area:** tangent line with an exponential term
**Question:** The curve x²eʸ + y³ = 1 passes through (1, 0). Find y' and the equation of the tangent line at (1, 0).
**Answer:** Differentiating: 2x eʸ + x² eʸ y' + 3y² y' = 0, so (x² eʸ + 3y²) y' = −2x eʸ and y' = −2x eʸ/(x² eʸ + 3y²). At (1, 0), y' = −2, so the tangent line is y = −2(x − 1). See `implicit-differentiation.md`.

## Q015
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** implicit-differentiation
**Focus Area:** mixed product relation
**Question:** For the curve x²y + cos y = 2x, find y', then the slope at (0, π/2) after first checking that the point lies on the curve.
**Answer:** Check: 0² · π/2 + cos(π/2) = 0 = 2(0), so the point is on the curve. Differentiating: 2xy + x² y' − sin y · y' = 2, so (x² − sin y) y' = 2 − 2xy and y' = (2 − 2xy)/(x² − sin y). At (0, π/2), y' = 2/(−1) = −2. See `implicit-differentiation.md`.

## Q016
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** implicit-differentiation
**Focus Area:** folium of Descartes
**Question:** For the folium of Descartes y³ + x³ = 2xy, find dy/dx and the tangent line at (1, 1).
**Answer:** Differentiating (product rule on 2xy): 3y² dy/dx + 3x² = 2y + 2x dy/dx. So dy/dx = (2y − 3x²)/(3y² − 2x), provided 3y² ≠ 2x. At (1, 1): slope = (2 − 3)/(3 − 2) = −1, so the tangent line is y − 1 = −(x − 1). See `implicit-differentiation.md`.

## Q017
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** implicit-differentiation
**Focus Area:** product and chain rule together
**Question:** If x² + 3xy − y² = 5, write an equation involving y' and solve for y'.
**Answer:** Differentiating: 2x + 3(y + x y') − 2y y' = 0. Collecting: (3x − 2y) y' = −(2x + 3y), so when 3x − 2y ≠ 0, y' = −(2x + 3y)/(3x − 2y). See `implicit-differentiation.md`.

## Q018
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** implicit-differentiation
**Focus Area:** substituting the point too early
**Question:** A student wants the slope of a curve at (a, b), so they substitute x = a and y = b into the original equation before differentiating. Explain what goes wrong.
**Answer:** Substituting before differentiating destroys the dependence of x and y and turns the relation into a numerical identity, so there is nothing left to differentiate. Differentiate first, solve for y', and only then substitute the point. See `implicit-differentiation.md`.

## Q019
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** implicit-differentiation
**Focus Area:** horizontal and vertical tangent checkpoints
**Question:** Implicit differentiation gives y' = −A(x, y)/B(x, y). What conditions give candidates for horizontal and vertical tangents, what happens if A = B = 0, and what must every candidate also satisfy?
**Answer:** A = 0 with B ≠ 0 is the checkpoint for a horizontal tangent; B = 0 with A ≠ 0 is the checkpoint for a vertical tangent. If A = B = 0 the test is inconclusive and the point may be singular. Every candidate must also satisfy the original curve equation. See `implicit-differentiation.md`.

## Q020
**Status:** active
**Type:** conceptual
**Difficulty:** introductory
**Topic:** implicit-differentiation
**Focus Area:** curves that are not functions
**Question:** The folium of Descartes x³ + y³ = 2xy is not a function. Why can we still find tangent lines to it?
**Answer:** We may still construct tangent lines where the curve looks like a differentiable function when zoomed in; treating y as a function of x locally, F(x, f(x)) = 0 is completely in terms of x and can be differentiated with the chain rule. See `implicit-differentiation.md`.

## Q021
**Status:** active
**Type:** mcq
**Difficulty:** introductory
**Topic:** inverse-trig-derivatives
**Focus Area:** principal ranges
**Question:** Which is the principal range of arccos? (A) [−π/2, π/2]  (B) [0, π]  (C) (−π/2, π/2)  (D) (0, π)
**Answer:** (B) [0, π]. (arcsin has range [−π/2, π/2]; arctan has range (−π/2, π/2).) See `inverse-trig-derivatives.md`.

## Q022
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** inverse-trig-derivatives
**Focus Area:** basic derivatives
**Question:** State the derivatives of arcsin x, arccos x and arctan x, with the x-values for which each holds.
**Answer:** d/dx arcsin x = 1/√(1 − x²) for |x| < 1; d/dx arccos x = −1/√(1 − x²) for |x| < 1; d/dx arctan x = 1/(1 + x²) for all x ∈ ℝ. See `inverse-trig-derivatives.md`.

## Q023
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** inverse-trig-derivatives
**Focus Area:** exact values from principal ranges
**Question:** Without a calculator, evaluate arccos(−1/2) and arctan(−√3), naming the principal range that makes each answer unique.
**Answer:** arccos(−1/2): find θ ∈ [0, π] with cos θ = −1/2; reference angle π/3 and cosine is negative in Quadrant II, so the value is 2π/3. arctan(−√3): find θ ∈ (−π/2, π/2) with tan θ = −√3; reference angle π/3 and the angle is negative, so the value is −π/3. See `inverse-trig-derivatives.md`.

## Q024
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** inverse-trig-derivatives
**Focus Area:** absolute value in arcsec
**Question:** Why does the derivative of arcsec x contain |x| in 1/(|x|√(x² − 1)) rather than x?
**Answer:** It is a sign issue, not decoration: √(1 − 1/x²) = √(x² − 1)/√(x²) = √(x² − 1)/|x|, because √(x²) = |x|. See `inverse-trig-derivatives.md`.

## Q025
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** inverse-trig-derivatives
**Focus Area:** chain rule inside an inverse trig function
**Question:** Differentiate h(x) = arctan(√(1 + x²)) and state where h' is defined.
**Answer:** Let u = √(1 + x²), u' = x/√(1 + x²). Then h'(x) = u'/(1 + u²) = x/((x² + 2)√(1 + x²)). Since 1 + x² > 0 the square root is differentiable for every real x and arctan accepts every real input, so h' is defined on all of ℝ. See `inverse-trig-derivatives.md`.

## Q026
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** inverse-trig-derivatives
**Focus Area:** domain of a function vs. its derivative
**Question:** Differentiate y = arccos(2x − 1) and state where the function is defined and where its derivative is finite.
**Answer:** With u = 2x − 1, u' = 2, so y' = −2/√(1 − (2x − 1)²). The function is defined when −1 ≤ 2x − 1 ≤ 1, i.e. 0 ≤ x ≤ 1, but the derivative is finite only when −1 < 2x − 1 < 1, i.e. 0 < x < 1. See `inverse-trig-derivatives.md`.

## Q027
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** inverse-trig-derivatives
**Focus Area:** domain of a function vs. its derivative
**Question:** Give two examples from the inverse trig functions where a function is defined at a point but its derivative is not finite there, and explain the distinction.
**Answer:** arcsin and arccos are defined at x = ±1 but their derivatives (±1/√(1 − x²)) are finite only for |x| < 1; arcsec and arccsc are defined for |x| ≥ 1 but their derivatives are finite only for |x| > 1. The domain of a function can be larger than the domain of its derivative. See `inverse-trig-derivatives.md`.

## Q028
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** inverse-trig-derivatives
**Focus Area:** reciprocal inverse trig definitions
**Question:** How does the course define arcsec, arccsc and arccot in terms of arccos, arcsin and arctan, and what x-values are required? What is special about the arccot convention?
**Answer:** arcsec x = arccos(1/x) and arccsc x = arcsin(1/x), requiring |x| ≥ 1 (so 1/x ∈ [−1, 1]); arccot x = arctan(1/x), requiring x ≠ 0. The arccot relation is the course-specific branch convention (range (−π/2, 0) ∪ (0, π/2)), differing from the common continuous convention whose range is (0, π). See `inverse-trig-derivatives.md`.

## Q029
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** inverse-trig-derivatives
**Focus Area:** deriving (csc⁻¹ x)'
**Question:** Using csc⁻¹ x = sin⁻¹(1/x), derive the derivative of csc⁻¹ x and state where it holds.
**Answer:** By the chain rule, (csc⁻¹ x)' = [1/√(1 − 1/x²)]·(−1/x²) = −1/√(x⁴(1 − 1/x²)) = −1/√(x²(x² − 1)) = −1/(|x|√(x² − 1)), for x > 1 or x < −1. See `inverse-trig-derivatives.md`.

## Q030
**Status:** active
**Type:** true-false
**Difficulty:** introductory
**Topic:** inverse-trig-derivatives
**Focus Area:** arccot derivative
**Question:** True or false: d/dx arccot x = −1/(1 + x²) for x ≠ 0.
**Answer:** True. See `inverse-trig-derivatives.md`.

## Q031
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** inverse-trig-derivatives
**Focus Area:** why restrict domains
**Question:** Why must sin, cos and tan be restricted before they can be inverted, and what restrictions are used for arcsin and arctan?
**Answer:** The three basic trig functions are not one-to-one (they fail the horizontal line test), so they are not invertible. sin is restricted to [−π/2, π/2] to define arcsin, and tan is restricted to (−π/2, π/2) to define arctan (cos is restricted to [0, π]). See `inverse-trig-derivatives.md`.

## Q032
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** hyperbolic-functions
**Focus Area:** definitions
**Question:** Give the exponential definitions of sinh x and cosh x, and the definition of tanh x.
**Answer:** sinh x = (eˣ − e⁻ˣ)/2, cosh x = (eˣ + e⁻ˣ)/2, tanh x = sinh x/cosh x = (eˣ − e⁻ˣ)/(eˣ + e⁻ˣ). See `hyperbolic-functions.md`.

## Q033
**Status:** active
**Type:** mcq
**Difficulty:** introductory
**Topic:** hyperbolic-functions
**Focus Area:** fundamental identity
**Question:** Which identity holds for all real x? (A) cosh²x + sinh²x = 1  (B) cosh²x − sinh²x = 1  (C) sinh²x − cosh²x = 1  (D) 1 + tanh²x = sech²x
**Answer:** (B) cosh²x − sinh²x = 1. (Also 1 − tanh²x = sech²x.) See `hyperbolic-functions.md`.

## Q034
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** hyperbolic-functions
**Focus Area:** derivative list
**Question:** State the derivatives of sinh, cosh, tanh, sech, coth and csch.
**Answer:** (sinh x)' = cosh x; (cosh x)' = sinh x; (tanh x)' = sech²x; (sech x)' = −sech x tanh x; (coth x)' = −csch²x; (csch x)' = −csch x coth x (coth and csch require x ≠ 0). See `hyperbolic-functions.md`.

## Q035
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** hyperbolic-functions
**Focus Area:** symmetry and range
**Question:** State the parity (odd/even) and range of sinh, cosh, tanh and sech, and the minimum value of cosh.
**Answer:** sinh is odd (range ℝ, strictly increasing); cosh is even with range [1, ∞) and minimum value 1 at x = 0; tanh is odd, strictly increasing, with range (−1, 1); sech is even with range (0, 1]. See `hyperbolic-functions.md`.

## Q036
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** hyperbolic-functions
**Focus Area:** hyperbolic chain rule
**Question:** Differentiate s(x) = cosh(2x) − 3 sinh(x²).
**Answer:** Apply the chain rule to each term: d/dx cosh(2x) = 2 sinh(2x) (inner derivative 2), and d/dx[−3 sinh(x²)] = −3 cosh(x²)(2x). So s'(x) = 2 sinh(2x) − 6x cosh(x²). See `hyperbolic-functions.md`.

## Q037
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** hyperbolic-functions
**Focus Area:** hyperbolic chain rule
**Question:** Differentiate y = tanh(x³).
**Answer:** With u = x³, u' = 3x², and (tanh u)' = sech²u · u', so y' = 3x² sech²(x³). See `hyperbolic-functions.md`.

## Q038
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** hyperbolic-functions
**Focus Area:** product, chain and exact values
**Question:** Differentiate r(x) = sech x tanh²x, then evaluate r'(ln 2) given tanh(ln 2) = 3/5 and sech(ln 2) = 4/5.
**Answer:** By the product and chain rules, r'(x) = −sech x tanh³x + 2 sech³x tanh x. At ln 2: r'(ln 2) = −(4/5)(3/5)³ + 2(4/5)³(3/5) = 276/625. See `hyperbolic-functions.md`.

## Q039
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** hyperbolic-functions
**Focus Area:** verify the identity
**Question:** Verify from the exponential definitions that cosh²x − sinh²x = 1.
**Answer:** cosh²x − sinh²x = [(eˣ + e⁻ˣ)² − (eˣ − e⁻ˣ)²]/4 = 4eˣe⁻ˣ/4 = 1 (the squared terms cancel and the cross terms contribute 4eˣe⁻ˣ = 4). See `hyperbolic-functions.md`.

## Q040
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** hyperbolic-functions
**Focus Area:** why 'hyperbolic'
**Question:** Why are these functions called 'hyperbolic'?
**Answer:** The parametrization (X, Y) = (cosh t, sinh t) satisfies X² − Y² = 1, so sinh and cosh play for the unit hyperbola the role that sine and cosine play for the unit circle. See `hyperbolic-functions.md`.

## Q041
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** inverse-hyperbolic-functions
**Focus Area:** restricting cosh
**Question:** Why must cosh be restricted to [0, ∞) before inverting, and what does arcosh x mean as a result?
**Answer:** cosh is even, so it is not one-to-one on ℝ. Restricting to [0, ∞) makes cosh: [0, ∞) → [1, ∞) one-to-one, and y = arcosh x always means the nonnegative solution of cosh y = x. See `inverse-hyperbolic-functions.md`.

## Q042
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** inverse-hyperbolic-functions
**Focus Area:** derivatives with domains
**Question:** State the derivatives of arsinh x, arcosh x and artanh x, with the x-values for which each holds.
**Answer:** d/dx arsinh x = 1/√(1 + x²) for x ∈ ℝ; d/dx arcosh x = 1/√(x² − 1) for x > 1; d/dx artanh x = 1/(1 − x²) for |x| < 1. See `inverse-hyperbolic-functions.md`.

## Q043
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** inverse-hyperbolic-functions
**Focus Area:** chain rule with arsinh
**Question:** Differentiate y = arsinh(4x).
**Answer:** With u = 4x, u' = 4, and (arsinh u)' = u'/√(1 + u²), so y' = 4/√(1 + 16x²). See `inverse-hyperbolic-functions.md`.

## Q044
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** inverse-hyperbolic-functions
**Focus Area:** domain vs. derivative
**Question:** Differentiate q(x) = arcosh(2x − 1) and state the domain of q and where q' is finite.
**Answer:** Domain: 2x − 1 ≥ 1, so x ≥ 1. With (arcosh u)' = u'/√(u² − 1): q'(x) = 2/√((2x − 1)² − 1) = 1/√(x(x − 1)). q is defined at x = 1 (arcosh 1 = 0) but q' is finite only for x > 1. See `inverse-hyperbolic-functions.md`.

## Q045
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** inverse-hyperbolic-functions
**Focus Area:** deriving arsinh's logarithmic form
**Question:** Derive the logarithmic formula for arsinh x by solving x = sinh y for y.
**Answer:** x = (eʸ − e⁻ʸ)/2. Multiplying by 2eʸ: e²ʸ − 2x eʸ − 1 = 0, a quadratic in eʸ. The quadratic formula gives eʸ = x ± √(x² + 1). Since eʸ > 0, the positive branch is required, so y = ln(x + √(x² + 1)). See `inverse-hyperbolic-functions.md`.

## Q046
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** inverse-hyperbolic-functions
**Focus Area:** logarithmic forms
**Question:** Give the logarithmic forms of arsinh, arcosh and artanh with their domains.
**Answer:** arsinh x = ln(x + √(x² + 1)) for x ∈ ℝ; arcosh x = ln(x + √(x² − 1)) for x ≥ 1; artanh x = ½ ln((1 + x)/(1 − x)) for |x| < 1. See `inverse-hyperbolic-functions.md`.

## Q047
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** inverse-hyperbolic-functions
**Focus Area:** remaining inverse hyperbolic functions
**Question:** How does the course define arccsch, arcsech and arccoth, and with what domains?
**Answer:** arccsch x = arsinh(1/x) (x ≠ 0); arcsech x = arcosh(1/x) (0 < x ≤ 1); arccoth x = artanh(1/x) (|x| > 1). See `inverse-hyperbolic-functions.md`.

## Q048
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** inverse-hyperbolic-functions
**Focus Area:** derivatives of remaining inverses
**Question:** State the derivatives of arccsch x, arcsech x and arccoth x with their domains.
**Answer:** d/dx arccsch x = −1/(|x|√(1 + x²)) for x ≠ 0; d/dx arcsech x = −1/(x√(1 − x²)) for 0 < x < 1; d/dx arccoth x = 1/(1 − x²) for |x| > 1. See `inverse-hyperbolic-functions.md`.

## Q049
**Status:** active
**Type:** true-false
**Difficulty:** intermediate
**Topic:** inverse-hyperbolic-functions
**Focus Area:** endpoint behavior
**Question:** True or false: since arcosh 1 = 0 is defined, its derivative 1/√(x² − 1) is finite at x = 1.
**Answer:** False. arcosh is defined at x = 1 (arcosh 1 = 0) but its derivative is not finite at that endpoint; the derivative formula holds for x > 1. See `inverse-hyperbolic-functions.md`.

## Q050
**Status:** active
**Type:** mcq
**Difficulty:** introductory
**Topic:** choosing-a-differentiation-strategy
**Focus Area:** choosing the method
**Question:** You are given an equation that mixes x and y and asked for dy/dx. Which approach does the course indicate? (A) Apply the inverse-function rule  (B) Differentiate both sides and attach y' to every differentiated y-term  (C) Use the hyperbolic identities  (D) Solve for eʸ
**Answer:** (B). An equation mixing x and y calls for implicit differentiation: differentiate both sides and attach y' to every differentiated y-term. See `choosing-a-differentiation-strategy.md`.

## Q051
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** choosing-a-differentiation-strategy
**Focus Area:** notation traps
**Question:** Explain the three notation traps involving −1 exponents and 'inverse' notation.
**Answer:** (1) f⁻¹ is an inverse function, but x⁻¹ = 1/x is a reciprocal power. (2) sin⁻¹ x means arcsin x, while 1/sin x = csc x. (3) sinh⁻¹ x is commonly used for arsinh x, not for csch x; context and parentheses matter. See `choosing-a-differentiation-strategy.md`.

## Q052
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** choosing-a-differentiation-strategy
**Focus Area:** common thread
**Question:** What single idea underlies inverse-function differentiation, implicit differentiation, and the derivatives of inverse hyperbolic functions?
**Answer:** Inverse-function and implicit differentiation are both consequences of the chain rule, and inverse hyperbolic functions are differentiated by the same reciprocal-slope (inverse-function) principle used for inverse trig functions. See `choosing-a-differentiation-strategy.md`.

## Q053
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** choosing-a-differentiation-strategy
**Focus Area:** matching problem to method
**Question:** For each, state the method: (a) find (f⁻¹)'(b); (b) differentiate arcsin(g(x)); (c) differentiate an inverse hyperbolic formula explicitly.
**Answer:** (a) Find the corresponding point a with f(a) = b, then take the reciprocal of f'(a). (b) Use the derivative formula for the outer inverse function, then multiply by g'(x). (c) Use the inverse-function derivative rule; to obtain an explicit form, rewrite with exponentials and solve for eʸ. See `choosing-a-differentiation-strategy.md`.

## Q054
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** implicit-differentiation
**Focus Area:** differentiating with respect to x and tangent line, exponential term (targeted follow-up to Q014)
**Question:** The curve x eʸ + y² = 1 passes through (1, 0). After checking that the point lies on the curve, find y' (differentiating with respect to x) and the tangent line at (1, 0).
**Answer:** Check: 1·e⁰ + 0² = 1, so the point is on the curve. Differentiating with respect to x (product rule on x eʸ, chain rule on eʸ and y²): eʸ + x eʸ y' + 2y y' = 0, so (x eʸ + 2y) y' = −eʸ and y' = −eʸ/(x eʸ + 2y), valid where x eʸ + 2y ≠ 0. At (1, 0), y' = −1/1 = −1, so the tangent line is y = −(x − 1) = −x + 1. See `implicit-differentiation.md`.

## Q055
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** implicit-differentiation
**Focus Area:** checking a point lies on the curve (targeted follow-up to Q014)
**Question:** Does (1, 1) lie on the curve x eʸ + y² = 1? Explain why this check comes before computing a tangent slope, and how it differs from the "substituting too early" mistake.
**Answer:** Substituting into the original equation: 1·e¹ + 1² = e + 1 ≠ 1, so (1, 1) is not on the curve and no tangent line exists there, even though the formula for y' would return a number. This check on the original equation is done to confirm the point is on the curve; the mistake to avoid is substituting the point before differentiating, which turns the relation into a numerical identity with nothing left to differentiate. See `implicit-differentiation.md`.
