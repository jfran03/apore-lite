# Continuity

## Definition

We say `f` is **continuous at `x = a`** if

$$\lim_{x \to a} f(x) = f(a)$$
> Source: limits.pdf

We say `f` is **continuous on an interval `I`** if $\lim_{x \to a} f(x) = f(a)$ for every $a \in I$.
> Source: limits.pdf

The source notes `I` could be any of: `(c,d)`, `(c,d]`, `[c,d)`, `[c,d]`, `(c,∞)`, `[c,∞)`, `(-∞,d)`, `(-∞,d]`, `ℝ`.
> Source: limits.pdf

## Key Concepts

- **Continuity at a point is a three-part condition packed into one equation.** For $\lim_{x\to a} f(x) = f(a)$ to hold, the limit must exist, `f(a)` must be defined, and the two must be equal.
  > Source: limits.pdf

- **Graphical characterization:** `f` is continuous on `I` if the graph above `I` is a **single component**.
  > Source: limits.pdf

- **Defined ≠ continuous.** The source shows two graphs over the same interval `I`: one where the curve is a single unbroken piece ("f is continuous on I"), and one where the curve jumps ("f is defined on I but not continuous").
  > Source: limits.pdf

- **Standard continuous families.** All polynomials, rational functions, roots of `x`, trig, inverse trig, exp and log are continuous **on intervals within their domains**.
  > Source: limits.pdf

- **The qualifier "within their domains" matters.** These functions are not continuous everywhere on `ℝ` — they are continuous on each interval where they are defined, which is why the examples below list *several* intervals rather than one.
  > Source: limits.pdf

## Examples

- **(i)** $f(x) = \dfrac{1}{x}$ is continuous on $(-\infty, 0)$ and $(0, \infty)$.
  > Source: limits.pdf

- **(ii)** $g(x) = \dfrac{x^2}{(x-1)(x-2)}$ is continuous on $(-\infty, 1)$, $(1,2)$ and $(2,\infty)$.

  The intervals break exactly at the zeros of the denominator.
  > Source: limits.pdf

## Added from MATH275-Week01-Lecture-Notes.pdf

- **The three conditions, written out separately.** `f` is continuous at `a` when:
  1. `f(a)` is defined,
  2. $\lim_{x\to a} f(x)$ exists,
  3. $\lim_{x\to a} f(x) = f(a)$.

  This source states explicitly what `limits.pdf` compresses into the single equation $\lim_{x\to a} f(x) = f(a)$.
  > Source: MATH275-Week01-Lecture-Notes.pdf

- **Piecewise functions: check the junctions.** "For a piecewise continuous function, possible discontinuities occur at junctions; check the two one-sided limits and the assigned function value there."
  > Source: MATH275-Week01-Lecture-Notes.pdf

- **Domain language matters.** A function such as $1/x$ is continuous **on its domain** $\mathbb{R}\setminus\{0\}$. It is **not meaningful** to say that it is continuous at `0`, because `0` is not in its domain.

  This sharpens the `limits.pdf` phrasing "continuous on intervals within their domains": the question "is `f` continuous at `a`?" is only well-posed when `a` is in the domain.
  > Source: MATH275-Week01-Lecture-Notes.pdf

- **`CORE` — Repair a piecewise function.** Find `c` so that
  $$f(x) = \begin{cases} x^2 - 1, & x < 1 \\ cx + 1, & x \geq 1 \end{cases}$$
  is continuous at `x = 1`.

  Continuity requires $\lim_{x\to 1^-} f(x) = f(1)$, i.e. $0 = c + 1$, so $c = -1$.

  Note which quantities are matched: the left-hand limit (from the $x<1$ branch, giving $1^2 - 1 = 0$) against the assigned value `f(1)` (from the $x \geq 1$ branch, giving $c+1$).
  > Source: MATH275-Week01-Lecture-Notes.pdf

- **Takeaway on the role of continuity.** "Continuity allows limit information to pass through a function, and the IVT converts continuity plus endpoint data into an existence guarantee."
  > Source: MATH275-Week01-Lecture-Notes.pdf

## Related Topics

- [The Notion of a Limit](notion-of-a-limit.md)
- [One-Sided Limits](one-sided-limits.md)
- [Computing Finite Limits](computing-finite-limits.md)
- [The Intermediate Value Theorem](intermediate-value-theorem.md)
- [Infinite Limits and Vertical Asymptotes](infinite-limits.md)
