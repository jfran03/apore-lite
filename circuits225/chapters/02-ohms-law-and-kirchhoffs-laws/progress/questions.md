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
**Topic:** resistors-and-ohms-law
**Focus Area:** What Ohm's Law relates
**Question:** In Ohm's Law, precisely which voltage and which current are being related?
**Answer:** The voltage *across* the resistor and the current *through* the resistor. Based on resistors-and-ohms-law.md.

## Q002
**Status:** active
**Type:** mcq
**Difficulty:** introductory
**Topic:** resistors-and-ohms-law
**Focus Area:** Ohm's Law sign convention
**Question:** A resistor R is labelled so that the current i enters the + terminal of the voltage V (current in the direction of voltage drop). Which form of Ohm's Law must be used? (a) V = iR (b) V = −iR (c) V = i/R (d) V = R/i
**Answer:** (a) V = iR. When the current through the resistor is shown in the direction of voltage drop, use V = iR — in this case the resistor "looks like an energy-absorbing element." Based on resistors-and-ohms-law.md.

## Q003
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** resistors-and-ohms-law
**Focus Area:** Ohm's Law with current in direction of voltage rise
**Question:** If the current through a resistor is labelled in the direction of voltage rise (it enters the − terminal), what form of Ohm's Law must you use, and why does the sign change?
**Answer:** Use V = −iR. The minus sign appears because the current is labelled in the direction of voltage rise rather than voltage drop — the reference labelling, not the physics, changes the sign. Based on resistors-and-ohms-law.md.

## Q004
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** resistors-and-ohms-law
**Focus Area:** Conductance definition and unit
**Question:** Define conductance in terms of Ohm's Law, give its symbol, and state its unit (including its former name).
**Answer:** From Ohm's Law, i = (1/R)·V. The quantity 1/R is the conductance, G. Its unit is the Siemens (Ω⁻¹), once called the mho (℧). Based on resistors-and-ohms-law.md.

## Q005
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** resistors-and-ohms-law
**Focus Area:** Arbitrary reference direction yields the same physical current
**Question:** In the 100 V / 10 Ω circuit, choosing i_R one way gives i_R = 10 A and choosing it the opposite way gives i_R = −10 A. Explain why these two results describe the same physical situation.
**Answer:** In the second case the current sees the − terminal first, so Ohm's Law must be written V_R = −i_R·R, giving i_R = −V_R/R = −100 V / 10 Ω = −10 A. The negative sign means the actual current flows opposite to the assumed reference direction — which is the same actual current as the first case, 10 A in the original direction. Based on resistors-and-ohms-law.md.

## Q006
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** power-and-energy
**Focus Area:** Power as product and as rate
**Question:** State the two expressions the source gives for power in an electric circuit, and show how they connect.
**Answer:** Power is the product of voltage and current, P = Vi; and power is the rate of energy transfer, P = dw/dt [J/s]. They connect because P = (dw/dq)·(dq/dt), where dw/dq is the voltage V and dq/dt is the current i. Based on power-and-energy.md.

## Q007
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** power-and-energy
**Focus Area:** Passive reference direction
**Question:** What is the "passive reference direction," and which power formula must be used when an element is labelled that way?
**Answer:** The passive reference direction is when the current is labelled in the direction of voltage drop (current enters the + terminal). It implies the element is absorbing power, and in that case we must use P = Vi. Based on power-and-energy.md.

## Q008
**Status:** active
**Type:** true-false
**Difficulty:** intermediate
**Topic:** power-and-energy
**Focus Area:** Sign interpretation of computed power
**Question:** True or False: If you compute power using P = −Vi and get a positive result, the element is supplying power.
**Answer:** False. In both cases — whether using P = Vi or P = −Vi — if P > 0 the element is absorbing power, and if P < 0 the element is supplying power. Based on power-and-energy.md.

## Q009
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** power-and-energy
**Focus Area:** Worked sign-convention example (a)
**Question:** An element has V₁ = 12 V and i₁ = 10 A, with the current labelled in the direction of voltage rise. Compute the power and state whether the element absorbs or supplies.
**Answer:** P = −V₁i₁ = −(12 V)(10 A) = −120 W. Since P < 0, the element supplies 120 W. Based on power-and-energy.md.

## Q010
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** power-and-energy
**Focus Area:** Worked sign-convention example (b) — two routes to the same answer
**Question:** An element has V₁ = 60 V and i₁ = −10 A, with the current labelled in the direction of voltage rise. Compute the power two different ways and explain why both give the same result.
**Answer:** Route 1: P = −V₁i₁ = −(60 V)(−10 A) = 600 W, so the element absorbs 600 W. Route 2: change the direction of the current to match the actual direction, which makes the current +10 A in the direction of voltage drop, giving P = Vi = (60 V)(10 A) = 600 W. Both give 600 W absorbed because relabelling the reference direction flips both the sign of the current value and the formula used, leaving the physical result unchanged. Based on power-and-energy.md.

## Q011
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** power-and-energy
**Focus Area:** Energy from power
**Question:** Given p(t), how do you find the energy transferred between times t₁ and t₂, and what does that quantity correspond to graphically?
**Answer:** Since P = dw/dt, energy is W = ∫[t₁ to t₂] P(t) dt. Graphically it is the area under the p(t) curve over that interval. Based on power-and-energy.md.

## Q012
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** power-and-energy
**Focus Area:** Exponential-current energy example
**Question:** An element has v(t) = 10 V and i(t) = 2e^(−t) A with the current in the direction of voltage drop. Find p(t), then the total energy from t = 0 to ∞, and state whether the element absorbs or supplies energy.
**Answer:** p(t) = v(t)·i(t) = 10 × 2e^(−t) = 20e^(−t) W. Then w = ∫₀^∞ 20e^(−t) dt = −20e^(−t)|₀^∞ = 0 − (−20) = 20 J. Since w > 0, the element absorbs energy. Based on power-and-energy.md.

## Q013
**Status:** active
**Type:** mcq
**Difficulty:** intermediate
**Topic:** power-and-energy
**Focus Area:** kWh conversion
**Question:** According to the source, 1 kWh equals how many joules? (a) 3600 J (b) 1000 J (c) 3600 × 1000 J (d) 1/3600 J
**Answer:** (c) 3600 × 1000 J. Since 1 W = 1 J/s, 1 J = 1 W·s = (1/1000) kW · (1/3600) h, so 1 kWh = 3600 × 1000 J. Based on power-and-energy.md.

## Q014
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** power-and-energy
**Focus Area:** Electricity bill example
**Question:** Energy costs $0.12 per kWh and a 30-day bill is $60.00, with power constant over the period. Find the power in watts, then the current if the voltage is 120 V.
**Answer:** Total energy over 30 days: W = $60.00 / ($0.12/kWh) = 500 kWh. Power: P = W/t = 500 kWh / (30 × 24) h = 694.4 W. Current: from P = Vi, i = P/V = 694.4 W / 120 V = 5.8 A. Based on power-and-energy.md.

## Q015
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** power-in-resistors
**Focus Area:** Power formulas for a resistor
**Question:** Starting from P = Vi and Ohm's Law, derive the two resistor power formulas.
**Answer:** Substituting V = iR into P = Vi gives P = i²·R; substituting i = V/R gives P = V²/R. Based on power-in-resistors.md.

## Q016
**Status:** active
**Type:** true-false
**Difficulty:** introductory
**Topic:** power-in-resistors
**Focus Area:** Sign of resistor power
**Question:** True or False: Depending on how the current reference direction is drawn, a resistor can be found to supply power.
**Answer:** False. P is always positive for resistors — they will always absorb power. Based on power-in-resistors.md.

## Q017
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** power-in-resistors
**Focus Area:** 100 V / 10 Ω worked example — solution steps
**Question:** Walk through the four steps the source uses to find the power for both elements in the 100 V source / 10 Ω resistor circuit.
**Answer:** Step 1: Find the voltage across the resistor — it is connected to the same 2 points as the 100 V source, so V_R = 100 V (B is higher in potential than A by 100 V). Step 2: Choose an arbitrary direction for i_R. Step 3: From Ohm's Law, i_R = 100 V / 10 Ω = 10 A, so for the resistor P = V_R·i_R = (100 V)(10 A) = 1000 W absorbed (also computable as (i_R)²R or (V_R)²/R). Step 4: That current continues through the source, and since the current sees the (−) terminal first, P_source = −V·i_R = −(100 V)(10 A) = −1000 W, i.e. the source supplies 1000 W. Based on power-in-resistors.md.

## Q018
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** power-in-resistors
**Focus Area:** Opposite reference direction, same physical result
**Question:** In the 100 V / 10 Ω circuit, if i_R is chosen in the opposite direction so that i_R = −10 A, what power results do you get for the resistor and the source?
**Answer:** For the resistor, P = −V_R·i_R = −(100 V)(−10 A) = 1000 W (absorbed). For the source, P_source = (100 V)·i_R = (100 V)(−10 A) = −1000 W (supplied). Both match the results from the original choice of direction. Based on power-in-resistors.md.

## Q019
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** kirchhoffs-current-law
**Focus Area:** Statement of KCL and definition of a node
**Question:** State Kirchhoff's Current Law and define a "node."
**Answer:** KCL states that the algebraic sum of all currents at a node must be zero. A node is the joining of 2 or more circuit elements. Based on kirchhoffs-current-law.md.

## Q020
**Status:** active
**Type:** mcq
**Difficulty:** introductory
**Topic:** kirchhoffs-current-law
**Focus Area:** KCL sign convention
**Question:** Using the convention introduced with KCL in this chapter, how are currents signed at a node? (a) Entering adds, leaving subtracts (b) Entering subtracts, leaving adds (c) All currents add (d) The signs depend on the element type
**Answer:** (a) Current entering the node adds; current leaving the node subtracts. The source notes this convention must be applied consistently, and that later, in the Node Voltage Method, the opposite convention will be used. Based on kirchhoffs-current-law.md.

## Q021
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** kirchhoffs-current-law
**Focus Area:** Connection points forming a single node
**Question:** Two connection points in a circuit are joined directly to each other by a conductor. How should they be treated when applying KCL, and what principle justifies this?
**Answer:** They constitute one node — connection points connected directly to each other by conductors are a single node. This is why, in the worked example, M (drawn as two joined connection points) is treated as a single node when writing KCL. Based on kirchhoffs-current-law.md.

## Q022
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** kirchhoffs-current-law
**Focus Area:** Node M example — two solution routes
**Question:** At node M, currents of −5 A, 3 A, and 6 A enter and i₁ leaves. Find i₁ two ways: treating M as a single node, and by writing KCL at the individual connection points N and P inside M.
**Answer:** Single node: −5 + 3 + 6 − i₁ = 0, so i₁ = 4 A. Connection points: choosing an arbitrary direction for i₂, KCL at N gives −5 + 3 − i₂ = 0 so i₂ = −2 A; KCL at P gives −2 (that is, i₂) + 6 − i₁ = 0, so i₁ = 4 A. Both routes give i₁ = 4 A. Based on kirchhoffs-current-law.md.

## Q023
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** kirchhoffs-current-law
**Focus Area:** Circuits that violate KCL
**Question:** Why is a circuit with a 5 A source and a 10 A source joined in series at a node prohibited?
**Answer:** Because KCL is violated at that node: 5 − 10 ≠ 0, and the algebraic sum of all currents at a node must be zero. Based on kirchhoffs-current-law.md.

## Q024
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** series-connections
**Focus Area:** Definition of series
**Question:** State the precise condition for two elements to be in series.
**Answer:** Two elements are in series if they are connected at one node only and there is no other element connected to that node. Based on series-connections.md.

## Q025
**Status:** active
**Type:** true-false
**Difficulty:** intermediate
**Topic:** series-connections
**Focus Area:** Same-current rule and its caveat
**Question:** True or False: Elements in series always have the same current, with no qualification needed.
**Answer:** False. Elements in series have the same current *only if the currents are labelled with the same direction*. If they are labelled in opposite directions, the relationship becomes i_C = −i_D, as in the C-and-D example. Based on series-connections.md.

## Q026
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** series-connections
**Focus Area:** Deriving the series current rule from KCL
**Question:** For elements 1, 2, 3 in a chain with nodes A and B between them, show how KCL proves they carry the same current.
**Answer:** KCL at node A gives i₁ − i₂ = 0, so i₁ = i₂. KCL at node B gives i₂ − i₃ = 0, so i₂ = i₃. Therefore i₁ = i₂ = i₃. Based on series-connections.md.

## Q027
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** series-connections
**Focus Area:** How to identify series elements in a drawn circuit
**Question:** What practical procedure does the source give for spotting series elements in a circuit diagram?
**Answer:** Examine all nodes and identify the ones at which only 2 elements are joined. Based on series-connections.md.

## Q028
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** kirchhoffs-voltage-law
**Focus Area:** Statement of KVL, loop definition, origin
**Question:** State Kirchhoff's Voltage Law, define a "loop," and say what physical principle KVL is derived from.
**Answer:** KVL states that the algebraic sum of all voltages around a loop must be zero. A loop is a closed path starting at a node and finishing back at the same node. KVL is derived from conservation of energy. Based on kirchhoffs-voltage-law.md.

## Q029
**Status:** active
**Type:** true-false
**Difficulty:** intermediate
**Topic:** kirchhoffs-voltage-law
**Focus Area:** Loop direction
**Question:** True or False: The direction you travel around a loop when applying KVL must match the direction of current flow.
**Answer:** False. The loop direction is chosen arbitrarily and has no relation to current direction. Based on kirchhoffs-voltage-law.md.

## Q030
**Status:** active
**Type:** mcq
**Difficulty:** intermediate
**Topic:** kirchhoffs-voltage-law
**Focus Area:** KVL sign convention
**Question:** Travelling in the chosen loop direction, you reach an element labelled `− V +` (you meet the − terminal first). What do you do with V in the KVL sum? (a) Add V (b) Subtract V (c) Add V only if it is a source (d) Ignore it
**Answer:** (b) Subtract V. By convention, an element met as `+ V −` in the loop direction is added, and one met as `− V +` is subtracted. Based on kirchhoffs-voltage-law.md.

## Q031
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** kirchhoffs-voltage-law
**Focus Area:** Loops containing open circuits
**Question:** Can a KVL loop include an open circuit? What must you be careful to do if so, and what does the resulting equation look like in the source's example?
**Answer:** Yes — loops can contain open circuits. It is important to account for the potential difference across the open circuit. In the example, with V_OC the open-circuit voltage, KVL gives −V_A − V_B + V_OC = 0. Based on kirchhoffs-voltage-law.md.

## Q032
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** kirchhoffs-voltage-law
**Focus Area:** Circuits prohibited by KVL
**Question:** Give the source's example of a circuit prohibited by KVL and the equation that shows why.
**Answer:** A 12 V source whose terminals form a loop by themselves (shorted). KVL around that loop gives −12 ≠ 0, which violates the requirement that the algebraic sum of voltages around a loop be zero. Based on kirchhoffs-voltage-law.md.

## Q033
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** parallel-connections
**Focus Area:** Definition of parallel
**Question:** State the condition for two elements to be in parallel, in both of the ways the source phrases it.
**Answer:** Two elements are parallel if their terminals are directly connected to each other — in other words, if they are connected to the same 2 nodes. Based on parallel-connections.md.

## Q034
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** parallel-connections
**Focus Area:** Same-voltage rule derived from KVL
**Question:** Use KVL to show that two parallel elements A and B have the same voltage, and state the caveat on that rule.
**Answer:** Around the loop formed by the two parallel elements, KVL gives −V_A + V_B = 0, therefore V_A = V_B. The caveat: this holds only if the polarities are labelled consistently. Based on parallel-connections.md.

## Q035
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** parallel-connections
**Focus Area:** Inconsistently labelled polarities
**Question:** Two elements are in parallel but their voltage polarities are labelled in opposite senses. What is the relationship between V_A and V_B, and how does KVL confirm it?
**Answer:** V_A = −V_B. KVL around the loop gives −V_A − V_B = 0, therefore V_A = −V_B. Based on parallel-connections.md.

## Q036
**Status:** active
**Type:** true-false
**Difficulty:** intermediate
**Topic:** parallel-connections
**Focus Area:** Disguised parallel connections
**Question:** True or False: If two resistors are drawn on opposite sides of a circuit diagram in a crossed layout, they cannot be in parallel.
**Answer:** False. The source warns to watch for parallel connections that may not appear like parallel elements at first glance, and shows R₁, R₂, R₃, R₄ in a crossed layout redrawn as four elements all connected between node 1 and node 2. What matters is whether the terminals are directly connected to the same 2 nodes, not how the circuit is drawn. Based on parallel-connections.md.

## Q037
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** parallel-connections
**Focus Area:** Combined series/parallel worked example
**Question:** In the circuit with elements A, B, C, D and nodes 1, 2, 3: (a) identify what is in series and what is in parallel; (b) express i_C in terms of i_D; (c) given i_A = 3 A and i_C = 1 A, find i_B and i_D.
**Answer:** (a) Series: C and D — connected at one node only with nothing else connected there. Parallel: A and B — connected to the same 2 nodes (1 and 3), with no circuit element separating their terminals. (b) C and D are in series so they must carry the same current; paying attention to the labelled directions, i_C = −i_D (equivalently, KCL at node 2 gives −i_C − i_D = 0). (c) i_D = −i_C = −1 A; KCL at node 1 gives i_A − i_B + i_C = 0, i.e. 3 − i_B + 1 = 0, so i_B = 4 A. Based on parallel-connections.md.

## Q038
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** parallel-connections
**Focus Area:** Strategy for power problems with dependent sources
**Question:** For the circuit containing a current source i_g, an 80 V source carrying controlling current i_Δ, a 4 A source, and a CCCS of value 2i_Δ with V₀ = 100 V across it, what strategy does the source give for finding the power in each element?
**Answer:** All voltages and currents are needed in order to calculate power, so use KVL and KCL to find the unknown voltages and currents, assuming a polarity or direction wherever one is unknown. (The source states this strategy but does not carry out the solution.) Based on parallel-connections.md.
