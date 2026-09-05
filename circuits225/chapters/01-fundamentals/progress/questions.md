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
**Type:** mcq
**Difficulty:** introductory
**Topic:** electric-circuits-and-elements
**Focus Area:** Definition of electric circuit
**Question:** Which of the following best defines an "electric circuit"? (a) A single circuit element carrying current (b) An interconnection of circuit elements in a closed path by conductors (c) A device that stores energy in an electric field (d) A source of electrical charge
**Answer:** (b) An interconnection of circuit elements in a closed path by conductors. Based on electric-circuits-and-elements.md.

## Q002
**Status:** active
**Type:** true-false
**Difficulty:** introductory
**Topic:** electric-circuits-and-elements
**Focus Area:** Capacitor vs. inductor energy storage
**Question:** True or False: A capacitor stores energy in a magnetic field, while an inductor stores energy in an electric field.
**Answer:** False — it's the reverse: a capacitor stores energy in an electric field, and an inductor stores energy in a magnetic field. Based on electric-circuits-and-elements.md.

## Q003
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** electric-circuits-and-elements
**Focus Area:** Short circuit vs. open circuit
**Question:** Explain the difference between a "short circuit" and an "open circuit" in terms of current and voltage.
**Answer:** A short circuit is an ideal conductor connecting two points, where current i flows through it but V = 0 across it (the points are "shorted" together). An open circuit is the absence of a conductor (a gap) between elements, where i = 0 and the voltage V across the gap is unknown until the circuit is solved. Based on electric-circuits-and-elements.md.

## Q004
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** electric-circuits-and-elements
**Focus Area:** Reshaping ideal conductors / equivalent circuits
**Question:** Why can ideal conductors be "shortened or lengthened" and redrawn without changing a circuit's behavior?
**Answer:** Because ideal conductors are used only to establish electrical connections between circuit elements; as long as the same terminals remain connected together, the circuit is electrically equivalent no matter how the conductors are drawn. Based on electric-circuits-and-elements.md.

## Q005
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** current
**Focus Area:** Current definition
**Question:** Write the formula relating current i(t) to charge q(t), and state the units of i(t) and q(t).
**Answer:** i(t) = dq(t)/dt. i(t) is in Amperes (A), q(t) is in Coulombs (C). Based on current.md.

## Q006
**Status:** active
**Type:** mcq
**Difficulty:** introductory
**Topic:** current
**Focus Area:** Elementary charge
**Question:** According to the source, charge exists in discrete quantities that are integer multiples of which value? (a) 1.6×10⁻¹⁹ C (b) 3.0×10⁸ C (c) 6.6×10⁻³⁴ C (d) 9.1×10⁻³¹ C
**Answer:** (a) 1.6×10⁻¹⁹ Coulomb, the charge of an electron. Based on current.md.

## Q007
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** current
**Focus Area:** Reference direction for current
**Question:** If you assign a reference direction for current i_A in a branch and later calculate i_A = -5 A when solving the circuit, what does this tell you about the actual current?
**Answer:** The actual current in branch A is 5 A, flowing in the direction opposite to the assumed reference direction. Based on current.md.

## Q008
**Status:** active
**Type:** true-false
**Difficulty:** introductory
**Topic:** current
**Focus Area:** DC vs. AC
**Question:** True or False: A battery is an example of an alternating current (AC) source.
**Answer:** False — a battery is an example of a direct current (DC) source, which has a constant value over time. House outlets are given as an example of an AC source. Based on current.md.

## Q009
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** current
**Focus Area:** Branch current notation
**Question:** If i_mn is the current flowing from terminal m to terminal n through an element, how is i_nm related to i_mn?
**Answer:** i_mn = -i_nm — they represent the same current measured in opposite reference directions. Based on current.md.

## Q010
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** current
**Focus Area:** Finding charge from current
**Question:** Given i(t) and an initial charge q(t₀) at time t₀, how do you find q(t)?
**Answer:** q(t) = ∫[t₀ to t] i(t) dt + q(t₀). Based on current.md.

## Q011
**Status:** active
**Type:** mcq
**Difficulty:** introductory
**Topic:** voltage
**Focus Area:** Voltage definition
**Question:** Voltage is best described as: (a) the rate of flow of charge (b) energy transferred to/from a circuit element per unit of charge flowing through it (c) the resistance of a circuit element (d) the total charge stored in a circuit element
**Answer:** (b) energy transferred to/from a circuit element per unit of charge flowing through it — also called potential difference. Based on voltage.md.

## Q012
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** voltage
**Focus Area:** Reference polarity and sign
**Question:** If you assign a reference polarity for voltage V_A across an element and the actual polarity turns out to be reversed, what does this mean about the calculated value of V_A?
**Answer:** The calculated value of V_A will be negative. Based on voltage.md.

## Q013
**Status:** active
**Type:** true-false
**Difficulty:** intermediate
**Topic:** voltage
**Focus Area:** Notation V_mn and V_nm
**Question:** True or False: V_mn and V_nm (referring to the same element, with the subscript order denoting the + terminal) are equal in value.
**Answer:** False — V_mn = -V_nm; they are negatives of each other. Based on voltage.md.

## Q014
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** power
**Focus Area:** Absorbed vs. supplied power
**Question:** How do the actual direction of current and actual voltage polarity together tell you whether a circuit element is absorbing or supplying power?
**Answer:** If the actual current enters the + terminal of the actual voltage polarity (current flows in the direction of a voltage drop), the element absorbs power. If the actual current flows in the direction of a voltage rise (enters the − terminal), the element supplies power. Based on power.md.

## Q015
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** circuit-analysis-example
**Focus Area:** Yani's cheap plastic circuit example
**Question:** In the "Yani's cheap plastic circuit" example (12V battery and 12Ω headlight load), after solving the circuit with i = 1 A, which element supplies power and which absorbs power, and why?
**Answer:** The battery supplies power because the actual current flows in the direction of a voltage rise through it. The resistor (load) absorbs power because the actual current flows in the direction of a voltage drop across it. Based on circuit-analysis-example.md and power.md.

## Q016
**Status:** active
**Type:** conceptual
**Difficulty:** introductory
**Topic:** circuit-analysis-example
**Focus Area:** Why voltage/current values matter
**Question:** Give two reasons, according to the source, why we care about determining the voltage and current values in a circuit like the battery-and-headlights example.
**Answer:** (1) Lights require a certain voltage to operate properly, so solving the circuit tells us if that voltage is provided. (2) Circuit elements have current ratings (maximum current before overheating, melting, or catching fire), so solving the circuit confirms current doesn't exceed that value. (The source also notes that once voltage and current are known, power and energy consumed/supplied can be calculated.) Based on circuit-analysis-example.md.

## Q017
**Status:** active
**Type:** mcq
**Difficulty:** intermediate
**Topic:** sources
**Focus Area:** Independent voltage source properties
**Question:** For an independent voltage source, which statement is true? (a) Its current is fixed and its voltage depends on the circuit (b) Its voltage is specified exactly and its current depends on the circuit it's connected to (c) Both its voltage and current are fixed regardless of the circuit (d) Neither its voltage nor current can be determined
**Answer:** (b) Its voltage (potential difference) is specified exactly and is not affected by other circuit elements; the current through it depends on the circuit and must be found by solving it. Based on sources.md.

## Q018
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** sources
**Focus Area:** VCVS vs. CCVS
**Question:** What is the difference between a voltage-controlled voltage source (VCVS) and a current-controlled voltage source (CCVS)?
**Answer:** A VCVS has value μV_x, where V_x is a controlling voltage elsewhere in the circuit and μ is a dimensionless constant. A CCVS has value μi_x, where i_x is a controlling current elsewhere in the circuit and μ is a constant with unit V/A. Based on sources.md.

## Q019
**Status:** active
**Type:** true-false
**Difficulty:** advanced
**Topic:** sources
**Focus Area:** Controlling variable direction/polarity
**Question:** True or False: For dependent sources, the given reference polarity or direction of the controlling variable (V_x or i_x) is always the actual polarity or direction once the circuit is solved.
**Answer:** False — the given reference polarity or direction for V_x or i_x is not necessarily the actual polarity or direction of voltage/current for the controlling element. Based on sources.md.

## Q020
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** sources
**Focus Area:** Dependent source example calculation
**Question:** In the dependent-source example circuit, if V_x is calculated to be 2 V and the VCVS is defined as 3V_x, what is the actual voltage of the VCVS, and what does this tell us about points a and b?
**Answer:** The VCVS becomes a 6 V source (3 × 2 V). This tells us point 'a' is higher in potential than point 'b' by 6 V. Based on sources.md.
