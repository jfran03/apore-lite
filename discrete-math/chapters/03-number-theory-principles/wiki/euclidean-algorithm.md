# The Euclidean Algorithm

## Definition

The **Euclidean Algorithm** is a method, first described by Euclid around 300 BCE, that uses division and remainders to find the greatest common divisor (GCD) of two integers — instead of listing all factors.
> Source: The Euclidean Algorithm.html

## Key Concepts

- **Core idea:** When we divide one integer by another we get `a = bq + r`, where a is the dividend, b the divisor, q the quotient, and r the remainder. If r = 0, then b divides a evenly and gcd(a, b) = b. If r ≠ 0, we continue with the smaller pair (b and r).
  > Source: The Euclidean Algorithm.html
- **Lemma 1 (the foundation):** If `a = bq + r`, then `gcd(a, b) = gcd(b, r)`. Any number that divides both a and b also divides r = a − bq, and conversely, so the common divisors of (a, b) and (b, r) are exactly the same — their GCDs are equal.
  > Source: The Euclidean Algorithm.html
- **Why it works:** Each application of the lemma simplifies the problem — the numbers get smaller but the GCD stays the same.
  > Source: The Euclidean Algorithm.html

## Step-by-Step Process

1. Divide the larger number by the smaller number.
2. Record the quotient and remainder.
3. Replace the larger number with the smaller one, and the smaller one with the remainder.
4. Repeat until the remainder is 0. The **last nonzero remainder is the GCD**.
> Source: The Euclidean Algorithm.html

## Examples

- **gcd(30, 12):** 30 = 12 × 2 + 6, so by Lemma 1 gcd(30, 12) = gcd(12, 6) = 6. (Confirmed directly: common factors of 30 and 12 are {1, 2, 3, 6}.)
  > Source: The Euclidean Algorithm.html
- **gcd(662, 414):** 662 = 414×1 + 248; 414 = 248×1 + 166; 248 = 166×1 + 82; 166 = 82×2 + 2; 82 = 2×41 + 0. Last nonzero remainder = 2, so gcd(662, 414) = 2.
  > Source: The Euclidean Algorithm.html
- **gcd(252, 198):** 252 = 198×1 + 54; 198 = 54×3 + 36; 54 = 36×1 + 18; 36 = 18×2 + 0. gcd = 18.
  > Source: The Euclidean Algorithm.html
- **gcd(420, 196):** 420 = 196×2 + 28; 196 = 28×7 + 0. gcd = 28.
  > Source: The Euclidean Algorithm.html

## Related Topics
- [Greatest Common Divisor (GCD) and Least Common Multiple (LCM)](gcd-and-lcm.md)
- [Bézout's Identity](bezouts-identity.md)
- [The Extended Euclidean Algorithm](extended-euclidean-algorithm.md)
