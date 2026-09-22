# Voltage Division

## Definition
In a series connection of resistors, the total voltage across the series branch of resistors divides among them proportional to their size.
> Source: Week 4 - Full.pdf

## Key Concepts
- **The formula:** For V across R₁, R₂, R₃ in series, V₁ = R₁/(R₁ + R₂ + R₃) · V.
  > Source: Week 4 - Full.pdf
- **Derivation:** R_eq = R₁ + R₂ + R₃. Ohm's Law on the reduced circuit gives i = V/R_eq = V/(R₁ + R₂ + R₃). Ohm's Law for R₁ on the original circuit gives V₁ = i·R₁ = [V/(R₁ + R₂ + R₃)]·R₁ = R₁/(R₁ + R₂ + R₃) · V.
  > Source: Week 4 - Full.pdf
- **The proportion in words:** R₁'s portion of total voltage V is the same as its portion of total resistance.
  > Source: Week 4 - Full.pdf
- **The voltages sum:** Total voltage V = V₁ + V₂ + V₃.
  > Source: Week 4 - Full.pdf
- **Opposite polarity needs a minus sign:** If V₁, V₂ or V₃ have opposite polarity to V, then add a (−) sign, e.g. V₂ = −R₂/(R₁ + R₂) · V.
  > Source: Week 4 - Full.pdf
- **One of the simple tools:** Voltage division is listed alongside current division as a simple resistive circuit analysis tool, as distinct from the systematic Node Voltage and Mesh Current methods.
  > Source: Week 4 - Full.pdf

## Common Misconceptions
- Applying the formula without checking polarity. The source explicitly flags the case where a branch voltage is labelled with opposite polarity to V, which requires a negative sign on the ratio.
  > Source: Week 4 - Full.pdf

## Related Topics
- [Resistors in Series](resistors-in-series.md)
- [Current Division](current-division.md)
- [Series/Parallel Circuit Analysis](series-parallel-circuit-analysis.md)
