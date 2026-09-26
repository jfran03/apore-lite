# Inverse Trigonometric Derivatives

## Definition
The inverse trigonometric functions are obtained by restricting the original trigonometric functions to intervals on which they are one-to-one (radians are used). The three basic trig functions are not invertible: sin, cos and tan all fail the horizontal line test.
> Source: MATH275-Week04-Lecture-Notes.pdf, Week of September 25 (Week 3) .pdf

## Key Concepts
- **Principal ranges:** arcsin x ∈ [−π/2, π/2], arccos x ∈ [0, π], arctan x ∈ (−π/2, π/2).
  > Source: MATH275-Week04-Lecture-Notes.pdf
- **Restrictions used:** sin is invertible on [−π/2, π/2]; cos is restricted to [0, π]; tan is restricted to (−π/2, π/2).
  > Source: Week of September 25 (Week 3) .pdf
- **Domains and ranges:** dom(sin⁻¹) = [−1, 1], ran(sin⁻¹) = [−π/2, π/2]; dom(cos⁻¹) = [−1, 1], ran(cos⁻¹) = [0, π]; dom(tan⁻¹) = ℝ, ran(tan⁻¹) = (−π/2, π/2). Composition identities: sin⁻¹(sin x) = x for x ∈ [−π/2, π/2] and sin(sin⁻¹ x) = x for x ∈ [−1, 1] (similarly for cos on [0, π] and tan on (−π/2, π/2)).
  > Source: Week of September 25 (Week 3) .pdf
- **Remaining inverses via reciprocals (course convention):** arcsec x = arccos(1/x), arccsc x = arcsin(1/x), arccot x = arctan(1/x). This rests on the identity (1/f)⁻¹(x) = f⁻¹(1/x). Thus arcsec x ∈ [0, π] \ {π/2}, arccsc x ∈ [−π/2, 0) ∪ (0, π/2], arccot x ∈ (−π/2, 0) ∪ (0, π/2). arcsec and arccsc require |x| ≥ 1 (so that 1/x ∈ [−1, 1]); arccot requires x ≠ 0.
  > Source: MATH275-Week04-Lecture-Notes.pdf, Week of September 25 (Week 3) .pdf
- **Course-specific arccot branch:** the displayed arccot relation is used only for x ≠ 0 and differs from the common continuous convention whose range is (0, π).
  > Source: MATH275-Week04-Lecture-Notes.pdf
- **Derivatives:**
  - d/dx arcsin x = 1/√(1 − x²), |x| < 1
  - d/dx arccos x = −1/√(1 − x²), |x| < 1
  - d/dx arctan x = 1/(1 + x²), x ∈ ℝ
  - d/dx arccot x = −1/(1 + x²), x ≠ 0
  - d/dx arcsec x = 1/(|x|√(x² − 1)), |x| > 1
  - d/dx arccsc x = −1/(|x|√(x² − 1)), |x| > 1
  > Source: MATH275-Week04-Lecture-Notes.pdf, Week of September 25 (Week 3) .pdf
- **How arcsin's derivative arises:** since (sin x)' = cos x is non-zero on (−π/2, π/2), the inverse function theorem applies: (sin⁻¹ x)' = 1/cos(sin⁻¹ x) = 1/√(1 − x²), using cos(sin⁻¹ x) = √(1 − x²) (the handwritten notes record "cos x = sin x'" beside this step) for −1 < x < 1.
  > Source: Week of September 25 (Week 3) .pdf
- **Why the absolute value in arcsec/arccsc:** √(1 − 1/x²) = √(x² − 1)/|x| because √(x²) = |x|. The absolute value is a sign issue, not decoration.
  > Source: MATH275-Week04-Lecture-Notes.pdf
- **Domain of a function vs. domain of its derivative:** arcsec and arccsc are defined for |x| ≥ 1 but their derivatives are finite only for |x| > 1; likewise arcsin and arccos are defined at x = ±1 but their derivatives are not finite there.
  > Source: MATH275-Week04-Lecture-Notes.pdf
- **Chain rule form:** for an inner function u(x), d/dx arctan(u) = u'/(1 + u²), d/dx arccos(u) = −u'/√(1 − u²), and similarly for the others.
  > Source: MATH275-Week04-Lecture-Notes.pdf

## Examples
- **(csc⁻¹ x)' via the chain rule:** csc⁻¹ x = sin⁻¹(1/x), so the derivative is [1/√(1 − 1/x²)]·(−1/x²) = −1/√(x⁴(1 − 1/x²)) = −1/√(x²(x² − 1)) = −1/(|x|√(x² − 1)) for x > 1 or x < −1.
  > Source: Week of September 25 (Week 3) .pdf
- **h(x) = arctan(√(1 + x²)):** with u = √(1 + x²), u' = x/√(1 + x²), so h'(x) = u'/(1 + u²) = x / ((x² + 2)√(1 + x²)). Since 1 + x² > 0, the square root is differentiable for every real x and arctan accepts every real input, so h' is defined on all of ℝ.
  > Source: MATH275-Week04-Lecture-Notes.pdf
- **Principal-range values:** arccos(−1/2) = 2π/3 (angle in [0, π] with cosine −1/2; reference angle π/3, Quadrant II) and arctan(−√3) = −π/3 (angle in (−π/2, π/2) with tangent −√3). The principal ranges make both answers unique.
  > Source: MATH275-Week04-Lecture-Notes.pdf
- **y = arccos(2x − 1):** with u = 2x − 1, u' = 2, y' = −2/√(1 − (2x − 1)²). The function is defined for 0 ≤ x ≤ 1, but the derivative is finite only for 0 < x < 1.
  > Source: MATH275-Week04-Lecture-Notes.pdf

## Common Misconceptions
- **sin⁻¹ x is not 1/sin x:** sin⁻¹ x = arcsin x, while 1/sin x = csc x.
  > Source: MATH275-Week04-Lecture-Notes.pdf

## Related Topics
- [Derivative of an Inverse Function](inverse-function-derivative.md)
- [Inverse Hyperbolic Functions](inverse-hyperbolic-functions.md)
- [Choosing a Differentiation Strategy](choosing-a-differentiation-strategy.md)
