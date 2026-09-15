# Applied Differential Problems

## Definition
A dependable modelling workflow is:
1. define the input and output, with units;
2. write the function relating them;
3. identify the current input and the small input change;
4. compute dy = f'(x)dx;
5. interpret the sign and units, then decide whether an absolute or percentage change is asked.
> Source: MATH275-Week03-Lecture-Notes.pdf

## Key Concepts
- **When differentials are useful.** The method is valuable when f(x) and f'(x) are simple at the
  chosen base point while the nearby exact value is difficult. If the differential still contains
  a value that is just as hard to compute as the original expression, the approximation may offer
  little practical benefit.
  > Source: MATH275-Week03-Lecture-Notes.pdf
- **Units must be made consistent before substituting.** Write dx in the same units as x before
  applying a differential formula.
  > Source: MATH275-Week03-Lecture-Notes.pdf

## Examples
- **PRACTICE — a geometric change with a constraint.** A taut, straight cable has a fixed vertical
  rise of 3 m and horizontal span x m. The rise and span are perpendicular, so the Pythagorean
  theorem gives ℓ² = x² + 3². Taking the positive square root, its length in metres is
  ℓ(x) = √(x² + 9). When the span is 4 m, the horizontal span increases by 0.02 m while the
  vertical rise stays fixed. Here x = 4, dx = 0.02 m, and
  ℓ'(x) = (1/2)(x² + 9)^(−1/2)(2x) = x/√(x² + 9), so ℓ'(4) = 4/5. Hence
  Δℓ ≈ dℓ = (4/5)(0.02) = 0.016 m. The factor 2x comes from the chain rule; the derivative of the
  fixed 9 is zero. Since 1 m is 100 cm, 0.016 m is 1.6 cm. The original length is ℓ(4) = 5 m, so
  the new length is approximately 5.016 m. The exact change is √((4.02)² + 9) − 5 metres, but the
  differential is easier to evaluate.
  > Source: MATH275-Week03-Lecture-Notes.pdf
- **Approximate increase in the volume of a sphere.** Determine the approximate increase in volume
  if the radius of a sphere is increased from 50 m to 51 m. Here Δr = 1 m and r = 50 m, and
  V(r) = (4/3)πr³. We know ΔV ≈ dV = V'(r)Δr = 4πr²Δr = 4π(50)²·1 = 10000π m³.
  > Source: Week 2 Video - Linear Approximation and Differentials .pdf
- **Estimating a rate of change in an applied setting.** For S(t) = 80/(t + 4), the change in S as
  t goes from 6 to 6.05 is estimated by ΔS ≈ dS = S'(6)(0.05) = −0.04, where the negative sign
  says the output decreases.
  > Source: MATH275-Week03-Lecture-Notes.pdf

## Related Topics
- [Differentials and Exact Changes](differentials-and-exact-changes.md)
- [Relative Change and Percentage Error](relative-change-and-percentage-error.md)
- [Choosing the Expansion Point](choosing-the-expansion-point.md)
