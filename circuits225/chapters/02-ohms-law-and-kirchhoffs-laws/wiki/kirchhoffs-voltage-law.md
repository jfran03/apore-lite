# Kirchhoff's Voltage Law (KVL)

## Definition
KVL states: the algebraic sum of all voltages around a loop must be zero. It is derived from conservation of energy.
> Source: Week 3 - Full.pdf

## Key Concepts
- **Loop:** A loop is a closed path starting at a node and finishing back at the same node (e.g. Y → Z → X → Y).
  > Source: Week 3 - Full.pdf
- **Loop direction is arbitrary:** The loop direction is chosen arbitrarily. It has no relation to current direction.
  > Source: Week 3 - Full.pdf
- **Sign convention (1):** If, travelling in the loop direction, the element is labelled `+ V −` (the loop meets the + terminal first), then add V.
  > Source: Week 3 - Full.pdf
- **Sign convention (2):** If, travelling in the loop direction, the element is labelled `− V +` (the loop meets the − terminal first), then subtract V.
  > Source: Week 3 - Full.pdf
- **Loops can contain open circuits:** It is important to account for the potential difference across an open circuit when applying KVL.
  > Source: Week 3 - Full.pdf
- **Circuits prohibited by KVL:** A 12 V source whose terminals form a loop by themselves is prohibited, since KVL around that loop gives −12 ≠ 0.
  > Source: Week 3 - Full.pdf

## Examples
- **Basic loop:** For the example circuit with elements A, B, C around a loop, KVL gives −V_B + V_C − V_A = 0.
  > Source: Week 3 - Full.pdf
- **Loop containing an open circuit:** With V_OC the voltage across the open circuit, KVL gives −V_A − V_B + V_OC = 0.
  > Source: Week 3 - Full.pdf
- **Parallel elements via KVL:** Around the loop formed by two parallel elements A and B, KVL gives −V_A + V_B = 0, therefore V_A = V_B.
  > Source: Week 3 - Full.pdf
- **Inconsistently labelled polarities:** If the polarities of two parallel elements are not labelled consistently, KVL gives −V_A − V_B = 0, therefore V_A = −V_B.
  > Source: Week 3 - Full.pdf

## Common Misconceptions
- The loop direction has no relation to current direction — it is purely an arbitrary choice for summing voltages.
  > Source: Week 3 - Full.pdf
- An open circuit in a loop cannot simply be ignored; its potential difference must be accounted for.
  > Source: Week 3 - Full.pdf

## Related Topics
- [Parallel Connections](parallel-connections.md)
- [Kirchhoff's Current Law (KCL)](kirchhoffs-current-law.md)
