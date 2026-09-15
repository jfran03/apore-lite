# Bonding Forces and Energies

## Definition
The most stable configuration between two atoms occurs at the minimum net energy, where net energy is the sum of attractive and repulsive energies.
> Source: before lecture-Chapter 2 - Atomic Structure and Interatomic Bonding.pdf, slide 13

## Key Concepts
- **Net energy equation:** E_N = E_A + E_R = -A/r + B/rⁿ, where E_A is attractive energy, E_R is repulsive energy, r is interatomic separation, and B and n are constants (n is approximately 8).
  > Source: before lecture-Chapter 2 - Atomic Structure and Interatomic Bonding.pdf, slide 13
- **Constant A:** A = (1/4πε₀)(|Z₁|e)(|Z₂|e).
  > Source: before lecture-Chapter 2 - Atomic Structure and Interatomic Bonding.pdf, slide 13
- **Force-potential energy relationship:** E = ∫−F dr, and F = −dE/dr.
  > Source: before lecture-Chapter 2 - Atomic Structure and Interatomic Bonding.pdf, slide 13
- **Equilibrium separation (r₀):** the interatomic separation at which net energy E_N reaches its minimum (E₀); at separations less than r₀ repulsive energy dominates, at separations greater than r₀ attractive energy dominates.
  > Source: before lecture-Chapter 2 - Atomic Structure and Interatomic Bonding.pdf, slide 13
- **Bonding energy and melting temperature:** the larger the bonding energy E₀ (deeper energy well), the higher the melting temperature T_m.
  > Source: before lecture-Chapter 2 - Atomic Structure and Interatomic Bonding.pdf, slide 29

## Added from the full lecture deck (Part 1 and Part 2)

### Forces at the equilibrium separation
- **Net force equation:** the net force is the sum of the attractive and repulsive forces, F_N = F_A + F_R (Eq. 2.3 from the textbook). At equilibrium, r = r₀ and F_N = 0.
  > Source: F26-D2L-Chapter 2- Introduction to Engineering Materials-Part 1 and part 2 (full).pdf, slide 31
- **r₀ is the bond length:** the equilibrium separation r₀ is the bond length — the distance between the centers of two bonded atoms at the lowest potential energy. At this particular separation the attractive and repulsive effects exactly balance, so the net force is zero. This is the most stable distance between atoms in a bond.
  > Source: F26-D2L-Chapter 2- Introduction to Engineering Materials-Part 1 and part 2 (full).pdf, slides 33, 34, 43
- **Dominant interaction by separation:** for r < r₀ the interaction is repulsive and pushes atoms apart; at r = r₀ the interaction is balanced and F = 0; for r > r₀ the interaction is attractive and pulls atoms together.
  > Source: F26-D2L-Chapter 2- Introduction to Engineering Materials-Part 1 and part 2 (full).pdf, slide 35
- **The three regimes described physically:** when atoms are too far apart, attractive and repulsive forces are both negligible and potential energy ≈ 0 (as r → ∞). At the equilibrium separation ("just right"), attractive and repulsive forces balance (net force = 0) and potential energy is a minimum (V = −ε). When atoms are too close, electron clouds strongly overlap, the repulsive force increases very rapidly, and potential energy rises sharply.
  > Source: F26-D2L-Chapter 2- Introduction to Engineering Materials-Part 1 and part 2 (full).pdf, slide 32

### Coulombic attractive and repulsive energies
- **Attractive energy (Eq. 2.9):** the attractive bonding forces are coulombic — positive and negative ions, by virtue of their net electrical charge, attract one another. For two isolated ions, E_A = −A/r.
  > Source: F26-D2L-Chapter 2- Introduction to Engineering Materials-Part 1 and part 2 (full).pdf, slide 44
- **The constant A (Eq. 2.10):** A = (1/4πε₀)(|Z₁|e)(|Z₂|e), where ε₀ is the permittivity of a vacuum (8.85 × 10⁻¹² F/m), |Z₁| and |Z₂| are absolute values of the valences for the two ion types, and e is the electronic charge (1.602 × 10⁻¹⁹ C). This value of A assumes the bond between ions 1 and 2 is totally ionic; because bonds in most of these materials are not 100% ionic, A is normally determined from experimental data rather than computed.
  > Source: F26-D2L-Chapter 2- Introduction to Engineering Materials-Part 1 and part 2 (full).pdf, slide 44
- **Repulsive energy (Eq. 2.11):** E_R = B/rⁿ, where B and n are constants whose values depend on the particular ionic system. The value of n is approximately 8.
  > Source: F26-D2L-Chapter 2- Introduction to Engineering Materials-Part 1 and part 2 (full).pdf, slide 44

### The Lennard-Jones potential
- **Form of the potential:** V(r) = 4ε[(σ/r)¹² − (σ/r)⁶], where V(r) is the potential energy of interaction between two atoms. (Note: the earlier "before lecture" deck wrote this prefactor as 3ε; the full Part 1 and Part 2 deck and the Week 2 example problems both use 4ε.)
  > Source: F26-D2L-Chapter 2- Introduction to Engineering Materials-Part 1 and part 2 (full).pdf, slides 36–38; EXAMPLE PROBLEMS 1 - WEEK 2.docx, Problem 3
- **Repulsive term:** 4ε(σ/r)¹² represents the very strong short-range repulsive interaction; the r⁻¹² term increases very rapidly when atoms get close, so small r → repulsion dominates.
  > Source: F26-D2L-Chapter 2- Introduction to Engineering Materials-Part 1 and part 2 (full).pdf, slide 36
- **Attractive term:** −4ε(σ/r)⁶ represents the attractive interaction between the atoms; the negative sign means this contribution lowers the potential energy, so larger r → attraction dominates.
  > Source: F26-D2L-Chapter 2- Introduction to Engineering Materials-Part 1 and part 2 (full).pdf, slide 36
- **σ versus r₀:** σ is a characteristic distance — the separation at which the potential energy is zero, i.e. V(σ) = 0 — and it is the distance where the Lennard-Jones potential crosses zero. r₀ is the distance where the potential reaches its minimum. Therefore σ ≠ r₀; specifically r₀ = 2^(1/6)σ.
  > Source: F26-D2L-Chapter 2- Introduction to Engineering Materials-Part 1 and part 2 (full).pdf, slides 34, 37
- **ε is the bond energy / well depth:** ε is the depth of the potential-energy well and is the bond energy — the amount of energy required to separate two bonded atoms from their equilibrium spacing to an infinite distance. At equilibrium V(r₀) = −ε. A deeper potential well means more energy is required to separate the atoms, so a larger ε means a stronger interatomic interaction: a shallow well → weaker bonding, a deep well → stronger bonding. The higher the depth of the potential well (the more negative the potential energy), the stronger the bond.
  > Source: F26-D2L-Chapter 2- Introduction to Engineering Materials-Part 1 and part 2 (full).pdf, slides 34, 38
- **Derivation, step 1 — differentiate the potential:** rewrite as V(r) = 4ε[σ¹²r⁻¹² − σ⁶r⁻⁶] and apply the power rule d(rⁿ)/dr = n rⁿ⁻¹, giving dV/dr = 4ε[−12σ¹²/r¹³ + 6σ⁶/r⁷].
  > Source: F26-D2L-Chapter 2- Introduction to Engineering Materials-Part 1 and part 2 (full).pdf, slide 40
- **Derivation, step 2 — apply the equilibrium condition:** set the derivative to zero at r = r₀. Since ε is positive, 4ε ≠ 0 and both sides may be divided by it: 12σ¹²/r₀¹³ = 6σ⁶/r₀⁷. Multiplying by r₀¹³ gives 12σ¹² = 6σ⁶r₀⁶, so r₀⁶ = 2σ⁶ and, taking the positive sixth root because separation is positive, r₀ = ⁶√2 × σ ≈ 1.122σ.
  > Source: F26-D2L-Chapter 2- Introduction to Engineering Materials-Part 1 and part 2 (full).pdf, slide 41
- **Derivation, final step — minimum potential energy:** since r₀⁶ = 2σ⁶, (σ/r₀)⁶ = 1/2 and (σ/r₀)¹² = 1/4. Substituting, E(r₀) = 4ε[1/4 − 1/2] = 4ε[−1/4] = −ε. The well depth is +ε, while the energy at the minimum is −ε.
  > Source: F26-D2L-Chapter 2- Introduction to Engineering Materials-Part 1 and part 2 (full).pdf, slide 42
- **Which kind of equilibrium:** "equilibrium distance" here means mechanical equilibrium — not chemical equilibrium nor thermal equilibrium. Mechanical equilibrium is achieved when the force acting between the two atoms is zero.
  > Source: EXAMPLE PROBLEMS 1 - WEEK 2.docx, Problem 3
- **Why bond energy is quoted as a positive number:** the potential energy at the equilibrium distance must be negative, because positive work must be done to break the bond and liberate the two atoms. The work done against the interatomic force in taking the atoms from r₀ to infinity is a positive quantity, so bond energy is customarily stated as a positive number even though the potential energy at r₀ is negative. ε is therefore a positive quantity called the depth of the potential well, because V looks like a well when plotted against r.
  > Source: EXAMPLE PROBLEMS 1 - WEEK 2.docx, Problem 3
- **Model parameters:** σ and ε are called the (model) parameters of the Lennard-Jones potential energy, and the two parameters are determined by experiments for the material of the two interacting atoms.
  > Source: EXAMPLE PROBLEMS 1 - WEEK 2.docx, Problem 3

## Examples
- Determine the equilibrium interatomic distance and bond energy between two atoms under a Lennard-Jones potential energy: V(r) = 3ε[(σ/r)¹² − (σ/r)⁶], where r is interatomic distance.
  > Source: before lecture-Chapter 2 - Atomic Structure and Interatomic Bonding.pdf, slide 30
- **Example Problem 3 (worked) — Lennard-Jones equilibrium and bond energy:** for V(r) = 4ε[(σ/r)¹² − (σ/r)⁶], setting the interatomic force (the negative derivative of V) to zero gives r₀ = 2^(1/6)σ ≈ 1.122σ, so σ is proportional to the equilibrium interatomic distance. Substituting r₀ back into V gives the bond energy V(r₀) = −ε.
  > Source: F26-D2L-Chapter 2- Introduction to Engineering Materials-Part 1 and part 2 (full).pdf, slides 36–42; EXAMPLE PROBLEMS 1 - WEEK 2.docx, Problem 3
- **Example Problem 5 (worked) — force of attraction between ions:** calculate the force of attraction between a K⁺ and an O²⁻ ion whose centers are separated by 1.5 nm. The attractive force is the negative derivative with respect to interatomic separation of the attractive energy expression, with A = (1/4πε₀)(|Z₁|e)(|Z₂|e). Since the valences of K⁺ and O²⁻ are +1 and −2, Z₁ = 1 and Z₂ = 2, giving a magnitude of 2.05 × 10⁻¹⁰ N (the sign is removed because the force is known to be attractive and the magnitude is what is reported).
  > Source: F26-D2L-Chapter 2- Introduction to Engineering Materials-Part 1 and part 2 (full).pdf, slide 45; EXAMPLE PROBLEMS 1 - WEEK 2.docx, Problem 5
- Bonding energy and melting temperature data by bond type: Ionic — NaCl (640 kJ/mol, 801°C), LiF (850 kJ/mol, 848°C), MgO (1000 kJ/mol, 2800°C), CaF₂ (1548 kJ/mol, 1418°C). Covalent — Cl₂ (121 kJ/mol, −102°C), Si (450 kJ/mol, 1410°C), InSb (523 kJ/mol, 942°C), C diamond (713 kJ/mol, >3550°C), SiC (1230 kJ/mol, 2830°C). Metallic — Hg (62 kJ/mol, −39°C), Al (330 kJ/mol, 660°C), Ag (285 kJ/mol, 962°C), W (850 kJ/mol, 3414°C). van der Waals — Ar (7.7 kJ/mol, −189°C), Kr (11.7 kJ/mol, −158°C), CH₄ (18 kJ/mol, −182°C), Cl₂ (31 kJ/mol, −101°C).
  > Source: before lecture-Chapter 2 - Atomic Structure and Interatomic Bonding.pdf, slide 29

## Common Misconceptions
- σ and r₀ are not the same distance: σ is where the Lennard-Jones potential crosses zero (V(σ) = 0), while r₀ is where the potential reaches its minimum, with r₀ = 2^(1/6)σ.
  > Source: F26-D2L-Chapter 2- Introduction to Engineering Materials-Part 1 and part 2 (full).pdf, slides 34, 37
- The well depth and the energy at the minimum have opposite signs: the well depth is +ε while the energy at the minimum is −ε. Bond energy is quoted as a positive number because it equals the positive work required to break the bond.
  > Source: F26-D2L-Chapter 2- Introduction to Engineering Materials-Part 1 and part 2 (full).pdf, slide 42; EXAMPLE PROBLEMS 1 - WEEK 2.docx, Problem 3

## Related Topics
- [Interatomic Bonding Overview](interatomic-bonding-overview.md)
- [Ionic Bonding](ionic-bonding.md)
- [Covalent Bonding](covalent-bonding.md)
- [Metallic Bonding](metallic-bonding.md)
- [Secondary Bonding](secondary-bonding.md)
