# Working with Binary, Octal and Hexadecimal

## Definition
Computers use several different number systems to represent, store and process data. At the heart of it all is **binary (base 2)**, a simple system made of only two digits; for readability, humans often use **octal (base 8)** and **hexadecimal (base 16)** as shorthand forms. Binary is the foundation, and octal and hexadecimal are the shortcuts that make it human-friendly.
> Source: Working with Binary, Octal, and Hexadecimal.html

## Key Concepts
- **Why computers use binary:** Computers have electronic switches that can be on or off, true or false, 1 or 0. Binary perfectly matches this physical reality — 1 = current is flowing (ON), 0 = no current (OFF). Everything a computer does is built from these binary states.
  > Source: Working with Binary, Octal, and Hexadecimal.html
- **Bit and byte:** Each binary digit (bit) represents a tiny piece of information. 8 bits = 1 byte, which can represent 256 (2⁸) unique values.
  > Source: Working with Binary, Octal, and Hexadecimal.html
- **Binary representation (base 2):** Digits used 0, 1; smallest unit is 1 bit; common use is internal computer operations, logic and data storage. Each position represents a power of 2. Example: 1011₂ = 1×8 + 0×4 + 1×2 + 1×1 = 8 + 0 + 2 + 1 = 11₁₀.
  > Source: Working with Binary, Octal, and Hexadecimal.html
- **Octal representation (base 8):** Uses a single symbol to represent three binary digits (bits). Every group of three binary digits can be replaced by one octal digit and vice versa. Octal is easier for humans to read/write than long binary strings, is used in older operating systems (like UNIX permissions) and digital hardware design, and every 3 bits = 1 octal digit.
  > Source: Working with Binary, Octal, and Hexadecimal.html
- **Hexadecimal representation (base 16):** Uses 16 symbols (digits 0–9 and letters A–F) to represent four binary digits (bits) at once. It is compact and readable for humans, common in programming (memory addresses, colors, machine code), and every 4 bits = 1 hex digit, so one byte = 2 hex digits.
  > Source: Working with Binary, Octal, and Hexadecimal.html
- **Connecting the three systems:** Binary, octal and hexadecimal are closely related because their bases (2, 8, 16) are powers of 2. You can convert between them quickly by grouping bits: 3 bits = 1 octal digit; 4 bits = 1 hex digit; 8 bits ≈ 3 octal digits = 2 hex digits. You can jump directly between binary ↔ octal or binary ↔ hex just by regrouping bits — no need to go through decimal every time.
  > Source: Working with Binary, Octal, and Hexadecimal.html

## Examples
- Binary → octal grouping: 110010₂ = 62₈ — group the binary digits into blocks of 3 (from right to left): 110 010 → (6)(2).
  > Source: Working with Binary, Octal, and Hexadecimal.html
- Binary → hexadecimal grouping: 111010111100₂ = EBC₁₆ — group bits in 4s: 1110 1011 1100; convert each group: 1110 (E), 1011 (B), 1100 (C); combine → EBC₁₆.
  > Source: Working with Binary, Octal, and Hexadecimal.html
- Reading binary: 1001₂ = 9, 1111₂ = 15, 1010₂ = 10 (multiply each digit by its power of 2 and add).
  > Source: Working with Binary, Octal, and Hexadecimal.html
- Hex color codes: In HTML/CSS, #FF0000 means pure red — FF = 255 (red), 00 = 0 (green), 00 = 0 (blue); this is hexadecimal notation for binary color values.
  > Source: Working with Binary, Octal, and Hexadecimal.html
- Flip-card conversions: 110111₂ = 67₈; 110111₂ = 37₁₆; 3F₁₆ = 111111₂.
  > Source: Working with Binary, Octal, and Hexadecimal.html

## Common Misconceptions
- Hexadecimal is **not** used only for representing fractions; fractions depend on floating-point format, not base.
  > Source: Working with Binary, Octal, and Hexadecimal.html
- Hexadecimal does **not** eliminate the need for binary — binary is still the underlying representation.
  > Source: Working with Binary, Octal, and Hexadecimal.html
- Hexadecimal is **not** "the same as octal but with letters" — hexadecimal and octal are distinct systems.
  > Source: Working with Binary, Octal, and Hexadecimal.html

## Related Topics
- [Understanding Base Number Systems](understanding-base-number-systems.md)
- [Converting Between Bases](converting-between-bases.md)
