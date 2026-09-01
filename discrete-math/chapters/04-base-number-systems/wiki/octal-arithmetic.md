# Octal Arithmetic

## Definition
Octal (base 8) arithmetic works just like binary or decimal arithmetic. The only difference is that digits range from 0 to 7. Whenever a sum or difference exceeds 7 or drops below 0, you carry or borrow just like in other base systems. Octal provides a convenient shorthand for binary because three binary bits = one octal digit.
> Source: Octal Arithmetic.html

## Key Concepts
- **Octal digits and place values:** Octal numbers use digits 0 through 7. Each position represents a power of 8: 1st (ones) = 8⁰ = 1; 2nd (eights) = 8¹ = 8; 3rd (sixty-fours) = 8² = 64; 4th = 8³ = 512. Each column is 8 times larger than the column to its right, which is why we carry whenever a column's total equals or exceeds 8.
  > Source: Octal Arithmetic.html
- **Octal addition:** Line up digits, add each column, and carry when the sum equals or exceeds 8. A sum of 0–7 is written as-is (carry 0); a sum of 8 (10₈) writes 0 and carries 1; 9 (11₈) writes 1 carry 1; …; 15 (17₈) writes 7 carry 1. In decimal we carry 1 when the sum ≥ 10; in octal we carry 1 when the sum ≥ 8.
  > Source: Octal Arithmetic.html
- **Octal subtraction:** Nearly identical to decimal subtraction. If the top digit (minuend) is smaller than the bottom digit (subtrahend), borrow 1 from the next column to the left. In octal, borrowing 1 means adding 8 to the current digit (in base 10 borrowing 1 adds 10).
  > Source: Octal Arithmetic.html

## Examples
- Place-value expansion: 157₈ = (1×8²) + (5×8¹) + (7×8⁰).
  > Source: Octal Arithmetic.html
- Addition: 73₈ + 25₈ = 120₈ (3+5=8 → write 0 carry 1; 7+2+1=10₈ → write 2 carry 1; write final carry).
  > Source: Octal Arithmetic.html
- Addition: 157₈ + 645₈ = 1024₈.
  > Source: Octal Arithmetic.html
- Addition (try-it): 246 + 517 = 765₈.
  > Source: Octal Arithmetic.html
- Subtraction: 645₈ − 257₈ = 366₈ (borrowing adds 8 to the current column).
  > Source: Octal Arithmetic.html
- Subtraction: 703₈ − 446₈ = 235₈ (451 − 294 = 157 = 235₈).
  > Source: Octal Arithmetic.html
  > Note: the source states this result as 255₈, but its own borrowing steps yield 235₈ (255₈ = 173, not 157). After the first borrow the middle column is 0−1−4, which requires a second borrow: (0−1+8)−4 = 3, then 7−1−4 = 2 → 235₈.
- Subtraction (try-it): 514 − 327 = 165₈.
  > Source: Octal Arithmetic.html
- Knowledge-check answers: 342 + 467 = 1031₈; 652 − 475 = 155₈.
  > Source: Octal Arithmetic.html

## Related Topics
- [Binary Arithmetic](binary-arithmetic.md)
- [Hexadecimal Arithmetic](hexadecimal-arithmetic.md)
- [Working with Binary, Octal and Hexadecimal](binary-octal-hex-representation.md)
