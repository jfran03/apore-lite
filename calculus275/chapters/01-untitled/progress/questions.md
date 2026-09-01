# Question Bank

> Generated from `wiki/` during the compile step. Extended on wrong-answer targeting and graduation.
> Do not edit manually — all changes are made by Claude during compile and session flows.

---

<!-- Question format (do not delete this comment):

## Q{NNN}
**Status:** active | retired
**Type:** mcq | short-answer | conceptual | true-false
**Difficulty:** introductory | intermediate | advanced
**Topic:** {topic-slug}
**Focus Area:** {specific concept or sub-topic}
**Question:** {question text}
**Answer:** {model answer — sourced from wiki only}

-->

## Q001
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** notion-of-a-limit
**Focus Area:** definition of a limit
**Question:** State the definition of $\lim_{x \to a} f(x) = L$ as given in the notes, including the condition on where `f` must be defined.
**Answer:** Suppose `f` is a function defined around (but not necessarily at) `x = a`. We say $\lim_{x \to a} f(x) = L$, for some finite `L`, if `f(x)` can be made arbitrarily close to `L` by moving `x` towards `a`.

## Q002
**Status:** active
**Type:** true-false
**Difficulty:** introductory
**Topic:** notion-of-a-limit
**Focus Area:** function need not be defined at the point
**Question:** True or false: for $\lim_{x \to a} f(x)$ to exist, `f` must be defined at `x = a`.
**Answer:** False. The definition requires `f` to be defined *around* `a`, but not necessarily *at* `a`. The notes' second graph shows a case where `a` is not in the domain and the limit still equals `L`.

## Q003
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** notion-of-a-limit
**Focus Area:** the three graphical cases
**Question:** The notes present three graphs that all have $\lim_{x \to a} f(x) = L$. Describe how the three cases differ with respect to `f(a)`.
**Answer:** Case 1: $L = f(a)$ and `a` is in the domain — the curve passes through the point. Case 2: `a` is not in the domain — there is a hole at `x = a`, so `f(a)` does not exist. Case 3: `a` is in the domain but $L \neq f(a)$ — there is a hole at height `L` and a separate filled point at a different height, which is the actual value of `f(a)`.

## Q004
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** notion-of-a-limit
**Focus Area:** factoring to evaluate a limit
**Question:** Evaluate $\lim_{x \to 4} \frac{\sqrt{x}-2}{x-4}$, and explain why direct substitution fails.
**Answer:** Direct substitution fails because 4 is not in the domain — the denominator is zero there. Factor by difference of squares: $x - 4 = (\sqrt{x}-2)(\sqrt{x}+2)$. So for $x \neq 4$, $\frac{\sqrt{x}-2}{x-4} = \frac{1}{\sqrt{x}+2}$, and $\lim_{x \to 4}\frac{1}{\sqrt{x}+2} = \frac{1}{\sqrt{4}+2} = \frac{1}{2+2} = \frac{1}{4}$. After cancelling, `x = 4` *is* in the domain of the reduced expression, so substitution is now valid.

## Q005
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** notion-of-a-limit
**Focus Area:** direct substitution
**Question:** Evaluate $\lim_{x \to 1} x^3 - 3x$.
**Answer:** $1^3 - 3 \cdot 1 = -2$, which also equals `f(1)`. The notes label this a limit of direct substitution / evaluation.

## Q006
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** one-sided-limits
**Focus Area:** definition of one-sided limits
**Question:** Define $\lim_{x \to a^+} f(x) = L$ and $\lim_{x \to a^-} f(x) = L$, being explicit about the direction of approach.
**Answer:** $\lim_{x \to a^+} f(x) = L$ if `f(x)` can be made arbitrarily close to `L` by moving `x` towards `a` from the right (i.e. `x > a`). $\lim_{x \to a^-} f(x) = L$ if `f(x)` can be made arbitrarily close to `L` by moving `x` towards `a` from the left (i.e. `x < a`).

## Q007
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** one-sided-limits
**Focus Area:** two-sided existence criterion
**Question:** State the "if and only if" relationship between the two-sided limit and the one-sided limits. Why is it not enough for both one-sided limits merely to exist?
**Answer:** $\lim_{x \to a} f(x) = L$ occurs if and only if both one-sided limits exist and equal `L`. Existence alone is insufficient because the two one-sided limits could exist but disagree — the notes' jump example has $\lim_{x \to a^+} f(x) = f(a)$ and $\lim_{x \to a^-} f(x) = L$ with $f(a) \neq L$, and concludes the two-sided limit DNE.

## Q008
**Status:** active
**Type:** true-false
**Difficulty:** intermediate
**Topic:** one-sided-limits
**Focus Area:** DNE from mismatched one-sided limits
**Question:** True or false: if $\lim_{x \to a^+} f(x)$ and $\lim_{x \to a^-} f(x)$ both exist, then $\lim_{x \to a} f(x)$ exists.
**Answer:** False. Both must exist *and* be equal. The notes' jump example has both one-sided limits existing but unequal, and the two-sided limit does not exist.

## Q009
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** limits-that-do-not-exist
**Focus Area:** two failure modes
**Question:** The notes give two examples of limits that do not exist, and the reasons are different in kind. Identify both.
**Answer:** (1) Oscillation: $\lim_{x \to 0^{\pm}} \sin(1/x)$ DNE — the "topologist's sine curve" oscillates between 1 and -1 with the oscillations compressing without bound near 0, so it never settles near any value. (2) Divergence: $\lim_{x \to 0^+} 1/x$ DNE, annotated "(is infinity)" — it grows without bound.

## Q010
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** limits-that-do-not-exist
**Focus Area:** DNE vs. infinity
**Question:** The notes write $\lim_{x \to 0^+} \frac{1}{x}$ DNE and then annotate it "(is infinity)". Reconcile these two statements.
**Answer:** The limit fails to exist as a *finite* `L` — the definition of $\lim_{x\to a} f(x) = L$ requires a finite `L`. Writing "is infinity" records *why* it fails: the function diverges rather than oscillating. The notation $= \infty$ is a description of the manner of failure, not a claim that a finite limit exists.

## Q011
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** limits-that-do-not-exist
**Focus Area:** topologist's sine curve
**Question:** For the topologist's sine curve, which one-sided limits at 0 fail, and how does this differ structurally from a jump discontinuity?
**Answer:** Both fail — $\lim_{x \to 0^+} \sin(1/x)$ DNE and $\lim_{x \to 0^-} \sin(1/x)$ DNE. This differs from a jump, where the two one-sided limits each exist but disagree; here neither side approaches anything at all.

## Q012
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** limit-laws
**Focus Area:** sum, product, quotient laws
**Question:** Given $\lim_{x \to a} f(x) = L$ and $\lim_{x \to a} g(x) = M$, state the limit laws for sum/difference, product, and quotient.
**Answer:** (i) $\lim_{x\to a} f(x) \pm g(x) = L \pm M$. (ii) $\lim_{x\to a} f(x)g(x) = LM$. (iii) $\lim_{x\to a} \frac{f(x)}{g(x)} = \frac{L}{M}$, provided $M \neq 0$ and $g(x) \neq 0$ for all `x` close to `a`.

## Q013
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** limit-laws
**Focus Area:** hypotheses of the quotient law
**Question:** The quotient law carries two separate provisos. State both and explain why one does not imply the other.
**Answer:** The provisos are $M \neq 0$ and $g(x) \neq 0$ for all `x` "close" to `a`. They are distinct: `M` is the *limit* of `g`, while the second condition is about the *values* of `g` near `a`. A function can have nonzero limit while still taking the value zero at points near `a`, which would make the quotient undefined there.

## Q014
**Status:** active
**Type:** true-false
**Difficulty:** intermediate
**Topic:** limit-laws
**Focus Area:** hypothesis that both limits exist
**Question:** True or false: the limit laws let you conclude $\lim_{x\to a}[f(x) + g(x)] = L + M$ without first knowing whether $\lim_{x\to a} f(x)$ and $\lim_{x\to a} g(x)$ exist.
**Answer:** False. The laws are stated under the supposition that $\lim_{x\to a} f(x) = L$ and $\lim_{x\to a} g(x) = M$ — that both limits exist is a hypothesis, not a conclusion.

## Q015
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** limit-laws
**Focus Area:** integer power law
**Question:** State the power law for limits as given in the notes, including its restriction.
**Answer:** $\lim_{x \to a} f(x)^n = L^n$ for $n \in \mathbb{Z}$ (the integers), provided $L \neq 0$ when $n < 0$.

## Q016
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** limit-laws
**Focus Area:** applying the laws by evaluation
**Question:** Evaluate $\lim_{x \to 2} \frac{x^3 - \sin\left(\frac{\pi x}{2}\right)}{x \cos\left(\frac{\pi x^2}{4}\right)}$.
**Answer:** $\frac{2^3 - \sin(\pi)}{2\cos(\pi)} = \frac{8 - 0}{-2} = -4$.

## Q017
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** infinite-limits
**Focus Area:** definition of infinite limits
**Question:** Define $\lim_{x \to a} f(x) = \infty$ and $\lim_{x \to a} f(x) = -\infty$, and state what they imply about the graph of `f`.
**Answer:** $\lim_{x\to a} f(x) = \infty$ if `f(x)` can be made arbitrarily large as `x` moves towards `a`. $\lim_{x\to a} f(x) = -\infty$ if `f(x)` can be made arbitrarily large and negative as `x` moves towards `a`. In either case, `f` has a vertical asymptote at `x = a`.

## Q018
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** infinite-limits
**Focus Area:** one-sided infinite limits and vertical asymptotes
**Question:** How many cases does the source identify as producing a vertical asymptote at `x = a`, and must the behaviour on the two sides agree?
**Answer:** Four cases: $\lim_{x \to a^{\pm}} f(x) = \infty$ and $\lim_{x \to a^{\pm}} f(x) = -\infty$. The notes state a V.A. exists at `x = a` in each of these 4 cases. The two sides need not agree — the four-case example has the function going to `+∞` on one side and `-∞` on the other, and the asymptote exists regardless.

## Q019
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** infinite-limits
**Focus Area:** sign analysis of a vanishing denominator
**Question:** Evaluate $\lim_{x \to 0^+} \frac{3-x}{\sin(\pi x)}$ and explain each step of the reasoning.
**Answer:** Direct evaluation fails since $\sin 0 = 0$. For `x` close to 0 with `x > 0`: the numerator $3 - x \approx 3$, and $\sin(\pi x) \to 0$ but $\sin(\pi x) > 0$. So the expression "looks like" $\frac{3}{0^+}$ — a fixed positive numerator over a positive quantity approaching 0 — which is $\infty$. The critical step is establishing the *sign* the denominator approaches from, not merely that it approaches 0.

## Q020
**Status:** active
**Type:** mcq
**Difficulty:** intermediate
**Topic:** infinite-limits
**Focus Area:** why one-sided analysis is needed
**Question:** In evaluating $\lim_{x \to 0^+} \frac{3-x}{\sin(\pi x)}$, why does the source restrict attention to `x > 0`? (a) Because `sin` is undefined for `x < 0`; (b) Because the sign of $\sin(\pi x)$ near 0 depends on the side of approach, and that sign determines the answer; (c) Because `3 - x` is only positive for `x > 0`; (d) Because the limit laws require one-sided limits.
**Answer:** (b). The reasoning turns on $\sin(\pi x) > 0$, which the source asserts for `x` close to 0 with `x > 0`. The sign of the vanishing denominator is what makes the quotient $+\infty$ rather than $-\infty$.

## Q021
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** limits-at-infinity
**Focus Area:** definition of limits at infinity
**Question:** Define $\lim_{x \to \infty} f(x) = L$ and $\lim_{x \to -\infty} f(x) = L$.
**Answer:** $\lim_{x\to\infty} f(x) = L$ if `f(x)` can be made arbitrarily close to `L` for sufficiently large input. $\lim_{x\to-\infty} f(x) = L$ if `f(x)` can be made arbitrarily close to `L` for sufficiently large negative input.

## Q022
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** limits-at-infinity
**Focus Area:** formal technique for ratios
**Question:** State the formal technique for a ratio of diverging quantities, then apply it to $\lim_{x \to \infty} \frac{3x^2 - x}{-2x^2+4}$.
**Answer:** Divide numerator and denominator by the highest order term in the denominator. Multiplying by $\frac{1/x^2}{1/x^2}$: $\lim_{x\to\infty} \frac{3 - \frac{1}{x}}{-2 + \frac{4}{x^2}} = \frac{3-0}{-2+0} = -\frac{3}{2}$, using $\lim_{x\to\pm\infty}\frac{1}{x^n} = 0$ for `n > 0`. The short technique — drop the lower order terms — gives $\lim \frac{3x^2}{-2x^2} = -\frac{3}{2}$.

## Q023
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** limits-at-infinity
**Focus Area:** identifying the dominant term
**Question:** In $\lim_{x \to -\infty} \frac{3x^3 + x^2\sqrt{3-x} + 2}{-x^2+1}$, why is the $x^2\sqrt{3-x}$ term discarded, and what is the value of the limit?
**Answer:** $x^2\sqrt{3-x}$ behaves like $x^{2.5}$, which is dominated by $x^3$ for large negative `x`. Dropping lower order terms: $\lim_{x\to-\infty} \frac{3x^3}{-x^2} = \lim_{x\to-\infty} -3x = \infty$, since `x → -∞` makes `-3x` positive and unbounded.

## Q024
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** limits-at-infinity
**Focus Area:** growth hierarchy
**Question:** State the growth hierarchy from the notes, then use it to evaluate $\lim_{x \to \infty} \frac{2^x + \ln(x^4+x^2)}{(1.5)^x + x^3 - x^2}$.
**Answer:** Exponential growth >>>> polynomial growth >>>> logarithmic growth. Here $\ln(x^4+x^2) \approx \ln(x^4) = 4\ln x$, which is far smaller than $2^x$; likewise $x^3 - x^2$ is dominated by $(1.5)^x$. So the limit is $\lim_{x\to\infty} \frac{2^x}{(1.5)^x} = \lim_{x\to\infty}\left(\frac{2}{1.5}\right)^x = \lim_{x\to\infty}\left(\frac{4}{3}\right)^x = \infty$.

## Q025
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** limits-at-infinity
**Focus Area:** horizontal asymptotes
**Question:** What are $\lim_{x\to\infty} \arctan(x)$ and $\lim_{x\to-\infty}\arctan(x)$, and what does this say about horizontal asymptotes?
**Answer:** $\lim_{x\to\infty}\arctan(x) = \frac{\pi}{2}$ and $\lim_{x\to-\infty}\arctan(x) = -\frac{\pi}{2}$. So `f` has horizontal asymptotes at $y = \pm\frac{\pi}{2}$ — a single function can have two different horizontal asymptotes, one in each direction.

## Q026
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** squeeze-theorem
**Focus Area:** statement of the theorem
**Question:** State the Squeeze Theorem in full, including all hypotheses.
**Answer:** Suppose $f(x) \leq g(x) \leq h(x)$ for all `x` near `a`, and that $\lim_{x\to a} f(x) = \lim_{x\to a} h(x) = L$. Then $\lim_{x\to a} g(x)$ exists and is also equal to `L`.

## Q027
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** squeeze-theorem
**Focus Area:** the theorem delivers existence
**Question:** Why is it significant that the Squeeze Theorem's conclusion is phrased as "$\lim_{x\to a} g(x)$ **exists** and is also equal to L" rather than just "equals L"?
**Answer:** Because you are not assuming the middle limit exists in order to compute it — the squeeze *proves* existence. This matters for functions like $x^2\sin(e^{1/x})$, where the oscillating factor means you have no independent reason to believe the limit exists; the bounding argument establishes both existence and value at once.

## Q028
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** squeeze-theorem
**Focus Area:** applying the squeeze theorem
**Question:** Compute $\lim_{x \to 0} x^2 \sin\left(e^{\frac{1}{x}}\right)$, justifying each step.
**Answer:** Begin with $-1 \leq \sin(\theta) \leq 1$ for any `θ`, so $-1 \leq \sin(e^{1/x}) \leq 1$. Multiply by $x^2$; since $x^2 \geq 0$ the inequality direction is preserved, giving $-x^2 \leq x^2\sin(e^{1/x}) \leq x^2$. Both outer bounds tend to 0 as `x → 0`, so by the squeeze theorem the limit is 0.

## Q029
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** squeeze-theorem
**Focus Area:** squeeze at infinity
**Question:** The notes remark the squeeze theorem holds in settings beyond two-sided finite limits. Name them, and evaluate $\lim_{x \to \infty} \frac{x^2 + \sin(e^x)}{2x^2+1}$.
**Answer:** It also holds for one-sided limits, limits at infinity, and infinite limits. Since $-1 \leq \sin(e^x) \leq 1$: $\frac{x^2-1}{2x^2+1} \leq \frac{x^2+\sin(e^x)}{2x^2+1} \leq \frac{x^2+1}{2x^2+1}$. Both outer expressions tend to $\frac{1}{2}$, so by squeeze the limit is $\frac{1}{2}$.

## Q030
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** continuity
**Focus Area:** definition of continuity
**Question:** Define what it means for `f` to be continuous at `x = a`, and for `f` to be continuous on an interval `I`.
**Answer:** `f` is continuous at `x = a` if $\lim_{x\to a} f(x) = f(a)$. `f` is continuous on an interval `I` if $\lim_{x\to a} f(x) = f(a)$ for every $a \in I$.

## Q031
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** continuity
**Focus Area:** continuity as a three-part condition
**Question:** The single equation $\lim_{x\to a} f(x) = f(a)$ encodes three separate requirements. Identify them, and match each to one of the three graphical cases from the notes' opening section.
**Answer:** (1) The limit must exist; (2) `f(a)` must be defined; (3) the two must be equal. Matching to the three graphs: case 2 (`a` not in the domain) fails requirement 2; case 3 ($L \neq f(a)$) fails requirement 3; case 1 ($L = f(a)$, `a` in the domain) satisfies all three and is the continuous one.

## Q032
**Status:** active
**Type:** true-false
**Difficulty:** intermediate
**Topic:** continuity
**Focus Area:** defined vs. continuous
**Question:** True or false: if `f` is defined at every point of an interval `I`, then `f` is continuous on `I`.
**Answer:** False. The notes show two graphs over the same interval — one a single unbroken component ("f is continuous on I") and one with a jump ("f is defined on I but not continuous"). Being defined everywhere on `I` is necessary but not sufficient.

## Q033
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** continuity
**Focus Area:** intervals of continuity for standard functions
**Question:** On which intervals is $g(x) = \frac{x^2}{(x-1)(x-2)}$ continuous, and what general principle determines the answer?
**Answer:** On $(-\infty, 1)$, $(1,2)$ and $(2,\infty)$. The principle: polynomials, rational functions, roots, trig, inverse trig, exp and log are continuous on intervals *within their domains*. The breakpoints are exactly the zeros of the denominator, which are excluded from the domain.

## Q034
**Status:** active
**Type:** mcq
**Difficulty:** intermediate
**Topic:** continuity
**Focus Area:** graphical characterization
**Question:** According to the notes, `f` is continuous on `I` if: (a) `f` is defined at every point of `I`; (b) the graph above `I` is a single component; (c) `f` has no vertical asymptotes; (d) `f` is a polynomial.
**Answer:** (b). The notes give the graphical characterization "f is continuous on I if the graph above I is a single component."

## Q035
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** intermediate-value-theorem
**Focus Area:** statement of IVT
**Question:** State the Intermediate Value Theorem, including all three hypotheses and the precise form of the conclusion.
**Answer:** Suppose `f` is continuous on `[a,b]` with $f(a) \neq f(b)$, and `N` is some value strictly between `f(a)` and `f(b)`. Then there is at least one `c` with `a < c < b` and `f(c) = N`. The notes summarize: "Continuous functions fill gaps in their range."

## Q036
**Status:** active
**Type:** true-false
**Difficulty:** intermediate
**Topic:** intermediate-value-theorem
**Focus Area:** existence, not uniqueness
**Question:** True or false: the IVT guarantees exactly one `c` in `(a,b)` with `f(c) = N`.
**Answer:** False. It guarantees *at least one*. The notes' diagram shows three distinct points $c_1, c_2, c_3$ in `(a,b)` all satisfying $f(c_i) = N$.

## Q037
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** intermediate-value-theorem
**Focus Area:** strategy for applying IVT to an equation
**Question:** Describe the notes' strategy for using the IVT to show an equation has a solution. What plays the role of `N`?
**Answer:** You need `f`, `N` and `[a,b]` from the IVT, and the `c` in the IVT should be a solution to the given equation. Rearrange the equation so one side is zero and let that expression be `f`; then `N = 0`. Guess some `a` where `f(a) < 0` and some `b` where `f(b) > 0` — then 0 lies strictly between them, and IVT supplies a `c` with `f(c) = 0`.

## Q038
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** intermediate-value-theorem
**Focus Area:** worked IVT application
**Question:** Show that $e^x = x^3 + 4$ has at least one solution, following the notes' method.
**Answer:** Set $f(x) = e^x - (x^3+4) = e^x - x^3 - 4$; solving the original equation is now solving `f(x) = 0`, so `N = 0`. Evaluate: $f(0) = e^0 - 0 - 4 = 1 - 4 = -3 < 0$, and $f(10) = e^{10} - 10^3 - 4 \ggg 0$. Since 0 lies strictly between `f(0)` and `f(10)`, by IVT there is at least one `c` in `(0,10)` with $e^c - c^3 - 4 = 0$.

## Q039
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** computing-finite-limits
**Focus Area:** naming the obstruction
**Question:** The Week 1 notes give a table matching four obstructions to four techniques. Reproduce it.
**Answer:** Common factor → factor and cancel (valid for $x \neq a$, which is enough for a limit). Difference of radicals → multiply by the conjugate. Absolute value → split into left and right cases before simplifying. Bounded oscillation → look for a squeeze.

## Q040
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** computing-finite-limits
**Focus Area:** removable obstruction
**Question:** Evaluate $\lim_{x \to 2} \frac{x^2-x-2}{x-2}$.
**Answer:** For $x \neq 2$, $\frac{x^2-x-2}{x-2} = \frac{(x-2)(x+1)}{x-2} = x+1$, so the limit is 3. The notes stress that we simplified nearby values; we did not substitute into the original undefined expression.

## Q041
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** computing-finite-limits
**Focus Area:** why cancellation is legitimate
**Question:** Cancelling $(x-2)$ changes the function at $x=2$. Why is the cancelled expression still valid for computing the limit?
**Answer:** Because cancellation is valid for $x \neq a$, and that is enough for a limit — a limit depends only on the values of the function near $a$, never on the value at $a$. The takeaway from the notes: limits are controlled by nearby behaviour, not by the isolated value at the point.

## Q042
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** computing-finite-limits
**Focus Area:** conjugate combined with one-sided analysis
**Question:** Evaluate the one-sided limits of $\frac{\sqrt{1+x}-\sqrt{1-x}}{|x|}$ at 0 and decide whether the two-sided limit exists.
**Answer:** For $x \neq 0$, rationalizing gives $\frac{2x}{|x|(\sqrt{1+x}+\sqrt{1-x})}$. Since $x/|x| = -1$ on the left and $+1$ on the right, and the remaining factor tends to $\frac{2}{2}=1$, the one-sided limits are $-1$ and $1$. They disagree, so the two-sided limit does not exist.

## Q043
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** computing-finite-limits
**Focus Area:** absolute value forces a split
**Question:** Why does an $|x|$ in an expression turn a limit problem into a one-sided problem?
**Answer:** Because $|x|$ has different algebraic forms on the two sides of 0 ($x/|x| = -1$ for $x<0$ and $+1$ for $x>0$). The notes' technique table says to split into left and right cases *before* simplifying, since a single algebraic simplification cannot be valid on both sides at once.

## Q044
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** one-sided-limits
**Focus Area:** fast diagnostic
**Question:** State the Week 1 "fast diagnostic" for a two-sided limit, including what it says about $f(a)$.
**Answer:** If the left- and right-hand limits disagree, the two-sided limit does not exist. The isolated value $f(a)$ cannot repair that disagreement.

## Q045
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** one-sided-limits
**Focus Area:** three independent pieces of information
**Question:** Sketch (or describe) a function satisfying $\lim_{x\to 1^-} f(x) = 2$, $\lim_{x\to 1^+} f(x) = -1$, and $f(1) = 3$. Does $\lim_{x\to 1} f(x)$ exist?
**Answer:** The graph approaches height 2 from the left (open circle at $(1,2)$), approaches $-1$ from the right (open circle at $(1,-1)$), and has a filled point at $(1,3)$. The limit does not exist: the one-sided limits disagree, and $f(1)=3$ cannot repair that. The exercise demonstrates that the left limit, right limit, and function value are three independent pieces of information.

## Q046
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** infinite-limits
**Focus Area:** asymptote definitions
**Question:** State the Week 1 definitions of vertical and horizontal asymptote. What does the phrase "at least one" do in each?
**Answer:** A line $x=a$ is a vertical asymptote when at least one one-sided limit at $a$ is $+\infty$ or $-\infty$. A line $y=L$ is a horizontal asymptote when at least one of $\lim_{x\to+\infty}f(x)$ or $\lim_{x\to-\infty}f(x)$ equals $L$. "At least one" means the two sides need not agree — one-sided blow-up is enough for a V.A., and a single direction is enough for an H.A.

## Q047
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** infinite-limits
**Focus Area:** finding both kinds of asymptote
**Question:** Find all vertical and horizontal asymptotes of $f(x) = \frac{2x+1}{x-3}$, with justification.
**Answer:** At $x=3$ the numerator tends to $7>0$ while the denominator changes sign, giving $\lim_{x\to3^-}f(x) = -\infty$ and $\lim_{x\to3^+}f(x)=+\infty$; so $x=3$ is a vertical asymptote. Dividing by the highest order term, $\lim_{x\to\pm\infty}\frac{2+1/x}{1-3/x}=2$; so $y=2$ is a horizontal asymptote.

## Q048
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** limits-at-infinity
**Focus Area:** the sign checkpoint
**Question:** State the identity the notes call "the key sign checkpoint" and its two cases.
**Answer:** $\sqrt{x^2} = |x|$, with $|x| = x$ as $x \to +\infty$ and $|x| = -x$ as $x \to -\infty$.

## Q049
**Status:** active
**Type:** true-false
**Difficulty:** intermediate
**Topic:** limits-at-infinity
**Focus Area:** sign flip when dividing by x
**Question:** True or false: as $x \to -\infty$, $\frac{\sqrt{x^2-4x+7}}{x} \to 1$.
**Answer:** False — it tends to $-1$. Writing $\frac{\sqrt{x^2-4x+7}}{x} = \frac{|x|}{x}\sqrt{1-\frac{4}{x}+\frac{7}{x^2}}$ and using $|x| = -x$ at negative infinity gives $\frac{|x|}{x} = -1$. The notes flag this as the place where dividing by $x$ can silently flip an answer.

## Q050
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** limits-at-infinity
**Focus Area:** radical cancellation at negative infinity
**Question:** Evaluate $\lim_{x\to-\infty}\left(\sqrt{x^2-4x+7}+x\right)$, showing where the sign checkpoint is used.
**Answer:** Rationalize: $\sqrt{x^2-4x+7}+x = \frac{-4x+7}{\sqrt{x^2-4x+7}-x}$. Divide numerator and denominator by $-x = |x|$ (this is the sign checkpoint, since $x\to-\infty$), giving $\frac{4-7/x}{\sqrt{1-4/x+7/x^2}+1} \to \frac{4}{2} = 2$.

## Q051
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** squeeze-theorem
**Focus Area:** applying the squeeze to a cosine
**Question:** Show that $\lim_{x\to0} x^2\cos\left(\frac{3}{x}\right) = 0$.
**Answer:** Since $-1 \leq \cos(3/x) \leq 1$ and $x^2 \geq 0$, multiplying through gives $-x^2 \leq x^2\cos(3/x) \leq x^2$. Both outer functions tend to 0, so by the squeeze theorem the limit is 0.

## Q052
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** squeeze-theorem
**Focus Area:** when the squeeze is the right tool
**Question:** According to the Week 1 notes, what shape of problem calls for the squeeze theorem?
**Answer:** It is most useful when the middle expression oscillates but its amplitude shrinks. The obstruction table lists "bounded oscillation → look for a squeeze" — you bound the factor you cannot simplify and let the shrinking amplitude drive both bounds to the same limit.

## Q053
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** continuity
**Focus Area:** three conditions written separately
**Question:** List the three separate conditions for $f$ to be continuous at $a$, as the Week 1 notes state them.
**Answer:** (1) $f(a)$ is defined; (2) $\lim_{x\to a} f(x)$ exists; (3) $\lim_{x\to a} f(x) = f(a)$.

## Q054
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** continuity
**Focus Area:** repairing a piecewise function
**Question:** Find $c$ so that $f(x) = x^2-1$ for $x<1$ and $f(x) = cx+1$ for $x \geq 1$ is continuous at $x=1$.
**Answer:** Continuity requires $\lim_{x\to1^-} f(x) = f(1)$. The left-hand limit uses the $x<1$ branch: $1^2-1 = 0$. The value $f(1)$ uses the $x\geq1$ branch: $c+1$. So $0 = c+1$, giving $c = -1$.

## Q055
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** continuity
**Focus Area:** domain language
**Question:** Is $1/x$ discontinuous at $0$? Answer using the notes' "domain language" remark.
**Answer:** No — the question is not well-posed. $1/x$ is continuous on its domain $\mathbb{R}\setminus\{0\}$. It is not meaningful to say it is continuous *or* discontinuous at 0, because 0 is not in its domain. Continuity at a point is only defined at points of the domain.

## Q056
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** continuity
**Focus Area:** where to check a piecewise function
**Question:** For a piecewise-defined function, where can discontinuities occur, and what three quantities must you compare there?
**Answer:** Possible discontinuities occur at the junctions between branches. At each junction you check the two one-sided limits and the assigned function value there.

## Q057
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** intermediate-value-theorem
**Focus Area:** discrepancy between the two sources
**Question:** The two sources state the IVT's conclusion differently. Identify the difference in where $c$ is located, and in what each requires of $N$.
**Answer:** `limits.pdf` requires $f(a) \neq f(b)$ with $N$ **strictly** between $f(a)$ and $f(b)$, and concludes $a < c < b$ — strictly interior. `MATH275-Week01-Lecture-Notes.pdf` says $N$ "lies between" $f(a)$ and $f(b)$ and concludes $c \in [a,b]$ — endpoints permitted. The Week 1 version is consistent with its own worked example, where equality of the parameter gives the endpoint root $x=1$. The wiki records both and flags that you should confirm which convention your course uses.

## Q058
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** intermediate-value-theorem
**Focus Area:** root-finding recipe
**Question:** State the three-step recipe the Week 1 notes give for using the IVT to show a root exists, and the two things the theorem does not provide.
**Answer:** Apply the theorem to $f(c)=0$: (1) verify continuity, (2) compute endpoint signs, (3) conclude existence. The theorem does not give the root, and does not claim uniqueness.

## Q059
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** intermediate-value-theorem
**Focus Area:** parameter threshold from endpoint data
**Question:** For which $A$ does the IVT guarantee that $Axe^{2x}-3=0$ has a solution in $[0,1]$? Give both directions of the argument.
**Answer:** Let $g_A(x) = Axe^{2x}-3$, continuous on $[0,1]$ for every real $A$. *Sufficiency:* if $A \geq 3e^{-2}$ then $g_A(0) = -3 < 0$ and $g_A(1) = Ae^2-3 \geq 0$, so IVT gives a root. *Necessity:* for $0 \leq x \leq 1$ we have $0 \leq xe^{2x} \leq e^2$; if $A \leq 0$ then $g_A(x) \leq -3 < 0$, and if $0 < A < 3e^{-2}$ then $g_A(x) \leq Ae^2-3 < 0$ — so no root exists. The exact range is $A \geq 3e^{-2}$.

## Q060
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** intermediate-value-theorem
**Focus Area:** endpoint sufficiency vs. necessity
**Question:** In the $Axe^{2x}-3$ problem, why is checking the endpoint values not enough to determine the exact range of $A$?
**Answer:** The endpoint check only produces a *sufficient* condition — it shows the IVT applies when $A \geq 3e^{-2}$, but says nothing about smaller $A$. Ruling those out needs a separate bounding argument over the whole interval ($0 \leq xe^{2x} \leq e^2$ on $[0,1]$), which shows $g_A(x) < 0$ everywhere when $A < 3e^{-2}$. The notes' instruction reflects this two-part structure: after obtaining a sufficient condition from the endpoints, determine whether any smaller value of $A$ can work.

## Q061
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** sequential-criterion
**Focus Area:** statement of the sequential test
**Question:** State the sequential criterion for limits, including the conditions on the sequence.
**Answer:** If $\lim_{x\to a} f(x) = L$, then every sequence $x_n \to a$ contained in the domain of $f$ with $x_n \neq a$ must satisfy $f(x_n) \to L$.

## Q062
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** sequential-criterion
**Focus Area:** use via the contrapositive
**Question:** The sequential criterion is stated as a necessary condition. How is it actually used, and why is that form the useful one?
**Answer:** Through its contrapositive: if you can find two sequences approaching $a$ whose output sequences approach different numbers, the limit cannot exist. This is useful because proving a limit exists requires checking all sequences, whereas disproving it requires only two well-chosen ones.

## Q063
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** sequential-criterion
**Focus Area:** disproving a limit with two sequences
**Question:** Use the sequential criterion to prove $\lim_{x\to0}\sin\left(\frac{1}{x}\right)$ does not exist. Why does killing the right-hand limit suffice?
**Answer:** Take $x_n = \frac{1}{2\pi n + \pi/2}$ and $y_n = \frac{1}{2\pi n + 3\pi/2}$. Both tend to $0^+$, while $\sin(1/x_n) = 1$ and $\sin(1/y_n) = -1$. If the right-hand limit existed, the sequential test would force both output sequences to approach the same number; they do not, so the right-hand limit fails to exist. Since a two-sided limit requires both one-sided limits to exist and agree, the two-sided limit fails as well.

## Q064
**Status:** active
**Type:** mcq
**Difficulty:** intermediate
**Topic:** sequential-criterion
**Focus Area:** choosing the sequences
**Question:** In the proof that $\lim_{x\to0}\sin(1/x)$ DNE, why are $x_n = \frac{1}{2\pi n+\pi/2}$ and $y_n = \frac{1}{2\pi n+3\pi/2}$ chosen? (a) They are the only sequences tending to 0; (b) They make $1/x_n$ land on sine's peaks and $1/y_n$ on its troughs, forcing outputs of $+1$ and $-1$; (c) They tend to 0 from opposite sides; (d) They make $\sin(1/x)$ undefined.
**Answer:** (b). $1/x_n = 2\pi n + \pi/2$ gives $\sin = 1$ and $1/y_n = 2\pi n + 3\pi/2$ gives $\sin = -1$. Note (c) is wrong — the notes state both sequences tend to $0^+$, the same side.

## Q065
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** continuity
**Focus Area:** exit check
**Question:** Complete the Week 1 exit check: (1) A two-sided limit exists exactly when ___; (2) when $x\to-\infty$, $\sqrt{x^2} = $ ___; (3) the squeeze theorem needs ___; (4) continuity at a piecewise junction requires ___; (5) before using the IVT, I must state ___.
**Answer:** (1) the left- and right-hand limits both exist and are equal; (2) $|x| = -x$; (3) an inequality $g \leq f \leq h$ holding near $a$ with both outer functions approaching the same $L$; (4) that the two one-sided limits and the assigned function value at the junction all agree; (5) the hypotheses — continuity on the closed interval and that $N$ lies between the endpoint values.
