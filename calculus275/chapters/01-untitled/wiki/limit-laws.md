# Limit Laws

## Definition

Suppose $\lim_{x \to a} f(x) = L$ and $\lim_{x \to a} g(x) = M$. Then:

**(i)** $\displaystyle\lim_{x \to a} f(x) \pm g(x) = \lim_{x \to a} f(x) \pm \lim_{x \to a} g(x) = L \pm M$

**(ii)** $\displaystyle\lim_{x \to a} f(x)\,g(x) = LM$

**(iii)** $\displaystyle\lim_{x \to a} \frac{f(x)}{g(x)} = \frac{L}{M}$ — provided $M \neq 0$ **and** $g(x) \neq 0$ for all `x` "close" to `a`.
> Source: limits.pdf

## Key Concepts

- **The hypothesis is that both limits already exist.** The laws are stated as "Suppose $\lim f(x) = L$ and $\lim g(x) = M$" — they are conditional on both limits existing before the law can be applied.
  > Source: limits.pdf

- **The quotient law carries two separate conditions**, not one: `M ≠ 0` *and* `g(x) ≠ 0` for all `x` close to `a`. The source writes both explicitly.
  > Source: limits.pdf

- **Constants.** For $c \in \mathbb{R}$: $\displaystyle\lim_{x \to a} c = c$ and $\displaystyle\lim_{x \to a} c f(x) = cL$.
  > Source: limits.pdf

- **Integer powers.** $\displaystyle\lim_{x \to a} f(x)^n = L^n$ for $n \in \mathbb{Z}$, where the source notes $\mathbb{Z} = \{\ldots, -3, -2, -1, 0, 1, 2, \ldots\}$ — provided $L \neq 0$ for $n < 0$.
  > Source: limits.pdf

## Examples

- **Applying the laws by direct evaluation.**
  $$\lim_{x \to 2} \frac{x^3 - \sin\left(\frac{\pi x}{2}\right)}{x \cos\left(\frac{\pi x^2}{4}\right)} = \frac{2^3 - \sin(\pi)}{2 \cdot \cos(\pi)} = \frac{8 - 0}{-2} = -4$$
  > Source: limits.pdf

## Added from MATH275-Week01-Lecture-Notes.pdf

- **Compact statement.** If $\lim f(x) = L$ and $\lim g(x) = M$ **for the same limiting process**, then
  $$\lim (cf + g) = cL + M, \qquad \lim (fg) = LM, \qquad \lim \frac{f}{g} = \frac{L}{M} \quad (M \neq 0)$$
  > Source: MATH275-Week01-Lecture-Notes.pdf

- **"For the same limiting process"** is this source's way of saying the laws apply uniformly — the same statements hold for two-sided limits, one-sided limits, and limits at infinity, provided both limits are taken in the same sense.
  > Source: MATH275-Week01-Lecture-Notes.pdf

- **This source states only $M \neq 0$ on the quotient law**, whereas `limits.pdf` states both $M \neq 0$ *and* $g(x) \neq 0$ for `x` close to `a`. The `limits.pdf` version is the stricter one.
  > Source: MATH275-Week01-Lecture-Notes.pdf; limits.pdf

- **Use the laws only after naming the obstruction.** The Week 1 notes place the laws immediately after the instruction "When direct substitution produces an indeterminate form, name the obstruction before doing algebra" — see [Computing Finite Limits](computing-finite-limits.md).
  > Source: MATH275-Week01-Lecture-Notes.pdf

## Related Topics

- [The Notion of a Limit](notion-of-a-limit.md)
- [Computing Finite Limits](computing-finite-limits.md)
- [Limits at Infinity and Horizontal Asymptotes](limits-at-infinity.md)
- [Continuity](continuity.md)
