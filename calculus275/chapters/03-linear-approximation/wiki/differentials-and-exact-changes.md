# Differentials and Exact Changes

## Definition
Here the notation shifts: x now denotes the current input (the role played by a earlier), and
x + Δx is the new input. Suppose f is differentiable at this current input. Always compute a
signed change as new minus old. The exact changes are

    Δx = (x + Δx) − x,      Δy = f(x + Δx) − f(x).

Set dx = Δx. The corresponding differential is

    dy = f'(x) dx.
> Source: MATH275-Week03-Lecture-Notes.pdf

Given y = f(x), let Δx denote a (small) change in x. Then Δy = f(x + Δx) − f(x) is the exact
change in y given Δx. Setting dx = Δx gives dy = (dy/dx)Δx = f'(x)Δx, and hence the
**differential approximation** Δy ≈ f'(x)Δx.
> Source: Week 2 Video - Linear Approximation and Differentials .pdf

## Key Concepts
- **dx is chosen, not unknown.** dx is the chosen input change, not an additional unknown and
  not necessarily positive.
  > Source: MATH275-Week03-Lecture-Notes.pdf
- **Evaluate the derivative at the old input.** Evaluate f'(x) at the old input.
  > Source: MATH275-Week03-Lecture-Notes.pdf
- **What is exact and what is approximate.** The equation defining dy is exact: it is the change
  along the tangent line. Only the replacement of the curve's change Δy by dy is approximate.
  For small Δx, Δy ≈ dy = f'(x)Δx.
  > Source: MATH275-Week03-Lecture-Notes.pdf
- **Geometric reading.** Since dy/dx is the slope of the tangent (rise/run), dy can be thought of
  as the "rise" of the tangent line over the "run" dx. In the picture, Δy is the rise along the
  curve from f(x) to f(x + Δx), while dy is the rise along the tangent line over the same Δx = dx.
  > Source: Week 2 Video - Linear Approximation and Differentials .pdf
- **Why dy ≈ Δy.** Since the tangent line is the best linear approximation to f near x, dy ≈ Δy,
  and this approximation improves for smaller Δx.
  > Source: Week 2 Video - Linear Approximation and Differentials .pdf
- **Key idea of the method.** Differential approximation is about approximating the change in
  output of a function given a fixed input change.
  > Source: Week 2 Video - Linear Approximation and Differentials .pdf
- **Same statement as linear approximation.** Applying linear approximation at the current input
  x to the new input x + Δx gives f(x + Δx) ≈ f(x) + f'(x)Δx; after subtracting f(x) this becomes
  Δy ≈ f'(x)Δx = dy.
  > Source: MATH275-Week03-Lecture-Notes.pdf

## Examples
- **CORE — estimate a change rather than a new value.** Let S(t) = 80/(t + 4). Estimate the
  change in S when t increases from 6 to 6.05. The old input is t = 6, so dt = 6.05 − 6 = 0.05.
  Using S(t) = 80(t + 4)^(−1) gives S'(t) = −80/(t + 4)², so S'(6) = −0.8. Therefore
  ΔS ≈ dS = S'(6) dt = (−0.8)(0.05) = −0.04. The sign says that the output decreases. This is a
  change, not the new output: S(6) = 80/10 = 8, so S(6.05) ≈ 8 − 0.04 = 7.96. For comparison, the
  exact change is 80/10.05 − 8 = −8/201 ≈ −0.03980, close to the differential estimate.
  > Source: MATH275-Week03-Lecture-Notes.pdf

## Common Misconceptions
- **Reporting the estimated change as the new output.** dS is a change, not the new output; the
  new output is the old output plus the estimated change.
  > Source: MATH275-Week03-Lecture-Notes.pdf

## Related Topics
- [Linear Approximation](linear-approximation.md)
- [Best Linear Approximation](best-linear-approximation.md)
- [Relative Change and Percentage Error](relative-change-and-percentage-error.md)
- [Applied Differential Problems](applied-differential-problems.md)
