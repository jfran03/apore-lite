# Understanding Base Number Systems

## Definition
Every number we write is based on a **base** (or **radix**): a system that defines how digits represent values. A base tells you how many unique digits a system uses before "rolling over" to a new place value, just like how 9 rolls over to 10 in decimal.
> Source: Understanding Base Number Systems.html

## Key Concepts
- **Base / radix:** A system that defines how digits represent values; it determines how many unique digits exist before the count "rolls over." When we "run out" of symbols, we add another place — the base determines when that happens.
  > Source: Understanding Base Number Systems.html
- **Digit vs. Number:** A *digit* is a single symbol allowed in a base. A *number* is made up of digits multiplied by powers of the base. Example: in 245₁₀ the digits are 2, 4, and 5, and the number is two hundred forty-five.
  > Source: Understanding Base Number Systems.html
- **Common bases and why they exist:** Different bases fit different purposes.
  - Binary (Base 2): Matches the on/off logic of computer circuits; digits 0, 1.
  - Octal (Base 8): Groups binary digits in sets of 3, making long binary numbers shorter; digits 0–7.
  - Decimal (Base 10): Perfect for human counting and everyday calculations; digits 0–9.
  - Hexadecimal (Base 16): Groups binary digits in sets of 4, widely used in programming and digital systems; digits 0–9 and A–F, where A–F represent 10–15.
  > Source: Understanding Base Number Systems.html
- **Base-b Expansion Theorem:** For any integer *n* and base *b* > 1, *n* can be written uniquely as *n* = aₖbᵏ + aₖ₋₁bᵏ⁻¹ + … + a₁b + a₀, where 0 ≤ aᵢ < b for all *i*. This expression is called the base-b expansion of *n*. No matter what base you choose, every positive integer can be written using only the digits allowed in that base, and this representation is **unique**.
  > Source: Understanding Base Number Systems.html

## Examples
- Counting 0 to 12 and noticing roll-over: Decimal (base 10): 0, 1, 2, …, 8, 9, 10; Binary (base 2): 0, 1, 10, 11, 100, 101, 110, 111, 1000; Octal (base 8): 0, 1, 2, …, 6, 7, 10, 11, 12.
  > Source: Understanding Base Number Systems.html
- Writing 37 in base 5 using the theorem: the largest power of 5 less than 37 is 5² = 25; 37 ÷ 25 = 1 remainder 12; 12 ÷ 5 = 2 remainder 2. So 37₁₀ = 1×5² + 2×5¹ + 2×5⁰ = 122₅.
  > Source: Understanding Base Number Systems.html
- Base 10 expansion: 965₁₀ = 9×10² + 6×10¹ + 5×10⁰.
  > Source: Understanding Base Number Systems.html
- Base 2 expansion: 1011₂ = 1×2³ + 0×2² + 1×2¹ + 1×2⁰ = 11₁₀.
  > Source: Understanding Base Number Systems.html

## Common Misconceptions
- A base does **not** determine how many digits a number can have in total — the number of digits is unlimited; the base affects *which* digits exist.
  > Source: Understanding Base Number Systems.html
- The base is **not** always 10 — 10 is just one possible base; many cultures used different bases long before computers.
  > Source: Understanding Base Number Systems.html

## Related Topics
- [Working with Binary, Octal and Hexadecimal](binary-octal-hex-representation.md)
- [Converting Between Bases](converting-between-bases.md)
