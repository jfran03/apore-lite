# Relative Change and Percentage Error

## Definition
The signed change Δy records the change in the output's units; its magnitude is |Δy|. Relative
change compares the signed change with the original output:

    relative change = Δy/y ≈ dy/y,      percentage change ≈ 100(dy/y) %.

Here y = f(x) ≠ 0 is the original output.
> Source: MATH275-Week03-Lecture-Notes.pdf

## Key Concepts
- **The ratios are unitless.** The ratios have no units because numerator and denominator have
  the same units.
  > Source: MATH275-Week03-Lecture-Notes.pdf
- **Converting between ratio and percentage.** To enter a percentage in a formula, divide by 100;
  to report a ratio as a percentage, multiply by 100 and append %.
  > Source: MATH275-Week03-Lecture-Notes.pdf
  > Source: Week 2 Video - Linear Approximation and Differentials .pdf
- **Power-law rule.** For a power law y = Cx^n with C ≠ 0 and x > 0 (so any real exponent n is
  allowed), dy = Cnx^(n−1) dx and dy/y = Cnx^(n−1)dx / (Cx^n) = n(dx/x). The constant C cancels
  and x^(n−1)/x^n = x^(−1). Thus the exponent multiplies the approximate relative change; a
  negative exponent reverses its sign.
  > Source: MATH275-Week03-Lecture-Notes.pdf
- **Keep the sign, units, and reference value visible.** A percentage change divides by the
  original output, not by the change. For a positive original output, a negative percentage
  change means a decrease. An unsigned relative error uses |Δy|/|y| ≈ |dy|/|y|. Write dx in the
  same units as x before applying a differential formula.
  > Source: MATH275-Week03-Lecture-Notes.pdf
- **First-order estimate, not a maximum-error bound.** The relative-error result is a first-order
  estimate, not a rigorous maximum-error bound.
  > Source: MATH275-Week03-Lecture-Notes.pdf

## Examples
- **PRACTICE — propagation of measurement error in a wire.** The resistance of a cylindrical wire
  of fixed length is R(r) = K/r², where K > 0 is constant. Suppose the measured radius is 1.5%
  too large. Let r be the true radius, dr the measured radius minus the true radius, and
  R = Kr^(−2) the true resistance. Then dR/R = −2(dr/r). Here dr/r = 1.5/100 = 0.015, not 1.5,
  and the measured radius is r + dr = 1.015r. The exact output error is ΔR = R(r + dr) − R(r),
  estimated using dR: ΔR/R ≈ dR/R = −2(0.015) = −0.03. Since 100(−0.03) = −3, the computed
  resistance is approximately 3% too small. Its unsigned relative error is estimated by
  |ΔR|/R ≈ |dR|/R = 0.03.
  > Source: MATH275-Week03-Lecture-Notes.pdf
- **Relative error in the surface area of a cubic box.** A cubic box is constructed. If the error
  in the length measurement is at most 1%, estimate the resulting error in the surface area. The
  surface area is A = 6ℓ², so A'(ℓ) = 12ℓ. We want the ratio ΔA/A (this gives a proportion;
  multiply by 100 to get %). Then ΔA/A ≈ dA/A = A'(ℓ)dℓ/A = 12ℓ dℓ / (6ℓ²) = 2(dℓ/ℓ). We are
  given dℓ/ℓ = ±0.01 (1% variation; it is fine to leave this as 0.01). Thus
  ΔA/A ≈ 2(dℓ/ℓ) = ±0.02, i.e. a 2% range.
  > Source: Week 2 Video - Linear Approximation and Differentials .pdf

## Common Misconceptions
- **Entering the percentage figure instead of the ratio.** In the wire example, dr/r = 1.5/100
  = 0.015, not 1.5.
  > Source: MATH275-Week03-Lecture-Notes.pdf
- **Dividing by the change instead of the original output.** A percentage change divides by the
  original output, not by the change.
  > Source: MATH275-Week03-Lecture-Notes.pdf

## Related Topics
- [Differentials and Exact Changes](differentials-and-exact-changes.md)
- [Applied Differential Problems](applied-differential-problems.md)
