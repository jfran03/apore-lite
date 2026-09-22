# Series/Parallel Circuit Analysis

## Definition
Circuit analysis is the procedure for determining all voltages and currents in every circuit element. The resistor equivalents may be used to analyze a circuit.
> Source: Week 4 - Full.pdf

## Key Concepts
- **Collapse, solve, then expand:** Reduce the network to a single equivalent resistance, solve the simple circuit, then work back to the original circuit step by step, restoring one equivalent at a time.
  > Source: Week 4 - Full.pdf
- **Unwinding a series equivalent:** When replacing R_eq with the original series resistors, these resistors will have the same current as R_eq.
  > Source: Week 4 - Full.pdf
- **Unwinding a parallel equivalent:** When replacing R_eq with the original parallel resistors, they have the same voltage.
  > Source: Week 4 - Full.pdf
- **Two ways to get the voltage across the final resistor:** (i) KVL around the loop: −80 + V_R = 0, therefore V_R = 80 V; or (ii) because of the voltage source, node A is higher than node D by 80 V, i.e. V_AD = 80 V, therefore V_R = V_AD = 80 V.
  > Source: Week 4 - Full.pdf
- **Check as you go:** Each expansion step is verified with a KVL or KCL check on the restored circuit.
  > Source: Week 4 - Full.pdf
- **Power forms for a resistor:** Resistor power may be computed as P = V·i, as V²/R, or as i²R.
  > Source: Week 4 - Full.pdf
- **What comes later:** Later, well-established systematic methods for analysis will be used: Node Voltage and Mesh Current. Other simple resistive circuit analysis tools are voltage division and current division.
  > Source: Week 4 - Full.pdf

## Examples
- **Worked example — "Find power in each element":** An 80 V source at node A feeds a 60 Ω from A to B, a 40 Ω from B to D, and a 10 Ω from B to C with a 30 Ω from C to D; D is the bottom node.
  > Source: Week 4 - Full.pdf
- **Reduction phase:** 10 Ω + 30 Ω in series → R_eq = 40 Ω; then 40 Ω ∥ 40 Ω → R_eq = 20 Ω; then 60 Ω + 20 Ω in series → R_eq = 80 Ω. The circuit is now the 80 V source across a single 80 Ω.
  > Source: Week 4 - Full.pdf
- **Solve the reduced circuit:** V_R = 80 V, so from Ohm's Law i = V_R/80 Ω = 1 A. To find i_src, KCL at node A: i_src − i = 0, therefore i_src = 1 A.
  > Source: Week 4 - Full.pdf
- **Expansion step 1 (series):** Restoring the 60 Ω and the 20 Ω combination — both carry the same 1 A as R_eq. From Ohm's Law: V₆₀ = 60 Ω × 1 A = 60 V and V_BD = 20 Ω × 1 A = 20 V. KVL check: −80 + V₆₀ + V_BD = 0 ✓ (80 = 60 + 20).
  > Source: Week 4 - Full.pdf
- **Expansion step 2 (parallel):** Restoring the two 40 Ω branches — both have the same voltage V_BD = 20 V. From Ohm's Law: i₁ = V_BD/40 Ω = 20 V/40 Ω = 0.5 A and i₂ = V_BD/40 Ω = 0.5 A. KCL check at node B: i − i₁ − i₂ = 0 ✓ (1 A = 0.5 A + 0.5 A).
  > Source: Week 4 - Full.pdf
- **Expansion step 3 (series again):** Replacing the right 40 Ω with the original series 10 Ω and 30 Ω from the original circuit, both carrying i₂ = 0.5 A. From Ohm's Law: V₁₀ = i₂ × 10 = 5 V and V₃₀ = i₂ × 30 = 15 V. KVL check around the right loop: −V_BD + V₁₀ + V₃₀ = 0 ✓ (20 = 5 + 15).
  > Source: Week 4 - Full.pdf
- **Power in each element:**
  | Element | Power |
  |---|---|
  | 80 V source | P = −vi = −(80 V)(1 A) = −80 W (supplies 80 W) |
  | 60 Ω | P = V₆₀·i = (V₆₀)²/60 Ω = i²(60 Ω) = 60 W |
  | 40 Ω | P = V_BD·i₁ = V_BD²/40 Ω = i₁²(40 Ω) = 10 W |
  | 10 Ω | P = V₁₀·i₂ = (V₁₀)²/10 Ω = i₂²(10 Ω) = 2.5 W |
  | 30 Ω | P = V₃₀·i₂ = (V₃₀)²/30 = i₂²(30 Ω) = 7.5 W |

  ΣP = 0 ✓ — energy balance.
  > Source: Week 4 - Full.pdf

## Related Topics
- [Equivalent Resistance](equivalent-resistance.md)
- [Resistors in Series](resistors-in-series.md)
- [Resistors in Parallel](resistors-in-parallel.md)
- [Voltage Division](voltage-division.md)
- [Current Division](current-division.md)
