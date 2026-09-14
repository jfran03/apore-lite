# Parallel Connections

## Definition
Two elements are parallel if their terminals are directly connected to each other — in other words, they are connected to the same 2 nodes.
> Source: Week 3 - Full.pdf

## Key Concepts
- **Same voltage:** Elements in parallel have the same voltage — provided the polarities are labelled consistently.
  > Source: Week 3 - Full.pdf
- **Follows from KVL:** Around the loop formed by parallel elements A and B, KVL gives −V_A + V_B = 0, therefore V_A = V_B.
  > Source: Week 3 - Full.pdf
- **Inconsistent polarity labelling:** If the polarities are not labelled consistently, then V_A = −V_B. This can be confirmed with KVL: −V_A − V_B = 0, therefore V_A = −V_B.
  > Source: Week 3 - Full.pdf
- **More than two elements:** More than 2 elements can be in parallel, in which case V_A = V_B = V_C.
  > Source: Week 3 - Full.pdf
- **Parallel connections can be disguised:** Watch for parallel connections that may not appear like parallel elements at first glance. The source shows a circuit with R₁, R₂, R₃, R₄ drawn in a crossed layout that is redrawn as four elements all connected between node 1 and node 2.
  > Source: Week 3 - Full.pdf
- **Test for parallel:** Parallel elements have no circuit element separating their terminals, so they share a common voltage.
  > Source: Week 3 - Full.pdf

## Examples
- **Combined series/parallel example.** For the circuit with elements A, B, C, D and nodes 1, 2, 3:
  - (a) *What's in series and parallel?* Series: C and D — connected at one node only, with nothing else connected there. Parallel: A and B — connected to the same 2 nodes (1 and 3), with no circuit element separating their terminals, so they share a common voltage.
  - (b) *i_C in terms of i_D:* C and D are in series, so they must have the same current; paying attention to directions, i_C = −i_D. The same result follows from KCL at node 2: −i_C − i_D = 0, therefore i_C = −i_D.
  - (c) *Given i_A = 3 A and i_C = 1 A, find i_B and i_D:* i_D = −i_C = −1 A. KCL at node 1 gives i_A − i_B + i_C = 0, i.e. 3 − i_B + 1 = 0, therefore i_B = 4 A.
  > Source: Week 3 - Full.pdf
- **Dependent-source power problem (setup only).** Let V₀ = 100 V; find the power for each element in a circuit containing a current source i_g, an 80 V source (with controlling current i_Δ through it), a 4 A source, and a CCCS of value 2i_Δ with V₀ across it. The stated strategy: all voltages and currents are needed to calculate power, so use KVL and KCL to find the unknown voltages and currents, assuming a polarity/direction where unknown. *(The source states the strategy but does not carry out the solution.)*
  > Source: Week 3 - Full.pdf

## Common Misconceptions
- Parallel connections may not look parallel as drawn; the source explicitly warns to watch for parallel connections that "may not appear like parallel elements at first glance."
  > Source: Week 3 - Full.pdf
- "Same voltage" holds only if the polarities are labelled consistently; otherwise V_A = −V_B.
  > Source: Week 3 - Full.pdf

## Related Topics
- [Kirchhoff's Voltage Law (KVL)](kirchhoffs-voltage-law.md)
- [Series Connections](series-connections.md)
- [Kirchhoff's Current Law (KCL)](kirchhoffs-current-law.md)
