# Integration by Parts

## Definition
**Integration by parts** reverses the product rule. For continuously differentiable U, V,

∫ U dV = UV − ∫ V dU,  ∫ₐᵇ U V′ dx = [UV]ₐᵇ − ∫ₐᵇ V U′ dx.

> Source: MATH275-Week09-Lecture-Notes.pdf

## Key Concepts
- **Derivation ("inverting the product rule"):** The product rule says (f(x)g(x))′ = f′(x)g(x) + f(x)g′(x), so f(x)g(x) = ∫ f′(x)g(x) dx + ∫ f(x)g′(x) dx. Letting U = f(x), V = g(x), so that dU = f′(x) dx and dV = g′(x) dx, gives UV = ∫ V dU + ∫ U dV, rewritten as ∫ U dV = UV − ∫ V dU.
  > Source: Week of October 30.pdf, MATH275-Week09-Lecture-Notes.pdf
- **When it is effective:** for choices of U and V for which ∫ V dU is easier to compute. Choose U so that differentiation simplifies it (its derivative is easy to compute), and choose dV so that you can find V. Check the minus sign.
  > Source: Week of October 30.pdf, MATH275-Week09-Lecture-Notes.pdf
- **Typical choices:**
  - Polynomial times an exponential or trigonometric function: differentiating the polynomial lowers its degree.
  - A logarithm or an inverse trigonometric function: differentiating often removes the logarithm or inverse function.
  - Even a single function can be written as a product with 1 (e.g. ln x = 1·ln x, with dV = 1·dx).
  > Source: MATH275-Week09-Lecture-Notes.pdf, Week of October 30.pdf
- **V can be any antiderivative:** when finding V from dV, any antiderivative may be chosen (e.g. V = x for dV = 1·dx).
  > Source: Week of October 30.pdf
- **Definite version:** ∫ₐᵇ f(x)g′(x) dx = f(x)g(x)|ₓ₌ₐᵇ − ∫ₐᵇ g(x)f′(x) dx.
  > Source: Week of October 30.pdf

## Examples
- ∫ ln x dx: this does not look like a product, but it is: 1·ln x. Let U = ln x, dV = 1·dx, so dU = (1/x) dx, V = x. Then ∫ ln x dx = x ln x − ∫ x·(1/x) dx = x ln x − x + C. "Check this!"
  > Source: Week of October 30.pdf
- ∫ x eˣ dx: U = x, dV = eˣ dx, so dU = dx, V = eˣ. Then x eˣ − ∫ eˣ dx = x eˣ − eˣ + C.
  > Source: Week of October 30.pdf
- ∫ tan⁻¹x dx: U = tan⁻¹x, dV = dx, so dU = dx/(1 + x²), V = x. Then x tan⁻¹x − ∫ x/(1 + x²) dx. The remaining integral is a substitution: u = 1 + x², du/2 = x dx, giving x tan⁻¹x − (1/2)∫ du/u = x tan⁻¹x − (1/2) ln |u| + C = x tan⁻¹x − (1/2) ln(1 + x²) + C.
  > Source: Week of October 30.pdf
- ∫ x cos(3x) dx: U = x, dV = cos(3x) dx, so dU = dx, V = (1/3) sin(3x). Then x sin(3x)/3 − (1/3)∫ sin(3x) dx = x sin(3x)/3 + cos(3x)/9 + C. Differentiation cancels the extra sin(3x)/3 terms and returns x cos(3x).
  > Source: MATH275-Week09-Lecture-Notes.pdf
- ∫₁ᵉ x² ln x dx (definite): U = ln x, dV = x² dx, so dU = dx/x, V = x³/3. Then [x³ ln x / 3]₁ᵉ − (1/3)∫₁ᵉ x² dx = e³/3 − [x³/9]₁ᵉ = (2e³ + 1)/9. The boundary term at 1 is zero, but the lower-endpoint contribution from the second integral is 1/9.
  > Source: MATH275-Week09-Lecture-Notes.pdf
- ∫ₑ^{e²} x ln x dx (definite): U = ln x, dV = x dx, so dU = (1/x) dx, V = (1/2)x². Then (1/2)x² ln x |ₓ₌ₑ^{e²} − ∫ₑ^{e²} (1/2)x²·(1/x) dx = (1/2)e⁴·2 − (1/2)e²·1 − (1/2)∫ₑ^{e²} x dx = e⁴ − (1/2)e² − (1/2)[(1/2)x²]ₑ^{e²} = e⁴ − (1/2)e² − (1/4)e⁴ + (1/4)e² = (3/4)e⁴ − (1/4)e².
  > Source: Week of October 30.pdf

## Common Misconceptions
- **Dropping the minus sign or a lower-endpoint term:** check the minus sign; in definite problems, a boundary term can vanish at an endpoint while the second integral still contributes there (as in ∫₁ᵉ x² ln x dx).
  > Source: MATH275-Week09-Lecture-Notes.pdf

## Related Topics
- [Repeated and Cyclic Integration by Parts](repeated-cyclic-parts.md)
- [Combining Methods & Integral-Defined Functions](combining-methods.md)
- [Integration by Substitution (Indefinite)](substitution-rule.md)
