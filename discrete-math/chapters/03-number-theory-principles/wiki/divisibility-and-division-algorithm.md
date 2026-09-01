# Divisibility and the Division Algorithm

## Definition

**Divisibility.** If a and b are integers, we say that *a divides b* (written `a | b`) if there is some integer k such that `b = a × k`. If no such integer exists, we write `a ∤ b` ("a does not divide b"). When a divides b, a is called a **divisor** or **factor** of b, and b is called a **multiple** of a.
> Source: Divisibility and the Division Algorithm.html

**Division Algorithm.** For any integers a and d (where d ≠ 0), there exist unique integers q (the quotient) and r (the remainder) such that `a = d × q + r`, where `0 ≤ r < |d|`. This expresses any integer a as a multiple of d plus a non-negative remainder r.
> Source: Divisibility and the Division Algorithm.html

## Key Concepts

- **Divides notation:** "a divides b" means b ÷ a is an integer. Examples: `3 | 12` because 12 = 3 × 4; `3 ∤ 7` because 7 ÷ 3 is not an integer.
  > Source: Divisibility and the Division Algorithm.html
- **Roles in the Division Algorithm:** d is the divisor, a is the dividend, q is the quotient, r is the remainder. In programming-style notation, `q = a div d` and `r = a mod d`.
  > Source: Divisibility and the Division Algorithm.html
- **Remainder is always non-negative:** The remainder r always satisfies `0 ≤ r < |d|`, even when a is negative.
  > Source: Divisibility and the Division Algorithm.html

## Properties of Divisibility

- **Transitive Property:** If `a | b` and `b | c`, then `a | c`. Example: if 2 divides 4 and 4 divides 8, then 2 divides 8.
  > Source: Divisibility and the Division Algorithm.html
- **Linear Combination Property:** If `a | b` and `a | c`, then `a | (sb + tc)` for any integers s and t. Any integer combination of b and c is also divisible by a. Example: with a = 3, b = 6, c = 9, since 3 ∣ 6 and 3 ∣ 9, then 3 ∣ (2×6 + (−1)×9) because 2×6 − 9 = 3.
  > Source: Divisibility and the Division Algorithm.html
- **Zero Property:** For any integer a, `a | 0` since 0 = a × 0.
  > Source: Divisibility and the Division Algorithm.html
- **Reflexive Property:** For any nonzero integer a, `a | a` since a = a × 1.
  > Source: Divisibility and the Division Algorithm.html

## Finding the Quotient and Remainder

Process: (1) Divide a by d to get a decimal result. (2) Take the integer part as the quotient q. (3) Multiply the divisor by q to find the largest multiple of d ≤ a. (4) Subtract from a to find the remainder r. (5) Check that `0 ≤ r < |d|`.
> Source: Divisibility and the Division Algorithm.html

## Examples

- **101 ÷ 11:** 101 ÷ 11 = 9.18…, so q = 9. Then 11 × 9 = 99, and 101 − 99 = 2, so r = 2. Check: 0 ≤ 2 < 11. ✅
  > Source: Divisibility and the Division Algorithm.html
- **87 ÷ 8:** 87 ÷ 8 = 10.875, so q = 10. Then 8 × 10 = 80, and 87 − 80 = 7, so r = 7. Check: 87 = 8 × 10 + 7. Written as `87 div 8 = 10` and `87 mod 8 = 7`.
  > Source: Divisibility and the Division Algorithm.html
- **−11 ÷ 3:** −11 = 3 × (−4) + 1, so quotient = −4, remainder = 1. The remainder stays non-negative even though a is negative. Written as `−11 div 3 = −4` and `−11 mod 3 = 1`.
  > Source: Divisibility and the Division Algorithm.html
- **29 ÷ 5:** 29 = 5 × 5 + 4, so q = 5, r = 4. The remainder 4 satisfies 0 ≤ r < 5.
  > Source: Divisibility and the Division Algorithm.html

## Related Topics
- [Prime, Composite, and Relatively Prime Numbers](prime-composite-relatively-prime.md)
- [The Euclidean Algorithm](euclidean-algorithm.md)
- [Introduction to Modular Arithmetic](introduction-to-modular-arithmetic.md)
