# Variable Limits and the Chain Rule

## Definition
Let H(u) = ∫꜀ᵘ f(t) dt. Since H′ = f, the chain rule gives d/dx H(g(x)) = f(g(x)) g′(x). For two moving endpoints, write the integral as H(v(x)) − H(u(x)).
> Source: MATH275-Week08-Lecture-Notes.pdf

**Both limits depending on x:** if f is continuous on an interval containing the limits and u, v are differentiable, then
d/dx ∫_{u(x)}^{v(x)} f(t) dt = f(v(x)) v′(x) − f(u(x)) u′(x).
> Source: MATH275-Week08-Lecture-Notes.pdf

## Key Concepts
- **Order of terms:** use the upper-limit term first and subtract the lower-limit term. The formula applies even when the limits cross. The integrand depends only on t.
  > Source: MATH275-Week08-Lecture-Notes.pdf
- **Composite upper limit requires FTC I plus the chain rule:** write G(x) = F(g(x)) where F(x) = ∫ₐˣ f(t) dt, then G′(x) = F′(g(x)) g′(x).
  > Source: Week of October 23.pdf
- **Moving lower limit:** reverse the limits to put the variable on top, introducing a minus sign.
  > Source: MATH275-Week08-Lecture-Notes.pdf

## Examples
- G(x) = ∫₂^{x³} e^t sec(t) dt. For F(x) = ∫₂ˣ e^t sec(t) dt, FTC I gives F′(x) = e^x sec x. Since G(x) = F(x³), the chain rule gives G′(x) = F′(x³)(x³)′ = e^{x³} sec(x³)·3x².
  > Source: Week of October 23.pdf
- B(x) = ∫_{1−x²}^{e^x} √(1 + t⁶) dt. The integrand is continuous on ℝ and both limits are differentiable. Upper limit contributes √(1 + (e^x)⁶)·e^x; lower limit contributes √(1 + (1 − x²)⁶)·(−2x), which must be subtracted. So B′(x) = e^x √(1 + e^{6x}) + 2x √(1 + (1 − x²)⁶). The plus sign in the second term comes from subtracting the derivative −2x of the lower limit.
  > Source: MATH275-Week08-Lecture-Notes.pdf
- For x > 0, C(x) = ∫_{ln x}^{2} e^{t²} dt. Reversing the limits: C(x) = −∫₂^{ln x} e^{t²} dt. FTC I and the chain rule give C′(x) = −e^{(ln x)²}/x. Differentiating −x⁻¹ e^{(ln x)²} with the product and chain rules: C″(x) = x⁻² e^{(ln x)²} − x⁻¹ e^{(ln x)²}·(2 ln x)/x = (e^{(ln x)²}/x²)(1 − 2 ln x).
  > Source: MATH275-Week08-Lecture-Notes.pdf

## Common Misconceptions
- Forgetting the factor v′(x) (or u′(x)) from the chain rule when a limit is a function of x.
  > Source: Week of October 23.pdf, MATH275-Week08-Lecture-Notes.pdf
- Sign errors on the lower-limit term: it is subtracted, so a negative u′(x) produces a plus sign.
  > Source: MATH275-Week08-Lecture-Notes.pdf

## Related Topics
- [FTC Part I](ftc-part-1.md)
