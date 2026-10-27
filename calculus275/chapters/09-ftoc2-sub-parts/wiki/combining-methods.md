# Combining Methods & Integral-Defined Functions

## Definition
Choose a method for the integral currently in front of you. A substitution can expose a product suitable for integration by parts; a trigonometric identity can turn the remaining integral into the original one.
> Source: MATH275-Week09-Lecture-Notes.pdf

FTC Part I constructs an antiderivative of every continuous function, including functions whose antiderivatives have no elementary formula. Substitution and integration by parts still apply to these accumulation functions.
> Source: MATH275-Week09-Lecture-Notes.pdf

## Key Concepts
- **Substitution then parts:** a substitution may turn the integrand into a product (e.g. u eᵘ) that integration by parts handles.
  > Source: MATH275-Week09-Lecture-Notes.pdf
- **Parts then substitution:** integration by parts can leave an integral that needs a substitution (e.g. ∫ tan⁻¹x dx leaves ∫ x/(1 + x²) dx).
  > Source: Week of October 30.pdf
- **Integral-defined functions in answers:** a function like S(x) = ∫₀ˣ cos(t²) dt can appear as part of an answer; its derivative comes from FTC Part I and its value at the lower limit is 0.
  > Source: MATH275-Week09-Lecture-Notes.pdf

## Examples
- ∫₀^{√(ln 2)} x³ e^(x²) dx (substitute first, then integrate by parts): u = x², du = 2x dx, x³ dx = (1/2)u du; the limits become 0 and ln 2. So the integral is (1/2)∫₀^{ln 2} u eᵘ du. With U = u, dV = eᵘ du: (1/2)[(u − 1)eᵘ]₀^{ln 2} = (1/2)[2(ln 2 − 1) − (−1)] = (1/2)(2 ln 2 − 1) = ln 2 − 1/2.
  > Source: MATH275-Week09-Lecture-Notes.pdf
- **Accumulation function S(x) = ∫₀ˣ cos(t²) dt, x ∈ ℝ:**
  - (a) The integrand is continuous, so FTC Part I gives S′(x) = cos(x²), and S(0) = 0.
  - (b) For x ≥ 1, H(x) = ∫₁^{x²} (cos t / √t) dt: use t = u² with u ≥ 1, so dt = 2u du and √t = u. Since x ≥ 1, the upper limit becomes u = x, giving H(x) = 2∫₁ˣ cos(u²) du = 2(S(x) − S(1)).
  - (c) K(x) = ∫₀ˣ S(t) dt: integrate by parts with U = S(t), dV = dt, so dU = cos(t²) dt, V = t. Then K(x) = [t S(t)]₀ˣ − ∫₀ˣ t cos(t²) dt. In the remaining integral put u = t², du = 2t dt: ∫₀ˣ t cos(t²) dt = (1/2)∫₀^{x²} cos u du = (1/2) sin(x²). Therefore K(x) = x S(x) − (1/2) sin(x²) for every real x. Check: differentiating gives S(x) + x cos(x²) − x cos(x²) = S(x), and its value at 0 is 0.
  > Source: MATH275-Week09-Lecture-Notes.pdf

## Related Topics
- [The Fundamental Theorem of Calculus, Part II](ftoc-part-2.md)
- [Substitution in Definite Integrals](definite-substitution.md)
- [Integration by Parts](integration-by-parts.md)
- [Repeated and Cyclic Integration by Parts](repeated-cyclic-parts.md)
