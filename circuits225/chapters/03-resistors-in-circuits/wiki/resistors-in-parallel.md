# Resistors in Parallel

## Definition
Resistors in parallel combine reciprocally: R_eq = (1/R₁ + 1/R₂ + 1/R₃)⁻¹.
> Source: Week 4 - Full.pdf

## Key Concepts
- **Common voltage:** Parallel elements share a common voltage. With a source V_s across three parallel resistors, each resistor has V_s across it.
  > Source: Week 4 - Full.pdf
- **Derivation from KCL and Ohm's Law:** For a source V_s driving R₁, R₂, R₃ in parallel between nodes A and B — KCL at node A: i − i₁ − i₂ − i₃ = 0; from Ohm's Law: i₁ = V_s/R₁, i₂ = V_s/R₂, i₃ = V_s/R₃. Substituting gives i − V_s/R₁ − V_s/R₂ − V_s/R₃ = 0, so i = V_s(1/R₁ + 1/R₂ + 1/R₃).
  > Source: Week 4 - Full.pdf
- **The equivalent resistor:** Rearranging gives V_s = i(1/R₁ + 1/R₂ + 1/R₃)⁻¹, which "looks like" V_s = iR. The bracketed factor is R_eq.
  > Source: Week 4 - Full.pdf
- **Product over sum (two resistors):** For 2 resistors in parallel, R_eq = (1/R₁ + 1/R₂)⁻¹ = 1/(1/R₁ + 1/R₂) = R₁·R₂/(R₁ + R₂) — product over sum.
  > Source: Week 4 - Full.pdf

## Examples
- **Two equal resistors:** 40 Ω in parallel with 40 Ω gives R_eq = (40 × 40)/(40 + 40) = 20 Ω.
  > Source: Week 4 - Full.pdf
- **Grouping for current division:** 60 Ω in parallel with 30 Ω gives (60 × 30)/(60 + 30) = 20 Ω.
  > Source: Week 4 - Full.pdf

## Common Misconceptions
- The product-over-sum shortcut is stated specifically "for 2 resistors in parallel"; the general case is the reciprocal form R_eq = (1/R₁ + 1/R₂ + 1/R₃)⁻¹.
  > Source: Week 4 - Full.pdf

## Related Topics
- [Resistors in Series](resistors-in-series.md)
- [Identifying Parallel Connections](identifying-parallel-connections.md)
- [Current Division](current-division.md)
