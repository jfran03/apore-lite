# Hexadecimal Arithmetic

## Definition
Hexadecimal (base 16) arithmetic extends what you learned in binary and octal. It uses 16 unique digits (0 through 9 and A through F) to represent numbers compactly. Since 16 = 2⁴, every hexadecimal digit corresponds neatly to a group of four binary bits, making it a favorite system in programming and digital electronics.
> Source: Hexadecimal Arithmetic.html

## Key Concepts
- **Hex digit values:** Hexadecimal needs symbols beyond 9, so A–F fill in for 10–15: A = 10, B = 11, C = 12, D = 13, E = 14, F = 15.
  > Source: Hexadecimal Arithmetic.html
- **Hexadecimal addition:** Works the same as decimal or octal addition — line up the digits, add each column, and carry 1 whenever the sum equals or exceeds 16. You don't need to memorize the full addition table; just remember that when the sum exceeds F (15), you carry 1 to the next column (F + 1 = 10₁₆).
  > Source: Hexadecimal Arithmetic.html
- **Hexadecimal subtraction:** Uses the same borrowing logic as other bases — if the top digit is smaller than the one below it, borrow 1 (equal to 16 in base 16) from the next higher place. Rule: Top ≥ Bottom → subtract directly; Top < Bottom → borrow 1 (adds 16 to top). Decimal borrowing adds 10, octal borrowing adds 8, and hexadecimal borrowing adds 16.
  > Source: Hexadecimal Arithmetic.html
- **Why do arithmetic by hand when calculators exist:** Understanding base systems builds intuition for real computing tasks — insight into how computers "think" (they process everything in binary; hex is a compact human-friendly way to read those values, e.g. a color like #FFAA33 or an address like 0x7FFE); debugging and error checking of raw data shown in hexadecimal; and pattern recognition across bases (powers of two, modular overflow, bitwise operations). The goal isn't to replace your calculator — it's to understand what your calculator is doing for you.
  > Source: Hexadecimal Arithmetic.html
- **Link to binary:** Each hex digit corresponds perfectly to 4 binary bits, which is why programmers use hex for representing memory, colors and instructions.
  > Source: Hexadecimal Arithmetic.html

## Examples
- Addition: B7₁₆ + 4C₁₆ = 103₁₆ (7 + C(12) = 19 = 13₁₆ → write 3 carry 1; B(11) + 4 + 1 = 16 = 10₁₆ → write 0 carry 1).
  > Source: Hexadecimal Arithmetic.html
- Addition: 9A₁₆ + E7₁₆ = 181₁₆ (A(10) + 7 = 17 = 11₁₆ → write 1 carry 1; 9 + E(14) + 1 = 24 = 18₁₆ → write 8 carry 1).
  > Source: Hexadecimal Arithmetic.html
- Addition (try-it): 5F + A9 = 108₁₆.
  > Source: Hexadecimal Arithmetic.html
- Subtraction: 9A₁₆ − 5C₁₆ = 3E₁₆ (A(10) − C(12) → borrow → (10+16)−12 = 14 = E; 9 becomes 8 after the borrow, 8 − 5 = 3).
  > Source: Hexadecimal Arithmetic.html
  > Note: the source's result line states 5E₁₆, but its own worked steps produce left digit 3 and right digit E → 3E₁₆ (154 − 92 = 62 = 3E₁₆; 5E₁₆ = 94).
- Subtraction: 1A7₁₆ − 9D₁₆ = 10A₁₆ (7 − D(13) → borrow → (7+16)−13 = 10 = A; 9 after borrow − 9 = 0; 1 − 0 = 1).
  > Source: Hexadecimal Arithmetic.html
- Subtraction (try-it): B4 − 7E = 36₁₆.
  > Source: Hexadecimal Arithmetic.html
- Knowledge-check answers: 8B₁₆ + 79₁₆ = 104₁₆; C2₁₆ − 7B₁₆ = 47₁₆ (2 − B → borrow → (2+16)−11 = 7; C after borrow = B, B − 7 = 4).
  > Source: Hexadecimal Arithmetic.html
  > Note: the source's practice answer key lists "13D₁₆" for C2₁₆ − 7B₁₆, but 13D₁₆ equals C2 + 7B; applying the source's own subtraction/borrowing method gives 47₁₆.

## Related Topics
- [Binary Arithmetic](binary-arithmetic.md)
- [Octal Arithmetic](octal-arithmetic.md)
- [Working with Binary, Octal and Hexadecimal](binary-octal-hex-representation.md)
