# Worked Problems

Hints supplied on the problem slides: a = 2r for SC, a = 4r/√3 for BCC, a = 2√2 r for FCC; and n ≈ 1 ⇒ SC, n ≈ 2 ⇒ BCC, n ≈ 4 ⇒ FCC.
> Source: F26-D2L-Chapter 3 - Crystalline Structure-Part 1.pdf (slides 33, 35)

---

## Example Problem 6 — Atomic radius from density

**Problem:** Calculate the radius of an iridium atom, given that Ir has an FCC crystal structure, a density of 22.4 g/cm³, and an atomic weight of 192.2 g/mol.
> Source: F26-D2L-Chapter 3 - Crystalline Structure-Part 1.pdf (slides 33, 34)

**Solution path:**
1. For FCC, n = 4 atoms/unit cell, and V_C = 16R³√2.
2. Start with the density equation ρ = nA / (V_C N_A), so ρ = nA_Ir / [(16R³√2) N_A].
3. Solving for R yields R = [ nA_Ir / (16 ρ N_A √2) ]^(1/3).
4. Substituting: R = [ (4 atoms/unit cell)(192.2 g/mol) / ((16)(22.4 g/cm³)(6.022 × 10²³ atoms/mol)(√2)) ]^(1/3).

**Answer:** R = 1.36 × 10⁻⁸ cm = **0.136 nm**.
> Source: F26-D2L-Chapter 3 - Crystalline Structure-Part 1.pdf (slide 34)

---

## Example Problem 8 — Identifying the structure of alloys

**Problem:** Determine whether the alloys A, B, C below have an FCC, BCC, or simple cubic unit cell.

| Alloy | Atomic Weight (g/mol) | Density (g/cm³) | Atomic Radius (nm) |
|---|---|---|---|
| A | 77.4 | 8.22 | 0.125 |
| B | 107.6 | 13.42 | 0.133 |
| C | 127.3 | 9.23 | 0.142 |
> Source: F26-D2L-Chapter 3 - Crystalline Structure-Part 1.pdf (slide 35)

**Solution method:** consider the density formula ρ = nA/(V N_A), where N_A is Avogadro's number, n is the number of atoms in the unit cell of volume V, and A is atomic mass [g/mol]. We must find n to determine whether they have an FCC, BCC, or simple cubic unit cell. Thus use n = ρ V N_A / A, where V = a³, and a = 4r/√3 for BCC, a = 2√2 r for FCC, and a = 2r for the simple cubic.
> Source: F26-D2L-Chapter 3 - Crystalline Structure-Part 1.pdf (slide 35)

> **Note:** the results table of n(BCC), n(FCC), n(SC) for alloys A, B, C is covered over on the slide, so the final structure assignments are not stated in this source.
> Source: F26-D2L-Chapter 3 - Crystalline Structure-Part 1.pdf (slide 35)

---

## Example Problem 9 — Percent volume change in the iron allotropic transformation

**Problem:** Iron (Fe) undergoes an allotropic transformation at 912 °C: upon heating from a BCC (α phase, called ferrite phase) to an FCC (γ phase, called austenite phase). Accompanying this transformation is a change in the atomic radius of Fe — from r_BCC = 0.12584 nm to r_FCC = 0.12894 nm — and also a change in density (and volume). Compute the percent volume change associated with this reaction. Does the volume increase or decrease?

Given: r_BCC = 0.12584 nm, r_FCC = 0.12894 nm, A_Fe = 55.85 g/mol.

What must be determined: (1) the density of BCC iron, (2) the density of FCC iron, (3) the volume per unit mass for each, (4) the percent volume change, (5) whether the volume increases or decreases.
> Source: F26-D2L-Chapter 3 - Crystalline Structure-Part 1.pdf (slide 44)

**Part A — BCC iron**
- n = 2 atoms/unit cell; a = 4r/√3, so a_BCC = 4(0.12584)/√3 = 0.29062 nm.
- Using 1 nm = 10⁻⁷ cm: a_BCC = 2.9062 × 10⁻⁸ cm.
- V_BCC = a³ = (2.9062 × 10⁻⁸)³ = 2.454 × 10⁻²³ cm³.
- ρ_BCC = (2)(55.85) / [(2.454 × 10⁻²³)(6.022 × 10²³)] ≈ **7.56 g/cm³**.
> Source: F26-D2L-Chapter 3 - Crystalline Structure-Part 1.pdf (slides 45, 46)

**Part B — FCC iron**
- BCC → FCC, which means n = 4 atoms/unit cell.
- a = 4r/√2 = 2√2 r, so a_FCC = 2√2(0.12894) = 0.36470 nm = 3.6470 × 10⁻⁸ cm.
- V_FCC = (3.6470 × 10⁻⁸)³ ≈ 4.851 × 10⁻²³ cm³, and V_FCC > V_BCC.
- ρ_FCC = (4)(55.85) / [(4.851 × 10⁻²³)(6.022 × 10²³)] ≈ **7.65 g/cm³**.
> Source: F26-D2L-Chapter 3 - Crystalline Structure-Part 1.pdf (slides 46, 47)

**Comparing the same amount of iron:** since ρ = m/V, rearranging gives V/m = 1/ρ.
- V_BCC/m = 1/7.56 = 0.1323 cm³/g
- V_FCC/m = 1/7.65 = 0.1308 cm³/g
> Source: F26-D2L-Chapter 3 - Crystalline Structure-Part 1.pdf (slide 48)

**Percent volume change:** %ΔV = [(V_final − V_initial)/V_initial] × 100, with initial = BCC and final = FCC:
%ΔV = [(0.1308 − 0.1323)/0.1323] × 100 → **%ΔV ≈ −1.19%**.
> Source: F26-D2L-Chapter 3 - Crystalline Structure-Part 1.pdf (slide 49)

## Related Topics

- [Theoretical Density](theoretical-density.md)
- [Polymorphism and Allotropy](polymorphism-and-allotropy.md)
- [Unit Cell Geometry and Lattice Constants](unit-cell-geometry-and-lattice-constants.md)
- [Face-Centered Cubic Structure](face-centered-cubic-structure.md)
- [Body-Centered Cubic Structure](body-centered-cubic-structure.md)
