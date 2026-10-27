# Indeterminate Powers (0⁰, 1^∞, ∞⁰)

## Definition
The power forms below are handled by the same logarithmic conversion:

- **0⁰:** lim F(x) = 0 and lim G(x) = 0 (G ln F is 0 · ∞ type)
- **1^∞:** lim F(x) = 1 and lim |G(x)| = ∞ (G ln F is ∞ · 0 type)
- **∞⁰:** lim F(x) = ∞ and lim G(x) = 0 (G ln F is 0 · ∞ type)

In each case lim_(x→a) [F(x)]^G(x) = exp( lim_(x→a) G(x) ln F(x) ). Here F(x) > 0 is required near the limiting input. If lim G(x) ln F(x) = L ∈ ℝ ∪ {±∞}, then lim [F(x)]^G(x) = e^L, with e^(−∞) = 0 and e^(+∞) = +∞.
> Source: MATH275-Week05-Lecture-Notes.pdf

## Key Concepts
- **Not a ratio, so take the log:** a power such as (sin x)^(x²) is not a ratio. Trick: take the log of the limit, turn the result into a ratio, apply l'Hôpital, then exponentiate to retrieve the original.
  > Source: Week of October 2 (Week 4).pdf
- **The definition of e as a limit:** lim_(x→∞)(1 + 1/x)ˣ = e; one can define e as this limit.
  > Source: Week of October 2 (Week 4).pdf

## Examples
- **lim_(x→0⁺)(sin x)^(x²) (0⁰):** ln (sin x)^(x²) = x² ln sin x, form 0 × (−∞) as x → 0⁺. Write as ln sin x/(1/x²) (form −∞/∞). l'H: lim (cos x/sin x)/(−2/x³) = lim x³ cos x/(−2 sin x) (form 0/0). l'H again: lim (3x² cos x − x³ sin x)/(−2 cos x) = (0 − 0)/1 = 0. Thus lim (sin x)^(x²) = e⁰ = 1.
  > Source: Week of October 2 (Week 4).pdf
- **lim_(x→0⁺)(sin x)ˣ (0⁰ from the right):** for small x > 0, set yₓ = (sin x)ˣ > 0. ln yₓ = x ln(sin x) = ln(sin x)/(1/x); numerator → −∞, denominator → +∞, an ∞/∞ form. l'H: lim cot x/(−1/x²) = lim −x² cos x/sin x = 0, using x/sin x → 1. Thus the limit is 1.
  > Source: MATH275-Week05-Lecture-Notes.pdf
- **lim_(x→∞) x^(1/x) (∞⁰):** take the limit of the log: lim ln x^(1/x) = lim ln x/x (∞/∞) = (l'H) lim (1/x)/1 = 0. Answer: e⁰ = 1.
  > Source: Week of October 2 (Week 4).pdf
- **The nth root of n:** lim_(n→∞) n^(1/n). First consider the positive real variable x: ln x/x has form ∞/∞, and l'H gives lim (1/x)/1 = 0. Thus x^(1/x) = e^((ln x)/x) → e⁰ = 1. Restricting to positive integers gives lim n^(1/n) = 1.
  > Source: MATH275-Week05-Lecture-Notes.pdf
- **(ln x)^(1/x) as x → ∞ (∞⁰):** ln[(ln x)^(1/x)] = ln(ln x)/x → 0 by l'Hôpital's rule (the derivative quotient is 1/(x ln x)). Thus (ln x)^(1/x) → 1.
  > Source: MATH275-Week05-Lecture-Notes.pdf
- **lim_(x→∞)(1 + 1/x)ˣ (1^∞):** take the log: lim x ln(1 + 1/x), form ∞ × 0. Create a ratio: ln(1 + 1/x)/(1/x), form 0/0. l'H: [1/(1 + 1/x) · (−1/x²)]/(−1/x²) = 1/(1 + 1/x) → 1/(1 + 0) = 1. Exponentiate: the limit is e¹ = e.
  > Source: Week of October 2 (Week 4).pdf
- **A 1^∞ limit, (1 + 4/x²)ˣ as x → ∞:** ln yₓ = x ln(1 + 4/x²) = ln(1 + 4/x²)/(1/x), form 0/0. Differentiating gives lim [(−8/x³)/(1 + 4/x²)]/(−1/x²) = lim 8/(x(1 + 4/x²)) = 0. Hence the limit is e⁰ = 1.
  > Source: MATH275-Week05-Lecture-Notes.pdf
- **A refined 1^∞ limit:** lim_(x→0⁺) (e/(1 + x)^(1/x))^(1/x). The base is positive. ln yₓ = (1 − ln(1 + x)/x)/x = (x − ln(1 + x))/x², form 0/0. One application gives lim (1 − 1/(1 + x))/(2x) = lim 1/(2(1 + x)) = 1/2. Therefore the limit is e^(1/2).
  > Source: MATH275-Week05-Lecture-Notes.pdf

## Common Misconceptions
- **Forgetting to exponentiate:** the l'Hôpital computation gives the limit of the logarithm, L; the requested limit is e^L.
  > Source: MATH275-Week05-Lecture-Notes.pdf, Week of October 2 (Week 4).pdf

## Related Topics
- [Logarithmic Differentiation](logarithmic-differentiation.md)
- [Variable Powers](variable-powers.md)
- [Products and Differences (0·∞, ∞−∞)](products-and-differences.md)
- [L'Hôpital's Rule](lhopitals-rule.md)
