# Current Division

## Definition
In a parallel connection of resistors, the total current available to the parallel resistors divides among them inversely proportional to their size.
> Source: Week 4 - Full.pdf

## Key Concepts
- **The formula (two resistors):** For a total current i entering R₁ ∥ R₂, i₁ = R₂/(R₁ + R₂) · i — the numerator is the *other* branch.
  > Source: Week 4 - Full.pdf
- **Derivation:** i is the total current; it can only go through the parallel resistors R₁ and R₂, so i = i₁ + i₂. With R_eq = R₁R₂/(R₁ + R₂), Ohm's Law on the reduced circuit gives V = i·R_eq = i·R₁R₂/(R₁ + R₂). Ohm's Law for R₁ on the original circuit gives i₁ = V/R₁ = [i·R₁R₂/(R₁ + R₂)]/R₁ = R₂/(R₁ + R₂) · i.
  > Source: Week 4 - Full.pdf
- **The proportion in words:** R₁'s portion of total current i is the same as R₂'s portion of total resistance.
  > Source: Week 4 - Full.pdf
- **More than two resistors:** Current division is not as easy to apply when there are more than 2 resistors in parallel. We can group resistors to apply current division in this case.
  > Source: Week 4 - Full.pdf
- **Identify the true total current first:** To apply current division you need the total current going through the parallel resistors, which may have to be found by KCL when other sources feed the same node.
  > Source: Week 4 - Full.pdf

## Examples
- **Example — "Find i₃" (three parallel resistors):** A 10 A source feeds 60 Ω, 30 Ω and 10 Ω in parallel, with i₃ through the 10 Ω. Group the 60 Ω and 30 Ω: combine in parallel to get (60 × 30)/(60 + 30) = 20 Ω. Current division then gives i₃ = 20/(10 + 20) × 10 A = 6.6̄ A.
  > Source: Week 4 - Full.pdf
- **Example 2 — "How to apply current division here?":** i = 30 A enters node M, which feeds a 20 Ω branch (i₁), a 10 Ω branch (i₂), and a 10 A current source. The total current through the parallel resistors is i₁ + i₂; call this i_total. KCL at node M: +30 − i₁ − i₂ − 10 = 0, therefore i_total = i₁ + i₂ = 20 A. Now current division applies: i₁ = 10/(10 + 20) × i_total = 6.6̄ A.
  > Source: Week 4 - Full.pdf

## Common Misconceptions
- Writing i₃ = (60 + 30)/(60 + 30 + 10) × 10 A for three parallel resistors. The source marks this expression as wrong (crossed out) — the 60 Ω and 30 Ω must first be combined in parallel to 20 Ω, giving i₃ = 20/(10 + 20) × 10 A.
  > Source: Week 4 - Full.pdf
- Taking the source current as the total current for division. In Example 2 the 30 A entering node M is not what divides between the resistors; KCL first removes the 10 A drawn by the current source, leaving i_total = 20 A.
  > Source: Week 4 - Full.pdf

## Related Topics
- [Resistors in Parallel](resistors-in-parallel.md)
- [Voltage Division](voltage-division.md)
- [Equivalent Resistance](equivalent-resistance.md)
