# Equivalent Resistance

## Definition
A resistor network can be reduced to a single equivalent resistance by repeatedly applying the series and parallel rules, one combination at a time.
> Source: Week 4 - Full.pdf

## Key Concepts
- **Reduce step by step:** Each step identifies one series pair or one parallel pair, replaces it with its equivalent, and redraws the simpler circuit. The process repeats until a single resistor remains.
  > Source: Week 4 - Full.pdf
- **Resistance between two nodes:** Equivalent resistance can be asked for between two specified nodes/points a and b, with the rest of the network reduced as seen from those terminals.
  > Source: Week 4 - Full.pdf
- **Parallel notation:** The reduction may be written compactly with the parallel operator, e.g. R_eq = R₁ ∥ (R₂ + R₃ + R₄).
  > Source: Week 4 - Full.pdf

## Examples
- **"Find a single equivalent resistance":** A source at node A feeds a network with nodes A, B, C, D, E — a 25 Ω and a 5 Ω from A through B to C, a 40 Ω from C to E, and a 30 Ω and 10 Ω from C through D to E. The reduction runs:
  1. 25 Ω + 5 Ω in series → R_eq = 30 Ω
  2. 30 Ω + 10 Ω in series → R_eq = 40 Ω
  3. 40 Ω ∥ 40 Ω → R_eq = (40 × 40)/(40 + 40) = 20 Ω
  4. 30 Ω + 20 Ω in series → R_eq = 50 Ω

  The circuit ends as the source across a single 50 Ω resistor.
  > Source: Week 4 - Full.pdf
- **Aside — finding resistance between 2 nodes/points:** For a network seen from terminals a and b, with R₁ across a–b, and R₂, R₃, R₄ forming the outer path, the answer is R_eq = R₁ ∥ (R₂ + R₃ + R₄).
  > Source: Week 4 - Full.pdf

## Common Misconceptions
- In the a–b aside, you can't say R₁ and R₂ are in series, because there could be other circuit elements connected to the left side of a and b.
  > Source: Week 4 - Full.pdf

## Related Topics
- [Resistors in Series](resistors-in-series.md)
- [Resistors in Parallel](resistors-in-parallel.md)
- [Series/Parallel Circuit Analysis](series-parallel-circuit-analysis.md)
