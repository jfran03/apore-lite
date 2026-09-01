# Modern Applications of Number Theory

## Definition

This topic surveys how the number-theory concepts of the chapter — divisibility, primes, GCDs, and modular arithmetic — form the "invisible backbone" of the digital world, protecting data through encryption and enabling efficient computation.
> Source: Modern Applications of Number Theory.html

## Key Concepts

- **Prime numbers and cryptography:** The RSA encryption algorithm uses two very large prime numbers to create a public/private key pair. Their product is used as a modulus. Multiplying primes is easy, but factoring the product back into its primes is extremely hard — this one-way difficulty protects data like credit card numbers and passwords.
  > Source: Modern Applications of Number Theory.html
- **RSA key sizes:** RSA keys are typically 2048 bits (over 600 digits). Breaking the encryption would require factoring a 600+ digit number. Increasing key size from 1024 to 2048 bits can multiply the difficulty by millions.
  > Source: Modern Applications of Number Theory.html
- **The Euclidean Algorithm and secure keys:** When creating encryption keys, the algorithm ensures two numbers are coprime (GCD = 1), which guarantees a modular inverse exists — the inverse is needed to decrypt messages. Without it, systems like RSA would not work.
  > Source: Modern Applications of Number Theory.html
- **Modular arithmetic in cybersecurity:** Computers work with a fixed number of bits, so they naturally compute "modulo" a power of two. Modular exponentiation (aᵇ mod n) is central to RSA and Diffie–Hellman; modular operations with large primes help hash functions distribute data; checksums and CRCs use modular arithmetic for error detection.
  > Source: Modern Applications of Number Theory.html
- **Divisibility and LCM in computing:** Divisibility determines whether one quantity fits evenly into another (data chunks, storage blocks, memory addresses). The LCM identifies when repeating events coincide, used to synchronize processes and schedule recurring tasks.
  > Source: Modern Applications of Number Theory.html
- **Beyond security:** Number theory also underpins pseudorandom number generators (PRNGs), hash functions and hash tables, blockchain and digital signatures, error-detection/correction codes (parity bits, CRCs, Reed–Solomon), and procedural generation in computer graphics.
  > Source: Modern Applications of Number Theory.html

## Examples

- **RSA walkthrough (small scale):** Choose primes p = 5, q = 11, so n = 55 and Euler's totient φ(n) = (p−1)(q−1) = 4 × 10 = 40. Choose public exponent e = 3 (coprime with 40). Find private exponent d = modular inverse of e mod 40 using the Extended Euclidean Algorithm: 40 = 3×13 + 1, so 1 = 40 − 3×13, giving −13×3 ≡ 1 (mod 40); −13 ≡ 27 (mod 40), so d = 27. Encrypt M = 9: C = 9³ mod 55 = 729 mod 55 = 14. Decrypt: 14²⁷ mod 55 = 9 (matches). The Euclidean Algorithm made this possible by finding d = 27.
  > Source: Modern Applications of Number Theory.html
- **Task synchronization with LCM:** Two processes running every 4 ms and every 6 ms align again every 12 ms, because lcm(4, 6) = 12. Similarly, tasks running every 4, 6, and 8 seconds align every 24 seconds, since lcm(4, 6, 8) = 24.
  > Source: Modern Applications of Number Theory.html

## Related Topics
- [Prime, Composite, and Relatively Prime Numbers](prime-composite-relatively-prime.md)
- [The Euclidean Algorithm](euclidean-algorithm.md)
- [The Extended Euclidean Algorithm](extended-euclidean-algorithm.md)
- [Modular Inverses](modular-inverses.md)
- [Greatest Common Divisor (GCD) and Least Common Multiple (LCM)](gcd-and-lcm.md)
