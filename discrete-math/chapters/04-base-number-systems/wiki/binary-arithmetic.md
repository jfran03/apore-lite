# Binary Arithmetic

## Definition
Binary arithmetic works on the same principles as ordinary arithmetic in base 10. The only difference is the base: instead of ten digits (0–9), binary has just two digits, 0 and 1. That simplicity makes binary perfect for digital logic circuits, where every switch is either off (0) or on (1). Addition, subtraction, multiplication and division all work the same way — you just "carry" or "borrow" when sums or differences exceed 1 instead of 9.
> Source: Binary Arithmetic.html

## Key Concepts
- **Binary addition:** Add digits in each column, carrying to the next position when the total equals or exceeds the base. In base 2 you carry when the sum is 2 (10₂). Column rules: 0+0=0 (carry 0); 0+1=1 (carry 0); 1+0=1 (carry 0); 1+1=0 (carry 1). The pattern is the same as base 10 (9+1 → carry 1), just the threshold happens sooner.
  > Source: Binary Arithmetic.html
- **Binary subtraction:** Mirrors decimal subtraction. When a smaller digit must subtract a larger one, you borrow 1 from the next position; in base 2, borrowing "1" is like borrowing 2₂. Column rules: 0−0=0; 1−0=1; 1−1=0; 0−1=1 (borrow 1).
  > Source: Binary Arithmetic.html
- **Binary multiplication:** Easier than decimal because there are only two digits — 0 × anything = 0; 1 × anything = that number. The rest is shifting (multiplying by powers of 2) and adding the partial results.
  > Source: Binary Arithmetic.html
- **Binary division:** The inverse of multiplication; works just like long division in base 10. See how many times the divisor fits into parts of the dividend, starting from the leftmost bits; at each step subtract, bring down the next bit and continue. If the divisor fits into the current bits → write 1 in the quotient; if not → write 0 and bring down the next bit.
  > Source: Binary Arithmetic.html
- **Binary vs. decimal arithmetic:** Every rule works exactly the same in base 2 as in base 10 — the only difference is *when* you carry or borrow. In decimal you roll over at 10; in binary you roll over at 2.
  > Source: Binary Arithmetic.html

## Examples
- Addition: 1110₂ + 1011₂ = 11001₂.
  > Source: Binary Arithmetic.html
- Addition: 1011₂ + 1101₂ = 11000₂.
  > Source: Binary Arithmetic.html
- Addition (try-it): 1111 + 1 = 10000₂.
  > Source: Binary Arithmetic.html
- Subtraction: 10010₂ − 1101₂ = 101₂ (check: 18₁₀ − 13₁₀ = 5₁₀ = 101₂).
  > Source: Binary Arithmetic.html
- Subtraction (try-it): 111 − 101 = 10₂ = 2₁₀.
  > Source: Binary Arithmetic.html
- Multiplication: 101₂ × 11₂ = 1111₂ = 15₁₀ (partial products 101 and 1010, then add).
  > Source: Binary Arithmetic.html
- Multiplication (try-it): 1001 × 10 = 10010₂ = 18₁₀.
  > Source: Binary Arithmetic.html
- Division: 1101₂ ÷ 11₂ (13 ÷ 3) → quotient 100₂, remainder 1₂. Verification: (100₂ × 11₂) + 1₂ = 1101₂.
  > Source: Binary Arithmetic.html
- Division (try-it): 10110 ÷ 10 → quotient 1011₂, remainder 0₂.
  > Source: Binary Arithmetic.html
- Knowledge-check answers: 1011 + 111 = 10010₂; 10110 − 1101 = 1001₂; 110 × 101 = 11110₂ (6 × 5 = 30); 10110 ÷ 11 → quotient 111₂, remainder 1₂ (22 ÷ 3 = 7 r1).
  > Source: Binary Arithmetic.html
  > Note: the source's practice answer key lists 11010₂ for 110 × 101 and quotient 110₂/remainder 0₂ for 10110 ÷ 11; both are incorrect (110 × 101 = 11110₂ = 30, and 3 does not divide 22 evenly — 22 ÷ 3 = 7 remainder 1).

## Related Topics
- [Octal Arithmetic](octal-arithmetic.md)
- [Hexadecimal Arithmetic](hexadecimal-arithmetic.md)
- [Converting Between Bases](converting-between-bases.md)
