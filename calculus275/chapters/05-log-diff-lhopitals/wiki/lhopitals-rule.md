# L'Hôpital's Rule

## Definition
**Theorem (formal statement).** Let I be an open interval. Let a be a finite endpoint of I, or let a = +∞ (respectively, a = −∞) when I is unbounded above (respectively, below). Let f and g be differentiable on I, and suppose that g(x) ≠ 0 and g′(x) ≠ 0 for every x ∈ I. Assume that, as x → a through points of I, one of the following holds:

f(x) → 0 and g(x) → 0, or |f(x)| → ∞ and |g(x)| → ∞.

If the limit lim_(x→a) f′(x)/g′(x) = L exists in ℝ ∪ {±∞}, then lim_(x→a) f(x)/g(x) = L.

For a two-sided limit at a finite interior point, choose a left-hand and a right-hand interval and apply the theorem separately on each side.
> Source: MATH275-Week05-Lecture-Notes.pdf

**Theorem (informal statement).** Suppose f and g are differentiable near x = a and lim_(x→a) f(x)/g(x) is of the form 0/0 or ±∞/∞. If lim_(x→a) f′(x)/g′(x) = L exists, then so does the original limit and lim_(x→a) f(x)/g(x) = L. This is also true for one-sided limits and a = ±∞.
> Source: Week of October 2 (Week 4).pdf

## Key Concepts
- **Why it works:** the ratio of growth rates determines the eventual ratio of the underlying quantities.
  > Source: Week of October 2 (Week 4).pdf
- **Verify the form first:** only after verifying an indeterminate quotient form (0/0 or ∞/∞) may we consider l'Hôpital's rule.
  > Source: MATH275-Week05-Lecture-Notes.pdf
- **Existence of the derivative-quotient limit is a hypothesis:** if lim f′(x)/g′(x) does not exist, l'Hôpital's rule gives no conclusion and cannot be used directly to evaluate lim f(x)/g(x). The original quotient limit may still exist; use algebra, a comparison, a known limit, or another argument instead.
  > Source: MATH275-Week05-Lecture-Notes.pdf
- **Repeated application:** after each differentiation, recheck the form before applying the rule again. Some limits need two or three applications.
  > Source: MATH275-Week05-Lecture-Notes.pdf
- **Powers dominate logarithms:** for α > 0 and k ∈ ℕ, lim_(x→∞) x^α/(ln x)ᵏ = +∞. Proof: show the reciprocal tends to 0; applying l'Hôpital's rule k times (each stage ∞/∞) gives lim (ln x)ᵏ/x^α = lim k!/(αᵏ x^α) = 0.
  > Source: MATH275-Week05-Lecture-Notes.pdf
- **ln x grows very slowly:** y = ln x → ∞ as x → ∞, but grows very slowly.
  > Source: Week of October 2 (Week 4).pdf

## Examples
- **lim_(x→0) x²/tan x (0/0):** l'H gives lim 2x/sec² x = 0/1 = 0.
  > Source: Week of October 2 (Week 4).pdf
- **lim_(x→∞) (2x² − 1)/(3x² + x + 2) (∞/∞):** l'H gives lim 4x/(6x + 1), still ∞/∞; l'H again gives lim 4/6 = 2/3.
  > Source: Week of October 2 (Week 4).pdf
- **A quotient that needs two applications:** for x → 0, (e^(2x) − 1 − 2x)/x² has form 0/0. After one differentiation the quotient 2(e^(2x) − 1)/(2x) still has form 0/0. A second application gives lim 4e^(2x)/2 = 2.
  > Source: MATH275-Week05-Lecture-Notes.pdf
- **A second-order 0/0 limit:** lim_(x→0) (ln(1 + x) − x)/x². Both tend to zero. For x near 0 with x ≠ 0, x > −1 and 2x ≠ 0. One application followed by algebra: (1/(1 + x) − 1)/(2x) = −1/(2(1 + x)) → −1/2.
  > Source: MATH275-Week05-Lecture-Notes.pdf
- **Growth at infinity:** lim_(x→∞) ln x/√x. Both → +∞; the denominator derivative is nonzero for x > 0, so l'H gives lim (1/x)/(1/(2√x)) = lim 2/√x = 0.
  > Source: MATH275-Week05-Lecture-Notes.pdf
- **Comparing two logarithmic growth rates:** lim_(x→∞) ln(1 + x²)/ln(1 + x). Both → +∞; the denominator derivative 1/(1 + x) is nonzero for x > 0, so l'H gives lim [2x/(1 + x²)]/[1/(1 + x)] = lim 2x(1 + x)/(1 + x²) = 2.
  > Source: MATH275-Week05-Lecture-Notes.pdf
- **A third-order 0/0 quotient:** lim_(x→0) (x − sin x)/x³ = lim (1 − cos x)/(3x²) = lim sin x/(6x) = lim cos x/6 = 1/6 (three justified applications).
  > Source: MATH275-Week05-Lecture-Notes.pdf
- **An existing limit without usable l'Hôpital data:** lim_(x→0⁺) x sin(1/x). Since −x ≤ x sin(1/x) ≤ x for x > 0, the squeeze theorem gives the limit 0. But writing it as x² sin(1/x)/x and differentiating produces (2x sin(1/x) − cos(1/x))/1, which has no limit as x → 0⁺. The original limit exists, but the derivative-quotient hypothesis fails, so l'Hôpital's rule gives no conclusion.
  > Source: MATH275-Week05-Lecture-Notes.pdf

## Common Misconceptions
- **"If f′/g′ has no limit, then f/g has no limit":** false. When lim f′/g′ fails to exist, the rule simply gives no conclusion; the original limit may still exist (e.g. x sin(1/x) → 0 as x → 0⁺).
  > Source: MATH275-Week05-Lecture-Notes.pdf
- **Using l'Hôpital without checking the form:** the form must be 0/0 or ∞/∞; a quotient tending to (3)/(0⁺) is not indeterminate.
  > Source: MATH275-Week05-Lecture-Notes.pdf

## Related Topics
- [Indeterminate Forms](indeterminate-forms.md)
- [Products and Differences (0·∞, ∞−∞)](products-and-differences.md)
- [Indeterminate Powers](indeterminate-powers.md)
- [Limit Analysis with L'Hôpital](limit-analysis.md)
