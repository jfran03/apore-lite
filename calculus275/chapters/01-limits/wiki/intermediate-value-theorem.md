# The Intermediate Value Theorem

## Definition

**Theorem (Intermediate Value Theorem).** Suppose `f` is continuous on `[a,b]` with $f(a) \neq f(b)$, and `N` is some value **strictly between** `f(a)` and `f(b)`. Then there is **at least one** `c` with `a < c < b` and `f(c) = N`.
> Source: limits.pdf

The source's plain-language summary:
> "Continuous functions fill gaps in their range."

> Source: limits.pdf

## Key Concepts

- **Three hypotheses, all required:** `f` continuous on the **closed** interval `[a,b]`; $f(a) \neq f(b)$; and `N` strictly between `f(a)` and `f(b)`.
  > Source: limits.pdf

- **The conclusion is existence, not uniqueness.** "At least one c" — the source's diagram shows three distinct points $c_1, c_2, c_3$ in `(a,b)` with $f(c_1) = f(c_2) = f(c_3) = N$.
  > Source: limits.pdf

- **The `c` is strictly interior:** `a < c < b`.
  > Source: limits.pdf

- **Solving-an-equation strategy.** To use IVT on an equation, the source's method is: "Need f, N and [a,b] from IVT. The c in IVT should be solutions to the given equation." Rearrange the equation so one side is zero, let that expression be `f`, and take `N = 0`.
  > Source: limits.pdf

## Examples

- **Show that $e^x = x^3 + 4$ has at least one solution.**

  Set $f(x) = e^x - (x^3+4) = e^x - x^3 - 4$. Now we are solving `f(x) = 0`, and the source marks that `0` as the `N` of the theorem.

  "We can guess some `a` where `f(a) < 0` and some `b` where `f(b) > 0`. Then by IVT there is a `c` with `f(c) = 0`."

  $$f(0) = e^0 - 0 - 4 = 1 - 4 = -3 < 0$$
  $$f(10) = e^{10} - 10^3 - 4 \ggg 0$$

  By IVT there is at least one `c` in `(0,10)` with $e^c - c^3 - 4 = 0$.
  > Source: limits.pdf

## Added from MATH275-Week01-Lecture-Notes.pdf

- **Statement (Week 1 form).** If `f` is continuous on the closed interval `[a,b]` and `N` lies between `f(a)` and `f(b)`, then there is at least one $c \in [a,b]$ such that `f(c) = N`.
  > Source: MATH275-Week01-Lecture-Notes.pdf

- **⚠ The two sources state the conclusion differently.**

  | | `limits.pdf` | `MATH275-Week01-Lecture-Notes.pdf` |
  |---|---|---|
  | Requires $f(a) \neq f(b)$ | yes, stated | not stated |
  | Position of `N` | **strictly** between `f(a)` and `f(b)` | "lies between" |
  | Location of `c` | $a < c < b$ (**open**) | $c \in [a,b]$ (**closed**) |

  The Week 1 version permits `c` to be an endpoint; the `limits.pdf` version does not. The Week 1 notes' own worked example is consistent with their closed-interval form — it concludes "Equality gives the endpoint root `x = 1`; for $A > 3e^{-2}$ the guaranteed root lies in `(0,1)`."

  Both statements are recorded here as written. Check which convention your course uses before relying on either in a proof.
  > Source: limits.pdf; MATH275-Week01-Lecture-Notes.pdf

- **Root-finding recipe.** "For a root, apply the theorem to `f(c) = 0`: verify continuity, compute endpoint signs, and conclude existence. The theorem does not give the root or claim uniqueness."
  > Source: MATH275-Week01-Lecture-Notes.pdf

- **`STUDIO` — A parameter threshold from endpoint data.** For which values of `A` does the IVT guarantee that $Axe^{2x} - 3 = 0$ has a solution in `[0,1]`?

  Let $g_A(x) = Axe^{2x} - 3$. For every $A \in \mathbb{R}$, $g_A$ is continuous on `[0,1]`.

  *Sufficiency.* If $A \geq 3e^{-2}$, then $g_A(0) = -3 < 0$ and $g_A(1) = Ae^2 - 3 \geq 0$, so the IVT guarantees a root.

  *Necessity.* For $0 \leq x \leq 1$, $0 \leq xe^{2x} \leq e^2$. If $A \leq 0$ then $g_A(x) \leq -3 < 0$. If $0 < A < 3e^{-2}$ then $g_A(x) = Axe^{2x} - 3 \leq Ae^2 - 3 < 0$. Thus no root exists when $A < 3e^{-2}$.

  Therefore the exact range is $A \geq 3e^{-2}$. Equality gives the endpoint root `x = 1`; for $A > 3e^{-2}$ the guaranteed root lies in `(0,1)`.

  The source's framing instruction: "Record the hypothesis and endpoint values before solving the inequality. After obtaining a sufficient condition from the endpoints, determine whether any smaller value of `A` can work." Note the two-part structure — the endpoints give sufficiency, and a separate bounding argument is needed for necessity.
  > Source: MATH275-Week01-Lecture-Notes.pdf

- **`In class` — turn a picture into an IVT argument.** Sketch a continuous graph on `[a,b]` with $f(a) < 0 < f(b)$. Then add: (i) a graph with three roots, showing why uniqueness is not guaranteed; (ii) a jump discontinuity that skips `0`, showing why continuity is essential.
  > Source: MATH275-Week01-Lecture-Notes.pdf

## Related Topics

- [Continuity](continuity.md)
- [Computing Finite Limits](computing-finite-limits.md)
- [The Notion of a Limit](notion-of-a-limit.md)
