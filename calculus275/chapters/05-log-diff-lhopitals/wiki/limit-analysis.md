# Limit Analysis with L'Hôpital (Proofs and Structure)

## Definition
The ANALYSIS-level exercises in the Week 5 notes use l'Hôpital's rule, local expansions, and the mean value theorem to prove general statements about limits of functions and their derivatives.
> Source: MATH275-Week05-Lecture-Notes.pdf

## Key Concepts
- **Symmetric second-difference quotient:** if f is twice differentiable at a, then lim_(h→0) [f(a + h) + f(a − h) − 2f(a)]/h² = f″(a). Proof: twice differentiability gives f(a ± h) = f(a) ± f′(a)h + ½ f″(a)h² + o(h²). Adding and subtracting 2f(a) cancels the constant and linear terms, leaving f″(a)h² + o(h²); divide by h².
  > Source: MATH275-Week05-Lecture-Notes.pdf
- **Recovering information about an unknown function:** given lim_(x→0)(sin(6x) − x f(x))/x³ = 0, find lim_(x→0)(6 − f(x))/x². Split: (6 − f(x))/x² = (6x − sin(6x))/x³ + (sin(6x) − x f(x))/x³. The second term → 0 by hypothesis. For the first, l'H twice: lim (6 − 6 cos(6x))/(3x²) = lim 36 sin(6x)/(6x) = 36. So the required limit is 36.
  > Source: MATH275-Week05-Lecture-Notes.pdf
- **A bounded function with a derivative limit:** if f is differentiable on [a, ∞), bounded there, and lim_(x→∞) f′(x) = A exists, then A = 0. If A > 0, then f′(x) > A/2 for all sufficiently large x, so the mean value theorem shows f eventually increases at least linearly, contradicting boundedness. If A < 0, apply the same argument to −f.
  > Source: MATH275-Week05-Lecture-Notes.pdf
- **Why the converse fails:** f(x) = sin(x²)/x for x > 0, f(0) = 0 is differentiable on [0, ∞) with f(x) → 0 (since |f(x)| ≤ 1/x), but f′(x) = 2 cos(x²) − sin(x²)/x² has no limit at +∞: along xₙ = √(2πn) it tends to 2, along yₙ = √((2n + 1)π) it tends to −2. Also f′(0) = 1.
  > Source: MATH275-Week05-Lecture-Notes.pdf
- **First-order asymptotic differential equation:** let f be differentiable on (0, ∞), a > 0, and lim_(x→∞)(a f(x) + f′(x)) = L. Then lim f(x) = L/a. Proof: put r(x) = a f(x) + f′(x) − L → 0; multiplying by e^(ax) and integrating from a fixed X > 0 gives f(x) = e^(−a(x−X)) f(X) + ∫_X^x e^(−a(x−t))(L + r(t)) dt. The constant part is (L/a)(1 − e^(−a(x−X))); given ε > 0, choose X with |r(t)| < aε for t ≥ X so the remaining integral is at most ε in absolute value.
  > Source: MATH275-Week05-Lecture-Notes.pdf
- **Second-order asymptotic differential equation:** if f ∈ C²((0, ∞)) and lim (f + f′ + f″) = L, then lim f = L. Set h = f + f′; then h + h′ = f + f′ + f″ → L, so (first-order result with a = 1) h → L; applying the same result again to f gives f → L.
  > Source: MATH275-Week05-Lecture-Notes.pdf
- **Optional extension, nth finite difference:** if f ∈ Cⁿ near a, then f⁽ⁿ⁾(a) = lim_(h→0) (1/hⁿ) Σ_(k=0)^n (−1)^(n−k) C(n,k) f(a + kh). Repeated l'Hôpital gives (1/n!) lim Σ (−1)^(n−k) C(n,k) kⁿ f⁽ⁿ⁾(a + kh). Intermediate numerators tend to 0 because Σ (−1)^(n−k) C(n,k) kʳ = 0 for 0 ≤ r < n, while the same sum equals n! when r = n; continuity of f⁽ⁿ⁾ finishes it.
  > Source: MATH275-Week05-Lecture-Notes.pdf

## Related Topics
- [L'Hôpital's Rule](lhopitals-rule.md)
