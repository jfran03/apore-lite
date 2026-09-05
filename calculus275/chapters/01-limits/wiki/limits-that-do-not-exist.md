# Limits That Do Not Exist

## Definition

If no finite `L` exists satisfying the limit definition — two-sided or one-sided — we say the limit **does not exist** (DNE).
> Source: limits.pdf

## Key Concepts

- **Two distinct failure modes appear in the source:** oscillation (the function never settles near any one value) and divergence to infinity (the function grows without bound).
  > Source: limits.pdf

- **"DNE" and "is infinity" are not the same statement.** The source writes $\lim_{x \to 0^+} \frac{1}{x}$ **DNE** and annotates it "(is infinity)" — the limit fails to exist as a finite number, and the reason is that it diverges.
  > Source: limits.pdf

## Examples

- **Oscillation — the "topologist's sine curve."**
  $$\lim_{x \to 0^+} \sin\left(\tfrac{1}{x}\right) \text{ DNE} \quad \text{and} \quad \lim_{x \to 0^-} \sin\left(\tfrac{1}{x}\right) \text{ DNE}$$

  The source labels this curve the "topologist's sine curve." The accompanying graph shows the function oscillating between `1` and `-1` with the oscillations compressing without bound as `x` approaches `0` from either side.

  Note that **both** one-sided limits fail here — the failure is not a mismatch between two sides, it is that neither side approaches anything.
  > Source: limits.pdf

- **Divergence.**
  $$\lim_{x \to 0^+} \frac{1}{x} \text{ DNE} \quad \text{(is infinity)}$$

  The graph shows `f(x) = 1/x` rising without bound as `x` decreases toward `0` from the right.
  > Source: limits.pdf

## Added from MATH275-Week01-Lecture-Notes.pdf

- **A rigorous tool for proving non-existence.** `limits.pdf` asserts that $\lim_{x\to 0^{\pm}}\sin(1/x)$ DNE on graphical grounds. The Week 1 notes supply an actual proof via the sequential criterion — see [The Sequential Criterion for Limits](sequential-criterion.md).
  > Source: MATH275-Week01-Lecture-Notes.pdf

- **Disagreement of one-sided limits as a failure mode.** In addition to oscillation and divergence, the Week 1 notes work an example whose limit fails because the two one-sided limits are $-1$ and $1$ — see the conjugate example in [Computing Finite Limits](computing-finite-limits.md).
  > Source: MATH275-Week01-Lecture-Notes.pdf

## Related Topics

- [One-Sided Limits](one-sided-limits.md)
- [The Sequential Criterion for Limits](sequential-criterion.md)
- [Computing Finite Limits](computing-finite-limits.md)
- [Infinite Limits and Vertical Asymptotes](infinite-limits.md)
- [The Squeeze Theorem](squeeze-theorem.md)
