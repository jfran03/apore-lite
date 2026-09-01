# Introduction to Modular Arithmetic

## Definition

**Modular arithmetic** is a special kind of arithmetic where numbers wrap around after reaching a certain value called the **modulus**. When numbers exceed the modulus, they loop back to the beginning, creating a repeating pattern.
> Source: Introduction to Modular Arithmetic.html

**Modulus / mod notation.** Let a be an integer and d a positive integer. There exist integers q and r with `0 ≤ r < d` such that `a = dq + r`. Here d is the divisor or modulus, `q = a div d`, and `r = a mod d`. The expression `a mod d` means "the remainder when a is divided by d."
> Source: Introduction to Modular Arithmetic.html

## Key Concepts

- **The clock analogy:** A 12-hour clock uses mod 12 arithmetic — after 12 comes 1 again. The clock "wraps around" after 12 hours, just as modular arithmetic wraps around after its modulus.
  > Source: Introduction to Modular Arithmetic.html
- **Cycle of remainders:** Every modulus defines its own circle of numbers. Modulus 5 → {0, 1, 2, 3, 4}; modulus 7 → {0,…,6}; modulus 12 → {0,…,11}. After modulus − 1, the sequence restarts at 0.
  > Source: Introduction to Modular Arithmetic.html
- **Negative numbers:** If a < 0, then `a mod m = (a + m) mod m`. Add the modulus until the result is non-negative.
  > Source: Introduction to Modular Arithmetic.html
- **Patterns/properties:** Numbers that differ by a multiple of the modulus have the same remainder (e.g., 7, 12, 17 all give remainder 2 mod 5). Remainders always fall between 0 and m − 1. The pattern repeats every modulus steps: a, a+m, a+2m, … give the same remainder.
  > Source: Introduction to Modular Arithmetic.html

## Examples

- **26 mod 6:** 26 = 6 × 4 + 2, so 26 mod 6 = 2.
  > Source: Introduction to Modular Arithmetic.html
- **43 mod 8:** 43 = 8 × 5 + 3, so 43 mod 8 = 3.
  > Source: Introduction to Modular Arithmetic.html
- **Clock (9 + 7) mod 12:** = 16 mod 12 = 4 → it will be 4 o'clock.
  > Source: Introduction to Modular Arithmetic.html
- **−3 mod 7:** = (−3 + 7) mod 7 = 4.
  > Source: Introduction to Modular Arithmetic.html
- **−10 mod 6:** −10 + 6 = −4; −4 + 6 = 2, so −10 mod 6 = 2.
  > Source: Introduction to Modular Arithmetic.html

## Related Topics
- [Divisibility and the Division Algorithm](divisibility-and-division-algorithm.md)
- [Congruences and Their Properties](congruences-and-properties.md)
- [Modular Inverses](modular-inverses.md)
