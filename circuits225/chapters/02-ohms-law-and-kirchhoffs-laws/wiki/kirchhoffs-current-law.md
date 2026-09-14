# Kirchhoff's Current Law (KCL)

## Definition
KCL states: the algebraic sum of all currents at a node must be zero.
> Source: Week 3 - Full.pdf

## Key Concepts
- **Why Kirchhoff's Laws:** Having seen the fundamental electrical quantities V and i (and P, w) and circuit elements with their own V–i relationships, Kirchhoff's Laws define how V and i distribute *in a circuit*.
  > Source: Week 3 - Full.pdf
- **Node:** A node is the joining of 2 or more circuit elements.
  > Source: Week 3 - Full.pdf
- **Connection points form one node:** Connection points connected directly to each other by conductors constitute one node.
  > Source: Week 3 - Full.pdf
- **Sign convention:** Choose a consistent way to distinguish incoming and outgoing currents at a node. Current *entering* the node adds; current *leaving* the node subtracts.
  > Source: Week 3 - Full.pdf
- **Convention is not universal:** Later, in the Node Voltage Method, the opposite convention will be used.
  > Source: Week 3 - Full.pdf
- **Circuits that violate KCL:** A circuit with a 5 A source and a 10 A source joined at a node B is prohibited, because KCL at node B gives 5 − 10 ≠ 0.
  > Source: Week 3 - Full.pdf

## Examples
- **Fluid analogy:** An ideal pipe (no leaks!) with water entering at 6 L/min and 3 L/min and leaving at 9 L/min illustrates KCL.
  > Source: Week 3 - Full.pdf
- **Basic node sum:** At a node A with i₁ and i₂ entering and i₃ leaving: i₁ + i₂ − i₃ = 0, so i₁ + i₂ = i₃.
  > Source: Week 3 - Full.pdf
- **Determine i₁ at node M:** M is a single node (its connection points are joined directly by conductors). With −5 A and 3 A and 6 A entering M and i₁ leaving: −5 + 3 + 6 − i₁ = 0, therefore i₁ = 4 A.
  > Source: Week 3 - Full.pdf
- **Same problem, solved connection point by connection point:** Alternatively, KCL can be written for each connection point inside node M. Choosing an arbitrary direction for i₂: at connection point N, −5 + 3 − i₂ = 0, so i₂ = −2 A. At connection point P, −2 (that is, i₂) + 6 − i₁ = 0, so i₁ = 4 A — the same answer.
  > Source: Week 3 - Full.pdf

## Common Misconceptions
- Several separate-looking connection points may in fact be a *single* node; the source explicitly flags "Note that M is a single node" before applying KCL.
  > Source: Week 3 - Full.pdf

## Related Topics
- [Series Connections](series-connections.md)
- [Kirchhoff's Voltage Law (KVL)](kirchhoffs-voltage-law.md)
- [Parallel Connections](parallel-connections.md)
