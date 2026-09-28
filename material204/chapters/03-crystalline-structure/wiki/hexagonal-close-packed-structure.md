# Hexagonal Close-Packed (HCP) Structure

> **HCP is Optional** for this chapter.
> Source: F26-D2L-Chapter 3 - Crystalline Structure-Part 1.pdf (slide 22)

## Definition

The HCP structure is presented as a large hexagonal prism unit cell with a middle layer of atoms between the top and bottom hexagonal faces. Atoms touch along the edges of the hexagonal base, so **a = 2R**.
> Source: F26-D2L-Chapter 3 - Crystalline Structure-Part 1.pdf (slide 23)

## Key Concepts

- **Symbols used in the derivation:**

  | Symbol | Meaning |
  |---|---|
  | a = 2R | Distance between neighbouring atom centres in one close-packed layer |
  | c | Full height of the hexagonal unit cell |
  | d = x | Distance from the centre of a small equilateral triangle to one corner |
  | h△ | Height of that equilateral triangle, measured within the horizontal plane |
  | h layer = c/2 | Vertical separation between neighbouring atomic layers |
  > Source: F26-D2L-Chapter 3 - Crystalline Structure-Part 1.pdf (slide 24)

- **Atoms per unit cell = 6:** N = 12(1/6) + 2(1/2) + 3 = 6, counting 12 corners (6 top + 6 bottom) at 1/6 each, 2 face centres at 1/2 each, and 3 atoms completely inside the middle layer.
  > Source: F26-D2L-Chapter 3 - Crystalline Structure-Part 1.pdf (slide 23)

- **Step 1 — horizontal distance d:** the triangle has side length *a*; joining its centre to a corner divides the 60° corner angle into two 30° angles. In the resulting right triangle, cos 30° = (a/2)/d, so d = (a/2)/(√3/2) → **d = x = a/√3**.
  > Source: F26-D2L-Chapter 3 - Crystalline Structure-Part 1.pdf (slide 25)

- **Step 2 — unit-cell height c:** using a right triangle between two atomic layers with horizontal side d = a/√3, vertical side c/2, and sloping side 2R = a (because the two atoms touch): d² + (c/2)² = a² → a²/3 + c²/4 = a² → c²/4 = 2a²/3 → c² = 8a²/3 → **c = √(8/3) a ≈ 1.633a**.
  > Source: F26-D2L-Chapter 3 - Crystalline Structure-Part 1.pdf (slide 26)

- **Step 3 — area of the hexagonal base:** divide the hexagon into six equilateral triangles of side *a*. h△² + (a/2)² = a² → h△² = 3a²/4 → h△ = (√3/2)a. One triangle has area A△ = ½ · a · h△ = (√3/4)a², so **A_hexagon = 6A△ = (3√3/2)a²**.
  > Source: F26-D2L-Chapter 3 - Crystalline Structure-Part 1.pdf (slide 27)

- **Step 4 — volume of the hexagonal unit cell:** V_cell = A_hexagon × c = (3√3/2)a² × √(8/3) a. Since √(8/3) = 2√2/√3, V_cell = **3√2 a³**. Using a = 2R, **V_cell = 3√2(2R)³ = 24√2 R³**.
  > Source: F26-D2L-Chapter 3 - Crystalline Structure-Part 1.pdf (slide 28)

- **Step 5 — atomic packing factor:** the large hexagonal prism contains 6 atoms, so V_atoms = 6 × (4/3)πR³ = 8πR³. APF = 8πR³ / (24√2 R³) = π/(3√2) → **APF ≈ 0.7405 = 74.05%**.
  > Source: F26-D2L-Chapter 3 - Crystalline Structure-Part 1.pdf (slide 29)

## Related Topics

- [Atomic Packing Factor](atomic-packing-factor.md)
- [Atom Counting in Unit Cells](atom-counting-in-unit-cells.md)
- [Crystal and Lattice Systems](crystal-and-lattice-systems.md)
- [Face-Centered Cubic Structure](face-centered-cubic-structure.md)
