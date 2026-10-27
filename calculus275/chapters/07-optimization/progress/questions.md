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
**Topic:** closed-interval-method
**Focus Area:** fundamental fact about continuous functions
**Question:** State the fundamental fact about continuous functions that guarantees global extrema exist. Include its hypotheses.
**Answer:** If f is continuous on the closed interval [a, b], then f must achieve a global (absolute) max and min on that interval. Both hypotheses matter: continuity, and a closed interval [a, b]. See `closed-interval-method.md`.

## Q002
**Status:** active
**Type:** mcq
**Difficulty:** introductory
**Topic:** closed-interval-method
**Focus Area:** candidate list
**Question:** Under the closed interval method, f continuous on [a, b] achieves its global max and min at points within which list? (A) critical points only (B) critical points and endpoints only (C) critical points, singular points, and endpoints x = a, b (D) singular points and inflection points
**Answer:** (C). The list is (i) critical points, (ii) singular points, (iii) endpoints x = a, b. Critical and singular points coincide with local extrema. See `closed-interval-method.md`.

## Q003
**Status:** active
**Type:** true-false
**Difficulty:** intermediate
**Topic:** closed-interval-method
**Focus Area:** necessity of a closed interval
**Question:** True or false: if f is continuous on [a, b), then f must achieve a global maximum on [a, b).
**Answer:** False. The guarantee only holds on a closed interval [a, b]. The lecture's [a, b) example has a single local min (the global min) but no max, since lim_{x→b⁻} f(x) = ∞. See `closed-interval-method.md` and `global-interval-method.md`.

## Q004
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** closed-interval-method
**Focus Area:** procedure
**Question:** List the steps for using the closed interval method on f continuous on [a, b].
**Answer:** (1) Find the critical/singular points (f'(x) = 0 or f'(x) DNE) in [a, b]. (2) Evaluate f at these points and also at a and b. (3) The largest value from this list is the global max; the smallest is the global min. See `closed-interval-method.md`.

## Q005
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** closed-interval-method
**Focus Area:** finding critical and singular values
**Question:** For f(x) = ∛(x³ − 3x²) on [−5, 5], compute f'(x) and identify the critical values and singular values.
**Answer:** By the chain rule, f'(x) = (1/3)(x³ − 3x²)^(−2/3)(3x² − 6x), which simplifies to f'(x) = (x − 2) / [x^(1/3)(x − 3)^(2/3)]. Critical value: f'(x) = 0 ⇔ x = 2. Singular values: f'(x) DNE ⇔ x = 0, 3. All lie in [−5, 5]. See `closed-interval-method.md`.

## Q006
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** closed-interval-method
**Focus Area:** evaluating candidates
**Question:** For f(x) = ∛(x³ − 3x²) on [−5, 5], with candidates x = 0, 2, 3 and the endpoints, find the global max and min values and where they occur.
**Answer:** f(0) = 0, f(2) = ∛(−4), f(3) = 0, f(−5) = ∛(−200), f(5) = ∛50. Global min is ∛(−200) at x = −5; global max is ∛50 at x = 5. Both occur at endpoints. See `closed-interval-method.md`.

## Q007
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** closed-interval-method
**Focus Area:** where extrema can occur
**Question:** Explain why finding critical and singular points alone is not enough to locate global extrema on [a, b]. Give an example of a function shape from lecture where this fails.
**Answer:** Global extrema can also occur at the endpoints, which need not be critical or singular points. For example, an increasing function on [a, b] has both global extrema at the endpoints; and for ∛(x³ − 3x²) on [−5, 5], the global max and min are both at endpoints. So f must also be evaluated at a and b. See `closed-interval-method.md`.

## Q008
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** global-interval-method
**Focus Area:** when to use
**Question:** On what kinds of intervals is the global interval method used, and what condition must f satisfy?
**Answer:** Intervals like (a, b), (a, b], [a, b), (−∞, b), (−∞, b], (a, ∞), [a, ∞), i.e. intervals that are not closed and bounded. f must have only one critical/singular value on the interval. See `global-interval-method.md`.

## Q009
**Status:** active
**Type:** true-false
**Difficulty:** introductory
**Topic:** global-interval-method
**Focus Area:** local implies global
**Question:** True or false: if f has only one critical/singular value on (0, ∞) and f has a local min there, then that local min is the global min.
**Answer:** True. By the global interval method, if f has only one critical/singular value and has a local min (max) there, it must be the global min (max). See `global-interval-method.md`.

## Q010
**Status:** active
**Type:** true-false
**Difficulty:** intermediate
**Topic:** global-interval-method
**Focus Area:** existence of the other extremum
**Question:** True or false: whenever the global interval method applies and f has a global min, f also has a global max.
**Answer:** False. There may be no global max (and analogously, no global min); if one exists it could occur at an endpoint, if there is one. Example: f(x) = 4x² + 1/x on (0, ∞) has a global min at x = 1/2 but f(x) → ∞ as x → 0⁺ and as x → ∞, so there is no global max. See `global-interval-method.md`.

## Q011
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** global-interval-method
**Focus Area:** worked example 4x² + 1/x
**Question:** Find the global max/min (if they exist) of f(x) = 4x² + 1/x on (0, ∞). Justify your classification.
**Answer:** f'(x) = 8x − 1/x², which exists on (0, ∞). f'(x) = 0 ⇔ x³ = 1/8 ⇔ x = 1/2, the only critical point. Sign chart: f'(1/4) = 2 − 16 = −14 < 0 and f'(10) > 0, so by the first derivative test there is a local min at x = 1/2. By the global interval method, f(1/2) is the global min. There is no global max since lim_{x→0⁺} f(x) = ∞ and lim_{x→∞} f(x) = ∞. See `global-interval-method.md`.

## Q012
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** global-interval-method
**Focus Area:** missing extrema on non-closed intervals
**Question:** A continuous function on [a, b) has a single local min at a critical point and lim_{x→b⁻} f(x) = ∞. What can you conclude about its global max and min, and why?
**Answer:** The single local min is the global min (global interval method, only one critical value). There is no global max because f grows without bound as x → b⁻. This was the "correction from lecture." See `global-interval-method.md`.

## Q013
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** constrained-optimization
**Focus Area:** procedure
**Question:** List the steps of the constrained optimization procedure.
**Answer:** (1) Write down the function to maximize/minimize. (2) Write down the constraint as an equation. (3) Use the constraint to reduce the number of variables in the optimized quantity to one. (4) Use the closed or global interval method to optimize it. (5) If needed, use the constraint to find the other variable at the optimized points. See `constrained-optimization.md`.

## Q014
**Status:** active
**Type:** mcq
**Difficulty:** introductory
**Topic:** constrained-optimization
**Focus Area:** role of the constraint
**Question:** In constrained optimization, what is the constraint equation primarily used for? (A) To find the second derivative (B) To reduce the optimized quantity to a function of one variable (C) To determine the units (D) To replace the first derivative test
**Answer:** (B). The constraint gives a relation between the variables, used to reduce the number of variables in the optimized quantity down to one (and, if needed, later to recover the other variable). See `constrained-optimization.md`.

## Q015
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** constrained-optimization
**Focus Area:** setting up the objective
**Question:** An open-top rectangular hole with square base side x and depth y has volume 48 m³. Floor concrete uses 1 unit/m² and wall concrete 3 units/m² (walls are three times as thick). Write the amount of concrete M as a function of x alone, and state its domain.
**Answer:** M = M_base + M_walls = 1·x² + 3·4·xy = x² + 12xy. The constraint 48 = x²y gives y = 48/x², so M(x) = x² + 12x(48/x²) = x² + 576/x, with x > 0. See `constrained-optimization.md`.

## Q016
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** constrained-optimization
**Focus Area:** solving and justifying the global min
**Question:** Minimize M(x) = x² + 576/x for x > 0 (the concrete-lined hole). Find x and the corresponding depth y = 48/x², and justify that your answer is a global min.
**Answer:** M'(x) = 2x − 576/x² = 0 ⇔ x³ = 288 ⇔ x = ∛288 = 2∛36 ≈ 6.6 m. Sign of M': negative at x = 1, positive at x = 1000, so it is a local min; being the single critical point on (0, ∞), by the global interval method it is the global min. Then y = 48/288^(2/3) = 12/36^(2/3) ≈ 1.1 m. Dimensions ≈ 6.6 m base side, 1.1 m deep. See `constrained-optimization.md`.

## Q017
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** related-rates
**Focus Area:** process
**Question:** List the four steps of the process for solving related rates problems.
**Answer:** (1) Write down and label all quantities. (2) Determine the relationship between these quantities. (3) Differentiate that equation with respect to time. (4) Substitute in the known values (may require referencing the original equation) and compute the unknown rate. See `related-rates.md`.

## Q018
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** related-rates
**Focus Area:** expanding sphere
**Question:** The surface area of a sphere is expanding at 10π m²/s. How quickly is the volume changing when the surface area is 400π m²?
**Answer:** With V = (4/3)πr³ and A = 4πr², solve r = √(A/(4π)) to get V = (1/(6√π))A^(3/2). Differentiating w.r.t. t (chain rule): dV/dt = (A^(1/2)/(4√π)) · dA/dt. Substituting A = 400π, dA/dt = 10π: dV/dt = (20√π/(4√π)) · 10π = 50π m³/s. See `related-rates.md`.

## Q019
**Status:** active
**Type:** mcq
**Difficulty:** introductory
**Topic:** related-rates
**Focus Area:** sign of a rate
**Question:** A rope of length z is being reeled in at 5 m/s. Which is correct? (A) dz/dt = 5 m/s (B) dz/dt = −5 m/s (C) dz/dt = 0 (D) dx/dt = −5 m/s
**Answer:** (B). The rope's length is decreasing, so dz/dt = −5 m/s. See `related-rates.md`.

## Q020
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** related-rates
**Focus Area:** boat and pier
**Question:** A boat is pulled to a pier by a rope attached 5 m higher on the pier than on the boat. The rope is reeled in at 5 m/s. Find dx/dt (x = horizontal distance from the pier) when x = 13 m.
**Answer:** Let z = rope length. Then z² = 25 + x². Differentiating: 2z · dz/dt = 2x · dx/dt, so dx/dt = (z/x) · dz/dt. When x = 13, z = √(25 + 169) = √194. With dz/dt = −5 m/s: dx/dt = (√194/13)(−5) m/s. See `related-rates.md`.

## Q021
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** related-rates
**Focus Area:** substituting values / referencing the original equation
**Question:** In the boat-and-pier problem, the differentiated equation dx/dt = (z/x)(dz/dt) needs z, which is not given. Where does z come from, and what step of the process does this illustrate?
**Answer:** z comes from the original relationship z² = 25 + x²: at x = 13, z = √194. This illustrates step 4, substituting known values, which "can be the hard part and may require referencing the original equation." See `related-rates.md`.

## Q022
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** related-rates
**Focus Area:** relating the given and wanted quantities
**Question:** In the expanding sphere problem, you know dA/dt and want dV/dt. Why did the solution first rewrite V in terms of A, and what tool is then used to differentiate?
**Answer:** The known and wanted rates involve different quantities (A and V), so they must be related in a single equation; solving A = 4πr² for r and substituting gives V = (1/(6√π))A^(3/2). Since all quantities depend on t, implicit differentiation with the chain rule then gives dV/dt = (1/(6√π))(3/2)A^(1/2) · dA/dt. See `related-rates.md`.
