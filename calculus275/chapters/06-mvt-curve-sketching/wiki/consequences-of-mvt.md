# Consequences and Applications of the MVT

## Definition
Suppose f is continuous on an interval I and differentiable on its interior. For any x < y in I, the MVT on [x, y] gives
f(y) − f(x) = f′(c)(y − x), for some c with x < c < y.
Continuity is required at any endpoints included in I; differentiability is required only in its interior.
> Source: MATH275-Week06-Lecture-Notes.pdf

## Key Concepts
- **Zero derivative ⟹ constant:** if f′ = 0 throughout the interior of I, then f is constant on I. Consequently, two functions continuous on I with the same derivative on its interior differ by a constant.
  > Source: MATH275-Week06-Lecture-Notes.pdf, Week of October 9 (Week 5).pdf
- **Sign of f′ ⟹ monotonicity:** if f′ > 0 throughout the interior of I, then f is strictly increasing on I (so if b > a then f(b) > f(a)); if f′ < 0, f is strictly decreasing (if b > a then f(b) < f(a)). The inequalities f′ ≥ 0 and f′ ≤ 0 imply nondecreasing and nonincreasing behaviour, respectively.
  > Source: MATH275-Week06-Lecture-Notes.pdf, Week of October 9 (Week 5).pdf
- **Derivative bound ⟹ change bound:** if |f′| ≤ M throughout the interior of I, where M ≥ 0, then |f(y) − f(x)| ≤ M|y − x| for all x, y ∈ I.
  > Source: MATH275-Week06-Lecture-Notes.pdf
- **The converse need not hold:** a strictly increasing function need not have f′ > 0 everywhere. f(x) = x³ is strictly increasing on ℝ although f′(0) = 0. So a zero derivative alone does not show that a function stops increasing or has a local extremum.
  > Source: MATH275-Week06-Lecture-Notes.pdf
- **The interval condition matters:** f(x) = 1/x has f′(x) < 0 on its domain, but the monotonicity conclusion applies separately on (−∞, 0) and (0, ∞). It is not decreasing on the whole disconnected domain: −1 < 1 yet f(−1) = −1 < f(1) = 1. The MVT cannot compare these values because f is undefined at 0, inside [−1, 1].
  > Source: MATH275-Week06-Lecture-Notes.pdf
- **Proving inequalities with an auxiliary function:** define F as the difference of the two sides, show F(0) = 0 and F′ > 0 for x > 0, then use the MVT on [0, x] to conclude F(x) > F(0) = 0.
  > Source: MATH275-Week06-Lecture-Notes.pdf
- **Repeated Rolle's theorem bounds roots:** if F has n distinct roots, Rolle's theorem between consecutive roots gives n − 1 distinct zeros of F′, and so on for higher derivatives.
  > Source: MATH275-Week06-Lecture-Notes.pdf

## Examples
- **Error bound for √t:** for x, y ≥ 4, the derivative of √t between them is at most 1/4, so the MVT gives |√y − √x| ≤ (1/4)|y − x|. In particular 0 < √4.04 − 2 ≤ 0.01.
  > Source: MATH275-Week06-Lecture-Notes.pdf
- **x/(1 + x²) < arctan x < x for x > 0:** arctan t is continuous on [0, x] and differentiable on (0, x). The MVT gives c ∈ (0, x) with arctan x − arctan 0 = x/(1 + c²). Since 0 < c < x, 1/(1 + x²) < 1/(1 + c²) < 1. Multiplying by x > 0 proves both strict inequalities.
  > Source: MATH275-Week06-Lecture-Notes.pdf
- **x − x²/2 < ln(1 + x) < x for x > 0:** let F(x) = x − ln(1 + x) for x ≥ 0. Then F(0) = 0 and F′(x) = x/(1 + x) > 0 for x > 0, so the MVT on [0, x] gives F(x) > F(0) = 0 (upper bound). For the lower bound let G(x) = ln(1 + x) − x + x²/2; G(0) = 0 and G′(x) = 1/(1 + x) − 1 + x = x²/(1 + x) > 0 for x > 0, so G(x) > 0.
  > Source: MATH275-Week06-Lecture-Notes.pdf
- **eˣ − Ax² − Bx − C = 0 has at most three distinct real roots:** set F(x) = eˣ − Ax² − Bx − C and suppose four distinct roots r₁ < r₂ < r₃ < r₄. F is smooth, so Rolle on each [rᵢ, rᵢ₊₁] gives three distinct zeros s₁ < s₂ < s₃ of F′. Rolle on F′ over [s₁, s₂] and [s₂, s₃] gives two distinct zeros t₁ < t₂ of F″. One more application gives a zero of F‴ in (t₁, t₂), contradicting F‴(x) = eˣ > 0 for every x.
  > Source: MATH275-Week06-Lecture-Notes.pdf
- **lim_{x→+∞} x²[ln(arctan(x + 1)) − ln(arctan x)] = 2/π:** for t > 0 let H(t) = ln(arctan t), with H′(t) = 1/[(1 + t²) arctan t]. For each x > 0 the MVT on [x, x + 1] gives cₓ ∈ (x, x + 1) with x²[H(x + 1) − H(x)] = (x²/(1 + cₓ²)) · (1/arctan cₓ). Since 1 < cₓ/x < 1 + 1/x, cₓ/x → 1 and cₓ → +∞. Hence x²/(1 + cₓ²) = 1/[x⁻² + (cₓ/x)²] → 1 while arctan cₓ → π/2. The limit is 2/π.
  > Source: MATH275-Week06-Lecture-Notes.pdf
- **Two applications of Rolle (interpolation error bound):** let a < b, f continuous on [a, b], twice differentiable on (a, b), f(a) = f(b) = 0. For each x ∈ (a, b) there is ξₓ ∈ (a, b) with f(x) = (f″(ξₓ)/2)(x − a)(x − b). Proof: fix x, set λ = 2f(x)/((x − a)(x − b)) and F(t) = f(t) − (λ/2)(t − a)(t − b). Then F(a) = F(x) = F(b) = 0. Rolle on [a, x] and [x, b] gives u, v with F′(u) = F′(v) = 0; Rolle on F′ over [u, v] gives ξₓ with 0 = F″(ξₓ) = f″(ξₓ) − λ. Consequence: if |f″(t)| ≤ M on (a, b), then |f(x)| ≤ (M/2)(x − a)(b − x) ≤ M(b − a)²/8 for every x ∈ [a, b], because (x − a)(b − x) = (b − a)²/4 − (x − (a + b)/2)². At the endpoints the bound follows from f(a) = f(b) = 0.
  > Source: MATH275-Week06-Lecture-Notes.pdf

## Common Misconceptions
- **"f′(c) = 0 means f stops increasing":** false; x³ is strictly increasing on ℝ with f′(0) = 0.
  > Source: MATH275-Week06-Lecture-Notes.pdf
- **"f′ < 0 on the domain means decreasing on the domain":** false for disconnected domains; 1/x is decreasing on each of (−∞, 0) and (0, ∞) separately, not on their union.
  > Source: MATH275-Week06-Lecture-Notes.pdf

## Related Topics
- [Rolle's Theorem and the Mean Value Theorem](rolle-and-mean-value-theorem.md)
- [Monotonicity and the First Derivative Test](monotonicity-and-first-derivative-test.md)
