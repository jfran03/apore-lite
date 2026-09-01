# Bézout's Identity

## Definition

**Bézout's Identity.** For any integers a and b (not both zero), there exist integers s and t such that `gcd(a, b) = s·a + t·b`. The numbers s and t are called **Bézout coefficients**. They are not unique, but any valid pair produces the same GCD.
> Source: Bézout's Identity.html

## Key Concepts

- **Linear combination:** A linear combination of two integers a and b is any number of the form `s·a + t·b`, where s and t are integers (positive, negative, or zero).
  > Source: Bézout's Identity.html
- **Connection to the Euclidean Algorithm:** Bézout's Identity is a direct result of the Euclidean Algorithm. Each division step `a = bq + r` can be rewritten as `r = a − bq`; substituting backward through the steps expresses the GCD entirely in terms of a and b.
  > Source: Bézout's Identity.html
- **Coefficients are not unique:** For a = 6, b = 9, both (s, t) = (2, −1) and (−1, 1) give 3 = gcd(6, 9).
  > Source: Bézout's Identity.html

## Examples

- **a = 6, b = 9:** Trying integer values of s and t: (1,1)→15, (2,−1)→5... and (2,−1) and (−1,1) both yield 3, which is gcd(6, 9). *(Note: the source's worked table lists these results while stating the coefficients (2,−1) and (−1,1) reproduce the gcd of 3.)*
  > Source: Bézout's Identity.html
- **gcd(252, 198) = 18 as a linear combination:** Run the Euclidean Algorithm (252 = 198×1 + 54; 198 = 54×3 + 36; 54 = 36×1 + 18; 36 = 18×2 + 0), then work backward: 18 = 54 − 36; substitute 36 = 198 − 54×3, then 54 = 252 − 198, giving `18 = 4 × 252 − 5 × 198`. Here s = 4, t = −5.
  > Source: Bézout's Identity.html

## Related Topics
- [The Euclidean Algorithm](euclidean-algorithm.md)
- [The Extended Euclidean Algorithm](extended-euclidean-algorithm.md)
- [Modular Inverses](modular-inverses.md)
