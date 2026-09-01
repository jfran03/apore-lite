# The Sequential Criterion for Limits

## Definition

**Sequential test.** If $\lim_{x \to a} f(x) = L$, then every sequence $x_n \to a$ contained in the domain of `f` with $x_n \neq a$ must satisfy $f(x_n) \to L$.
> Source: MATH275-Week01-Lecture-Notes.pdf

The source marks this section `ANALYSIS` — its label for proof-based / trickier material.
> Source: MATH275-Week01-Lecture-Notes.pdf

## Key Concepts

- **The criterion is used through its contrapositive.** As stated, it is a *necessary* condition for a limit to exist. To disprove a limit, exhibit two sequences approaching `a` whose output sequences approach different numbers.
  > Source: MATH275-Week01-Lecture-Notes.pdf

- **The sequences must avoid the point itself:** $x_n \neq a$, and must lie in the domain of `f`.
  > Source: MATH275-Week01-Lecture-Notes.pdf

- **Killing a one-sided limit kills the two-sided limit.** In the worked example both sequences approach `0` from the right, which disproves the right-hand limit — and hence the two-sided limit — in one stroke.
  > Source: MATH275-Week01-Lecture-Notes.pdf

## Examples

- **`ANALYSIS` — Disprove a limit with two sequences.** Prove that $\lim_{x \to 0} \sin\left(\frac{1}{x}\right)$ does not exist.

  Take
  $$x_n = \frac{1}{2\pi n + \pi/2}, \qquad y_n = \frac{1}{2\pi n + 3\pi/2}$$

  Then $x_n, y_n \to 0^+$, while
  $$\sin(1/x_n) = 1, \qquad \sin(1/y_n) = -1$$

  If the right-hand limit existed, the sequential test would force both sequences of function values to approach the same number. They do not, so the right-hand limit — and hence the two-sided limit — does not exist.

  Note how the sequences are constructed: they are chosen so that $1/x_n$ lands exactly on the peaks of sine and $1/y_n$ exactly on the troughs.
  > Source: MATH275-Week01-Lecture-Notes.pdf

## Related Topics

- [Limits That Do Not Exist](limits-that-do-not-exist.md)
- [One-Sided Limits](one-sided-limits.md)
- [The Notion of a Limit](notion-of-a-limit.md)
