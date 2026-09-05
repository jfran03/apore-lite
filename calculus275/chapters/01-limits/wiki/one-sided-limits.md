# One-Sided Limits

## Definition

**Right-hand limit.** We say $\lim_{x \to a^+} f(x) = L$ if `f(x)` can be made arbitrarily close to `L` by moving `x` towards `a` **from the right** (i.e. `x > a`).
> Source: limits.pdf

**Left-hand limit.** We say $\lim_{x \to a^-} f(x) = L$ if `f(x)` can be made arbitrarily close to `L` by moving `x` towards `a` **from the left** (i.e. `x < a`).
> Source: limits.pdf

## Key Concepts

- **Remark (i):** If no such `L` exists in any of the above, we say the limit **does not exist**.
  > Source: limits.pdf

- **Remark (ii):** $\lim_{x \to a} f(x) = L$ occurs **if and only if** both one-sided limits exist and equal `L`.
  > Source: limits.pdf

- **Two-sided existence requires agreement:** the two-sided limit is not just "the value it approaches" — the left and right limits must both exist *and* be the same number.
  > Source: limits.pdf

## Examples

- **A jump where the two-sided limit fails.** The source's diagram shows a function with a jump at `x = a`:
  - $\lim_{x \to a^+} f(x) = f(a)$
  - $\lim_{x \to a^-} f(x) = L$

  Since $f(a) \neq L$, the source concludes $\lim_{x \to a} f(x)$ **DNE**.

  Note the structure of this example: the right-hand limit happens to equal the function's value at `a` (the filled point), the left-hand limit approaches a different height `L` (the open circle), and the mismatch is what kills the two-sided limit.
  > Source: limits.pdf

## Added from MATH275-Week01-Lecture-Notes.pdf

- **Existence criterion, restated.** A two-sided limit exists exactly when
  $$\lim_{x \to a^-} f(x) = \lim_{x \to a^+} f(x) = L$$
  > Source: MATH275-Week01-Lecture-Notes.pdf

- **The three independent pieces of information.** The statement $\lim_{x\to a} f(x) = L$ describes the values of `f(x)` when `x` is near `a`. The value `f(a)` may equal `L`, may be different from `L`, or may not be defined.
  > Source: MATH275-Week01-Lecture-Notes.pdf

- **Fast diagnostic.** "If the left- and right-hand limits disagree, the two-sided limit does not exist. The isolated value `f(a)` cannot repair that disagreement."
  > Source: MATH275-Week01-Lecture-Notes.pdf

- **`In class` exercise — one graph separating three pieces of information.** Sketch a function satisfying
  $$\lim_{x \to 1^-} f(x) = 2, \qquad \lim_{x \to 1^+} f(x) = -1, \qquad f(1) = 3$$
  Then mark open and closed circles and state whether $\lim_{x\to 1} f(x)$ exists.

  (The source leaves the axes blank for live work. By the fast diagnostic above, the left and right limits disagree, so the two-sided limit does not exist.)
  > Source: MATH275-Week01-Lecture-Notes.pdf

- **Absolute value makes a problem one-sided.** The worked conjugate example in [Computing Finite Limits](computing-finite-limits.md) is a case where $|x|$ in the denominator forces separate left and right analysis, yielding $-1$ and $1$.
  > Source: MATH275-Week01-Lecture-Notes.pdf

## Related Topics

- [The Notion of a Limit](notion-of-a-limit.md)
- [Limits That Do Not Exist](limits-that-do-not-exist.md)
- [Computing Finite Limits](computing-finite-limits.md)
- [The Sequential Criterion for Limits](sequential-criterion.md)
- [Infinite Limits and Vertical Asymptotes](infinite-limits.md)
- [Continuity](continuity.md)
