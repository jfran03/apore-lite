# Greatest Common Divisor (GCD) and Least Common Multiple (LCM)

## Definition

**Greatest Common Divisor (GCD).** For two integers a and b (not both zero), the GCD, written `gcd(a, b)`, is the largest positive integer that divides both a and b evenly.
> Source: Greatest Common Divisor (GCD) and Least Common Multiple (LCM).html

**Least Common Multiple (LCM).** For two positive integers a and b, the LCM, written `lcm(a, b)`, is the smallest positive integer that is a multiple of both a and b.
> Source: Greatest Common Divisor (GCD) and Least Common Multiple (LCM).html

## Key Concepts

- **GCD looks at shared factors; LCM looks at shared multiples.** GCD captures how two numbers overlap in their factors; LCM stretches to their common ground in multiples.
  > Source: Greatest Common Divisor (GCD) and Least Common Multiple (LCM).html
- **The GCD–LCM relationship:** `gcd(a, b) × lcm(a, b) = a × b` for any two positive integers. This lets you find one value when you know the other: `lcm(a, b) = (a × b) / gcd(a, b)` and `gcd(a, b) = (a × b) / lcm(a, b)`.
  > Source: Greatest Common Divisor (GCD) and Least Common Multiple (LCM).html
- **Connection to relatively prime numbers:** If gcd(a, b) = 1, then a and b are relatively prime (e.g., gcd(8, 15) = 1).
  > Source: Greatest Common Divisor (GCD) and Least Common Multiple (LCM).html

## Finding GCD and LCM Using Prime Factorization

Process: (1) Write each number as a product of primes. (2) For the **GCD**, take the *lowest* powers of all primes that appear in *both* numbers. (3) For the **LCM**, take the *highest* powers of all primes that appear in *either* number.
> Source: Greatest Common Divisor (GCD) and Least Common Multiple (LCM).html

## Examples

- **gcd(24, 36):** common factors {1, 2, 3, 4, 6, 12} → gcd = 12.
  > Source: Greatest Common Divisor (GCD) and Least Common Multiple (LCM).html
- **lcm(4, 6):** common multiples {12, 24, 36, …} → lcm = 12.
  > Source: Greatest Common Divisor (GCD) and Least Common Multiple (LCM).html
- **48 and 180 by prime factorization:** 48 = 2⁴ × 3, 180 = 2² × 3² × 5. GCD uses lowest powers: 2² × 3 = 12. LCM uses highest powers: 2⁴ × 3² × 5 = 720. Check: 12 × 720 = 8640 = 48 × 180. ✅
  > Source: Greatest Common Divisor (GCD) and Least Common Multiple (LCM).html
- **12 and 18:** gcd = 6, lcm = 36. Check: 6 × 36 = 216 = 12 × 18. ✅
  > Source: Greatest Common Divisor (GCD) and Least Common Multiple (LCM).html
- **gcd(18, 30) = 6** (6 divides both and no larger number does).
  > Source: Greatest Common Divisor (GCD) and Least Common Multiple (LCM).html
- **lcm(6, 8) = 24** (smallest number divisible by both 6 and 8).
  > Source: Greatest Common Divisor (GCD) and Least Common Multiple (LCM).html

## Related Topics
- [The Fundamental Theorem of Arithmetic](fundamental-theorem-of-arithmetic.md)
- [Prime, Composite, and Relatively Prime Numbers](prime-composite-relatively-prime.md)
- [The Euclidean Algorithm](euclidean-algorithm.md)
