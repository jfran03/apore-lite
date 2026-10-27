# Choosing a Useful Substitution

## Definition
A substitution should remove a composition or simplify the algebra. For exponentials, try u = e^(kx) when the remaining exponential powers can be expressed in u. For trigonometric products, first expose the derivative of the chosen sine or cosine.
> Source: MATH275-Week09-Lecture-Notes.pdf

## Key Concepts
- **Trigonometric powers sinᵐx cosⁿx:**
  - An odd power of cosine lets you save one factor cos x dx, use u = sin x, and rewrite the remaining even powers by cos²x = 1 − sin²x.
  - An odd power of sine similarly suggests saving sin x dx, using u = cos x, and rewriting with sin²x = 1 − cos²x.
  - Even powers may require the half-angle identities sin²x = (1 − cos 2x)/2 and cos²x = (1 + cos 2x)/2.
  > Source: MATH275-Week09-Lecture-Notes.pdf
- **The "natural" choice may not be the best:** for ∫ e^(3x)/(1 + e^(2x)) dx, the natural choice u = 1 + e^(2x) (du/2 = e^(2x) dx) leaves e^(3x) dx/(1 + e^(2x)) = eˣ du/(2u) with eˣ = √(u − 1), giving √(u − 1)/(2u) du, which still leaves an integral requiring more techniques.
  > Source: Week of October 30.pdf
- **Divide before integrating:** when the substitution produces a rational function whose numerator is not of lower degree, rewrite it first, e.g. u²/(1 + u²) = (1 + u² − 1)/(1 + u²) = 1 − 1/(1 + u²), or u/(u + 4) = 1 − 4/(u + 4).
  > Source: Week of October 30.pdf, MATH275-Week09-Lecture-Notes.pdf

## Examples
- ∫ e^(3x)/(1 + e^(2x)) dx: instead try u = eˣ, du = eˣ dx. Then e^(3x) dx = e^(2x)·eˣ dx = u² du, so the integral is ∫ u²/(1 + u²) du = ∫ (1 − 1/(1 + u²)) du = u − tan⁻¹(u) + C = eˣ − tan⁻¹(eˣ) + C.
  > Source: Week of October 30.pdf
- ∫ sin⁴x cos³x dx (save one cosine factor): write cos³x = (1 − sin²x) cos x. Set u = sin x, du = cos x dx. Then ∫ u⁴(1 − u²) du = sin⁵x/5 − sin⁷x/7 + C. Check: differentiating gives sin⁴x cos x (1 − sin²x) = sin⁴x cos³x.
  > Source: MATH275-Week09-Lecture-Notes.pdf
- ∫ e^(4x)/(4 + e^(2x)) dx (exponentials become a rational function): u = e^(2x), du = 2e^(2x) dx, e^(4x) dx = (1/2)u du. Then (1/2)∫ u/(u + 4) du = (1/2)∫ (1 − 4/(u + 4)) du = (1/2)(u − 4 ln(u + 4)) + C = (1/2)e^(2x) − 2 ln(4 + e^(2x)) + C. The logarithm's argument is positive. Check: the derivative simplifies to e^(2x) − 4e^(2x)/(4 + e^(2x)) = e^(4x)/(4 + e^(2x)).
  > Source: MATH275-Week09-Lecture-Notes.pdf

## Related Topics
- [Integration by Substitution (Indefinite)](substitution-rule.md)
- [Combining Methods & Integral-Defined Functions](combining-methods.md)
