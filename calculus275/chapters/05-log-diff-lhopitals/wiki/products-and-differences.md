# Products and Differences (0·∞, ∞−∞)

## Definition
Before applying l'Hôpital's rule, convert these forms to a quotient:

- **0 · ∞:** if lim_(x→a) f(x) = 0 and |g(x)| → ∞, then f(x)g(x) = f(x)/(1/g(x)) = g(x)/(1/f(x)).
- **∞ − ∞:** if f(x) → +∞ and g(x) → +∞, then f(x) − g(x) = (1/g(x) − 1/f(x)) / (1/(f(x)g(x))).
> Source: MATH275-Week05-Lecture-Notes.pdf

## Key Concepts
- **Choosing the quotient for a product:** choose the quotient that is simpler to differentiate.
  > Source: MATH275-Week05-Lecture-Notes.pdf
- **Choosing the method for a difference:** combining fractions, factoring, or rationalizing may be simpler than the reciprocal identity. In every case, check that the resulting quotient has form 0/0 or ∞/∞ before using the rule.
  > Source: MATH275-Week05-Lecture-Notes.pdf
- **A bad choice of ratio:** for x² ln sin x as x → 0⁺, the ratio x²/(1/ln sin x) is 0/0 and l'Hôpital can be used, but 1/ln sin x has a bad derivative. The ratio ln sin x/(1/x²) (form −∞/∞) is the better choice.
  > Source: Week of October 2 (Week 4).pdf
- **Not every ∞ − ∞ needs l'Hôpital:** lim_(x→∞)(x³ − x²) is ∞ − ∞, but factoring gives x²(x − 1), and ∞ × ∞ = ∞, so the limit is ∞. No need for l'H.
  > Source: Week of October 2 (Week 4).pdf

## Examples
- **lim_(x→0⁺) x ln x (0 × (−∞)):** write as a ratio ln x/(1/x) (form −∞/∞). l'H: lim (1/x)/(−1/x²) = lim (−x) = 0.
  > Source: Week of October 2 (Week 4).pdf
- **A product tending to a finite number:** as x → 0⁺, x ln(1/x) has form 0 · ∞. Write x ln(1/x) = ln(1/x)/(1/x). Both → +∞, so lim = lim (−1/x)/(−1/x²) = lim x = 0.
  > Source: MATH275-Week05-Lecture-Notes.pdf
- **A product of type 0 · ∞ at π:** lim_(x→π)(x − π) cot x. Write as (x − π)/tan x, which is 0/0. Since (tan x)′ = sec² x, l'H gives lim 1/sec² x = 1.
  > Source: MATH275-Week05-Lecture-Notes.pdf
- **A difference of two unbounded terms:** lim_(x→∞)(√(x² + 3x) − x) has form ∞ − ∞. Rationalization gives 3x/(√(x² + 3x) + x) = 3/(√(1 + 3/x) + 1) → 3/2. This algebraic step settles the limit without l'Hôpital's rule.
  > Source: MATH275-Week05-Lecture-Notes.pdf
- **A difference hidden inside reciprocals:** lim_(x→0)(1/sin x − 1/x). Combine first: (x − sin x)/(x sin x), which is 0/0. Two applications give lim (1 − cos x)/(sin x + x cos x) = lim sin x/(2 cos x − x sin x) = 0.
  > Source: MATH275-Week05-Lecture-Notes.pdf

## Related Topics
- [Indeterminate Forms](indeterminate-forms.md)
- [L'Hôpital's Rule](lhopitals-rule.md)
- [Indeterminate Powers](indeterminate-powers.md)
