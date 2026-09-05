# The Notion of a Limit

## Definition

Suppose `f` is a function defined **around** (but not necessarily **at**) `x = a`. We say

$$\lim_{x \to a} f(x) = L$$

(for some finite `L`) if `f(x)` can be made arbitrarily close to `L` by moving `x` towards `a`.
> Source: limits.pdf

## Key Concepts

- **The function need not be defined at `a`:** the source emphasizes "defined around (but not necessarily at) x = a." The value `f(a)` — and whether it exists at all — is separate from the value of the limit.
  > Source: limits.pdf

- **Three cases shown graphically.** The source presents three graphs side by side, all with the same limit value `L`:
  1. $\lim_{x \to a} f(x) = L = f(a)$ — "a is in the domain." The curve passes smoothly through the point.
  2. $\lim_{x \to a} f(x) = L$ — "a is **not** in the domain." The graph has a hole (open circle) at `x = a`.
  3. $\lim_{x \to a} f(x) = L \neq f(a)$ — "a is in the domain." The graph has a hole at height `L` and a separate filled point at a different height, which is the actual value `f(a)`.
  > Source: limits.pdf

- **Case 3 is the key distinction:** a function can have a limit at `a`, be defined at `a`, and still have those two values disagree.
  > Source: limits.pdf

## Examples

- **Direct substitution / evaluation.** $\lim_{x \to 1} x^3 - 3x = 1^3 - 3 \cdot 1 = -2 = f(1)$.
  The source labels this "(limit of direct substitution / evaluation)."
  > Source: limits.pdf

- **A limit where the point is not in the domain.** $\lim_{x \to 4} \dfrac{\sqrt{x} - 2}{x - 4}$, with the note "4 is not in the domain!"

  Use difference of squares to factor: $x - 4 = (\sqrt{x} - 2)(\sqrt{x} + 2)$.

  So for $x \neq 4$:
  $$\lim_{x \to 4} \frac{\sqrt{x}-2}{x-4} = \lim_{x \to 4} \frac{\sqrt{x}-2}{(\sqrt{x}-2)(\sqrt{x}+2)} = \lim_{x \to 4} \frac{1}{\sqrt{x}+2} = \frac{1}{\sqrt{4}+2} = \frac{1}{2+2} = \frac{1}{4}$$

  The source annotates the reduced form with "x = 4 **is** in the domain" — cancelling the common factor produces a function that *can* be evaluated by substitution.
  > Source: limits.pdf

## Added from MATH275-Week01-Lecture-Notes.pdf

- **The same point, restated.** "The statement $\lim_{x\to a} f(x) = L$ describes the values of `f(x)` when `x` is near `a`. The value `f(a)` may equal `L`, may be different from `L`, or may not be defined." These are exactly the three graphical cases recorded above from `limits.pdf`.
  > Source: MATH275-Week01-Lecture-Notes.pdf

- **Course takeaway.** "Limits are controlled by nearby behaviour, not by the isolated value at the point. Most computations become short once the obstruction is identified."
  > Source: MATH275-Week01-Lecture-Notes.pdf

## Related Topics

- [One-Sided Limits](one-sided-limits.md)
- [Limits That Do Not Exist](limits-that-do-not-exist.md)
- [Computing Finite Limits](computing-finite-limits.md)
- [Limit Laws](limit-laws.md)
- [Continuity](continuity.md)
