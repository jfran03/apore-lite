# Congruences and Their Properties

## Definition

**Congruence.** If a and b are integers and m is a positive integer, then a is **congruent to b modulo m** if m divides (a − b). We write `a ≡ b (mod m)`. If they are not congruent, we write `a ≢ b (mod m)`. Here m is the **modulus**.
> Source: Congruences and Their Properties.html

## Key Concepts

- **What it means:** `a ≡ b (mod m)` means a and b have the same remainder when divided by m. Example: 17 ≡ 5 (mod 12) because both leave remainder 5, and 17 − 5 = 12 is divisible by 12.
  > Source: Congruences and Their Properties.html
- **Three equivalent conditions:** The following all describe the same relationship — (1) m divides (a − b); (2) a mod m = b mod m; (3) there exists an integer k such that a = b + km.
  > Source: Congruences and Their Properties.html
- **Operations on congruences (theorem):** If `a ≡ b (mod m)` and `c ≡ d (mod m)`, then `a + c ≡ b + d (mod m)`, `a − c ≡ b − d (mod m)`, and `a × c ≡ b × d (mod m)`. Adding, subtracting, or multiplying keeps both sides differing by a multiple of m, so they remain congruent.
  > Source: Congruences and Their Properties.html
- **Division is special:** You can add, subtract, and multiply in modular arithmetic, but division only works when the divisor has a modular inverse — explored under Modular Inverses.
  > Source: Congruences and Their Properties.html

## Examples

- **(7 + 9) mod 5:** 7 + 9 = 16; 16 mod 5 = 1, so 7 + 9 ≡ 1 (mod 5).
  > Source: Congruences and Their Properties.html
- **(18 − 9) mod 7:** 18 − 9 = 9; 9 mod 7 = 2, so 18 − 9 ≡ 2 (mod 7).
  > Source: Congruences and Their Properties.html
- **(6 × 4) mod 5:** 6 × 4 = 24; 24 mod 5 = 4, so 6 × 4 ≡ 4 (mod 5).
  > Source: Congruences and Their Properties.html
- **(27 + 19) mod 8:** 27 + 19 = 46; 46 mod 8 = 6 remainder... 46 = 5×8 + 6? The source gives the answer as 6 — 46 = 5 × 8 + 6, so the result is 6.
  > Source: Congruences and Their Properties.html
- **(25 − 38) mod 12:** 25 − 38 ≡ 11 (mod 12).
  > Source: Congruences and Their Properties.html
- **(7 × 9) mod 10:** 7 × 9 = 63; 63 mod 10 = 3.
  > Source: Congruences and Their Properties.html
- **23 ≡ 3 (mod 10):** both behave the same way in any calculation mod 10.
  > Source: Congruences and Their Properties.html

## Related Topics
- [Introduction to Modular Arithmetic](introduction-to-modular-arithmetic.md)
- [Modular Inverses](modular-inverses.md)
