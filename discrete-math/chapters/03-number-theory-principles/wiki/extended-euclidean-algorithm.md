# The Extended Euclidean Algorithm

## Definition

The **Extended Euclidean Algorithm** not only finds the GCD of two integers but also produces the Bézout coefficients s and t such that `gcd(a, b) = s·a + t·b`. It combines the Euclidean Algorithm with Bézout's Identity.
> Source: The Extended Euclidean Algorithm.html

## Key Concepts

- **What it produces:** three things — the GCD of a and b, the coefficient s (multiplier for a), and the coefficient t (multiplier for b). These coefficients are exactly the integers from Bézout's Identity.
  > Source: The Extended Euclidean Algorithm.html
- **Recurrence relations:** While running the Euclidean Algorithm, also compute `sᵢ = sᵢ₋₂ − qᵢ·sᵢ₋₁` and `tᵢ = tᵢ₋₂ − qᵢ·tᵢ₋₁`, starting with `s₀ = 1, s₁ = 0` and `t₀ = 0, t₁ = 1`. The final s and t give the Bézout coefficients.
  > Source: The Extended Euclidean Algorithm.html
- **Tabular form:** Each row corresponds to one step, tracking a, b, q, r, s, and t. At the final nonzero remainder, the matching s and t values show how to write the GCD as a linear combination. This is how computers implement the algorithm.
  > Source: The Extended Euclidean Algorithm.html
- **gcd = 1 signals coprime numbers:** When the algorithm yields gcd = 1, the two numbers are relatively prime — a key condition in modular arithmetic and encryption.
  > Source: The Extended Euclidean Algorithm.html

## Examples

- **gcd(240, 46):** Euclidean steps: 240 = 46×5 + 10; 46 = 10×4 + 6; 10 = 6×1 + 4; 6 = 4×1 + 2; 4 = 2×2 + 0, so gcd = 2. Back-substituting gives `2 = (−9)×240 + 47×46`, so s = −9, t = 47.
  > Source: The Extended Euclidean Algorithm.html
- **gcd(99, 78):** Euclidean steps reduce to gcd = 3, and working backward gives `3 = (−11)×99 + 14×78`, so s = −11, t = 14.
  > Source: The Extended Euclidean Algorithm.html
- **gcd(85, 32):** Euclidean steps reduce to gcd = 1, and working backward gives `1 = (−3)×85 + 8×32`, so s = −3, t = 8. Because gcd = 1, 85 and 32 are relatively prime.
  > Source: The Extended Euclidean Algorithm.html

## Related Topics
- [The Euclidean Algorithm](euclidean-algorithm.md)
- [Bézout's Identity](bezouts-identity.md)
- [Modular Inverses](modular-inverses.md)
- [Modern Applications of Number Theory](modern-applications.md)
