# Fundamental Theorem of Calculus, Part I

## Definition
For a continuous function f, define its **accumulation function** (also called the **area function**) by A(x) = ∫ₐˣ f(t) dt. The input is x; the variable t only labels points inside the integral. A(x) is the area under f from a up to x.
> Source: MATH275-Week08-Lecture-Notes.pdf, Week of October 23.pdf

**FTC Part I:** If f is continuous on [a, b], then A(x) = ∫ₐˣ f(t) dt is continuous on [a, b], differentiable on (a, b), and
A′(x) = f(x).
In particular, A is an antiderivative of f, and A(a) = 0.
> Source: MATH275-Week08-Lecture-Notes.pdf

(The handwritten notes state the conclusion as "F is differentiable on [a, b] and F′(x) = f(x), i.e. F *is* an antiderivative for f." The typed lecture notes give the more precise statement above: continuous on [a, b], differentiable on (a, b).)
> Source: Week of October 23.pdf, MATH275-Week08-Lecture-Notes.pdf

## Key Concepts
- **Interpretation:** differentiation and integration are inverse operations to each other.
  > Source: Week of October 23.pdf
- **Why it works (intuition):** by additivity, F(x + h) − F(x) = ∫ₐˣ⁺ʰ f(t) dt − ∫ₐˣ f(t) dt = ∫ₐˣ⁺ʰ f(t) dt + ∫ₓᵃ f(t) dt = ∫ₓˣ⁺ʰ f(t) dt. For small h this area is close to the area of a rectangle with base h and height f(x), so F(x + h) − F(x) ≈ h f(x), giving (F(x + h) − F(x))/h ≈ f(x). Letting h → 0 gives F′(x) = f(x).
  > Source: Week of October 23.pdf
- **Why it works (precise):** for small h ≠ 0, (A(x + h) − A(x))/h = (1/h)∫ₓˣ⁺ʰ f(t) dt, the average value of f on the short interval between x and x + h (same interpretation when h < 0). With Iₕ the interval with endpoints x and x + h:
  |(1/h)∫ₓˣ⁺ʰ f(t) dt − f(x)| = |(1/h)∫ₓˣ⁺ʰ (f(t) − f(x)) dt| ≤ (1/|h|)∫_{Iₕ} |f(t) − f(x)| dt ≤ max_{t∈Iₕ} |f(t) − f(x)| → 0 by continuity. Therefore the difference quotient tends to f(x).
  > Source: MATH275-Week08-Lecture-Notes.pdf
- **Three different operations:**
  1. ∫ f(x) dx asks for a family of antiderivatives.
  2. ∫ₐᵇ f(t) dt with fixed a, b is a constant, so its derivative with respect to x is 0.
  3. d/dx ∫ₐˣ f(t) dt = f(x) differentiates an accumulation function. The answer does not include + C.
  > Source: MATH275-Week08-Lecture-Notes.pdf
- **No need to evaluate the integral:** FTC I gives the derivative directly, even when no elementary antiderivative of the integrand is available.
  > Source: Week of October 23.pdf, MATH275-Week08-Lecture-Notes.pdf

## Examples
- y = ∫₃ˣ cos(t²) dt. We do *not* need to compute the integral; FTC I directly implies dy/dx = cos(x²).
  > Source: Week of October 23.pdf
- A(x) = ∫₁ˣ cos(t³) dt. The integrand is continuous on ℝ, so FTC I gives A′(x) = cos(x³). By the chain rule, A″(x) = −3x² sin(x³). Finally A(1) = 0 because the integration limits coincide. No elementary antiderivative of cos(t³) is needed.
  > Source: MATH275-Week08-Lecture-Notes.pdf

## Common Misconceptions
- Adding + C to d/dx ∫ₐˣ f(t) dt: the answer is exactly f(x), with no constant.
  > Source: MATH275-Week08-Lecture-Notes.pdf
- Treating ∫ₐᵇ f(t) dt (fixed limits) as a function of x: it is a constant, so its x-derivative is 0.
  > Source: MATH275-Week08-Lecture-Notes.pdf

## Related Topics
- [Antiderivatives](antiderivatives.md)
- [Variable Limits and the Chain Rule](variable-limits.md)
- [Reading an Accumulation Function from a Graph](accumulation-graphs.md)
