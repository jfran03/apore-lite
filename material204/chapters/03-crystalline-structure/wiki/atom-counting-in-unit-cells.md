# Atom Counting in Unit Cells

## Definition

Count only the fraction of each atom that lies inside the unit cell. For SC, BCC and FCC:

> N (total atoms) = interior atoms + face atoms / 2 + corner atoms / 8

Equivalently, N = N_i + N_f/2 + N_c/8, where N_i is the number of interior atoms, N_f the number of face atoms, and N_c the number of corner atoms.
> Source: F26-D2L-Chapter 3 - Crystalline Structure-Part 1.pdf (slides 13, 17, 20)

## Key Concepts

- **Contribution by atom position:**

  | Atom position | Shared by | Contribution |
  |---|---|---|
  | Corner | 8 unit cells | 1/8 |
  | Face centre | 2 unit cells | 1/2 |
  | Inside the cell | 1 unit cell | 1 |
  > Source: F26-D2L-Chapter 3 - Crystalline Structure-Part 1.pdf (slide 20)

- **Applying the formula to the three cubic structures:**

  | Structure | Calculation | N |
  |---|---|---|
  | Simple cubic | 0 + 0 + 8/8 | 1 |
  | BCC | 1 + 0 + 8/8 | 2 |
  | FCC | 0 + 6/2 + 8/8 | 4 |
  > Source: F26-D2L-Chapter 3 - Crystalline Structure-Part 1.pdf (slide 21)

- **HCP counting (large hexagonal prism):** 12 corner atoms × 1/6 + 2 top/bottom face-centre atoms × 1/2 + 3 atoms completely inside the middle layer × 1 = 6 atoms.
  > Source: F26-D2L-Chapter 3 - Crystalline Structure-Part 1.pdf (slide 23)

## Common Misconceptions

- An atom is not physically cut into pieces. The unit-cell boundary divides its contribution for accounting. Corner atoms are shared by eight cells, face-centred atoms by two, and a body-centred atom belongs entirely to one cell.
  > Source: F26-D2L-Chapter 3 - Crystalline Structure-Part 1.pdf (slide 20)

## Related Topics

- [Simple Cubic Structure](simple-cubic-structure.md)
- [Body-Centered Cubic Structure](body-centered-cubic-structure.md)
- [Face-Centered Cubic Structure](face-centered-cubic-structure.md)
- [Hexagonal Close-Packed Structure](hexagonal-close-packed-structure.md)
- [Atomic Packing Factor](atomic-packing-factor.md)
