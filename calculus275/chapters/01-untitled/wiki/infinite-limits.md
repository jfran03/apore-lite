# Infinite Limits (Vertical Asymptotes)

## Definition

**(i)** We say $\lim_{x \to a} f(x) = \infty$ if `f(x)` can be made **arbitrarily large** as `x` moves towards `a`.
> Source: limits.pdf

**(ii)** We say $\lim_{x \to a} f(x) = -\infty$ if `f(x)` can be made **arbitrarily large and negative** as `x` moves towards `a`.
> Source: limits.pdf

In either case, `f` has a **vertical asymptote** at `x = a`.
> Source: limits.pdf

## Key Concepts

- **One-sided versions exist too.** Analogous notions exist for
  $$\lim_{x \to a^{\pm}} f(x) = \infty, \qquad \lim_{x \to a^{\pm}} f(x) = -\infty$$
  and the source states: "in each of these 4 cases, a V.A. exists at `x = a`."
  > Source: limits.pdf

- **A vertical asymptote does not require both sides to agree.** The source's four-case example has the function going to `+∞` on one side of a point and `-∞` on the other; the asymptote exists regardless.
  > Source: limits.pdf

- **Sign analysis of the denominator drives the result.** When a quotient's denominator approaches `0`, the source's technique is to determine *the sign* the denominator approaches from, not just that it approaches zero.
  > Source: limits.pdf

## Examples

- **A function with vertical asymptotes at `x = 2` and `x = -2`.** The source's graph shows a curve with asymptotes at both `x = 2` and `x = -2`, annotated:
  - $\lim_{x \to 2} f(x) = \infty$
  - $\lim_{x \to 2} f(x) = \infty$

  > **Transcription note:** both lines are written `x → 2` in the source, with no minus sign on the second. Since the graph shows asymptotes at *both* `x = 2` and `x = -2`, the second line appears to be a slip in the notes. Recorded here exactly as written. Verify against your course materials before relying on it.
  > Source: limits.pdf

- **The four one-sided cases.** A second graph, with asymptotes at `x = 2` and `x = -2`:
  - $\lim_{x \to 2^+} f(x) = \infty$
  - $\lim_{x \to 2^-} f(x) = -\infty$
  - $\lim_{x \to -2^+} f(x) = -\infty$
  - $\lim_{x \to -2^-} f(x) = \infty$
  > Source: limits.pdf

- **Determining the sign of a vanishing denominator.**
  $$\lim_{x \to 0^+} \frac{3 - x}{\sin(\pi x)}$$

  The source notes: "sin 0 = 0; we can't directly evaluate."

  Reasoning given: for `x` close to `0` and `x > 0`, we can say `3 - x ≈ 3`, and `sin(πx) → 0` **but** `sin(πx) > 0`.

  So $\dfrac{3-x}{\sin(\pi x)}$ "looks like" $\dfrac{3}{0^+} = \infty$, where `0⁺` is annotated as "a positive quantity approaching 0."
  > Source: limits.pdf

## Added from MATH275-Week01-Lecture-Notes.pdf

- **Asymptote definitions in terms of "at least one" limit.** A line `x = a` is a **vertical asymptote** when *at least one* one-sided limit at `a` is $+\infty$ or $-\infty$. A line `y = L` is a **horizontal asymptote** when at least one of $\lim_{x\to+\infty} f(x)$ or $\lim_{x\to-\infty} f(x)$ equals `L`.
  > Source: MATH275-Week01-Lecture-Notes.pdf

- **The sign checkpoint.** The identity $\sqrt{x^2} = |x|$ is the key sign checkpoint, with
  $$|x| = x \ (x \to +\infty), \qquad |x| = -x \ (x \to -\infty)$$
  > Source: MATH275-Week01-Lecture-Notes.pdf

- **`CORE` — Find both kinds of asymptote.** For $f(x) = \dfrac{2x+1}{x-3}$: the numerator tends to $7 > 0$ at `x = 3`, while the denominator changes sign. Moreover,
  $$\lim_{x\to 3^-} f(x) = -\infty, \qquad \lim_{x\to 3^+} f(x) = +\infty, \qquad \lim_{x\to\pm\infty} f(x) = \lim_{x\to\pm\infty}\frac{2+1/x}{1-3/x} = 2$$
  Thus `x = 3` is a vertical asymptote and `y = 2` is a horizontal asymptote.

  The method is worth noting: fix the sign of the numerator first, then track the sign change of the denominator across the point.
  > Source: MATH275-Week01-Lecture-Notes.pdf

## Related Topics

- [Limits That Do Not Exist](limits-that-do-not-exist.md)
- [One-Sided Limits](one-sided-limits.md)
- [Computing Finite Limits](computing-finite-limits.md)
- [Limits at Infinity and Horizontal Asymptotes](limits-at-infinity.md)
