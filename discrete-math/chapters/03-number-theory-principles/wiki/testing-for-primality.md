# Testing for Primality

## Definition

**Trial Division.** If n is a composite integer, then n has a prime divisor less than or equal to √n. This means to check if n is prime, we only need to test whether it is divisible by prime numbers less than or equal to √n — not every number.
> Source: Testing for Primality.html

(Reminder: a **prime number** is an integer greater than 1 that is divisible only by 1 and itself; if it has any other divisor, it is composite.)
> Source: Testing for Primality.html

## Key Concepts

- **The purpose:** Primality testing determines whether a large number is prime *without* fully factoring it.
  > Source: Testing for Primality.html
- **The rule:** If we find a divisor (other than 1 and itself), the number is composite; if we find none up to √n, the number is prime.
  > Source: Testing for Primality.html
- **Efficiency limits:** Trial division is not efficient for very large numbers, but it is the foundation for understanding more advanced primality tests used in computing and cryptography.
  > Source: Testing for Primality.html

## Step-by-Step: Trial Division Method

1. Start with a number n (greater than 1).
2. Find all prime numbers less than or equal to √n.
3. Check divisibility of n by each of these primes.
4. If any prime divides n evenly, n is composite.
5. If none divide n, n is prime.
> Source: Testing for Primality.html

## Examples

- **Is 101 prime?** √101 ≈ 10.05, so check primes 2, 3, 5, 7. None divide 101 evenly → **101 is prime**.
  > Source: Testing for Primality.html
- **Is 221 prime?** √221 ≈ 14.86, so check 2, 3, 5, 7, 11, 13. 221 ÷ 13 = 17 → **221 = 13 × 17 is composite**.
  > Source: Testing for Primality.html
- **Is 9,973,969 prime?** Trial division would require testing every prime up to √9,973,969 ≈ 3,157 — hundreds of primes. It is composite (3163 × 3155 per the source), illustrating why trial division is impractical for very large numbers.
  > Source: Testing for Primality.html
- **37:** prime, because no prime ≤ √37 divides it evenly.
  > Source: Testing for Primality.html
- **91:** composite, because 91 = 7 × 13.
  > Source: Testing for Primality.html
- **113:** prime, because no prime ≤ √113 divides it evenly.
  > Source: Testing for Primality.html

## Related Topics
- [Prime, Composite, and Relatively Prime Numbers](prime-composite-relatively-prime.md)
- [The Fundamental Theorem of Arithmetic](fundamental-theorem-of-arithmetic.md)
- [Divisibility and the Division Algorithm](divisibility-and-division-algorithm.md)
