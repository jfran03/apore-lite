# Choosing an Approach & Combining Methods

## Definition
Partial fractions apply to rational functions in whichever variable you are using. A substitution can turn an integral involving exponentials into a rational integral.
> Source: MATH275-Week10-Lecture-Notes.pdf

## Key Concepts
- **Strategy guide:**
  - A quadratic radical suggests completing the square, then a sine, tangent, or secant substitution. A simpler u-substitution may suffice if the derivative of the expression under the radical appears.
  - A rational function suggests division if necessary, real factorization, and partial fractions. For an irreducible quadratic factor q(x), use a numerator of the form Px + Q over each power of q(x).
  - A repeated quadratic may require another method after decomposition, such as a trigonometric substitution or integration by parts.
  - Check the proposed antiderivative by differentiation, and check the sign and size of a definite integral when possible.
  > Source: MATH275-Week10-Lecture-Notes.pdf

## Examples
- **∫ dx/(eˣ + 2):** let u = eˣ > 0; then dx = du/u. The integral is ∫ du/(u(u + 2)) = (1/2)∫ (1/u − 1/(u + 2)) du. Returning to x: x/2 − (1/2) ln(eˣ + 2) + C. Differentiation yields 1/2 − eˣ/(2(eˣ + 2)) = 1/(eˣ + 2).
  > Source: MATH275-Week10-Lecture-Notes.pdf
- **∫ x²/(x⁴ + 4) dx:** the difference of squares gives x⁴ + 4 = (x² + 2)² − (2x)² = (x² − 2x + 2)(x² + 2x + 2), both irreducible over ℝ. Clearing denominators gives x²/(x⁴ + 4) = (1/4)(x/(x² − 2x + 2) − x/(x² + 2x + 2)). Write x = (1/2)(2x − 2) + 1 in the first fraction and x = (1/2)(2x + 2) − 1 in the second. Since x² ∓ 2x + 2 = (x ∓ 1)² + 1:
  - ∫ x dx/(x² − 2x + 2) = (1/2) ln(x² − 2x + 2) + arctan(x − 1) + C₁
  - ∫ x dx/(x² + 2x + 2) = (1/2) ln(x² + 2x + 2) − arctan(x + 1) + C₂
  - One quarter of their difference: (1/8) ln((x² − 2x + 2)/(x² + 2x + 2)) + (1/4)(arctan(x − 1) + arctan(x + 1)) + C.
  - Both quadratic factors are positive, and the result holds on all of ℝ.
  > Source: MATH275-Week10-Lecture-Notes.pdf
- **Radical where u-substitution suffices:** in ∫ (2x + 5)/√(9 − (x − 1)²) dx, the part 2∫ u du/√(9 − u²) is done with v = 9 − u², while 7∫ du/√(9 − u²) needs the sine substitution. See [Completing the Square](completing-the-square.md).
  > Source: MATH275-Week10-Lecture-Notes.pdf

## Related Topics
- [Trigonometric (Inverse) Substitution](trig-substitution.md)
- [Partial Fraction Decomposition: Setup](partial-fractions-setup.md)
- [Irreducible Quadratic Factors](irreducible-quadratic-factors.md)
- [Completing the Square](completing-the-square.md)
