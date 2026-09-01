# Converting Between Bases

## Definition
Conversions let us express the same number in different forms — a skill essential for programming, data analysis and computer architecture. Every conversion method (division, expansion or regrouping) is built on the same simple idea: **powers of the base**.
> Source: Converting Between Bases.html

## Key Concepts
- **Decimal → another base (Successive Division Method):** Repeatedly divide by the new base and record the remainders; the remainders, read from bottom to top, form the digits of the new base. To convert a decimal number *n* to base *b*: divide *n* by *b*; record the remainder (this becomes the least significant digit); replace *n* with the quotient; repeat until the quotient is 0; read the remainders in reverse order.
  > Source: Converting Between Bases.html
- **Another base → decimal (Expansion Formula):** Applies the Base-b Expansion Theorem — for any integer *n* and base *b* > 1, *n* = aₖbᵏ + aₖ₋₁bᵏ⁻¹ + … + a₁b + a₀, where 0 ≤ aᵢ < b. To convert any base-*b* number back into decimal, multiply each digit by its corresponding power of the base and then add the results.
  > Source: Converting Between Bases.html
- **Binary ↔ Octal / Hexadecimal (regrouping):** Because bases 8 and 16 are powers of 2, you can convert between them by regrouping binary digits. Each octal digit = 3 binary bits; each hexadecimal digit = 4 binary bits.
  > Source: Converting Between Bases.html
- **Direction of the two decimal methods:** The successive division method moves outward from decimal; the expansion formula moves inward toward decimal. Grouping shortcuts between binary, octal and hexadecimal save time when bases are powers of 2.
  > Source: Converting Between Bases.html

## Examples
- Decimal → Binary (successive division): 241₁₀ = 11110001₂ (241÷2=120 r1, 120÷2=60 r0, 60÷2=30 r0, 30÷2=15 r0, 15÷2=7 r1, 7÷2=3 r1, 3÷2=1 r1, 1÷2=0 r1; read bottom to top).
  > Source: Converting Between Bases.html
- Decimal → Octal: 12345₁₀ = 30071₈ (12345÷8=1543 r1, 1543÷8=192 r7, 192÷8=24 r0, 24÷8=3 r0, 3÷8=0 r3; read bottom to top).
  > Source: Converting Between Bases.html
- Decimal → Hexadecimal: 177130₁₀ = 2B3EA₁₆ (177130÷16=11070 r10(A), 11070÷16=691 r14(E), 691÷16=43 r3, 43÷16=2 r11(B), 2÷16=0 r2; read bottom to top).
  > Source: Converting Between Bases.html
- Binary → Decimal (expansion): 1011₂ = (1×2³)+(0×2²)+(1×2¹)+(1×2⁰) = 8+0+2+1 = 11₁₀.
  > Source: Converting Between Bases.html
- Hex → Decimal (expansion): 3A₁₆ = (3×16¹)+(10×16⁰) = 48+10 = 58₁₀ (digit A = 10).
  > Source: Converting Between Bases.html
- Octal → Decimal (expansion): 30071₈ = (3×8⁴)+(0×8³)+(0×8²)+(7×8¹)+(1×8⁰) = 12288+0+0+56+1 = 12345₁₀.
  > Source: Converting Between Bases.html
- Regrouping binary → octal: 110111₂ = (110)(111) = 67 → 67₈.
  > Source: Converting Between Bases.html
- Regrouping binary → hexadecimal: 111010111100₂ = (1110)(1011)(1100) → EBC → EBC₁₆.
  > Source: Converting Between Bases.html
- Try-it answers: 200₁₀ = 11001000₂; 110010₂ = 50₁₀.
  > Source: Converting Between Bases.html

## Related Topics
- [Understanding Base Number Systems](understanding-base-number-systems.md)
- [Working with Binary, Octal and Hexadecimal](binary-octal-hex-representation.md)
- [Binary Arithmetic](binary-arithmetic.md)
