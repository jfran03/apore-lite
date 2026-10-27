# Antiderivatives and Indefinite Integrals

## Definition
An **antiderivative** of f on an interval I is a function F satisfying F′(x) = f(x) for every x ∈ I. Integration reverses differentiation, so an antiderivative is verified by differentiating the answer.
> Source: MATH275-Week08-Lecture-Notes.pdf, Week of October 23.pdf

The **indefinite integral** notation is used when computing a family of antiderivatives:
∫ f(x) dx = F(x) + C, where F′(x) = f(x), C ∈ ℝ.
> Source: MATH275-Week08-Lecture-Notes.pdf, Week of October 23.pdf

## Key Concepts
- **Antiderivatives are not unique:** F(x) = (1/3)x³ + 12 and G(x) = (1/3)x³ − 2 are both antiderivatives of f(x) = x². If F is an antiderivative of f, then so is F + C for any constant C.
  > Source: Week of October 23.pdf
- **Why the constant is necessary (the family of all antiderivatives):** If F′ = G′ = f on an interval I, then (F − G)′(x) = F′(x) − G′(x) = f(x) − f(x) = 0 for all x ∈ I. A consequence of the Mean Value Theorem implies F − G is constant. Conclusion: if F is *any* antiderivative of f, the set of *all* antiderivatives of f is {F(x) + C | C ∈ ℝ}.
  > Source: MATH275-Week08-Lecture-Notes.pdf, Week of October 23.pdf
- **Linearity properties:** (i) ∫ c f(x) dx = c ∫ f(x) dx; (ii) ∫ [f(x) ± g(x)] dx = ∫ f(x) dx ± ∫ g(x) dx. When integrating a sum term by term, use one arbitrary constant for the whole sum.
  > Source: Week of October 23.pdf, MATH275-Week08-Lecture-Notes.pdf
- **Basic formulas** (each applies on an interval where the integrand is defined; for arbitrary real p, take x > 0 in the power formula unless another real domain is specified):

  | Integrand | One antiderivative |
  |-----------|--------------------|
  | x^p (p ≠ −1) | x^(p+1)/(p + 1) (reverse power rule) |
  | 1/x | ln \|x\| (recall (ln \|x\|)′ = 1/x for x ≠ 0) |
  | e^x ; a^x (a > 0, a ≠ 1) | e^x ; a^x / ln a |
  | cos x ; sin x | sin x ; −cos x |
  | sec² x ; sec x tan x | tan x ; sec x |
  | 1/(1 + x²) ; 1/√(1 − x²) | arctan x ; arcsin x |
  > Source: MATH275-Week08-Lecture-Notes.pdf, Week of October 23.pdf
- **Rewrite before integrating:** convert roots and quotients to powers (e.g. √x = x^(1/2), 4/x = 4x^(−1)) and integrate term by term.
  > Source: MATH275-Week08-Lecture-Notes.pdf
- **Reverse chain rule with a linear inner function:** for constants k ≠ 0 and b, differentiating F(kx + b) introduces a factor k. Consequently, if F′ = f, then ∫ f(kx + b) dx = (1/k) F(kx + b) + C. This recognition works when the inner derivative is constant; more general substitution methods are developed separately.
  > Source: MATH275-Week08-Lecture-Notes.pdf
- **Initial conditions:** an initial value (e.g. v(0), s(0)) fixes the arbitrary constant. With v′ = a and s′ = v, integrate once to get v (constant C₁ found from v(0)), then again to get s (constant C₂ found from s(0)).
  > Source: MATH275-Week08-Lecture-Notes.pdf

## Examples
- ∫ (x^(−3/2) + 3e^x) dx = ∫ x^(−3/2) dx + 3∫ e^x dx = x^(−3/2+1)/(−3/2 + 1) + 3e^x + C = −2x^(−1/2) + 3e^x + C.
  > Source: Week of October 23.pdf
- ∫ cos(x) dx = sin(x) + C; ∫ sec²(x) dx = tan(x) + C; ∫ (1/x) dx = ln |x| + C.
  > Source: Week of October 23.pdf
- For x > 0: ∫ (6√x − 4/x + 5e^x) dx = ∫ (6x^(1/2) − 4x^(−1) + 5e^x) dx = 6·x^(3/2)/(3/2) − 4 ln x + 5e^x + C = 4x^(3/2) − 4 ln x + 5e^x + C. Differentiating gives 6√x − 4/x + 5e^x, as required.
  > Source: MATH275-Week08-Lecture-Notes.pdf
- **Scaled inverse tangent:** ∫ dx/(9 + 4x²). Differentiate the suggested arctan: d/dx arctan(2x/3) = (2/3)/(1 + 4x²/9) = (2/3)/((9 + 4x²)/9) = 6/(9 + 4x²). Therefore the answer is (1/6) arctan(2x/3) + C on ℝ.
  > Source: MATH275-Week08-Lecture-Notes.pdf
- **Scaled inverse sine:** ∫ dx/√(25 − 9x²). On −5/3 < x < 5/3, d/dx arcsin(3x/5) = (3/5)/√(1 − 9x²/25) = (3/5)/(√(25 − 9x²)/5) = 3/√(25 − 9x²). Thus (1/3) arcsin(3x/5) + C is the required family on that interval.
  > Source: MATH275-Week08-Lecture-Notes.pdf
- **Position from acceleration:** a(t) = 6t − 4 for t ≥ 0, v(0) = 3, s(0) = 2. v(t) = ∫ (6t − 4) dt = 3t² − 4t + C₁; v(0) = 3 gives C₁ = 3. s(t) = ∫ (3t² − 4t + 3) dt = t³ − 2t² + 3t + C₂; s(0) = 2 gives C₂ = 2. So v(t) = 3t² − 4t + 3 and s(t) = t³ − 2t² + 3t + 2. Check: differentiating twice recovers s″(t) = 6t − 4, and both initial conditions hold.
  > Source: MATH275-Week08-Lecture-Notes.pdf

## Common Misconceptions
- An antiderivative is not unique; omitting + C gives only one member of the family, not the full indefinite integral.
  > Source: Week of October 23.pdf, MATH275-Week08-Lecture-Notes.pdf
- The reverse-chain-rule shortcut (1/k)F(kx + b) only works when the inner derivative is constant.
  > Source: MATH275-Week08-Lecture-Notes.pdf

## Related Topics
- [FTC Part I](ftc-part-1.md)
