# Question Bank

> Generated from `wiki/` during the compile step. Extended on wrong-answer targeting and graduation.
> Do not edit manually — all changes are made by Claude during compile and session flows.

---

<!-- Question format (do not delete this comment):

## Q{NNN}
**Status:** active | retired
**Type:** mcq | short-answer | conceptual | true-false
**Difficulty:** introductory | intermediate | advanced
**Topic:** {topic-slug}
**Focus Area:** {specific concept or sub-topic}
**Question:** {question text}
**Answer:** {model answer — sourced from wiki only}

-->

## Q001
**Status:** active
**Type:** conceptual
**Difficulty:** introductory
**Topic:** understanding-base-number-systems
**Focus Area:** definition of a base/radix
**Question:** What does the "base" (or radix) of a number system tell you?
**Answer:** The base tells you how many unique digits a system uses before "rolling over" to a new place value — just as 9 rolls over to 10 in decimal. It defines how many unique digits exist before the count rolls over. (See understanding-base-number-systems.md)

## Q002
**Status:** active
**Type:** mcq
**Difficulty:** introductory
**Topic:** understanding-base-number-systems
**Focus Area:** describing a base number system
**Question:** Which statement best describes a base number system? (a) A base defines how many unique digits exist before the count "rolls over." (b) A base determines how many digits a number can have in total. (c) Bases are only used for computers. (d) The base always equals 10 because that's what humans use.
**Answer:** (a) A base defines how many unique digits exist before the count "rolls over" (e.g., base 2 uses digits 0 and 1 before rolling over). The number of digits a number can have is unlimited; 10 is just one possible base; and bases were used by many cultures before computers. (See understanding-base-number-systems.md)

## Q003
**Status:** active
**Type:** conceptual
**Difficulty:** introductory
**Topic:** understanding-base-number-systems
**Focus Area:** digit vs. number
**Question:** Distinguish between a "digit" and a "number."
**Answer:** A digit is a single symbol allowed in a base; a number is made up of digits multiplied by powers of the base. Example: in 245₁₀ the digits are 2, 4, and 5, while the number is two hundred forty-five. (See understanding-base-number-systems.md)

## Q004
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** understanding-base-number-systems
**Focus Area:** digits used by each base
**Question:** List the digits used by binary, octal, decimal, and hexadecimal.
**Answer:** Binary (base 2): 0, 1. Octal (base 8): 0–7. Decimal (base 10): 0–9. Hexadecimal (base 16): 0–9 and A–F, where A–F represent 10–15. (See understanding-base-number-systems.md)

## Q005
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** understanding-base-number-systems
**Focus Area:** Base-b Expansion Theorem
**Question:** State the Base-b Expansion Theorem.
**Answer:** For any integer n and base b > 1, n can be written uniquely as n = aₖbᵏ + aₖ₋₁bᵏ⁻¹ + … + a₁b + a₀, where 0 ≤ aᵢ < b for all i. This is the base-b expansion of n, and the representation is unique. (See understanding-base-number-systems.md)

## Q006
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** understanding-base-number-systems
**Focus Area:** applying base-b expansion
**Question:** Write 37 (base 10) in base 5 using the expansion process.
**Answer:** 122₅. The largest power of 5 less than 37 is 5² = 25; 37 ÷ 25 = 1 remainder 12; 12 ÷ 5 = 2 remainder 2, giving 37₁₀ = 1×5² + 2×5¹ + 2×5⁰ = 122₅. (See understanding-base-number-systems.md)

## Q007
**Status:** active
**Type:** true-false
**Difficulty:** introductory
**Topic:** binary-octal-hex-representation
**Focus Area:** why computers use binary
**Question:** True or false: Computers use binary because their electronic switches can be in one of two states (on/off, 1/0).
**Answer:** True. Computers have electronic switches that can be on or off (1 = current flowing/ON, 0 = no current/OFF), and binary perfectly matches this physical reality. (See binary-octal-hex-representation.md)

## Q008
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** binary-octal-hex-representation
**Focus Area:** bits and bytes
**Question:** How many bits are in a byte, and how many unique values can a byte represent?
**Answer:** 8 bits = 1 byte, which can represent 256 (2⁸) unique values. (See binary-octal-hex-representation.md)

## Q009
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** binary-octal-hex-representation
**Focus Area:** bit-grouping relationships
**Question:** How many binary bits does one octal digit represent, and how many does one hexadecimal digit represent?
**Answer:** One octal digit represents 3 binary bits; one hexadecimal digit represents 4 binary bits. This is because 8 and 16 are powers of 2. (See binary-octal-hex-representation.md)

## Q010
**Status:** active
**Type:** mcq
**Difficulty:** intermediate
**Topic:** binary-octal-hex-representation
**Focus Area:** why hexadecimal is used
**Question:** Why do computers often use hexadecimal notation? (a) It represents large binary values in fewer digits. (b) It allows fractional numbers. (c) It's the same as octal but with letters. (d) It eliminates the need for binary representation.
**Answer:** (a) It represents large binary values in fewer digits — each hex digit represents four bits, so binary values become shorter and easier to read. Fractions depend on floating-point format not base; hex and octal are distinct systems; and binary remains the underlying representation. (See binary-octal-hex-representation.md)

## Q011
**Status:** active
**Type:** true-false
**Difficulty:** introductory
**Topic:** binary-octal-hex-representation
**Focus Area:** hex-to-binary correspondence
**Question:** True or false: Each hexadecimal digit corresponds to a unique group of four binary digits (bits).
**Answer:** True. Every hex digit (0–F) represents exactly four bits, which is why hexadecimal is convenient for expressing binary data. (See binary-octal-hex-representation.md)

## Q012
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** binary-octal-hex-representation
**Focus Area:** binary place value
**Question:** Convert 1011₂ to decimal using binary place values.
**Answer:** 11₁₀. 1011₂ = 1×8 + 0×4 + 1×2 + 1×1 = 8 + 0 + 2 + 1 = 11₁₀. (See binary-octal-hex-representation.md)

## Q013
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** binary-octal-hex-representation
**Focus Area:** binary-to-octal regrouping
**Question:** Convert 110010₂ to octal by grouping bits.
**Answer:** 62₈. Group the binary digits into blocks of 3 from right to left: 110 010 → (6)(2) → 62₈. (See binary-octal-hex-representation.md)

## Q014
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** binary-octal-hex-representation
**Focus Area:** relationship among the three systems
**Question:** Why can you convert directly between binary, octal, and hexadecimal without going through decimal?
**Answer:** Because their bases (2, 8, 16) are all powers of 2, you can convert by regrouping bits: 3 bits = 1 octal digit and 4 bits = 1 hex digit. This lets you jump directly between binary ↔ octal or binary ↔ hex just by regrouping. (See binary-octal-hex-representation.md)

## Q015
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** converting-between-bases
**Focus Area:** successive division method
**Question:** Describe the successive division method for converting a decimal number to another base.
**Answer:** Repeatedly divide the number by the new base and record each remainder; replace the number with the quotient and repeat until the quotient is 0. The remainders read from bottom to top (reverse order) form the digits of the new base; the first remainder is the least significant digit. (See converting-between-bases.md)

## Q016
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** converting-between-bases
**Focus Area:** decimal to binary
**Question:** Convert 125 (base 10) to binary.
**Answer:** 1111101₂. Using successive division by 2 and reading the remainders from bottom to top gives 1111101. (See converting-between-bases.md)

## Q017
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** converting-between-bases
**Focus Area:** base to decimal via expansion
**Question:** Convert 110101₂ to decimal.
**Answer:** 53₁₀. Using the expansion formula: (1×2⁵)+(1×2⁴)+(0×2³)+(1×2²)+(0×2¹)+(1×2⁰) = 32+16+0+4+0+1 = 53. (See converting-between-bases.md)

## Q018
**Status:** active
**Type:** mcq
**Difficulty:** intermediate
**Topic:** converting-between-bases
**Focus Area:** binary to hexadecimal
**Question:** What is the hexadecimal representation of the binary number 11001011? (a) CB₁₆ (b) B3₁₆ (c) C9₁₆ (d) 19₁₆
**Answer:** (a) CB₁₆. Group into sets of four from left to right: 1100 = C and 1011 = B → CB₁₆. (See converting-between-bases.md)

## Q019
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** converting-between-bases
**Focus Area:** decimal to hexadecimal
**Question:** Convert 177130 (base 10) to hexadecimal using successive division.
**Answer:** 2B3EA₁₆. 177130÷16=11070 r10(A); 11070÷16=691 r14(E); 691÷16=43 r3; 43÷16=2 r11(B); 2÷16=0 r2. Reading remainders bottom to top gives 2B3EA. (See converting-between-bases.md)

## Q020
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** converting-between-bases
**Focus Area:** direction of the two decimal methods
**Question:** How do the successive division method and the expansion formula differ in direction?
**Answer:** The successive division method moves outward from decimal (decimal → another base), while the expansion formula moves inward toward decimal (another base → decimal). (See converting-between-bases.md)

## Q021
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** binary-arithmetic
**Focus Area:** binary addition carry rule
**Question:** In binary addition, when do you carry to the next column, and what is 1 + 1 in binary?
**Answer:** You carry when the column total equals or exceeds the base 2 — that is, when the sum is 2 (10₂). 1 + 1 = 0 with a carry of 1 (i.e., 10₂). (See binary-arithmetic.md)

## Q022
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** binary-arithmetic
**Focus Area:** binary addition
**Question:** Add the binary numbers 1011 + 111.
**Answer:** 10010₂. Adding column by column with carries (1011 = 11, 111 = 7, sum = 18 = 10010₂). (See binary-arithmetic.md)

## Q023
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** binary-arithmetic
**Focus Area:** binary subtraction
**Question:** Subtract the binary numbers 10110 − 1101.
**Answer:** 1001₂. Borrowing where needed (10110 = 22, 1101 = 13, difference = 9 = 1001₂); in binary, borrowing "1" adds 2 to the current column. (See binary-arithmetic.md)

## Q024
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** binary-arithmetic
**Focus Area:** binary multiplication
**Question:** Multiply the binary numbers 110 × 101.
**Answer:** 11110₂. Each bit of the multiplier creates a partial product; shift left and add: 110 = 6, 101 = 5, product = 30 = 11110₂. (See binary-arithmetic.md — note: the source answer key mistypes this as 11010₂, which equals 26.)

## Q025
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** binary-arithmetic
**Focus Area:** binary division
**Question:** Divide 10110 ÷ 11 in binary and give the quotient and remainder.
**Answer:** Quotient = 111₂, remainder = 1₂. 10110 = 22 and 11 = 3; 22 ÷ 3 = 7 remainder 1, and 7 = 111₂. (See binary-arithmetic.md — note: the source answer key gives quotient 110₂/remainder 0₂, but 3 does not divide 22 evenly.)

## Q026
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** binary-arithmetic
**Focus Area:** binary vs. decimal arithmetic
**Question:** How is binary arithmetic fundamentally the same as decimal arithmetic, and what is the one difference?
**Answer:** Every rule for addition, subtraction, multiplication, and division works exactly the same in base 2 as in base 10. The only difference is when you carry or borrow: in decimal you roll over at 10, in binary you roll over at 2. (See binary-arithmetic.md)

## Q027
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** octal-arithmetic
**Focus Area:** octal place values
**Question:** What power of 8 does each of the first four octal place positions (from the right) represent?
**Answer:** 1st (ones) = 8⁰ = 1; 2nd (eights) = 8¹ = 8; 3rd (sixty-fours) = 8² = 64; 4th = 8³ = 512. (See octal-arithmetic.md)

## Q028
**Status:** active
**Type:** true-false
**Difficulty:** introductory
**Topic:** octal-arithmetic
**Focus Area:** octal carry/borrow threshold
**Question:** True or false: In octal, you carry when a column's sum reaches 8, and borrowing 1 adds 8 to the current digit.
**Answer:** True. Octal uses digits 0–7, so you carry when a column's total equals or exceeds 8, and borrowing 1 means adding 8 to the current digit. (See octal-arithmetic.md)

## Q029
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** octal-arithmetic
**Focus Area:** octal addition
**Question:** Add 342 + 467 in base 8.
**Answer:** 1031₈. Carry 1 each time a column total reaches 8. (See octal-arithmetic.md)

## Q030
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** octal-arithmetic
**Focus Area:** octal subtraction
**Question:** Subtract 652 − 475 in base 8.
**Answer:** 155₈. When the top digit is smaller, borrow 1 (= 8) from the next column. (See octal-arithmetic.md)

## Q031
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** hexadecimal-arithmetic
**Focus Area:** hex digit values
**Question:** What decimal values do the hexadecimal digits A through F represent?
**Answer:** A = 10, B = 11, C = 12, D = 13, E = 14, F = 15. (See hexadecimal-arithmetic.md)

## Q032
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** hexadecimal-arithmetic
**Focus Area:** hex carry and borrow rules
**Question:** When do you carry in hexadecimal addition, and how much does borrowing add in hexadecimal subtraction?
**Answer:** In hex addition you carry 1 whenever the column sum equals or exceeds 16 (F + 1 = 10₁₆). In hex subtraction, borrowing 1 adds 16 to the current (top) digit. (By comparison, decimal borrowing adds 10 and octal borrowing adds 8.) (See hexadecimal-arithmetic.md)

## Q033
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** hexadecimal-arithmetic
**Focus Area:** hexadecimal addition
**Question:** Add 8B₁₆ + 79₁₆.
**Answer:** 104₁₆. You carry 1 when the column sum exceeds F. (See hexadecimal-arithmetic.md)

## Q034
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** hexadecimal-arithmetic
**Focus Area:** hexadecimal subtraction
**Question:** Subtract C2₁₆ − 7B₁₆.
**Answer:** 47₁₆. Rightmost: 2 − B(11) → borrow → (2+16) − 11 = 7; leftmost: C(12) becomes B(11) after the borrow, B − 7 = 4 → 47₁₆. (See hexadecimal-arithmetic.md — note: the source's answer key mistypes this as 13D₁₆, which is actually C2 + 7B.)

## Q035
**Status:** active
**Type:** multi-select
**Difficulty:** intermediate
**Topic:** binary-octal-hex-representation
**Focus Area:** true statements about octal and hexadecimal
**Question:** Which statements about octal and hexadecimal are true? (a) Octal groups binary digits in sets of three. (b) Hexadecimal uses the digits 0–9 and letters A–F. (c) Both systems are easier for humans to read than binary. (d) Hexadecimal is only used for representing fractions. (e) Octal digits correspond to four binary bits.
**Answer:** (a), (b), and (c) are true. Octal groups binary in sets of three; hexadecimal uses 0–9 and A–F; both are easier to read than binary. (d) is false (hex is not only for fractions) and (e) is false (octal digits correspond to three bits, not four). (See binary-octal-hex-representation.md)

## Q036
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** understanding-base-number-systems
**Focus Area:** base defines digit rollover (targeted follow-up to Q001)
**Question:** Base 8 uses the digits 0 through 7. When you count upward in base 8 and reach 7, what happens next — and what does that tell you about the role the base plays?
**Answer:** The next value is 10₈ — a new place value opens because 7 is the last unique digit available. This illustrates the role of the base: it defines how many unique digits exist before the count rolls over to a new place value. (See understanding-base-number-systems.md)

## Q037
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** binary-octal-hex-representation
**Focus Area:** byte value and hex-bit grouping (targeted follow-up to Q008)
**Question:** If 1 byte = 8 bits, how many unique values can 1 byte represent — and how many bits does a single hexadecimal digit correspond to?
**Answer:** 256 (2⁸) unique values. One hexadecimal digit corresponds to 4 binary bits. (See binary-octal-hex-representation.md)

## Q038
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** converting-between-bases
**Focus Area:** decimal to binary, reading remainder order (targeted follow-up to Q019)
**Question:** Convert 241 (base 10) to binary using successive division, and explicitly state the order you read the remainders in.
**Answer:** 11110001₂. 241÷2=120 r1, 120÷2=60 r0, 60÷2=30 r0, 30÷2=15 r0, 15÷2=7 r1, 7÷2=3 r1, 3÷2=1 r1, 1÷2=0 r1. Remainders must be read from bottom to top (last remainder computed is the most significant digit). (See converting-between-bases.md)
