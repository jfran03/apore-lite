# The Squeeze Theorem

## Definition

**Theorem (Squeeze).** Suppose $f(x) \leq g(x) \leq h(x)$ for all `x` near `a`, and that

$$\lim_{x \to a} f(x) = \lim_{x \to a} h(x) = L$$

Then $\lim_{x \to a} g(x)$ **exists** and is also equal to `L`.
> Source: limits.pdf

## Key Concepts

- **The theorem delivers existence, not just a value.** The source's phrasing is "Then $\lim_{x\to a} g(x)$ **exists** and is also equal to L" — you are not assuming the middle limit exists in order to compute it; the squeeze proves it does.
  > Source: limits.pdf

- **The inequality only has to hold near `a`**, not everywhere — "for all x near a."
  > Source: limits.pdf

- **The two outer limits must be equal.** Both `f` and `h` must approach the *same* `L`.
  > Source: limits.pdf

- **Remark — the squeeze theorem also holds for one-sided limits, limits at infinity, and infinite limits.**
  > Source: limits.pdf

- **Standard starting inequality:** $-1 \leq \sin(\theta) \leq 1$ for any `θ`. Both worked examples begin here.
  > Source: limits.pdf

## Examples

- **Compute $\lim_{x \to 0} x^2 \sin\left(e^{\frac{1}{x}}\right)$.**

  Begin with a basic inequality: $-1 \leq \sin(\theta) \leq 1$ for any `θ`, i.e. $-1 \leq \sin\left(e^{\frac{1}{x}}\right) \leq 1$.

  Multiply by `x²` to convert to an inequality concerning the original function. Since $x^2 \geq 0$, this implies:

  $$-x^2 \leq x^2 \sin\left(e^{\frac{1}{x}}\right) \leq x^2$$

  Both outer bounds `→ 0` as `x → 0`. By the squeeze theorem, $\lim_{x \to 0} x^2 \sin\left(e^{\frac{1}{x}}\right) = 0$.

  Note the source explicitly justifies multiplying through by `x²` on the grounds that `x² ≥ 0` — the direction of the inequality is preserved.
  > Source: limits.pdf

- **Squeeze applied at infinity.** $\displaystyle\lim_{x \to \infty} \frac{x^2 + \sin(e^x)}{2x^2+1}$

  Since $-1 \leq \sin(e^x) \leq 1$, we have

  $$\frac{x^2 - 1}{2x^2+1} \leq \frac{x^2 + \sin(e^x)}{2x^2+1} \leq \frac{x^2+1}{2x^2+1}$$

  Both outer expressions tend to $\frac{1}{2}$, so the middle tends to $\frac{1}{2}$ **by squeeze**.
  > Source: limits.pdf

## Added from MATH275-Week01-Lecture-Notes.pdf

- **Statement (Week 1 form).** If $g(x) \leq f(x) \leq h(x)$ near `a` and both outer functions approach `L`, then $f(x) \to L$.

  Note this source puts the *middle* function under the name `f`, whereas `limits.pdf` names the middle function `g`. Same theorem, different letters.
  > Source: MATH275-Week01-Lecture-Notes.pdf

- **When it is the right tool.** "The theorem is most useful when the middle expression oscillates but its amplitude shrinks." The Week 1 obstruction table lists "bounded oscillation → look for a squeeze."
  > Source: MATH275-Week01-Lecture-Notes.pdf

- **`CORE` — Bound the part you cannot simplify.** Show that $\lim_{x\to 0} x^2\cos\left(\frac{3}{x}\right) = 0$.

  Since $-1 \leq \cos(3/x) \leq 1$ and $x^2 \geq 0$,
  $$-x^2 \leq x^2\cos\left(\frac{3}{x}\right) \leq x^2$$
  Both outer functions tend to 0, so the squeeze theorem gives the result.

  Structurally identical to the $x^2\sin(e^{1/x})$ example from `limits.pdf`: bound the unsimplifiable oscillating factor, multiply by the non-negative amplitude, squeeze.
  > Source: MATH275-Week01-Lecture-Notes.pdf

## Related Topics

- [Limits That Do Not Exist](limits-that-do-not-exist.md)
- [Computing Finite Limits](computing-finite-limits.md)
- [Limits at Infinity and Horizontal Asymptotes](limits-at-infinity.md)
- [Limit Laws](limit-laws.md)
