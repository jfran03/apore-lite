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
**Topic:** identifying-parallel-connections
**Focus Area:** Why redrawing matters
**Question:** Why is it unsafe to decide whether two elements are in parallel just by looking at how the circuit is drawn?
**Answer:** Because parallel connections may not appear like parallel elements at first glance. The test is which nodes an element is connected between, not the arrangement on the page; tracing and labelling the nodes is what exposes parallel elements. Based on identifying-parallel-connections.md.

## Q002
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** identifying-parallel-connections
**Focus Area:** The four-resistor redrawing example
**Question:** In the example circuit with R₁ and R₄ along the bottom and R₂ and R₃ crossing diagonally, what is the actual relationship among R₁, R₂, R₃ and R₄, and how do you establish it?
**Answer:** All four are in parallel. Tracing the nodes shows every one of R₁, R₂, R₃ and R₄ is connected between node 1 and node 2, so the circuit redraws as four resistors side by side between node 2 (top) and node 1 (bottom). Based on identifying-parallel-connections.md.

## Q003
**Status:** active
**Type:** true-false
**Difficulty:** introductory
**Topic:** identifying-parallel-connections
**Focus Area:** Redrawing preserves the circuit
**Question:** True or false: redrawing a circuit so that parallel branches line up visually changes the circuit being analyzed.
**Answer:** False. The redrawn circuit is the same circuit — only the drawing changed. Based on identifying-parallel-connections.md.

## Q004
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** power-analysis-strategy
**Focus Area:** The three-part strategy
**Question:** State the strategy for finding the power in each element of a circuit.
**Answer:** (1) You need all voltages and currents to calculate power. (2) Use KVL and KCL to find the unknown voltages and currents, assuming a polarity/direction if unknown. (3) Use p = vi or p = −vi for each element, based on the direction of i and the polarity of v. Based on power-analysis-strategy.md.

## Q005
**Status:** active
**Type:** mcq
**Difficulty:** intermediate
**Topic:** power-analysis-strategy
**Focus Area:** Sign of power
**Question:** In the worked example, the 12 A source has P = +2160 W. What does this tell you? (a) The source is supplying 2160 W (b) The source is absorbing 2160 W (c) The assumed polarity must be wrong (d) The circuit violates conservation of energy
**Answer:** (b) The source is absorbing 2160 W. P > 0 means the element is absorbing power, including when that element is a source. Based on power-analysis-strategy.md.

## Q006
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** power-analysis-strategy
**Focus Area:** KCL with a dependent source
**Question:** In the worked example, KCL at node B gives 4 − i_Δ = 0. Using that result, apply KCL at node A to find i_g.
**Answer:** i_Δ = 4 A from node B. At node A: 2i_Δ + i_Δ − i_g = 0, where 2i_Δ enters A from the CCCS and i_Δ enters A from the 80 V source branch, while i_g leaves A. So i_g = 3i_Δ = 12 A. Based on power-analysis-strategy.md.

## Q007
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** power-analysis-strategy
**Focus Area:** Conservation of power as a check
**Question:** After computing the power of every element, what single check confirms the analysis, and what does it express physically?
**Answer:** ΣP = 0 — the powers of all elements must sum to zero. It expresses conservation of power/energy. In the worked example the five element powers (2160, −960, 320, −720, −800 W) sum to zero. Based on power-analysis-strategy.md.

## Q008
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** power-analysis-strategy
**Focus Area:** What a CCCS is
**Question:** What is a CCCS, and what role does i_Δ play in the worked example?
**Answer:** A current-controlled current source — a dependent source whose value is set by a controlling current elsewhere in the circuit. In the example the CCCS has value 2i_Δ, and i_Δ is the controlling current, flowing in the middle branch. Based on power-analysis-strategy.md.

## Q009
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** resistors-in-series
**Focus Area:** The series rule
**Question:** What single resistor can replace R₁, R₂ and R₃ in series, and what is shared by series elements?
**Answer:** R_eq = R₁ + R₂ + R₃ — resistors in series add. Series elements share a common current i. Based on resistors-in-series.md.

## Q010
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** resistors-in-series
**Focus Area:** Derivation of the series rule
**Question:** Derive R_eq = R₁ + R₂ + R₃ for three series resistors driven by a source V.
**Answer:** By KVL: −V + V₁ + V₂ + V₃ = 0. By Ohm's Law, with the common current i: V₁ = iR₁, V₂ = iR₂, V₃ = iR₃. Substituting: −V + iR₁ + iR₂ + iR₃ = 0, so V = i(R₁ + R₂ + R₃). This has the form V = iR, so the three resistors can be replaced by R_eq = R₁ + R₂ + R₃. Based on resistors-in-series.md.

## Q011
**Status:** active
**Type:** true-false
**Difficulty:** introductory
**Topic:** resistors-in-series
**Focus Area:** Common current
**Question:** True or false: the defining shared quantity for series elements is a common voltage.
**Answer:** False. Series elements share a common current; a common voltage is what parallel elements share. Based on resistors-in-series.md and resistors-in-parallel.md.

## Q012
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** resistors-in-parallel
**Focus Area:** The parallel rule
**Question:** Write the equivalent resistance of R₁, R₂ and R₃ in parallel, and state what parallel elements share.
**Answer:** R_eq = (1/R₁ + 1/R₂ + 1/R₃)⁻¹. Parallel elements share a common voltage — with a source V_s across them, each resistor has V_s across it. Based on resistors-in-parallel.md.

## Q013
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** resistors-in-parallel
**Focus Area:** Derivation of the parallel rule
**Question:** Derive the parallel equivalent resistance starting from KCL at the top node.
**Answer:** KCL at node A: i − i₁ − i₂ − i₃ = 0. From Ohm's Law, with the common voltage V_s: i₁ = V_s/R₁, i₂ = V_s/R₂, i₃ = V_s/R₃. Substituting: i − V_s/R₁ − V_s/R₂ − V_s/R₃ = 0, so i = V_s(1/R₁ + 1/R₂ + 1/R₃). Rearranged, V_s = i(1/R₁ + 1/R₂ + 1/R₃)⁻¹, which has the form V_s = iR, so R_eq is the bracketed factor. Based on resistors-in-parallel.md.

## Q014
**Status:** active
**Type:** mcq
**Difficulty:** introductory
**Topic:** resistors-in-parallel
**Focus Area:** Product over sum
**Question:** The formula R_eq = R₁R₂/(R₁ + R₂) applies to: (a) any number of resistors in parallel (b) exactly 2 resistors in parallel (c) any number of resistors in series (d) exactly 2 resistors in series
**Answer:** (b) exactly 2 resistors in parallel. It is stated specifically "for 2 resistors in parallel"; the general case is the reciprocal form R_eq = (1/R₁ + 1/R₂ + 1/R₃)⁻¹. Based on resistors-in-parallel.md.

## Q015
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** resistors-in-parallel
**Focus Area:** Applying product over sum
**Question:** Compute the equivalent resistance of 60 Ω in parallel with 30 Ω.
**Answer:** (60 × 30)/(60 + 30) = 20 Ω. Based on resistors-in-parallel.md.

## Q016
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** equivalent-resistance
**Focus Area:** The step-by-step reduction
**Question:** In the "Find a single equivalent resistance" example — 25 Ω and 5 Ω from A through B to C, a 40 Ω from C to E, and 30 Ω and 10 Ω from C through D to E — give the reduction sequence and the final answer.
**Answer:** (1) 25 + 5 in series → 30 Ω. (2) 30 + 10 in series → 40 Ω. (3) 40 ∥ 40 → (40 × 40)/(40 + 40) = 20 Ω. (4) 30 + 20 in series → 50 Ω. The circuit ends as the source across a single 50 Ω resistor. Based on equivalent-resistance.md.

## Q017
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** equivalent-resistance
**Focus Area:** Resistance between two terminals
**Question:** For a network seen from terminals a and b, with R₁ across a–b and R₂, R₃, R₄ forming the outer path, why can't you treat R₁ and R₂ as being in series — and what is R_eq?
**Answer:** You can't say R₁ and R₂ are in series because there could be other circuit elements connected to the left side of a and b. R_eq = R₁ ∥ (R₂ + R₃ + R₄). Based on equivalent-resistance.md.

## Q018
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** equivalent-resistance
**Focus Area:** Method of reduction
**Question:** Describe the general procedure for reducing a resistor network to a single equivalent resistance.
**Answer:** Repeatedly apply the series and parallel rules, one combination at a time: each step identifies one series pair or one parallel pair, replaces it with its equivalent, and redraws the simpler circuit, repeating until a single resistor remains. Based on equivalent-resistance.md.

## Q019
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** series-parallel-circuit-analysis
**Focus Area:** Definition of circuit analysis
**Question:** What does "circuit analysis" mean, as defined in this chapter?
**Answer:** The procedure for determining all voltages and currents in every circuit element. Based on series-parallel-circuit-analysis.md.

## Q020
**Status:** active
**Type:** mcq
**Difficulty:** intermediate
**Topic:** series-parallel-circuit-analysis
**Focus Area:** Unwinding equivalents
**Question:** When you replace an R_eq with the original resistors it came from, what is preserved? (a) Same current if the originals were series; same voltage if parallel (b) Same voltage if series; same current if parallel (c) Same power in both cases (d) Same resistance in both cases
**Answer:** (a). When replacing R_eq with original series resistors, those resistors have the same current as R_eq; when replacing R_eq with original parallel resistors, they have the same voltage. Based on series-parallel-circuit-analysis.md.

## Q021
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** series-parallel-circuit-analysis
**Focus Area:** Two routes to V_R
**Question:** In the reduced circuit — an 80 V source across a single 80 Ω — give two distinct arguments that V_R = 80 V.
**Answer:** (i) KVL around the loop: −80 + V_R = 0, therefore V_R = 80 V. (ii) Because of the voltage source, node A is higher than node D by 80 V, i.e. V_AD = 80 V, therefore V_R = V_AD = 80 V. Based on series-parallel-circuit-analysis.md.

## Q022
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** series-parallel-circuit-analysis
**Focus Area:** Full expansion phase
**Question:** In the worked example (80 V source, 60 Ω from A to B, 40 Ω from B to D, 10 Ω and 30 Ω from B through C to D), the reduced circuit gives i = 1 A. Walk through the expansion to find V₆₀, V_BD, i₁, i₂, V₁₀ and V₃₀, with the check at each stage.
**Answer:** Series step: the 60 Ω and the 20 Ω combination carry the same 1 A, so V₆₀ = 60 Ω × 1 A = 60 V and V_BD = 20 Ω × 1 A = 20 V; KVL check −80 + V₆₀ + V_BD = 0 ✓. Parallel step: the two 40 Ω branches have the same V_BD = 20 V, so i₁ = 20/40 = 0.5 A and i₂ = 20/40 = 0.5 A; KCL check at node B, i − i₁ − i₂ = 0 ✓. Series step again: the right 40 Ω restores to 10 Ω and 30 Ω both carrying i₂ = 0.5 A, so V₁₀ = 0.5 × 10 = 5 V and V₃₀ = 0.5 × 30 = 15 V; KVL check around the right loop, −V_BD + V₁₀ + V₃₀ = 0 ✓ (20 = 5 + 15). Based on series-parallel-circuit-analysis.md.

## Q023
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** series-parallel-circuit-analysis
**Focus Area:** Power forms for a resistor
**Question:** Give the three equivalent expressions used for the power absorbed by a resistor in the worked example, and apply one to the 60 Ω carrying 1 A.
**Answer:** P = V·i, P = V²/R, and P = i²R. For the 60 Ω: P = i²(60 Ω) = 1² × 60 = 60 W. Based on series-parallel-circuit-analysis.md.

## Q024
**Status:** active
**Type:** true-false
**Difficulty:** introductory
**Topic:** series-parallel-circuit-analysis
**Focus Area:** What comes later
**Question:** True or false: Node Voltage and Mesh Current are presented in this chapter as the systematic analysis methods to be used later, while voltage division and current division are the simple tools introduced now.
**Answer:** True. Based on series-parallel-circuit-analysis.md.

## Q025
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** voltage-division
**Focus Area:** Statement and formula
**Question:** State the voltage division principle and write the formula for V₁ across R₁ in a series string R₁, R₂, R₃ driven by V.
**Answer:** In a series connection of resistors, the total voltage across the series branch divides among them proportional to their size. V₁ = R₁/(R₁ + R₂ + R₃) · V. Based on voltage-division.md.

## Q026
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** voltage-division
**Focus Area:** Derivation
**Question:** Derive the voltage division formula from Ohm's Law applied to the reduced and original circuits.
**Answer:** R_eq = R₁ + R₂ + R₃. On the reduced circuit, i = V/R_eq = V/(R₁ + R₂ + R₃). On the original circuit, V₁ = i·R₁ = [V/(R₁ + R₂ + R₃)]·R₁ = R₁/(R₁ + R₂ + R₃) · V. In words: R₁'s portion of total voltage V is the same as its portion of total resistance. Based on voltage-division.md.

## Q027
**Status:** active
**Type:** mcq
**Difficulty:** advanced
**Topic:** voltage-division
**Focus Area:** Opposite polarity
**Question:** V₂ across R₂ is labelled with the opposite polarity to V, in a two-resistor series string. Which expression is correct? (a) V₂ = R₂/(R₁ + R₂) · V (b) V₂ = −R₂/(R₁ + R₂) · V (c) V₂ = R₁/(R₁ + R₂) · V (d) V₂ = −R₁/(R₁ + R₂) · V
**Answer:** (b) V₂ = −R₂/(R₁ + R₂) · V. If a branch voltage has opposite polarity to V, add a (−) sign. Based on voltage-division.md.

## Q028
**Status:** active
**Type:** true-false
**Difficulty:** introductory
**Topic:** voltage-division
**Focus Area:** Sum of divided voltages
**Question:** True or false: in a series string, the divided voltages satisfy V = V₁ + V₂ + V₃.
**Answer:** True — total voltage V = V₁ + V₂ + V₃. Based on voltage-division.md.

## Q029
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** current-division
**Focus Area:** Statement and formula
**Question:** State the current division principle and write i₁ for a total current i entering R₁ ∥ R₂.
**Answer:** In a parallel connection of resistors, the total current available to the parallel resistors divides among them inversely proportional to their size. i₁ = R₂/(R₁ + R₂) · i — the numerator is the other branch. Based on current-division.md.

## Q030
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** current-division
**Focus Area:** Why the other resistor appears on top
**Question:** Why does R₂ — not R₁ — appear in the numerator of the expression for i₁?
**Answer:** It falls out of the derivation: with R_eq = R₁R₂/(R₁ + R₂), Ohm's Law gives V = i·R₁R₂/(R₁ + R₂), and then i₁ = V/R₁ = [i·R₁R₂/(R₁ + R₂)]/R₁ = R₂/(R₁ + R₂) · i. In words, R₁'s portion of total current i is the same as R₂'s portion of total resistance — current divides inversely proportional to size, so the larger branch carries less. Based on current-division.md.

## Q031
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** current-division
**Focus Area:** Three parallel resistors — grouping
**Question:** A 10 A source feeds 60 Ω, 30 Ω and 10 Ω in parallel, with i₃ through the 10 Ω. Why is i₃ = (60 + 30)/(60 + 30 + 10) × 10 A wrong, and what is the correct value?
**Answer:** Current division is not as easy to apply with more than 2 resistors in parallel; that expression is marked wrong in the source. You must group first: combine the 60 Ω and 30 Ω in parallel to (60 × 30)/(60 + 30) = 20 Ω, then apply current division across the 10 Ω and the 20 Ω group: i₃ = 20/(10 + 20) × 10 A = 6.6̄ A. Based on current-division.md.

## Q032
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** current-division
**Focus Area:** Finding the true total current with KCL
**Question:** i = 30 A enters node M, which feeds a 20 Ω branch (i₁), a 10 Ω branch (i₂), and a 10 A current source. Find i₁.
**Answer:** Current division needs the total current going through the parallel resistors, i_total = i₁ + i₂ — not the 30 A. KCL at node M: +30 − i₁ − i₂ − 10 = 0, so i_total = 20 A. Then i₁ = 10/(10 + 20) × i_total = 6.6̄ A. Based on current-division.md.

## Q033
**Status:** active
**Type:** mcq
**Difficulty:** intermediate
**Topic:** current-division
**Focus Area:** Contrast with voltage division
**Question:** Current divides among parallel resistors ______ to their size; voltage divides among series resistors ______ to their size. (a) proportional / inversely proportional (b) inversely proportional / proportional (c) proportional / proportional (d) inversely proportional / inversely proportional
**Answer:** (b) inversely proportional / proportional. Based on current-division.md and voltage-division.md.
