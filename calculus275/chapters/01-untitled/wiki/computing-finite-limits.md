# Computing Finite Limits

## Definition

When direct substitution produces an indeterminate form, **name the obstruction before doing algebra**.
> Source: MATH275-Week01-Lecture-Notes.pdf

## Key Concepts

- **Catalogue of obstructions and their techniques:**

  | Obstruction | Technique |
  |---|---|
  | Common factor | Factor and cancel; remember that cancellation is valid for $x \neq a$, which is enough for a limit. |
  | Difference of radicals | Multiply by the conjugate. |
  | Absolute value | Split into left and right cases before simplifying. |
  | Bounded oscillation | Look for a squeeze. |

  > Source: MATH275-Week01-Lecture-Notes.pdf

- **Why cancellation is legitimate.** Cancelling a common factor changes the function at `x = a`, but a limit only depends on values *near* `a`, never at `a`. The source stresses: "we simplified nearby values; we did not substitute into the original undefined expression."
  > Source: MATH275-Week01-Lecture-Notes.pdf

- **Absolute value must be split before simplifying**, because $|x|$ has different algebraic forms on the two sides of `0` — this is what makes such problems one-sided problems in disguise.
  > Source: MATH275-Week01-Lecture-Notes.pdf

- **Limit laws (Week 1 statement).** If $\lim f(x) = L$ and $\lim g(x) = M$ for the same limiting process, then
  $$\lim (cf + g) = cL + M, \qquad \lim (fg) = LM, \qquad \lim \frac{f}{g} = \frac{L}{M} \quad (M \neq 0)$$
  > Source: MATH275-Week01-Lecture-Notes.pdf

## Examples

- **`CORE` — A removable obstruction.** Evaluate $\lim_{x \to 2} \frac{x^2 - x - 2}{x-2}$.

  For $x \neq 2$: $\frac{x^2-x-2}{x-2} = \frac{(x-2)(x+1)}{x-2} = x+1$. Therefore the limit is **3**.
  > Source: MATH275-Week01-Lecture-Notes.pdf

- **`In class` — Combining a conjugate with one-sided analysis.** Evaluate
  $$\lim_{x \to 0^-} \frac{\sqrt{1+x}-\sqrt{1-x}}{|x|}, \qquad \lim_{x \to 0^+} \frac{\sqrt{1+x}-\sqrt{1-x}}{|x|}$$

  For $x \neq 0$, rationalization gives
  $$\frac{\sqrt{1+x}-\sqrt{1-x}}{|x|} = \frac{2x}{|x|\left(\sqrt{1+x}+\sqrt{1-x}\right)}$$

  Since $x/|x| = -1$ on the left and $+1$ on the right, the one-sided limits are $-1$ and $1$ respectively. Therefore the two-sided limit **does not exist**.

  This problem exercises two techniques at once: the conjugate clears the radical difference, and the absolute value forces the split into cases.
  > Source: MATH275-Week01-Lecture-Notes.pdf

## Related Topics

- [One-Sided Limits](one-sided-limits.md)
- [Limit Laws](limit-laws.md)
- [The Notion of a Limit](notion-of-a-limit.md)
- [Limits at Infinity and Horizontal Asymptotes](limits-at-infinity.md)
