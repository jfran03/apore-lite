# Limits at Infinity (Horizontal Asymptotes)

## Definition

We say $\lim_{x \to \infty} f(x) = L$ if `f(x)` can be made arbitrarily close to `L` for **sufficiently large input**.
> Source: limits.pdf

We say $\lim_{x \to -\infty} f(x) = L$ if `f(x)` can be made arbitrarily close to `L` for **sufficiently large negative input**.
> Source: limits.pdf

## Key Concepts

- **Reciprocal power property.** $\displaystyle\lim_{x \to \pm\infty} \frac{1}{x^n} = 0$ for `n > 0`.
  > Source: limits.pdf

- **Formal technique for ratios:** divide numerator and denominator by the **highest order term in the denominator**.
  > Source: limits.pdf

- **"Short" technique:** drop the lower order terms.
  > Source: limits.pdf

- **Growth hierarchy.** Exponential growth `>>>>` polynomial growth `>>>>` logarithmic growth.
  > Source: limits.pdf

- **A function can have two different horizontal asymptotes**, one in each direction — the arctan example below has `y = π/2` and `y = -π/2`.
  > Source: limits.pdf

## Examples

- **Two horizontal asymptotes.**
  $$\lim_{x \to \infty} \arctan(x) = \frac{\pi}{2}, \qquad \lim_{x \to -\infty} \arctan(x) = -\frac{\pi}{2}$$
  The source concludes: "f has horizontal asymptotes at $y = \pm\frac{\pi}{2}$."
  > Source: limits.pdf

- **(i) Ratio of diverging quantities — both techniques.** $\displaystyle\lim_{x \to \infty} \frac{3x^2 - x}{-2x^2 + 4}$

  The source circles the `-x` and `+4` terms and annotates "these don't really matter."

  *Formal:*
  $$\lim_{x \to \infty} \frac{3x^2 - x}{-2x^2+4} \cdot \frac{\frac{1}{x^2}}{\frac{1}{x^2}} = \lim_{x \to \infty} \frac{3 - \frac{1}{x}}{-2 + \frac{4}{x^2}} = \frac{3-0}{-2+0} = -\frac{3}{2}$$

  *Short:*
  $$\lim_{x \to \infty} \frac{3x^2-x}{-2x^2+4} = \lim_{x \to \infty} \frac{3x^2}{-2x^2} = -\frac{3}{2}$$
  > Source: limits.pdf

- **(ii) Identifying the dominant term.** $\displaystyle\lim_{x \to -\infty} \frac{3x^3 + x^2\sqrt{3-x} + 2}{-x^2+1}$

  The source circles $x^2\sqrt{3-x}$ and notes it "behaves like $x^{2.5}$, which is dominated by $x^3$ for large negative x."

  $$= \lim_{x \to -\infty} \frac{3x^3}{-x^2} = \lim_{x \to -\infty} -3x = \infty$$

  (the source marks `x → -∞` beneath the `x`, giving a positive product).
  > Source: limits.pdf

- **(iii) Growth hierarchy in action.** $\displaystyle\lim_{x \to \infty} \frac{2^x + \ln(x^4 + x^2)}{(1.5)^x + x^3 - x^2}$

  The source annotates $\ln(x^4+x^2) \approx \ln(x^4) = 4\ln x \lll 2^x$, so:

  $$= \lim_{x \to \infty} \frac{2^x}{(1.5)^x} = \lim_{x \to \infty} \left(\frac{2}{1.5}\right)^x = \lim_{x \to \infty} \left(\frac{4}{3}\right)^x = \infty$$
  > Source: limits.pdf

## Added from MATH275-Week01-Lecture-Notes.pdf

- **The sign checkpoint for radicals.** $\sqrt{x^2} = |x|$, with $|x| = x$ as $x \to +\infty$ and $|x| = -x$ as $x \to -\infty$. This is the step that most often flips a sign silently.
  > Source: MATH275-Week01-Lecture-Notes.pdf

- **Why dividing by `x` can silently flip an answer.** At negative infinity,
  $$\frac{\sqrt{x^2-4x+7}}{x} = \frac{|x|}{x}\sqrt{1 - \frac{4}{x} + \frac{7}{x^2}} \longrightarrow -1$$
  **not** $+1$. The source flags this explicitly as a trap.
  > Source: MATH275-Week01-Lecture-Notes.pdf

- **`STUDIO` — Radical cancellation at negative infinity.** Evaluate $\lim_{x\to-\infty}\left(\sqrt{x^2-4x+7} + x\right)$.

  The source's instruction: "Before writing algebra: predict the sign of the expression and identify the cancellation. Then rationalize and divide by $-x = |x|$."

  Rationalizing first and using $|x| = -x$ as $x \to -\infty$:
  $$\sqrt{x^2-4x+7} + x = \frac{-4x+7}{\sqrt{x^2-4x+7} - x} = \frac{4 - 7/x}{\sqrt{1 - 4/x + 7/x^2} + 1} \longrightarrow \frac{4}{2} = 2$$
  > Source: MATH275-Week01-Lecture-Notes.pdf

- **Horizontal asymptote by division.** For $f(x) = \frac{2x+1}{x-3}$, $\lim_{x\to\pm\infty} f(x) = \lim_{x\to\pm\infty}\frac{2+1/x}{1-3/x} = 2$ — the same divide-by-the-highest-order-term technique recorded above from `limits.pdf`.
  > Source: MATH275-Week01-Lecture-Notes.pdf

## Related Topics

- [Infinite Limits and Vertical Asymptotes](infinite-limits.md)
- [Computing Finite Limits](computing-finite-limits.md)
- [Limit Laws](limit-laws.md)
- [The Squeeze Theorem](squeeze-theorem.md)
