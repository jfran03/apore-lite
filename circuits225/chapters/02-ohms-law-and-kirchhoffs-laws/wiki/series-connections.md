# Series Connections

## Definition
Two elements are in series if they are connected at one node only and there is no other element connected to that node.
> Source: Week 3 - Full.pdf

## Key Concepts
- **Same current:** Elements in series have the same current — provided the currents are labelled with the same direction.
  > Source: Week 3 - Full.pdf
- **Follows from KCL:** For elements 1, 2, 3 in series with nodes A and B between them: KCL at node A gives i₁ − i₂ = 0, so i₁ = i₂; KCL at node B gives i₂ − i₃ = 0, so i₂ = i₃. Therefore i₁ = i₂ = i₃.
  > Source: Week 3 - Full.pdf
- **How to spot series elements:** Examine all nodes and identify the ones at which only 2 elements are joined.
  > Source: Week 3 - Full.pdf

## Examples
- **"What's in series here?"** In the example circuit, elements A and B are in series, and elements D, E, F form a series group; element C is NOT in series with any element.
  > Source: Week 3 - Full.pdf
- **Series elements sharing a current (later example):** Elements C and D are in series — connected at one node only, with nothing else connected there — so they must have the same current. Paying attention to the labelled directions, i_C = −i_D. The same result follows from KCL at node 2: −i_C − i_D = 0, therefore i_C = −i_D.
  > Source: Week 3 - Full.pdf

## Common Misconceptions
- "Same current" holds only if the currents are labelled with the same direction; when directions are labelled oppositely, series elements satisfy i_C = −i_D rather than i_C = i_D.
  > Source: Week 3 - Full.pdf

## Related Topics
- [Kirchhoff's Current Law (KCL)](kirchhoffs-current-law.md)
- [Parallel Connections](parallel-connections.md)
