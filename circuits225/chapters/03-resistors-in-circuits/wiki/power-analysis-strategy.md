# Power Analysis Strategy (KVL, KCL and Dependent Sources)

## Definition
A strategy for finding the power in every element of a circuit: need all voltages and currents to calculate power; use KVL and KCL to find the unknown voltages and currents, assuming a polarity/direction if unknown; then use p = vi or p = −vi based on the direction of i and the polarity of v for each element.
> Source: Week 4 - Full.pdf

## Key Concepts
- **Assume when unknown:** If a voltage polarity or a current direction is not given, assume one and carry it through. Loop directions for KVL are likewise chosen arbitrarily.
  > Source: Week 4 - Full.pdf
- **Sign of power follows the labels:** For each element, p = vi or p = −vi is selected according to how that element's current direction sits relative to its voltage polarity.
  > Source: Week 4 - Full.pdf
- **P > 0 means absorbing:** A positive computed power means the element is absorbing power — including when that element is a source.
  > Source: Week 4 - Full.pdf
- **Current-controlled current source (CCCS):** A dependent source whose value is set by a controlling current elsewhere in the circuit, e.g. a CCCS of value 2i_Δ controlled by the current i_Δ.
  > Source: Week 4 - Full.pdf
- **Conservation of power/energy as the check:** The powers of all elements must sum to zero, ΣP = 0.
  > Source: Week 4 - Full.pdf

## Examples
- **Worked example — "Let V₀ = 100 V. Find the power for each element":** The circuit contains a current source i_g and an 80 V source in the left branch, an 80 V source and a 4 A source in the middle branch (carrying the controlling current i_Δ), and a CCCS of value 2i_Δ with V₀ across it in the right branch. Nodes A, B, C and D are labelled.
  > Source: Week 4 - Full.pdf
- **Step 1 — currents by KCL:** KCL at node B: 4 − i_Δ = 0, therefore i_Δ = 4 A (4 A enters, i_Δ leaves). KCL at node A: 2i_Δ + i_Δ − i_g = 0, therefore i_g = 12 A (2i_Δ enters A from the CCCS, i_Δ enters A from the 80 V source branch, i_g leaves A).
  > Source: Week 4 - Full.pdf
- **Step 2 — voltages by KVL:** With all currents known, two unknown voltages remain, V₄ (across the 4 A source) and V₁₂ (across the 12 A source); a polarity is assumed for each. KVL around loop 1: −100 − 80 + V₄ = 0, therefore V₄ = 180 V. KVL around loop 2: −V₄ + 80 + V₁₂ − 80 = 0, therefore V₁₂ = 180 V.
  > Source: Week 4 - Full.pdf
- **Step 3 — power in each element:**
  | Element | Power |
  |---|---|
  | 12 A source | P = V·i = V₁₂ × 12 A = 2160 W |
  | left 80 V source | P = −V·i = −(80 V)(12 A) = −960 W |
  | mid 80 V source | P = V·i = (80 V)(4 A) = 320 W |
  | 4 A source | P = −V·i = −V₄ × 4 A = −720 W |
  | CCCS | P = −V·i = −(100)(8 A) = −800 W |

  The 12 A source has P > 0, so that source is absorbing power. The CCCS carries 2i_Δ = 8 A with V₀ = 100 V across it. Summing: ΣP = 0 ✓ — conservation of power/energy.
  > Source: Week 4 - Full.pdf

## Common Misconceptions
- Assuming a source must deliver power. In this example the 12 A source produces P = +2160 W, and the note beside it reads "P > 0. Source is absorbing power."
  > Source: Week 4 - Full.pdf

## Related Topics
- [Identifying Parallel Connections](identifying-parallel-connections.md)
- [Series/Parallel Circuit Analysis](series-parallel-circuit-analysis.md)
