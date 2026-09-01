# Modular Inverses

## Definition

**Modular Inverse.** The modular inverse of an integer a modulo m is an integer x such that `a × x ≡ 1 (mod m)`. That is, x is the number you multiply a by to get 1 modulo m, written `x = a⁻¹ (mod m)`.
> Source: Modular Inverses.html

## Key Concepts

- **Why modular division is tricky:** Modular arithmetic is based on integers and remainders, not real numbers — there are no fractions. Division only makes sense when multiplication can be undone, which requires an inverse c⁻¹ satisfying c × c⁻¹ ≡ 1 (mod m).
  > Source: Modular Inverses.html
- **Existence and uniqueness (theorem):** If a and m are relatively prime, i.e. `gcd(a, m) = 1`, then an inverse of a mod m exists and is unique modulo m. If `gcd(a, m) ≠ 1`, then no modular inverse exists.
  > Source: Modular Inverses.html
- **Division = multiplication by an inverse:** Division in modular arithmetic is really multiplication by an inverse, and that inverse only exists when the number and modulus are coprime.
  > Source: Modular Inverses.html
- **Finding inverses with the Extended Euclidean Algorithm:** For integers a and b, it finds s and t such that gcd(a, b) = sa + tb. If gcd(a, b) = 1, then s is the modular inverse of a mod b: `a⁻¹ ≡ s (mod b)`. This is the most efficient method for large numbers.
  > Source: Modular Inverses.html
- **Solving modular equations:** To solve `ax ≡ b (mod m)`, multiply both sides by a⁻¹ (if it exists): `x ≡ a⁻¹b (mod m)`.
  > Source: Modular Inverses.html

## Examples

- **Inverse exists — 3 mod 11:** Reducing multiples of 3 mod 11 gives 3, 6, 9, 1, …; since 3 × 4 ≡ 1 (mod 11), the inverse of 3 mod 11 is 4.
  > Source: Modular Inverses.html
- **No inverse — 3 mod 6:** Multiples of 3 reduce mod 6 to 3, 0, 3, 0, …; none gives remainder 1, so no inverse exists.
  > Source: Modular Inverses.html
- **gcd test — 4 mod 6:** gcd(4, 6) = 2 ≠ 1, so 4 has no inverse mod 6.
  > Source: Modular Inverses.html
- **Which has an inverse mod 12:** 5 does, because gcd(5, 12) = 1.
  > Source: Modular Inverses.html
- **Large case — 101 mod 4620:** The Euclidean Algorithm shows gcd(101, 4620) = 1; back-substitution gives 1 = 1601×101 − 35×4620, so 101⁻¹ ≡ 1601 (mod 4620).
  > Source: Modular Inverses.html
- **Solving 4x ≡ 5 (mod 7):** 4⁻¹ ≡ 2 (mod 7) since 4 × 2 = 8 ≡ 1; so x ≡ 2 × 5 ≡ 10 ≡ 3 (mod 7).
  > Source: Modular Inverses.html

## Summary

- A modular inverse exists only if gcd(a, m) = 1.
- It satisfies a × a⁻¹ ≡ 1 (mod m).
- The Extended Euclidean Algorithm is the most efficient way to find it.
> Source: Modular Inverses.html

## Related Topics
- [Congruences and Their Properties](congruences-and-properties.md)
- [The Extended Euclidean Algorithm](extended-euclidean-algorithm.md)
- [Prime, Composite, and Relatively Prime Numbers](prime-composite-relatively-prime.md)
- [Modern Applications of Number Theory](modern-applications.md)
