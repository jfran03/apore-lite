# Linear Approximation

## Definition
If f is differentiable at a, its tangent line at (a, f(a)) is

    L_a(x) = f(a) + f'(a)(x − a)

and for x close to a, f(x) ≈ L_a(x).
> Source: MATH275-Week03-Lecture-Notes.pdf

The tangent line for f at x = a is given by y − f(a) = f'(a)(x − a), rewritten in function
notation as L(x) = f(a) + f'(a)(x − a).
> Source: Week 2 Video - Linear Approximation and Differentials .pdf

## Key Concepts
- **Reading the formula:** a is the fixed base input, x is the target input, and x − a is the
  signed input change. The term f'(a)(x − a) estimates the change in output; adding f(a)
  estimates the new value. The subscript in L_a records the chosen base input.
  > Source: MATH275-Week03-Lecture-Notes.pdf
- **Why it works:** The derivative definition says that [f(x) − f(a)]/(x − a) approaches f'(a)
  as x → a. Thus, for nearby inputs, the actual change f(x) − f(a) is approximately f'(a)(x − a).
  > Source: MATH275-Week03-Lecture-Notes.pdf
- **Two properties determine the tangent line:** (i) it contains the point (a, f(a)); (ii) the
  rate of change of y = f(x) with respect to x at x = a is the slope of this line.
  > Source: Week 2 Video - Linear Approximation and Differentials .pdf
- **How to use it:** To estimate f(x), find an a close to x so that f(a) and f'(a) are easy to
  compute, then use L(x) ≈ f(x), provided x ≈ a — equivalently f(x) ≈ f(a) + f'(a)(x − a),
  where all three pieces are easy to compute.
  > Source: Week 2 Video - Linear Approximation and Differentials .pdf
- **Radians are required:** All trigonometric derivative formulas, and therefore their linear
  approximations, use radians.
  > Source: MATH275-Week03-Lecture-Notes.pdf
- **"Nearby" is not an accuracy statement:** "nearby" alone does not specify an accuracy; a
  separate argument is needed to certify that the error is within a desired tolerance.
  > Source: MATH275-Week03-Lecture-Notes.pdf

## Examples
- **CORE — approximate arctan(1.04)** by linearizing f(x) = arctan x at a = 1. This base input
  is convenient because tan(π/4) = 1, so arctan(1) = π/4. With f(1) = π/4, f'(x) = 1/(1 + x²)
  and f'(1) = 1/2, the input change is 1.04 − 1 = 0.04 and the estimated output change is
  (1/2)(0.04) = 0.02. Therefore L_1(x) = π/4 + (1/2)(x − 1) and arctan(1.04) ≈ π/4 + 0.02.
  > Source: MATH275-Week03-Lecture-Notes.pdf
- **Estimate the fourth root of 15.98.** Use f(x) = x^(1/4) with a = 16. Then f(16) = 2,
  f'(x) = (1/4)x^(−3/4) = 1/(4(x^(1/4))³), so f'(16) = 1/(4·2³) = 1/32. Since 15.98 ≈ 16,
  f(15.98) ≈ L(15.98) = f(16) + f'(16)[15.98 − 16] = 2 + (1/32)(−0.02) = 2 − 2/3200 = 2 − 1/1600.
  > Source: Week 2 Video - Linear Approximation and Differentials .pdf
- **Estimate sec(46°).** Since 180° = π rad, 1° = π/180 rad, so 46° = 46π/180 rad. Use
  f(x) = sec(x) with a = π/4: f(π/4) = sec(π/4) = 1/cos(π/4) = √2, and f'(x) = sec(x)tan(x),
  so f'(π/4) = √2 · 1 = √2. Then f(46π/180) ≈ L(46π/180) = √2 + √2(46π/180 − π/4) = √2 + √2(π/180).
  > Source: Week 2 Video - Linear Approximation and Differentials .pdf

## Common Misconceptions
- **Treating L_a as a global model.** The formula L_a(x) may be evaluated for any x, but
  differentiability alone gives only a local guarantee of accuracy. A large |x − a|, a rapidly
  changing slope, or a singularity between a and x can make the approximation poor. Check that
  f(x) is defined at the target input.
  > Source: MATH275-Week03-Lecture-Notes.pdf

## Related Topics
- [Best Linear Approximation](best-linear-approximation.md)
- [Choosing the Expansion Point](choosing-the-expansion-point.md)
- [Overestimates and Underestimates](overestimates-and-underestimates.md)
- [Taylor's Remainder Bound](taylors-remainder-bound.md)
- [Differentials and Exact Changes](differentials-and-exact-changes.md)
