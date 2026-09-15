# Choosing the Expansion Point

## Definition
A useful expansion point a should satisfy two conditions:
- a is close to the input of interest;
- both f(a) and f'(a) are easy to compute.
> Source: MATH275-Week03-Lecture-Notes.pdf

To estimate f(x), find an a close to x so that f(a) and f'(a) are easy to compute, then use the
linear approximation.
> Source: Week 2 Video - Linear Approximation and Differentials .pdf

## Key Concepts
- **Closeness alone is not enough** if it leaves the same difficult calculation inside f(a) or f'(a).
  > Source: MATH275-Week03-Lecture-Notes.pdf
- **Choose the centre before differentiating.** Pick a first, then compute f(a) and f'(a) at it.
  > Source: MATH275-Week03-Lecture-Notes.pdf
- **Convenient base inputs come from known exact values.** a = 1 is convenient for arctan because
  tan(π/4) = 1; a = 16 is convenient for the fourth root because the fourth root of 16 is 2;
  a = π/4 is convenient for sec because sec(π/4) = 1/cos(π/4) = √2.
  > Source: MATH275-Week03-Lecture-Notes.pdf
  > Source: Week 2 Video - Linear Approximation and Differentials .pdf

## Examples
- **In class — estimate 1/4.08.** For f(x) = 1/x, choose a = 4. Rewrite f(x) = x^(−1), so
  f'(x) = −x^(−2). Thus f(4) = 1/4, f'(4) = −1/16, and the input change is 4.08 − 4 = 0.08. Then
  L_4(x) = 1/4 − (1/16)(x − 4), so 1/4.08 ≈ L_4(4.08) = 1/4 − 0.08/16 = 0.245. Choosing a = 4.1
  would be closer, but it would not simplify the starting value.
  > Source: MATH275-Week03-Lecture-Notes.pdf

## Common Misconceptions
- **Picking the closest possible a regardless of arithmetic.** a = 4.1 is closer to 4.08 than
  a = 4 is, but it does not simplify the starting value, so a = 4 is the better choice.
  > Source: MATH275-Week03-Lecture-Notes.pdf
- **Expecting the method to always pay off.** If the differential still contains a value that is
  just as hard to compute as the original expression, the approximation may offer little
  practical benefit. The method is valuable when f(x) and f'(x) are simple at the chosen base
  point while the nearby exact value is difficult.
  > Source: MATH275-Week03-Lecture-Notes.pdf

## Related Topics
- [Linear Approximation](linear-approximation.md)
- [Best Linear Approximation](best-linear-approximation.md)
- [Applied Differential Problems](applied-differential-problems.md)
