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
**Topic:** trig-substitution
**Focus Area:** the three standard substitutions and their ranges
**Question:** For a > 0, state the trigonometric substitution (with its θ-range) for each of √(a² − x²), √(a² + x²) and √(x² − a²), and what each radical becomes after substitution.
**Answer:** √(a² − x²): x = a sin θ, −π/2 < θ < π/2, radical becomes a cos θ. √(a² + x²): x = a tan θ, −π/2 < θ < π/2, radical becomes a sec θ. √(x² − a²): x = a sec θ with 0 < θ < π/2 when x > a and π/2 < θ < π when x < −a, radical becomes a|tan θ|. See `trig-substitution.md`.

## Q002
**Status:** active
**Type:** conceptual
**Difficulty:** introductory
**Topic:** trig-substitution
**Focus Area:** why it is called inverse substitution
**Question:** Why is trigonometric substitution called "inverse substitution"? Contrast it with ordinary u-substitution.
**Answer:** Because we replace x itself with an entire function of a new variable θ (e.g. x = 4 sin θ), whereas in ordinary substitution we replace a function of x by a variable u. See `trig-substitution.md`.

## Q003
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** sine-substitution
**Focus Area:** role of the θ-range in determining the sign of the radical
**Question:** With x = 4 sin θ, √(16 − x²) = √(16 cos²θ). Why may we write this as 4 cos θ rather than 4|cos θ|? What hypothesis justifies it?
**Answer:** √(16 cos²θ) = 4 cos θ only provided cos θ ≥ 0. Since −4 ≤ x ≤ 4, θ can be taken in [−π/2, π/2] (open range −π/2 < θ < π/2 in the lecture table), where cos θ ≥ 0. The chosen range is what determines the sign of the square root. See `sine-substitution.md`, `trig-substitution.md`.

## Q004
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** sine-substitution
**Focus Area:** sine substitution with back-substitution via a triangle
**Question:** Find ∫ (x + 1)/√(16 − x²) dx.
**Answer:** Let x = 4 sin θ, dx = 4 cos θ dθ, √(16 − x²) = 4 cos θ. The integral becomes ∫ (4 sin θ + 1) dθ = −4 cos θ + θ + C. With θ = sin⁻¹(x/4) and, from the triangle, cos θ = √(16 − x²)/4: −√(16 − x²) + sin⁻¹(x/4) + C. See `sine-substitution.md`.

## Q005
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** sine-substitution
**Focus Area:** sine substitution leading to csc θ − sin θ
**Question:** Find ∫ √(9 − x²)/x dx on 0 < x < 3.
**Answer:** x = 3 sin θ, 0 < θ < π/2, dx = 3 cos θ dθ, √(9 − x²) = 3 cos θ. The integral is 3∫ cos²θ/sin θ dθ = 3∫ (csc θ − sin θ) dθ = 3 ln|csc θ − cot θ| + 3 cos θ + C (since (csc θ − cot θ)′ = csc θ(csc θ − cot θ)). With cos θ = √(9 − x²)/3 and csc θ − cot θ = (3 − √(9 − x²))/x: √(9 − x²) + 3 ln((3 − √(9 − x²))/x) + C. The log's argument is positive on (0, 3). See `sine-substitution.md`.

## Q006
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** sine-substitution
**Focus Area:** basic arcsine integral
**Question:** Use a trigonometric substitution to find ∫ dx/√(25 − x²) on −5 < x < 5.
**Answer:** Let x = 5 sin θ, −π/2 < θ < π/2, so dx = 5 cos θ dθ and √(25 − x²) = 5 cos θ. The integral is ∫ dθ = θ + C = arcsin(x/5) + C. (Same pattern as ∫ du/√(9 − u²) = arcsin(u/3) + C in `sine-substitution.md`.)

## Q007
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** tangent-substitution
**Focus Area:** tangent substitution with power-reduction and back-substitution
**Question:** Find ∫ dx/(1 + x²)².
**Answer:** x = tan θ, 1 + x² = sec²θ, dx = sec²θ dθ. Integral = ∫ cos²θ dθ = (1/2)∫ (1 + cos 2θ) dθ = θ/2 + (1/4) sin 2θ + C. With θ = tan⁻¹x and sin 2θ = 2x/(1 + x²) (or (1/2) sin θ cos θ from the triangle): (1/2)[tan⁻¹x + x/(1 + x²)] + C. See `tangent-substitution.md`.

## Q008
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** tangent-substitution
**Focus Area:** definite integral by changing limits
**Question:** Evaluate ∫₀^√3 dx/(1 + x²)^{3/2}.
**Answer:** x = tan θ, −π/2 < θ < π/2. Since sec θ > 0, dx = sec²θ dθ and (1 + x²)^{3/2} = sec³θ. Limits: θ = 0 to π/3. Integral = ∫₀^{π/3} cos θ dθ = sin(π/3) = √3/2. See `tangent-substitution.md`.

## Q009
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** tangent-substitution
**Focus Area:** tangent substitution with half-angle identity, definite
**Question:** Evaluate ∫₀² x²/(x² + 4)² dx.
**Answer:** x = 2 tan θ, 0 ≤ θ ≤ π/4, dx = 2 sec²θ dθ, x² + 4 = 4 sec²θ. The integral becomes (1/2)∫₀^{π/4} sin²θ dθ. Using sin²θ = (1 − cos 2θ)/2: [θ/4 − sin 2θ/8]₀^{π/4} = π/16 − 1/8. Positive, as expected. See `tangent-substitution.md`.

## Q010
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** tangent-substitution
**Focus Area:** changing limits in a tangent substitution
**Question:** Evaluate ∫₀¹ dx/(1 + x²)^{3/2}.
**Answer:** x = tan θ gives ∫ cos θ dθ (as in `tangent-substitution.md`). The limits x = 0, 1 become θ = 0, π/4, so the value is [sin θ]₀^{π/4} = √2/2.

## Q011
**Status:** active
**Type:** mcq
**Difficulty:** introductory
**Topic:** secant-substitution
**Focus Area:** form of the radical after a secant substitution
**Question:** With x = 3 sec θ, the radical √(x² − 9) equals: (A) 3 tan θ for all x; (B) 3|tan θ|; (C) 3 sec θ; (D) 3 cos θ.
**Answer:** (B). √(9 sec²θ − 9) = √(9 tan²θ) = 3|tan θ|; it equals 3 tan θ only when x > 3 (0 < θ < π/2) and −3 tan θ when x < −3 (π/2 < θ < π). See `secant-substitution.md`.

## Q012
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** secant-substitution
**Focus Area:** sign handling on x < −a
**Question:** Find ∫ dx/(x²√(x² − 9)) on x < −3, explaining each step where the sign of tan θ matters.
**Answer:** x = 3 sec θ with π/2 < θ < π, dx = 3 sec θ tan θ dθ, √(x² − 9) = 3|tan θ| = −3 tan θ since tan θ < 0. The integrand becomes −(1/9) cos θ dθ, giving −(1/9) sin θ + C₋. With cos θ = 3/x and tan θ = −√(x² − 9)/3, sin θ = tan θ cos θ = −√(x² − 9)/x, so the result is √(x² − 9)/(9x) + C₋. Same shape as on x > 3, but the constant C₋ is independent of C₊. See `secant-substitution.md`.

## Q013
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** secant-substitution
**Focus Area:** two-case antiderivative
**Question:** Find ∫ dx/√(x² − 4) on each of x ≥ 2 and x ≤ −2 (in the form given by the written notes).
**Answer:** x = 2 sec θ, dx = 2 sec θ tan θ dθ, √(x² − 4) = 2|tan θ|. The integral is ∫ sec θ dθ for x ≥ 2 and −∫ sec θ dθ for x ≤ −2. With sec θ = x/2 and tan θ = ±√(x² − 4)/2: x ≥ 2: ln|x/2 + √(x² − 4)/2| + C; x ≤ −2: −ln|x/2 − √(x² − 4)/2| + C. See `secant-substitution.md`.

## Q014
**Status:** active
**Type:** true-false
**Difficulty:** intermediate
**Topic:** secant-substitution
**Focus Area:** independent constants on separate intervals
**Question:** True or false: in ∫ dx/(x²√(x² − 9)) = √(x² − 9)/(9x) + C, the constant must be the same on x > 3 and on x < −3.
**Answer:** False. The formula has the same shape on both components, but the constants C₊ and C₋ are independent. See `secant-substitution.md`.

## Q015
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** completing-the-square
**Focus Area:** completing the square to reach an arctangent
**Question:** Find ∫ dx/(x² + 6x + 13).
**Answer:** Complete the square: x² + 6x + 13 = (x + 3)² + 4. With u = (x + 3)/2 (as in the (x + 2)² + 4 example in `tangent-substitution.md`), dx = 2 du and the integral is (1/2)∫ du/(1 + u²) = (1/2) arctan((x + 3)/2) + C.

## Q016
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** completing-the-square
**Focus Area:** splitting the numerator into derivative plus constant
**Question:** Find ∫ (3x + 7)/(x² + 4x + 8) dx.
**Answer:** 3x + 7 = (3/2)(2x + 4) + 1 and x² + 4x + 8 = (x + 2)² + 4. So (3/2)∫ (2x + 4)/(x² + 4x + 8) dx + ∫ dx/((x + 2)² + 4) = (3/2) ln(x² + 4x + 8) + (1/2) arctan((x + 2)/2) + C (no absolute value needed: the quadratic is positive on ℝ). See `completing-the-square.md`.

## Q017
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** completing-the-square
**Focus Area:** shifted radical split into u-substitution and sine substitution
**Question:** Find ∫ (2x + 5)/√(9 − (x − 1)²) dx on −2 < x < 4.
**Answer:** u = x − 1, 2x + 5 = 2u + 7. Then 2∫ u du/√(9 − u²) + 7∫ du/√(9 − u²). First: v = 9 − u² gives −2√(9 − u²). Second: u = 3 sin θ gives arcsin(u/3). Result: −2√(9 − (x − 1)²) + 7 arcsin((x − 1)/3) + C. See `completing-the-square.md`.

## Q018
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** completing-the-square
**Focus Area:** Type II term integrated by shift then log + arctan
**Question:** Find ∫ x/(x² + 2x + 4) dx.
**Answer:** x² + 2x + 4 = (x + 1)² + 3. Let u = x + 1, so x = u − 1: ∫ u/(u² + 3) du − ∫ 1/(u² + 3) du = (1/2) ln(u² + 3) − (1/√3) tan⁻¹(u/√3) + C = (1/2) ln((x + 1)² + 3) − (1/√3) tan⁻¹((x + 1)/√3) + C. See `completing-the-square.md`.

## Q019
**Status:** active
**Type:** mcq
**Difficulty:** introductory
**Topic:** partial-fractions-setup
**Focus Area:** when to divide first
**Question:** Before decomposing N(x)/D(x) into partial fractions, you must first perform polynomial division when: (A) D has a repeated factor; (B) deg N ≥ deg D; (C) D has an irreducible quadratic factor; (D) N has a constant term.
**Answer:** (B). Divide first if deg N ≥ deg D. See `partial-fractions-setup.md`.

## Q020
**Status:** active
**Type:** true-false
**Difficulty:** introductory
**Topic:** partial-fractions-setup
**Focus Area:** irreducibility test
**Question:** True or false: x² + 2x + 5 is irreducible over ℝ.
**Answer:** True. A quadratic is irreducible over ℝ if its discriminant is negative; here 2² − 4·1·5 = −16 < 0. See `partial-fractions-setup.md`.

## Q021
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** partial-fractions-setup
**Focus Area:** writing the form of a decomposition
**Question:** Write the form (with unknown coefficients, not solved) of the partial fraction decomposition of (x + 1)/(x²(x² + 9)).
**Answer:** A/x + B/x² + (Cx + D)/(x² + 9). The repeated linear factor x² needs a term for each power, and the irreducible quadratic x² + 9 needs a linear numerator. See `partial-fractions-setup.md`, `linear-factors.md`.

## Q022
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** linear-factors
**Focus Area:** mixed repeated linear factors and coefficient count
**Question:** Write the form of the decomposition of (3x⁴ − 2x)/((x − 1)(x − 2)²(x − 3)³) and state how many unknown coefficients it has. Why that many?
**Answer:** A/(x − 1) + B₁/(x − 2) + B₂/(x − 2)² + C₁/(x − 3) + C₂/(x − 3)² + C₃/(x − 3)³. Six coefficients: the denominator has degree 6, and each factor contributes a term for every power up to its multiplicity. See `linear-factors.md`.

## Q023
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** linear-factors
**Focus Area:** two distinct linear factors
**Question:** Find ∫ (5x + 1)/((x − 1)(x + 2)) dx.
**Answer:** 5x + 1 = P(x + 2) + Q(x − 1). x = 1: P = 2; x = −2: Q = 3. Integral: 2 ln|x − 1| + 3 ln|x + 2| + C (on each interval where the integrand is defined). See `linear-factors.md`.

## Q024
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** linear-factors
**Focus Area:** distinct linear factors, roots method
**Question:** Find ∫ (x + 5)/((x − 1)(x + 3)) dx.
**Answer:** x + 5 = P(x + 3) + Q(x − 1). x = 1: 6 = 4P, P = 3/2. x = −3: 2 = −4Q, Q = −1/2. Integral: (3/2) ln|x − 1| − (1/2) ln|x + 3| + C. Method as in `linear-factors.md`.

## Q025
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** linear-factors
**Focus Area:** factor fully, then three distinct linear factors
**Question:** Find ∫ (x² + 2x + 3)/(x(x² − 4)) dx.
**Answer:** x(x² − 4) = x(x − 2)(x + 2). x² + 2x + 3 = C₁(x − 2)(x + 2) + C₂x(x + 2) + C₃x(x − 2). x = 0: C₁ = −3/4; x = 2: C₂ = 11/8; x = −2: C₃ = 3/8. Integral: −(3/4) ln|x| + (11/8) ln|x − 2| + (3/8) ln|x + 2| + C. See `linear-factors.md`.

## Q026
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** linear-factors
**Focus Area:** repeated linear factor; roots plus one easy value
**Question:** Find ∫ (3x² − 1)/(x³ + 4x² + 4x) dx.
**Answer:** x³ + 4x² + 4x = x(x + 2)². 3x² − 1 = A(x + 2)² + Bx(x + 2) + Cx. x = 0: A = −1/4; x = −2: 11 = −2C, C = −11/2; x = 1: 2 = 9A + 3B + C gives B = 13/4. Integral: A ln|x| + B ln|x + 2| − C/(x + 2) = −(1/4) ln|x| + (13/4) ln|x + 2| + 11/(2(x + 2)) + C. See `linear-factors.md`.

## Q027
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** linear-factors
**Focus Area:** repeated linear factor with a distinct factor
**Question:** Find ∫ (x² − 6x + 25)/((x + 1)(x − 3)²) dx.
**Answer:** P/(x + 1) + Q/(x − 3) + R/(x − 3)². x² − 6x + 25 = P(x − 3)² + Q(x + 1)(x − 3) + R(x + 1). x = −1: P = 2; x = 3: R = 4; x = 0: 25 = 9P − 3Q + R, Q = −1. Integral: 2 ln|x + 1| − ln|x − 3| − 4/(x − 3) + C; constants may differ on the components of ℝ \ {−1, 3}. See `linear-factors.md`.

## Q028
**Status:** active
**Type:** true-false
**Difficulty:** introductory
**Topic:** linear-factors
**Focus Area:** keep every power of a repeated factor
**Question:** True or false: for a denominator containing (x − 3)², it is enough to include the single term R/(x − 3)² in the decomposition.
**Answer:** False. Keep every power: both Q/(x − 3) and R/(x − 3)² are needed. See `linear-factors.md`.

## Q029
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** partial-fractions-setup
**Focus Area:** divide before decomposing
**Question:** Find ∫ (2x² + 1)/(x² + 1) dx.
**Answer:** Equal degrees, so divide: (2x² + 1)/(x² + 1) = 2 − 1/(x² + 1). Integral: 2x − arctan x + C. See `partial-fractions-setup.md`.

## Q030
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** partial-fractions-setup
**Focus Area:** division then standard log form
**Question:** Find ∫ x³/(x² + 1) dx.
**Answer:** deg 3 ≥ deg 2, so divide: x³/(x² + 1) = x − x/(x² + 1). Using ∫ x/(x² + a²) dx = (1/2) ln(a² + x²) + C: x²/2 − (1/2) ln(x² + 1) + C. See `partial-fractions-setup.md`.

## Q031
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** irreducible-quadratic-factors
**Focus Area:** linear plus irreducible quadratic factor
**Question:** Find ∫ (2x² + 3x + 6)/((x + 2)(x² + 4)) dx.
**Answer:** P/(x + 2) + (Qx + R)/(x² + 4). 2x² + 3x + 6 = P(x² + 4) + (Qx + R)(x + 2). x = −2: P = 1; x² coefficients: Q = 1; constants: R = 1 (x coefficient checks: 3 = 2Q + R). Integral: ln|x + 2| + (1/2) ln(x² + 4) + (1/2) arctan(x/2) + C. See `irreducible-quadratic-factors.md`.

## Q032
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** irreducible-quadratic-factors
**Focus Area:** repeated quadratic followed by tangent substitution
**Question:** Find ∫ (x² + 2)/(x² + 1)² dx.
**Answer:** (x² + 2)/(x² + 1)² = 1/(x² + 1) + 1/(x² + 1)². The second, with x = tan θ, is ∫ cos²θ dθ = θ/2 + sin 2θ/4 = (1/2) arctan x + x/(2(1 + x²)). Total: (3/2) arctan x + x/(2(1 + x²)) + C. See `irreducible-quadratic-factors.md`.

## Q033
**Status:** active
**Type:** mcq
**Difficulty:** intermediate
**Topic:** irreducible-quadratic-factors
**Focus Area:** form for repeated irreducible quadratics
**Question:** Which is the correct form for the (x² + 1)³ part of the decomposition of (4x² + 3x − 2)/((x − 1)²(x − 4)²(x² + 1)³)? (A) C/(x² + 1)³; (B) C₁/(x² + 1) + C₂/(x² + 1)² + C₃/(x² + 1)³; (C) (C₁x + D₁)/(x² + 1) + (C₂x + D₂)/(x² + 1)² + (C₃x + D₃)/(x² + 1)³; (D) (Cx + D)/(x² + 1)³.
**Answer:** (C). A repeated irreducible quadratic needs a term for each power, each with a linear numerator. See `irreducible-quadratic-factors.md`.

## Q034
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** irreducible-quadratic-factors
**Focus Area:** integrating a Type II term
**Question:** Describe the general strategy for integrating a term (Qx + R)/q(x), where q is an irreducible quadratic.
**Answer:** Write the numerator as λq′(x) + μ. The λq′(x)/q(x) part integrates to a logarithm; for the μ/q(x) part, complete the square so it reduces to an arctangent integral (substitution, inverse tangent substitution, or both). See `irreducible-quadratic-factors.md`, `completing-the-square.md`.

## Q035
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** choosing-an-approach
**Focus Area:** substitution turning an exponential into a rational integral
**Question:** Find ∫ dx/(eˣ + 2).
**Answer:** u = eˣ > 0, dx = du/u: ∫ du/(u(u + 2)) = (1/2)∫ (1/u − 1/(u + 2)) du = (1/2) ln u − (1/2) ln(u + 2) + C = x/2 − (1/2) ln(eˣ + 2) + C. See `choosing-an-approach.md`.

## Q036
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** choosing-an-approach
**Focus Area:** substitution then partial fractions
**Question:** Find ∫ dx/(eˣ + 1).
**Answer:** u = eˣ > 0, dx = du/u: ∫ du/(u(u + 1)) = ∫ (1/u − 1/(u + 1)) du = ln u − ln(u + 1) + C = x − ln(eˣ + 1) + C. Same method as ∫ dx/(eˣ + 2) in `choosing-an-approach.md`.

## Q037
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** choosing-an-approach
**Focus Area:** factoring a quartic over ℝ, then two Type II terms
**Question:** Find ∫ x²/(x⁴ + 4) dx.
**Answer:** x⁴ + 4 = (x² + 2)² − (2x)² = (x² − 2x + 2)(x² + 2x + 2), both irreducible. x²/(x⁴ + 4) = (1/4)(x/(x² − 2x + 2) − x/(x² + 2x + 2)). Splitting x = (1/2)(2x ∓ 2) ± 1 and using (x ∓ 1)² + 1: result (1/8) ln((x² − 2x + 2)/(x² + 2x + 2)) + (1/4)(arctan(x − 1) + arctan(x + 1)) + C. See `choosing-an-approach.md`.

## Q038
**Status:** active
**Type:** conceptual
**Difficulty:** introductory
**Topic:** partial-fractions-setup
**Focus Area:** factoring fully over ℝ before decomposing
**Question:** Why can't you write the decomposition of 1/(x⁴ − 16) directly from x⁴ − 16? Factor it over ℝ and give the form of the decomposition.
**Answer:** x⁴ − 16 must be factored further over ℝ before choosing the decomposition: x⁴ − 16 = (x² − 4)(x² + 4) = (x − 2)(x + 2)(x² + 4), with x² + 4 irreducible (negative discriminant). Form: A/(x − 2) + B/(x + 2) + (Cx + D)/(x² + 4). See `partial-fractions-setup.md`.

## Q039
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** sine-substitution
**Focus Area:** sine substitution with sin² power reduction
**Question:** Find ∫ x²/√(9 − x²) dx on −3 < x < 3.
**Answer:** x = 3 sin θ, dx = 3 cos θ dθ, √(9 − x²) = 3 cos θ, so the integral is 9∫ sin²θ dθ = 9(θ/2 − sin 2θ/4) + C (using sin²θ = (1 − cos 2θ)/2). With sin 2θ = 2 sin θ cos θ = 2(x/3)(√(9 − x²)/3): (9/2) arcsin(x/3) − (x/2)√(9 − x²) + C. Based on `sine-substitution.md` and `tangent-substitution.md` (power-reduction identity).

## Q040
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** choosing-an-approach
**Focus Area:** when a u-substitution suffices for a radical
**Question:** For ∫ x/√(9 − x²) dx, is a trigonometric substitution needed? Justify and evaluate.
**Answer:** No. A simpler u-substitution suffices when the derivative of the expression under the radical appears: v = 9 − x², dv = −2x dx gives −(1/2)∫ v^(−1/2) dv = −√(9 − x²) + C. (Compare the 2∫ u du/√(9 − u²) part in `completing-the-square.md`; strategy in `choosing-an-approach.md`.)
