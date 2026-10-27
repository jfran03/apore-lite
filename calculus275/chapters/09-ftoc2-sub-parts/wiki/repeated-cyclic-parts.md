# Repeated and Cyclic Integration by Parts

## Definition
A second use of integration by parts can either simplify the remaining integral further or bring back the original integral. In the latter case, collect the original integral on one side and solve for it.
> Source: MATH275-Week09-Lecture-Notes.pdf

## Key Concepts
- **Repeated (reducing):** each application lowers something, e.g. the power of a logarithm, until the remaining integral is elementary.
  > Source: MATH275-Week09-Lecture-Notes.pdf
- **Cyclic (returning):** after two applications the original integral reappears. Adding it to both sides and dividing solves for it. Constants may be temporarily suppressed and restored at the end.
  > Source: MATH275-Week09-Lecture-Notes.pdf, Week of October 30.pdf
- **Consistency in the cyclic case:** for e^(2x) sin(3x), in each step integrate the exponential and differentiate the trigonometric factor.
  > Source: MATH275-Week09-Lecture-Notes.pdf

## Examples
- ∫ x (ln x)² dx for x > 0 (reduce the power of a logarithm): U = (ln x)², dV = x dx, so dU = 2 ln x dx / x, V = x²/2. Then ∫ x (ln x)² dx = (x²/2)(ln x)² − ∫ x ln x dx. For the remaining integral, U = ln x, dV = x dx: ∫ x ln x dx = (x²/2) ln x − (1/2)∫ x dx = (x²/2) ln x − x²/4 + C. Combining: (x²/2)(ln x)² − (x²/2) ln x + x²/4 + C.
  > Source: MATH275-Week09-Lecture-Notes.pdf
- ∫ e^(2x) sin(3x) dx (integral returns after two applications): write I = ∫ e^(2x) sin(3x) dx and J = ∫ e^(2x) cos(3x) dx. Integrating the exponential and differentiating the trig factor: I = (1/2)e^(2x) sin(3x) − (3/2)J and J = (1/2)e^(2x) cos(3x) + (3/2)I. Substituting: I = (1/2)e^(2x) sin(3x) − (3/4)e^(2x) cos(3x) − (9/4)I, so (13/4)I = (1/2)e^(2x) sin(3x) − (3/4)e^(2x) cos(3x), and ∫ e^(2x) sin(3x) dx = (e^(2x)/13)(2 sin(3x) − 3 cos(3x)) + C. Check: in the derivative, the coefficient of cos(3x) is −6 + 6 = 0 and that of sin(3x) is 4 + 9 = 13.
  > Source: MATH275-Week09-Lecture-Notes.pdf
- ∫₁ᵉ sin(ln x) dx (definite, cyclic): U = sin(ln x), dV = 1·dx, dU = cos(ln x)·(1/x) dx, V = x. Then x sin(ln x)|₁ᵉ − ∫₁ᵉ cos(ln x) dx. By parts again with U = cos(ln x), dU = −sin(ln x)·(1/x) dx, V = x: = e sin(1) − 1·sin(0) − [x cos(ln x)|₁ᵉ + ∫₁ᵉ sin(ln x) dx] = e sin 1 − e cos 1 + 1 − ∫₁ᵉ sin(ln x) dx. Adding the integral to both sides and dividing by 2 gives ∫₁ᵉ sin(ln x) dx = (1/2)[e sin 1 − e cos 1 + 1].
  > Source: Week of October 30.pdf
- ∫ csc³x dx on an interval containing no zero of sin x: first, (csc x − cot x)′ = −csc x cot x + csc²x = csc x (csc x − cot x), so ∫ csc x dx = ln |csc x − cot x| + C. (The expression inside the absolute value never vanishes where it is defined, since (csc x − cot x)(csc x + cot x) = 1.) For I = ∫ csc³x dx, let U = csc x, dV = csc²x dx, so dU = −csc x cot x dx, V = −cot x. Suppressing constants: I = −csc x cot x − ∫ csc x cot²x dx = −csc x cot x − ∫ csc x (csc²x − 1) dx = −csc x cot x − I + ln |csc x − cot x|. Therefore ∫ csc³x dx = −(1/2) csc x cot x + (1/2) ln |csc x − cot x| + C. Here a trigonometric identity turns the remaining integral into the original one.
  > Source: MATH275-Week09-Lecture-Notes.pdf

## Related Topics
- [Integration by Parts](integration-by-parts.md)
- [Combining Methods & Integral-Defined Functions](combining-methods.md)
