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
**Type:** mcq
**Difficulty:** introductory
**Topic:** divisibility-and-division-algorithm
**Focus Area:** Definition of divisibility
**Question:** Which of the following correctly defines "a divides b"?
(A) b ÷ a = integer  (B) a ÷ b = integer  (C) a = b × k  (D) b = a + k
**Answer:** (A) b ÷ a = integer. "a divides b" (a | b) means there is an integer k with b = a × k, i.e., b ÷ a is an integer.

## Q002
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** divisibility-and-division-algorithm
**Focus Area:** Division Algorithm — quotient and remainder
**Question:** Using the Division Algorithm, find the quotient and remainder when 29 is divided by 5.
**Answer:** q = 5, r = 4, since 29 = 5 × 5 + 4 and the remainder satisfies 0 ≤ 4 < 5.

## Q003
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** divisibility-and-division-algorithm
**Focus Area:** Linear Combination Property
**Question:** If 4 divides both 12 and 20, what can you conclude about integer combinations of 12 and 20, and why?
**Answer:** Any integer combination s×12 + t×20 is also divisible by 4. By the Linear Combination Property, if a | b and a | c then a | (sb + tc) for any integers s and t.

## Q004
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** divisibility-and-division-algorithm
**Focus Area:** Remainders with negative dividends
**Question:** What are the quotient and remainder when −11 is divided by 3?
**Answer:** q = −4, r = 1, since −11 = 3 × (−4) + 1. The remainder stays non-negative (0 ≤ r < |d|) even though the dividend is negative.

## Q005
**Status:** active
**Type:** mcq
**Difficulty:** introductory
**Topic:** prime-composite-relatively-prime
**Focus Area:** Identifying primes
**Question:** Which of the following numbers is prime? (A) 21 (B) 25 (C) 19 (D) 27
**Answer:** (C) 19 — it is divisible only by 1 and itself. (21 = 3×7, 25 = 5×5, 27 = 3×9 are composite.)

## Q006
**Status:** active
**Type:** conceptual
**Difficulty:** introductory
**Topic:** prime-composite-relatively-prime
**Focus Area:** Why 1 is not prime
**Question:** Why is 1 not considered a prime number?
**Answer:** A prime number must be an integer greater than 1 that is divisible only by 1 and itself. 1 has only one divisor (itself), so it fails the definition; 1 is neither prime nor composite.

## Q007
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** prime-composite-relatively-prime
**Focus Area:** Relatively prime numbers
**Question:** Are 8 and 15 relatively prime? Explain.
**Answer:** Yes. Two positive integers are relatively prime if their gcd is 1, and gcd(8, 15) = 1 — they share no common factor except 1 (even though both are composite).

## Q008
**Status:** active
**Type:** true-false
**Difficulty:** introductory
**Topic:** prime-composite-relatively-prime
**Focus Area:** The only even prime
**Question:** True or False: 2 is the only even prime number.
**Answer:** True. Every other even number is divisible by 2, making it composite.

## Q009
**Status:** active
**Type:** mcq
**Difficulty:** introductory
**Topic:** fundamental-theorem-of-arithmetic
**Focus Area:** Statement of the theorem
**Question:** Which statement correctly describes the Fundamental Theorem of Arithmetic?
(A) Every integer can be expressed as a sum of primes. (B) Every integer greater than 1 can be written uniquely as a product of primes. (C) Only even integers can be written as products of primes. (D) Every integer greater than 1 has multiple distinct prime factorizations.
**Answer:** (B) Every integer greater than 1 can be written uniquely as a product of primes (apart from the order of the factors).

## Q010
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** fundamental-theorem-of-arithmetic
**Focus Area:** Computing prime factorization
**Question:** Find the prime factorization of 7007.
**Answer:** 7007 = 7 × 7 × 11 × 13 = 7² × 11 × 13 (7007 ÷ 7 = 1001; 1001 ÷ 7 = 143; 143 ÷ 11 = 13; 13 is prime).

## Q011
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** fundamental-theorem-of-arithmetic
**Focus Area:** Uniqueness despite different starting factorizations
**Question:** 210 can be started as 21 × 10, 15 × 14, or 7 × 30. Does this contradict the uniqueness claim of the FTA? Explain.
**Answer:** No. Those starting factors (10, 14, 15, 21, 30) are composite and factor further. Fully reducing every path yields the same primes: 210 = 2 × 3 × 5 × 7. Uniqueness means the final set of primes is always the same (order aside).

## Q012
**Status:** active
**Type:** mcq
**Difficulty:** introductory
**Topic:** gcd-and-lcm
**Focus Area:** Computing GCD
**Question:** What is the greatest common divisor of 18 and 30? (A) 3 (B) 6 (C) 9 (D) 12
**Answer:** (B) 6 — 6 divides both 18 and 30 evenly and no larger number does.

## Q013
**Status:** active
**Type:** mcq
**Difficulty:** intermediate
**Topic:** gcd-and-lcm
**Focus Area:** GCD–LCM relationship
**Question:** For any two positive integers a and b, which is true?
(A) gcd(a,b) + lcm(a,b) = a × b  (B) gcd(a,b) × lcm(a,b) = a × b  (C) gcd(a,b) − lcm(a,b) = a × b  (D) gcd(a,b) × lcm(a,b) = a + b
**Answer:** (B) gcd(a, b) × lcm(a, b) = a × b.

## Q014
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** gcd-and-lcm
**Focus Area:** GCD and LCM via prime factorization
**Question:** Using prime factorization (48 = 2⁴×3, 180 = 2²×3²×5), find gcd(48, 180) and lcm(48, 180).
**Answer:** GCD uses the lowest powers common to both: 2² × 3 = 12. LCM uses the highest powers in either: 2⁴ × 3² × 5 = 720. (Check: 12 × 720 = 8640 = 48 × 180.)

## Q015
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** gcd-and-lcm
**Focus Area:** Computing LCM
**Question:** Find the least common multiple of 6 and 8.
**Answer:** lcm(6, 8) = 24 — the smallest positive integer divisible by both 6 and 8.

## Q016
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** euclidean-algorithm
**Focus Area:** Applying the algorithm
**Question:** Use the Euclidean Algorithm to find gcd(252, 198).
**Answer:** 252 = 198×1 + 54; 198 = 54×3 + 36; 54 = 36×1 + 18; 36 = 18×2 + 0. The last nonzero remainder is 18, so gcd(252, 198) = 18.

## Q017
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** euclidean-algorithm
**Focus Area:** Lemma 1
**Question:** State the lemma that the Euclidean Algorithm is based on and explain why it holds.
**Answer:** Lemma 1: if a = bq + r, then gcd(a, b) = gcd(b, r). Any number dividing both a and b also divides r = a − bq, and any number dividing both b and r also divides a = bq + r, so (a, b) and (b, r) have exactly the same common divisors — hence equal GCDs.

## Q018
**Status:** active
**Type:** true-false
**Difficulty:** introductory
**Topic:** euclidean-algorithm
**Focus Area:** Identifying the GCD in the process
**Question:** True or False: In the Euclidean Algorithm, the GCD is the last nonzero remainder.
**Answer:** True. You repeat the division until the remainder is 0; the last nonzero remainder is the GCD.

## Q019
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** bezouts-identity
**Focus Area:** Statement and Bézout coefficients
**Question:** What does Bézout's Identity guarantee about the gcd of two integers a and b, and what are the Bézout coefficients?
**Answer:** For any integers a and b (not both zero), there exist integers s and t such that gcd(a, b) = s·a + t·b. The integers s and t are the Bézout coefficients; they are not unique but any valid pair produces the same gcd.

## Q020
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** bezouts-identity
**Focus Area:** Expressing gcd as a linear combination
**Question:** Express gcd(252, 198) = 18 as a linear combination of 252 and 198.
**Answer:** 18 = 4 × 252 − 5 × 198 (so s = 4, t = −5), obtained by back-substituting through the Euclidean Algorithm steps.

## Q021
**Status:** active
**Type:** true-false
**Difficulty:** intermediate
**Topic:** bezouts-identity
**Focus Area:** Non-uniqueness of coefficients
**Question:** True or False: The Bézout coefficients s and t for a given pair a, b are unique.
**Answer:** False. They are not unique — different pairs (e.g., (2, −1) and (−1, 1) for a = 6, b = 9) can produce the same gcd.

## Q022
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** extended-euclidean-algorithm
**Focus Area:** Finding gcd and coefficients
**Question:** Using the Extended Euclidean Algorithm, find gcd(240, 46) and its Bézout coefficients.
**Answer:** gcd(240, 46) = 2, with 2 = (−9) × 240 + 47 × 46, so s = −9 and t = 47.

## Q023
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** extended-euclidean-algorithm
**Focus Area:** What the algorithm produces
**Question:** How does the Extended Euclidean Algorithm differ from the standard Euclidean Algorithm?
**Answer:** The standard algorithm only finds the gcd. The extended version also tracks how each remainder is formed as a combination of a and b, producing the Bézout coefficients s and t such that gcd(a, b) = s·a + t·b.

## Q024
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** extended-euclidean-algorithm
**Focus Area:** gcd = 1 significance
**Question:** When the Extended Euclidean Algorithm gives gcd(85, 32) = 1, what does that tell you about 85 and 32, and why does it matter?
**Answer:** It means 85 and 32 are relatively prime (coprime). This matters in modular arithmetic and encryption because a modular inverse exists exactly when the gcd is 1.

## Q025
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** introduction-to-modular-arithmetic
**Focus Area:** Computing a mod m
**Question:** What does 19 mod 8 equal, and how do you find it?
**Answer:** 19 mod 8 = 3, since 19 = 8 × 2 + 3 (the remainder when 19 is divided by 8).

## Q026
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** introduction-to-modular-arithmetic
**Focus Area:** Modulo of negative numbers
**Question:** What is −10 mod 6?
**Answer:** −10 mod 6 = 2. Add the modulus until non-negative: −10 + 6 = −4, −4 + 6 = 2.

## Q027
**Status:** active
**Type:** conceptual
**Difficulty:** introductory
**Topic:** introduction-to-modular-arithmetic
**Focus Area:** Wrap-around concept
**Question:** Explain what "wrap-around" means in modular arithmetic, using the clock analogy.
**Answer:** In modular arithmetic numbers cycle through remainders 0 to m−1; once they reach the modulus they loop back to 0. A 12-hour clock uses mod 12 — e.g., (9 + 7) mod 12 = 16 mod 12 = 4, so it "wraps around" to 4 o'clock.

## Q028
**Status:** active
**Type:** mcq
**Difficulty:** intermediate
**Topic:** congruences-and-properties
**Focus Area:** Definition of congruence
**Question:** "a ≡ b (mod m)" is true when: (A) m divides (a − b) (B) a + b is divisible by m (C) a and b are both prime (D) a × b = m
**Answer:** (A) m divides (a − b). Equivalently, a and b have the same remainder when divided by m, or a = b + km for some integer k.

## Q029
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** congruences-and-properties
**Focus Area:** Operations on congruences
**Question:** Compute (27 + 19) mod 8.
**Answer:** 6. 27 + 19 = 46, and 46 = 5 × 8 + 6, so (27 + 19) mod 8 = 6.

## Q030
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** congruences-and-properties
**Focus Area:** Three equivalent conditions
**Question:** Give the three equivalent conditions that all mean a ≡ b (mod m).
**Answer:** (1) m divides (a − b); (2) a mod m = b mod m; (3) there exists an integer k such that a = b + km.

## Q031
**Status:** active
**Type:** mcq
**Difficulty:** intermediate
**Topic:** modular-inverses
**Focus Area:** Existence of a modular inverse
**Question:** Which number has a modular inverse modulo 12? (A) 2 (B) 3 (C) 4 (D) 5
**Answer:** (D) 5, because gcd(5, 12) = 1. An inverse exists only when the number and modulus are relatively prime.

## Q032
**Status:** active
**Type:** true-false
**Difficulty:** introductory
**Topic:** modular-inverses
**Focus Area:** Condition for inverse existence
**Question:** True or False: The number a has a modular inverse modulo m only if gcd(a, m) = 1.
**Answer:** True. A modular inverse of a mod m exists (and is unique mod m) exactly when gcd(a, m) = 1; if gcd(a, m) ≠ 1, no inverse exists.

## Q033
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** modular-inverses
**Focus Area:** Finding an inverse
**Question:** Find the modular inverse of 3 modulo 11.
**Answer:** 4, because 3 × 4 = 12 ≡ 1 (mod 11).

## Q034
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** modular-inverses
**Focus Area:** Solving a modular equation
**Question:** Solve 4x ≡ 5 (mod 7).
**Answer:** x ≡ 3 (mod 7). The inverse of 4 mod 7 is 2 (since 4 × 2 = 8 ≡ 1), so x ≡ 2 × 5 = 10 ≡ 3 (mod 7).

## Q035
**Status:** active
**Type:** mcq
**Difficulty:** intermediate
**Topic:** testing-for-primality
**Focus Area:** Trial division bound
**Question:** To test whether n is prime by trial division, you only need to check divisibility by primes up to: (A) n/2 (B) √n (C) n − 1 (D) n
**Answer:** (B) √n. If n is composite, it has a prime divisor less than or equal to √n, so testing primes up to √n suffices.

## Q036
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** testing-for-primality
**Focus Area:** Applying trial division
**Question:** Use trial division to determine whether 221 is prime.
**Answer:** Composite. √221 ≈ 14.86, so check primes 2, 3, 5, 7, 11, 13; 221 ÷ 13 = 17, so 221 = 13 × 17.

## Q037
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** testing-for-primality
**Focus Area:** Limits of trial division
**Question:** Why is trial division impractical for very large numbers such as those used in cryptography?
**Answer:** You must test every prime up to √n. For a number like 9,973,969 that means checking primes up to ≈3,157 — hundreds of divisions; for numbers with hundreds or thousands of digits it becomes practically impossible for humans and extremely time-consuming even for computers.

## Q038
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** modern-applications
**Focus Area:** Primes and RSA
**Question:** Why do prime numbers make RSA encryption secure?
**Answer:** RSA multiplies two very large primes to form a modulus. Multiplying primes is easy, but factoring the product back into those primes is extremely hard — this one-way difficulty protects data like credit card numbers and passwords.

## Q039
**Status:** active
**Type:** mcq
**Difficulty:** intermediate
**Topic:** modern-applications
**Focus Area:** LCM for synchronization
**Question:** Tasks A, B, and C run every 4, 6, and 8 seconds respectively. When do all three next run together? (A) 12 s (B) 16 s (C) 24 s (D) 48 s
**Answer:** (C) 24 seconds — the least common multiple of 4, 6, and 8 is 24. Systems use LCM to synchronize periodic events.

## Q040
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** modern-applications
**Focus Area:** Euclidean Algorithm and key generation
**Question:** What role does the Euclidean Algorithm play in generating encryption keys like those in RSA?
**Answer:** It confirms that two numbers are coprime (gcd = 1), which guarantees a modular inverse exists. That inverse (the private exponent) is what allows an encrypted message to be decrypted; without it, key generation for RSA would not work.

## Q041
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** bezouts-identity
**Focus Area:** Non-uniqueness of coefficients (targeted follow-up to Q021)
**Question:** You compute 18 = 4 × 252 − 5 × 198, expressing gcd(252, 198) as a linear combination. Does finding this one pair (s, t) = (4, −5) mean it is the *only* pair of coefficients that works? Explain.
**Answer:** No. Bézout coefficients are not unique — many integer pairs (s, t) satisfy gcd(a, b) = s·a + t·b, and (4, −5) is just one valid pair. Any valid pair produces the same gcd.

## Q042
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** gcd-and-lcm
**Focus Area:** Computing LCM (targeted follow-up to Q015)
**Question:** Find the least common multiple of 4 and 6.
**Answer:** lcm(4, 6) = 12. Listing common multiples of 4 and 6: {12, 24, 36, …} — the smallest is 12.

## Q043
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** gcd-and-lcm
**Focus Area:** LCM via the GCD–LCM relationship (targeted follow-up to Q015)
**Question:** Given gcd(12, 18) = 6, use the GCD–LCM relationship to find lcm(12, 18).
**Answer:** lcm(12, 18) = (12 × 18) / gcd(12, 18) = 216 / 6 = 36. Check: 6 × 36 = 216 = 12 × 18.

## Q044
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** gcd-and-lcm
**Focus Area:** Distinguishing "a common multiple" from "the least common multiple" (targeted follow-up to Q042)
**Question:** 24 is a common multiple of 4 and 6. Is it the *least* common multiple? If not, what is?
**Answer:** No. 24 is a common multiple, but not the smallest one. The least common multiple of 4 and 6 is 12 — the smallest positive integer that is a multiple of both.

## Q045
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** gcd-and-lcm
**Focus Area:** Computing LCM by listing multiples (targeted follow-up to Q042)
**Question:** Find the least common multiple of 3 and 5 by listing common multiples.
**Answer:** lcm(3, 5) = 15. Multiples of 3: 3, 6, 9, 12, 15…; multiples of 5: 5, 10, 15…; the smallest shared value is 15.

## Q046
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** gcd-and-lcm
**Focus Area:** GCD–LCM relationship, remembering to divide (targeted follow-up to Q043)
**Question:** Given gcd(8, 12) = 4, find lcm(8, 12) using the GCD–LCM relationship.
**Answer:** lcm(8, 12) = (8 × 12) / gcd(8, 12) = 96 / 4 = 24.

## Q047
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** gcd-and-lcm
**Focus Area:** Why divide by the gcd (targeted follow-up to Q043)
**Question:** Why do we divide by the gcd when computing lcm(a, b) = (a × b) / gcd(a, b), rather than just using a × b?
**Answer:** The GCD–LCM relationship states gcd(a, b) × lcm(a, b) = a × b. The raw product a × b double-counts the factors a and b share, so it's only a common multiple — not necessarily the *least* one (it only equals the lcm when gcd(a, b) = 1). Dividing by the gcd removes that double-counted overlap and gives the smallest common multiple.

## Q048
**Status:** active
**Type:** true-false
**Difficulty:** intermediate
**Topic:** gcd-and-lcm
**Focus Area:** When a × b equals lcm directly (targeted follow-up to Q047)
**Question:** True or False: a × b equals lcm(a, b) only when gcd(a, b) = 1.
**Answer:** True. Since gcd(a, b) × lcm(a, b) = a × b, if gcd(a, b) = 1 then lcm(a, b) = a × b directly. If gcd(a, b) ≠ 1, a × b double-counts the shared factors, so you must divide by the gcd to get the true lcm.

## Q049
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** gcd-and-lcm
**Focus Area:** Seeing the double-counted overlap concretely (targeted follow-up to Q047)
**Question:** For a = 6, b = 9 (gcd = 3), compute a × b and lcm(a, b) separately, and explain why they differ.
**Answer:** a × b = 54. lcm(6, 9): 6 = 2×3, 9 = 3², so lcm uses the highest powers of each prime: 2 × 3² = 18. They differ because gcd(6, 9) = 3 ≠ 1, so a × b = 54 double-counts the shared factor of 3; dividing by the gcd (54 / 3 = 18) removes that overlap and matches gcd(a, b) × lcm(a, b) = a × b, i.e. 3 × 18 = 54.

## Q050
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** gcd-and-lcm
**Focus Area:** Applying a×b vs. lcm distinction (targeted follow-up to Q049)
**Question:** For a = 4, b = 10 (gcd = 2), compute a × b, then find lcm(4, 10) using the GCD–LCM relationship.
**Answer:** a × b = 40. lcm(4, 10) = 40 / gcd(4, 10) = 40 / 2 = 20.

## Q051
**Status:** active
**Type:** conceptual
**Difficulty:** introductory
**Topic:** gcd-and-lcm
**Focus Area:** Plain-language reason a×b isn't usually the lcm (targeted follow-up to Q049)
**Question:** In plain terms, why isn't a × b usually the least common multiple of a and b?
**Answer:** By the GCD–LCM relationship, gcd(a, b) × lcm(a, b) = a × b. If a and b share common factors (gcd(a, b) > 1), then a × b counts those shared factors twice, giving a common multiple bigger than necessary — not the least one. Only when a and b share no factors (gcd(a, b) = 1) does a × b equal the lcm exactly.

## Q052
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** bezouts-identity
**Focus Area:** Naming and uniqueness of the coefficients (targeted follow-up to Q019)
**Question:** In the equation gcd(a, b) = s·a + t·b, what are s and t called, and are they unique?
**Answer:** They are called the Bézout coefficients. They are not unique — different valid pairs of integers (s, t) can produce the same gcd.

## Q053
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** bezouts-identity
**Focus Area:** Identifying a valid coefficient pair (targeted follow-up to Q019)
**Question:** For a = 6, b = 9, identify a valid pair of Bézout coefficients (s, t) satisfying gcd(6, 9) = s·6 + t·9.
**Answer:** (s, t) = (2, −1) or (−1, 1) both work: 2×6 + (−1)×9 = 3, and (−1)×6 + 1×9 = 3, and gcd(6, 9) = 3.

## Q054
**Status:** active
**Type:** true-false
**Difficulty:** introductory
**Topic:** bezouts-identity
**Focus Area:** Naming check (targeted follow-up to Q052)
**Question:** True or False: In gcd(a, b) = s·a + t·b, the integers s and t are called the Bézout coefficients.
**Answer:** True.

## Q055
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** bezouts-identity
**Focus Area:** Back-substitution through Euclidean Algorithm steps (targeted follow-up to Q053)
**Question:** Using the Euclidean Algorithm steps for gcd(30, 12) — 30 = 12×2 + 6; 12 = 6×2 + 0 — express gcd(30, 12) = 6 as a linear combination of 30 and 12.
**Answer:** 6 = 30 − 12×2, so s = 1, t = −2.

## Q056
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** bezouts-identity
**Focus Area:** The back-substitution process itself (targeted follow-up to Q053)
**Question:** Describe the general process for finding Bézout coefficients from the Euclidean Algorithm's steps.
**Answer:** Each division step a = bq + r can be rewritten as r = a − bq. Substituting backward through the steps — replacing each remainder in terms of the previous pair — expresses the gcd entirely in terms of the original a and b, revealing the coefficients s and t.
