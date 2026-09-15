# Taylor's Remainder Bound

## Definition
An approximation sign does not by itself say how close the values are. Suppose f is twice
differentiable on an open interval containing the closed segment joining a and x, and
|f''(t)| ≤ M for every t in that closed segment. Taylor's remainder estimate gives

    |f(x) − L_a(x)| ≤ (M/2)|x − a|².
> Source: MATH275-Week03-Lecture-Notes.pdf

## Key Concepts
- **Where the bound comes from.** Taylor's theorem states that, when x ≠ a,
  f(x) − L_a(x) = f''(ξ)(x − a)²/2 for some point ξ strictly between a and x. We usually do not
  know ξ, so we bound |f''| on the entire segment. Taking absolute values and using
  |f''(ξ)| ≤ M gives the bound.
  > Source: MATH275-Week03-Lecture-Notes.pdf
- **Quadratic dependence on the displacement.** The factor |x − a|² explains why halving the
  input displacement reduces this error bound by a factor of four, provided the same M is valid.
  > Source: MATH275-Week03-Lecture-Notes.pdf
- **How to choose M.** Write the interval with its smaller endpoint first, compute f'', and find
  a nonnegative number that bounds |f''(t)| everywhere on that interval.
  > Source: MATH275-Week03-Lecture-Notes.pdf
- **A ceiling, not the error.** The bound is a ceiling on the error, not its exact value; to
  certify a requested tolerance, check that (M/2)|x − a|² is no larger than that tolerance.
  > Source: MATH275-Week03-Lecture-Notes.pdf
- **M need not be sharp.** Any valid upper bound works; it need not be the smallest possible one.
  > Source: MATH275-Week03-Lecture-Notes.pdf

## Examples
- **ANALYSIS — certify an approximation to ln(1.04).** For f(x) = ln x, f'(x) = 1/x, so f(1) = 0
  and f'(1) = 1. Hence L_1(x) = x − 1 and ln(1.04) ≈ 0.04. The interval between the base and
  target inputs is [1, 1.04]. Here f''(t) = −1/t² < 0, so 0.04 is an overestimate. To bound the
  magnitude, note that t ≥ 1 implies t² ≥ 1, hence |f''(t)| = 1/t² ≤ 1. Choosing M = 1 gives
  |ln(1.04) − 0.04| ≤ (1/2)(0.04)² = 0.0008. Combining the error bound with the overestimate
  gives the certified interval 0.04 − 0.0008 ≤ ln(1.04) ≤ 0.04, that is,
  0.0392 ≤ ln(1.04) ≤ 0.04.
  > Source: MATH275-Week03-Lecture-Notes.pdf
- **Error bound for e^(−0.03).** Using L_0(x) = 1 + x, e^(−0.03) ≈ 0.97. On [−0.03, 0], t ≤ 0
  implies |f''(t)| = e^t ≤ e^0 = 1. Thus M = 1 is valid, and
  |e^(−0.03) − 0.97| ≤ (1/2)(0.03)² = 0.00045.
  > Source: MATH275-Week03-Lecture-Notes.pdf

## Common Misconceptions
- **Using |f''(a)| as M without checking the interval.** Use |f''(a)| for M only after showing
  that it bounds |f''| throughout the segment joining a and x. The bound must cover the whole
  interval.
  > Source: MATH275-Week03-Lecture-Notes.pdf

## Related Topics
- [Linear Approximation](linear-approximation.md)
- [Overestimates and Underestimates](overestimates-and-underestimates.md)
