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
**Type:** short-answer
**Difficulty:** introductory
**Topic:** introduction-to-probability
**Focus Area:** Core terms
**Question:** Define the four core terms of probability: experiment, outcome, sample space, and event.
**Answer:** An **experiment** is a process you carry out that leads to one or more outcomes (e.g. rolling a die). An **outcome** is a single result of the experiment (e.g. rolling a 4). The **sample space (S)** is the set of all possible outcomes (e.g. {1,2,3,4,5,6} for a fair six-sided die). An **event** is a subset of the sample space with one or more outcomes that we focus on (e.g. "rolling an even number" = {2,4,6}).

## Q002
**Status:** active
**Type:** true-false
**Difficulty:** introductory
**Topic:** introduction-to-probability
**Focus Area:** Range of probability
**Question:** True or false: a probability of 1 means the event is certain, and a probability of 0 means the event cannot happen.
**Answer:** **True.** For any event, 0 ⩽ P(A) ⩽ 1. P(A) = 0 means the event cannot happen (impossible event); P(A) = 1 means the event is certain (sure event). A value between 0 and 1 shows how likely the event is, with values closer to 1 being more likely.

## Q003
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** introduction-to-probability
**Focus Area:** Classical probability formula
**Question:** State the classical probability formula and the condition under which it applies.
**Answer:** P(A) = (number of favourable outcomes for A) / (total number of outcomes in S). It applies **when each outcome in the sample space is equally likely**.

## Q004
**Status:** active
**Type:** mcq
**Difficulty:** introductory
**Topic:** introduction-to-probability
**Focus Area:** Applying the classical formula
**Question:** Roll two fair six-sided dice and add the faces. What is the probability the total is 3?
(a) 1/36 (b) 1/18 (c) 1/12 (d) 2/12
**Answer:** **(b) 1/18.** There are 6 × 6 = 36 equally likely outcomes. Only (1, 2) and (2, 1) give a total of 3, so P = 2/36 = 1/18 ≈ 0.0556 — about 5.6 % of the time.

## Q005
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** introduction-to-probability
**Focus Area:** Theoretical vs experimental probability
**Question:** What is the difference between theoretical and experimental probability, and what connects them?
**Answer:** **Theoretical** probability is based on reasoning — it assumes all outcomes are equally likely and uses the classical formula; you don't need to perform the experiment. **Experimental** probability comes from real or simulated trials: P(A) = (number of times A occurs) / (total number of trials). They are connected by the **Law of Large Numbers**: the more times you repeat the experiment, the closer the experimental probability should get to the theoretical value. Theoretical is ideal for pure reasoning (card game odds, algorithm outcomes); experimental is used when you have data (system logs, sensor readings, randomised simulations).

## Q006
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** introduction-to-probability
**Focus Area:** Three interpretations of probability
**Question:** Name the three interpretations of probability given in the lecture notes, and state the problem identified with each of the first two.
**Answer:** (1) **The frequency interpretation** — the ratio of favourable outcomes over total outcomes, m/n, approaches P(A). *Problem:* the ratio only gets more "likely" to approach the fixed probability as n increases indefinitely. (2) **The subjective interpretation** — probability, or "credence," as a measure of subjective certainty or ignorance; start with total ignorance and update with each observation. *Problem:* independence of events is not well-defined in this interpretation, and rejection of theories is not a gradual process (example: the paradox of black ravens). (3) **The objective/classical interpretation**, based on symmetry — for n physically identical simple events, indistinguishable except for arbitrary labels, assign each simple event P = 1/n.

## Q007
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** introduction-to-probability
**Focus Area:** Coarse graining
**Question:** What is coarse graining, and how does the unfair-coin example demonstrate it?
**Answer:** Coarse graining is bundling events under the same label (which brings resolution down), so we can have different probabilities for different labels — it is how we start with and work with **unequal** probabilities. Example: a coin twice as heavy on the head side can be simulated with a *three*-sided coin, all sides equally weighted, labelling two sides H and one side T. Then P(H) = 1/3 + 1/3 = 2/3 and P(T) = 1/3.

## Q008
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** complement-events
**Focus Area:** Complement rule
**Question:** Define the complement of an event A and state the complement rule.
**Answer:** The complement of A, written Aᶜ (or A′ or Ā), is all the outcomes in the sample space that are **not** part of A: Aᶜ = S − A. The complement rule is **P(A) + P(Aᶜ) = 1**, or equivalently **P(Aᶜ) = 1 − P(A)**. This holds because between an event and its complement every possible outcome is covered — something either happens or it doesn't, with no overlap or gap.

## Q009
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** complement-events
**Focus Area:** Why complements are useful
**Question:** Give three reasons the wiki offers for why complements are useful.
**Answer:** (1) **They often make problems easier** — e.g. it's easier to find the probability of *not* rolling a 6 (5/6) than of rolling anything else. (2) **They reduce errors in reasoning** — thinking in terms of both an event and its complement forces you to consider the entire sample space. (3) **They're common in programming and logic** — in Boolean terms, the complement of a condition is its negation, the event that the condition evaluates to false.

## Q010
**Status:** active
**Type:** mcq
**Difficulty:** intermediate
**Topic:** complement-events
**Focus Area:** The birthday problem
**Question:** How many people are needed for the probability that at least two share a birthday to exceed 50%?
(a) 23 (b) 50 (c) 100 (d) 183
**Answer:** **(a) 23.** For n = 23, P(no shared birthday) ≈ 0.493, so P(at least two share) = 1 − 0.493 = 0.507, about 50.7%. Most people guess you'd need a much larger group, but in a small group shared birthdays are already more likely than not.

## Q011
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** complement-events
**Focus Area:** Complement reasoning in the birthday problem
**Question:** Why does the birthday problem get solved through the complement rather than directly?
**Answer:** Calculating "at least two share a birthday" directly would mean adding probabilities for one match, two matches, three matches, and so on — nearly impossible by hand. But the complement, "no shared birthdays," follows a simple pattern of sequential restrictions: P(Aᶜ) = (365/365) × (364/365) × … × ((365 − n + 1)/365), where each term is the probability a new person's birthday doesn't match any previous one. Complement reasoning turns a messy counting problem into one clean calculation.

## Q012
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** addition-and-multiplication-rules
**Focus Area:** The addition rule
**Question:** State the addition rule and explain why the final term is subtracted.
**Answer:** **P(A∪B) = P(A) + P(B) − P(A∩B)**. If you simply add the probabilities of two events, you may count the overlap twice — once in each event. Subtracting P(A∩B) removes that double-counted overlap. Note that in probability "or" is always **inclusive**: A∪B means "A or B or both."

## Q013
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** addition-and-multiplication-rules
**Focus Area:** Mutually exclusive events
**Question:** What does it mean for two events to be mutually exclusive, and how does the addition rule simplify?
**Answer:** Two events are mutually exclusive if they cannot occur together — for example, rolling both a 2 and a 3 on the same single die. Their overlap probability is zero, so the rule simplifies to **P(A∪B) = P(A) + P(B)**. The lecture notes state the same for **disjoint** events, and generalise: P(A or B or … or Z) = P(A) + P(B) + … + P(Z).

## Q014
**Status:** active
**Type:** mcq
**Difficulty:** intermediate
**Topic:** addition-and-multiplication-rules
**Focus Area:** Applying the addition rule
**Question:** In a standard deck, A = "card is a heart" and B = "card is a queen." What is P(A or B)?
(a) 0.25 (b) 0.269 (c) 0.308 (d) 0.327
**Answer:** **(c) 0.308.** P(A) = 13/52 = 0.25, P(B) = 4/52 = 0.0769, P(A∩B) = 1/52 = 0.0192 (the queen of hearts). So P(A∪B) = 0.25 + 0.0769 − 0.0192 = 0.3077 ≈ 0.308. Choosing 0.25 is the error of reporting only P(heart) without including the chance of drawing a queen.

## Q015
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** addition-and-multiplication-rules
**Focus Area:** Inclusion–exclusion for three sets
**Question:** State the inclusion–exclusion formula for the probability of a union of three events, and describe the pattern for more sets.
**Answer:** **P(A∪B∪C) = P(A) + P(B) + P(C) − P(A∩B) − P(A∩C) − P(B∩C) + P(A∩B∩C)**. The pattern continues for more sets: **+** individuals, **−** pairs, **+** triples, **−** quadruples, and so on, alternating signs.

## Q016
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** addition-and-multiplication-rules
**Focus Area:** Inclusion–exclusion worked example
**Question:** Find the probability of picking a number at random from 1 to 30 that is a multiple of 2, 3 or 4.
**Answer:** With 𝒰 = {1,…,30}: |A| = ⌊30/2⌋ = 15, |B| = ⌊30/3⌋ = 10, |C| = ⌊30/4⌋ = ⌊7.5⌋ = 7. Intersections use the least common multiple: |A∩B| = ⌊30/lcm(2,3)⌋ = ⌊30/6⌋ = 5, |A∩C| = ⌊30/lcm(2,4)⌋ = ⌊30/4⌋ = 7, |B∩C| = ⌊30/lcm(3,4)⌋ = ⌊30/12⌋ = 2, |A∩B∩C| = ⌊30/lcm(2,3,4)⌋ = 2. So |A∪B∪C| = 15 + 10 + 7 − 5 − 7 − 2 + 2 = 20 and **P = 20/30 = 0.6̄**.

## Q017
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** addition-and-multiplication-rules
**Focus Area:** The multiplication rule
**Question:** State the general multiplication rule and explain what each factor means.
**Answer:** **P(A ∩ B) = P(A) × P(B ∣ A)**, where P(A) is the probability that event A occurs and P(B ∣ A) is the probability that event B occurs *given* that A has already occurred. If A has no effect on B the events are **independent**, P(B∣A) = P(B), and the formula reduces to P(A ∩ B) = P(A) × P(B). If the outcome of A changes the likelihood of B, the events are **dependent**.

## Q018
**Status:** active
**Type:** mcq
**Difficulty:** intermediate
**Topic:** addition-and-multiplication-rules
**Focus Area:** Dependent events without replacement
**Question:** A drawer has 5 red socks and 3 blue socks. You pull one sock, then without replacing it pull a second. What is the probability both are blue?
(a) 0.083 (b) 0.107 (c) 0.125 (d) 0.214
**Answer:** **(b) 0.107.** P(first blue) = 3/8; after removing one blue, P(second blue ∣ first blue) = 2/7. So 3/8 × 2/7 = 3/28 = 0.107. The answer 0.125 comes from wrongly assuming independence, and 0.214 from multiplying 3/7 × 2/7 as if replacement occurred.

## Q019
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** addition-and-multiplication-rules
**Focus Area:** Dependent events — drawing two aces
**Question:** From a standard 52-card deck without replacement, what is the probability of drawing two aces in a row?
**Answer:** E = "first card is an ace" → P(E) = 4/52 = 1/13. F = "second card is an ace, given the first was an ace" → P(F∣E) = 3/51 = 1/17. So P(E ∩ F) = 1/13 × 1/17 = **1/221 ≈ 0.00452** — less than half a percent.

## Q020
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** addition-and-multiplication-rules
**Focus Area:** The Monty Hall problem
**Question:** In the Monty Hall problem, should you switch doors? Justify using conditional reasoning.
**Answer:** **Yes — switching doubles your chances.** Before Monty opens a door, P(car behind your chosen door) = 1/3 and P(car behind the other doors) = 2/3. Monty always opens a door with a goat, and this action *depends* on your first choice — it gives you information, since one of the losing doors is now gone. If your first choice was the car (1/3 chance), switching makes you lose; if your first choice was a goat (2/3 chance), switching makes you win because the only other unopened door must have the car. So P(win if you switch) = P(initially picked goat) = 2/3, while P(win if you stay) = P(initially picked car) = 1/3. The common "two doors left, 50–50" intuition is wrong.

## Q021
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** addition-and-multiplication-rules
**Focus Area:** Common pitfalls
**Question:** List the common pitfalls the wiki identifies when applying the addition and multiplication rules.
**Answer:** (1) **Confusing "or" with "and"** — "or" → addition rule, "and" → multiplication rule; mixing them is the most common student error. (2) **Assuming independence too quickly** — always ask whether one event changes the sample space of the other; in "without replacement" cases events are dependent. (3) **Ignoring overlap** — when two events can both happen, subtract P(A∩B) once; a Venn diagram helps visualise shared regions. (4) **Switching conditional directions** — P(A∣B) is not the same as P(B∣A); read carefully which condition comes after "given." (5) **Relying on intuition** — intuition often fails, as Monty Hall shows.

## Q022
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** conditional-probability-and-bayes
**Focus Area:** Conditional probability formula
**Question:** Write the formula for conditional probability P(B ∣ A) and say when it is most useful.
**Answer:** **P(B ∣ A) = P(A ∩ B) / P(A)**. It is a rearrangement of the multiplication rule, and is especially useful when you know the joint probability and want to find how one event depends on another. Conditional probability gives you a way to update your understanding once new information is introduced.

## Q023
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** conditional-probability-and-bayes
**Focus Area:** Joint, marginal and conditional
**Question:** Distinguish joint, marginal and conditional probabilities, and state how the three relate.
**Answer:** **Joint** — the probability of a combined outcome, e.g. P(1H). **Marginal** — the probability of one component outcome on its own, e.g. P(1) or P(H); found by summing the joint probabilities across a row or column. **Conditional** — the probability of one component given the other, e.g. P(H∣1). They relate as **joint = marginal × conditional**, e.g. P(1H) = P(1) · P(H∣1).

## Q024
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** conditional-probability-and-bayes
**Focus Area:** Testing for independence
**Question:** How can a contingency table be used to test whether two events are independent?
**Answer:** Compare the joint probability against the product of the marginals: **|P(1H) − P(1)P(H)| = 0 → independence; ≠ 0 → dependence**. The notes suggest this quantity could serve as a measure for dependence/correlation. Equivalently, if H is independent of the die outcome then **P(H∣1) = P(H∣1̄) = P(H)**.

## Q025
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** conditional-probability-and-bayes
**Focus Area:** Applying conditional probability to a contingency table
**Question:** Of 200 local MPs, 96 are male, of whom 46 are Conservative. If we randomly select one MP, what is the probability of getting a Conservative given that a male was selected?
**Answer:** P(C∣M) = P(CM)/P(M) = (46/200)/(96/200) = 46/96 = **23/48 ≈ 0.479**.

## Q026
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** conditional-probability-and-bayes
**Focus Area:** Bayes' theorem
**Question:** Write Bayes' theorem in the detailed form given in the lecture notes for the four-sided die and coin example, computing P(2∣T).
**Answer:** **P(2∣T) = P(T∣2)·P(2) / [ P(T∣1)P(1) + P(T∣2)P(2) + P(T∣3)P(3) + P(T∣4)P(4) ]**, where the denominator equals P(T1) + P(T2) + P(T3) + P(T4) = P(T). In the shorter form, P(2∣T) = P(2T)/P(T) = (1/12)/(3/8) = **2/9**. The point is that the conditional on one side of the tree is calculated from the conditional on the other side.

## Q027
**Status:** active
**Type:** mcq
**Difficulty:** advanced
**Topic:** conditional-probability-and-bayes
**Focus Area:** Conditioning changes the sample space
**Question:** Someone has two children and you're told at least one is a girl. What is the probability the other is also a girl?
(a) 1/4 (b) 1/3 (c) 1/2 (d) 2/3
**Answer:** **(b) 1/3.** Knowing at least one is a girl rules out only the Boy-Boy case, leaving three equally likely cases: Boy-Girl, Girl-Boy, Girl-Girl (each ¼ ÷ ¾ = ⅓). Only one has two girls. The births themselves are independent — each child has a 0.5 chance of being a girl — but the information you're given filters the sample space in a different way, which is why the intuitive ½ is wrong.

## Q028
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** permutations-and-combinations
**Focus Area:** Fundamental counting rule
**Question:** State the fundamental counting rule.
**Answer:** When a process happens in stages, the total number of possible outcomes is the product of the choices at each stage: **Total outcomes = n₁ × n₂ × n₃ × … × n_k**. Every choice at one step branches into all the choices at the next step, like a tree expanding from a trunk.

## Q029
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** permutations-and-combinations
**Focus Area:** Factorials
**Question:** Define n! and state the value of 0!.
**Answer:** The factorial of n, written n!, is the product of all positive integers from 1 up to n: **n! = n × (n−1) × (n−2) × … × 3 × 2 × 1**. By definition, **0! = 1**. Factorials grow extremely quickly, which is a key reason large-scale combinatorial problems are so computationally expensive.

## Q030
**Status:** active
**Type:** conceptual
**Difficulty:** introductory
**Topic:** permutations-and-combinations
**Focus Area:** Permutation vs combination
**Question:** What single question tells you whether to use a permutation or a combination?
**Answer:** Ask: **would swapping two items create a different outcome?** If yes → permutation (order matters), P(n,r) = n!/(n−r)!. If no → combination (order doesn't matter), C(n,r) = n!/[r!(n−r)!]. Example contrast: ranking 3 candidates gold/silver/bronze is a permutation; selecting 3 team members is a combination. For 10 items with 3 chosen, ₁₀P₃ = 720 but ₁₀C₃ = 120.

## Q031
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** permutations-and-combinations
**Focus Area:** Applying the permutation formula
**Question:** Eight runners compete in a race. How many ways can gold, silver and bronze medals be awarded (no ties)?
**Answer:** P(8,3) = 8!/(8−3)! = 8!/5! = **336** different outcomes for the top three positions. Change the order of any two runners and you've created a new permutation.

## Q032
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** permutations-and-combinations
**Focus Area:** Permutations with identical items
**Question:** How many distinct arrangements are there of the letters in BALLOON, and why is the answer not 7!?
**Answer:** **1,260.** BALLOON has 7 letters, so if all were unique there would be 7! = 5,040 arrangements. But the two L's and two O's are identical, so many of those 5,040 would look exactly the same. We divide by the ways the identical letters could swap places: 7!/(2! × 2!) = 5,040/4 = 1,260.

## Q033
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** permutations-and-combinations
**Focus Area:** Applying the combination formula
**Question:** A cybersecurity team has 12 analysts and must select 3 for a special audit. How many unique teams can be formed?
**Answer:** Order doesn't matter — the same three people form one team no matter who's picked first — so use combinations: **C(12,3) = 220**.

## Q034
**Status:** active
**Type:** mcq
**Difficulty:** introductory
**Topic:** permutations-and-combinations
**Focus Area:** Fundamental counting rule applied
**Question:** A software test suite runs across 4 browsers, 3 user roles and 2 operating systems. How many total test configurations are possible?
(a) 9 (b) 14 (c) 24 (d) 48
**Answer:** **(c) 24.** 4 × 3 × 2 = 24. These are independent choices, not alternatives — multiply them, don't add them. Each test dimension multiplies the total possibilities.

## Q035
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** permutations-and-combinations
**Focus Area:** The five counting cases
**Question:** State the five counting cases from the lecture notes with their formulas.
**Answer:** **Case 1** — choosing from n distinct objects r times *with* repetition: **nʳ**. **Case 2** — permuting n distinct objects (no repetitions): **n!**. **Case 3** — choosing and permuting r objects from n distinct objects (no repetition): **n!/(n−r)!** = ₙP_r. **Case 4** — choosing r objects from n distinct objects (no repetition, no permutation): ₙP_r/r! = **n!/[r!(n−r)!]** = ₙC_r. **Case 5** — partitioning n distinct objects into k partitions of sizes n₁,…,n_k (summing to n, all > 0): **n!/(n₁! n₂! … n_k!)**. Note ₙC_r is a partition into k = 2 partitions of sizes r and n−r.

## Q036
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** random-variables-and-distributions
**Focus Area:** Definition of a random variable
**Question:** What is a random variable, and what is its spectrum?
**Answer:** A random variable is a numerical value representing the outcome of a random process or experiment — "random" because you can't predict its exact value in advance, "variable" because it can take different values each time. The lecture notes call it a **place holder for the numeric labels for the events**. We label random variables with capital letters (X, Y, Z) and their values with lowercase (x, y, z). Its **spectrum** is the set of allowed labels, {x}.

## Q037
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** random-variables-and-distributions
**Focus Area:** Discrete vs continuous
**Question:** Distinguish discrete from continuous random variables, in terms of both examples and the spectrum.
**Answer:** **Discrete** random variables take on only specific, countable values (often integers) — number of emails in an inbox, number of errors in a log file, number of heads in 10 coin flips. Their spectrum has **gaps** between the labels and **can be listed**. **Continuous** random variables can take any value within a range or interval — server response time, CPU temperature, download speed. Their spectrum has **no gaps** and **cannot be listed**. A discrete random variable has a probability distribution {P(x)} for each label; a continuous one has a distribution for each *interval*, P(a ≤ x ≤ b).

## Q038
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** random-variables-and-distributions
**Focus Area:** Valid probability distributions
**Question:** State the two conditions a valid probability distribution must satisfy.
**Answer:** (1) **Each probability must be between 0 and 1:** 0 ≤ P(X = xᵢ) ≤ 1 — a probability can't be negative and can't exceed certainty. (2) **The total probability across all outcomes must equal 1:** ∑ P(X = xᵢ) = 1 — something from the sample space will happen. These act as a sanity check; if either fails, the table doesn't represent a valid random variable.

## Q039
**Status:** active
**Type:** true-false
**Difficulty:** intermediate
**Topic:** random-variables-and-distributions
**Focus Area:** Validity check
**Question:** True or false: the table P(0) = 0.04, P(1) = 0.26, P(2) = 0.36, P(3) = 0.20, P(4) = 0.08 is a genuine probability distribution.
**Answer:** **False.** Every individual probability is between 0 and 1, so the first condition holds, but the sum is 0.94 ≠ 1.00, so the second condition fails. It is not a genuine probability distribution.

## Q040
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** random-variables-and-distributions
**Focus Area:** Constructing a distribution
**Question:** For the sum of two fair six-sided dice, which sum is most likely and which are rarest? Give the probabilities.
**Answer:** The most likely sum is **7**, which occurs in six different ways, so P = 6/36 ≈ 16.7%. The rarest sums are **2 and 12**, each occurring only once, so P = 1/36 ≈ 2.8%. Not all sums are equally likely, because some can occur in more ways than others. This shape — low at the ends, high in the middle — is one of the first examples of a distribution curve.

## Q041
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** expected-value-variance-standard-deviation
**Focus Area:** Expected value
**Question:** Define the expected value of a discrete random variable and give its formula.
**Answer:** The expected value (also called the mean or expectation) represents the average outcome over the long run: **μ = E[X] = ∑ₓ [x · P(x)]** — multiply each x by P(x), then add all the outcomes. Think of it as the centre of the probability distribution, or a balance point: the value you'd expect if you repeated the experiment infinitely many times. It's not about predicting any one trial.

## Q042
**Status:** active
**Type:** mcq
**Difficulty:** introductory
**Topic:** expected-value-variance-standard-deviation
**Focus Area:** Expected value of a die roll
**Question:** A fair six-sided die is rolled once. What is the expected value of the outcome?
(a) 3 (b) 3.5 (c) 4 (d) 6
**Answer:** **(b) 3.5.** E[X] = (1+2+3+4+5+6)/6 = 21/6 = 3.5. You'll never roll a 3.5 — the expected value isn't a likely outcome, it's the average of all possible outcomes weighted by their probabilities, and it's the number a simulation of millions of dice rolls would approach.

## Q043
**Status:** active
**Type:** true-false
**Difficulty:** intermediate
**Topic:** expected-value-variance-standard-deviation
**Focus Area:** The mean need not be in the spectrum
**Question:** True or false: the expected value of a random variable must be one of its possible outcomes.
**Answer:** **False.** The mean value of X need not be — and usually isn't — in the spectrum of X. However, **min x ≤ μ_X ≤ max x** always holds.

## Q044
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** expected-value-variance-standard-deviation
**Focus Area:** Variance and standard deviation
**Question:** Give the definition formula for the variance of a discrete random variable, and explain why we also take a square root.
**Answer:** **σ² = ∑ (xᵢ − μ)² · P(X = xᵢ)**. The formula calculates how far each outcome is from the mean (xᵢ − μ), squares those deviations to avoid negatives, and weights them by their probabilities — giving the average of the squared deviations. Because of the squaring, variance is measured in **squared units**. Taking the square root gives the **standard deviation** σ, which returns to the original units of measurement and tells you roughly how far typical outcomes fall from the mean.

## Q045
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** expected-value-variance-standard-deviation
**Focus Area:** Shortcut formula
**Question:** State the shortcut formula for variance and describe the procedure.
**Answer:** **Var(X) = E[X²] − (E[X])²**, where E[X²] = ∑ xᵢ² · P(X = xᵢ). You calculate the expected value of the squares, then subtract the square of the expected value. Equivalently σ_X = √( ∑ₓ [x²·P(x)] − μ² ).

## Q046
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** expected-value-variance-standard-deviation
**Focus Area:** Applying the shortcut formula
**Question:** A QA tester records failed test cases per day as P(0) = 0.1, P(1) = 0.4, P(2) = 0.3, P(3) = 0.2. Find the mean, variance and standard deviation.
**Answer:** E[X] = 0(0.1) + 1(0.4) + 2(0.3) + 3(0.2) = **1.6**. E[X²] = 0²(0.1) + 1²(0.4) + 2²(0.3) + 3²(0.2) = **3.4**. Var(X) = 3.4 − (1.6)² = 3.4 − 2.56 = **0.84**. σ = √0.84 ≈ **0.916**. So on average 1.6 tests fail per run, with typical variation of about 0.916 failures around that mean.

## Q047
**Status:** active
**Type:** mcq
**Difficulty:** intermediate
**Topic:** expected-value-variance-standard-deviation
**Focus Area:** Interpreting standard deviation
**Question:** Two algorithms both average 10 ms. Algorithm A has σ = 0.2 ms, Algorithm B has σ = 3.5 ms. Which is more predictable?
(a) A, because its standard deviation is smaller (b) B, because its standard deviation is larger (c) Both equally, because the means match (d) Not enough information
**Answer:** **(a) Algorithm A.** A smaller standard deviation means results stay close to the mean, so A's times vary very little and its performance is consistent. The mean describes the central value, not the spread — two processes can share a mean but differ drastically in variability, so (c) is wrong; and the mean plus standard deviation give both centre and spread, which is enough to judge predictability, so (d) is wrong.

## Q048
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** expected-value-variance-standard-deviation
**Focus Area:** Rule of thumb for usual values
**Question:** State the "rule of thumb" range for usual values, and apply it to the World Series example (μ = 5.8 games, σ = 1.1 games).
**Answer:** The rule of thumb is **μ_X − 2σ_X ≤ x ≤ μ_X + 2σ_X**. For the World Series: 5.8 − 2.2 ≤ x ≤ 5.8 + 2.2, i.e. 3.6 ≤ x ≤ 8.0, so 4 ≤ x ≤ 7 games. Since a 4-game sweep falls inside this range, it is **not** unusual for a team to sweep by winning in four games.

## Q049
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** binomial-distribution
**Focus Area:** Conditions for a binomial random variable
**Question:** What three conditions must hold for a random variable to be binomial?
**Answer:** A binomial random variable counts the number of "successes" in a **fixed** number of trials, where: (1) each trial has only **two** possible outcomes, labelled "0" for failure and "1" for success; (2) each trial is **independent** from other trials; (3) the probability of failure and success of each trial remains **constant** for all trials. Such trials are called **independent identically distributed (iid)**.

## Q050
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** binomial-distribution
**Focus Area:** The binomial formula
**Question:** State the binomial probability formula and define every symbol.
**Answer:** **P(X = k) = (ₙC_k) · pᵏ · q^(n−k)**, where k is the number of successes, n is the total fixed number of trials, p = P(1) is the probability of success in each single trial (a constant), and q = 1 − p = P(0) is the probability of failure in each single trial. ₙC_k ("n choose k") counts the number of combinations in choosing k identical outcomes out of a total of n outcomes: ₙC_k = n!/[(n−k)! k!].

## Q051
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** binomial-distribution
**Focus Area:** Binomial mean and standard deviation
**Question:** Give the mean and standard deviation of a binomial random variable, and state how many parameters define it.
**Answer:** **μ_X = E(X) = np** and **σ_X = √(np(1−p)) = √(npq)**, where q = 1 − p. The binomial random variable has **two** parameters to define: n and p.

## Q052
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** binomial-distribution
**Focus Area:** Deriving the formula
**Question:** Toss a coin 5 times. Set up the random variable and write P(X = 3) in binomial form.
**Answer:** Always start with the random variable: let X count the number of heads in 5 tosses. Then n = 5; "success" = observing a head (label 1); "failure" = observing a tail (label 0); the spectrum of X is {0, 1, 2, 3, 4, 5}. With p = P(head on a single toss) and q = 1 − p, enumerating the tree and grouping by head-count gives P(X = 3) = (10) p³q² = **(₅C₃) p³ q^(5−3)**.

## Q053
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** binomial-distribution
**Focus Area:** Rule of thumb for independence
**Question:** When sampling without replacement, under what condition may events be treated as independent?
**Answer:** When **n < 0.05 N**, where n is the sample size and N is the total population size.

## Q054
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** poisson-distribution
**Focus Area:** What a Poisson random variable counts
**Question:** What does a Poisson random variable count, and what is its formula?
**Answer:** A Poisson random variable counts the number of **(independent) occurrences of a certain event over an interval** of time (or space, area, lengths…). Its formula is **P(X = k) = (μᵏ / k!) e^(−μ)**, where k is the number of occurrences in the given interval and μ is the mean number of occurrences in the same interval.

## Q055
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** poisson-distribution
**Focus Area:** Poisson as a limit of the binomial
**Question:** Explain how the Poisson distribution arises from the binomial, and why it is useful.
**Answer:** In the binomial distribution, if the number of trials n becomes very large while the probability of success in each trial becomes proportionally small, so that the expected amount **μ = np** remains the same, we can approximate the binomial by the simpler Poisson: ₙC_k pᵏ q^(n−k) ≈ (μᵏ/k!)e^(−μ). This is useful because binomial values are hard to calculate — ₙC_k involves many, many products for large n. The Poisson value becomes exact when n becomes unbounded and infinite. Conceptually, the number of "moments," which are infinite, replaces n as the number of trials.

## Q056
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** poisson-distribution
**Focus Area:** Parameters
**Question:** How many parameters does a Poisson random variable have, and what are its mean and standard deviation?
**Answer:** It has **only one** parameter, the mean number of occurrences μ. Then **μ_X = μ** and **σ_X = √μ**. Contrast the binomial, which needs two parameters (n and p), with μ_X = np and σ_X = √(npq) — and note that if n → ∞ and p → 0 (so q → 1), then np = μ and √(npq) = √(μ·1) = √μ, so the binomial parameters collapse into the Poisson ones.

## Q057
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** poisson-distribution
**Focus Area:** Matching the interval
**Question:** A switchboard receives a mean of 3 wrong numbers per minute. What must you do before computing the probability of receiving at least two wrong numbers in the next 2 minutes?
**Answer:** You must **rescale μ to match the counting interval**. The value of μ used in the formula must be the mean number of occurrences in the *same interval* as the interval over which the variable is counting occurrences. Since the question asks about 2 minutes but the given mean is per minute, you need to change μ to the mean for that 2-minute interval first, before calculating any probabilities.

## Q058
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** poisson-distribution
**Focus Area:** Poisson approximation rule of thumb
**Question:** Under what conditions may the Poisson distribution be used to approximate the binomial?
**Answer:** When **n ≥ 100** and **np ≤ 10**.

## Q059
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** normal-distribution
**Focus Area:** From histogram to density curve
**Question:** How does the picture of a probability distribution change when moving from a discrete to a continuous random variable?
**Answer:** For a discrete random variable the labels can be listed and indexed, so the distribution is a **histogram** — the condition ∑ P(xᵢ) = 1 means the areas of all rectangles must add to 1 (each rectangle has height P(xᵢ) and width 1). For a continuous random variable the labels have no gaps and cannot be listed or indexed by integers, so a **smooth curve replaces the sharp edges of the histogram**. The area under the curve for each interval gives the probability that the random variable falls in that interval: P(x₁ ≤ X ≤ x₂) = p.

## Q060
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** normal-distribution
**Focus Area:** Legitimate probability density
**Question:** What two conditions must a function f satisfy to be a legitimate probability density distribution?
**Answer:** (1) **f(x) ≥ 0** for all x in the spectrum of X. (2) **The total area under the curve must equal 1.** It follows that the area of each subset is less than or equal to 1. Note that because values don't come in rectangles of width 1, the *height* of the graph need not be below 1 — the height denotes the **probability density**.

## Q061
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** normal-distribution
**Focus Area:** Properties of the normal curve
**Question:** List the key properties of the Normal distribution curve.
**Answer:** It is **symmetric** and **bell-shaped** (also called the Gaussian curve). The **mean, mode and median are all equal**, located under the peak. The **tails on left and right approach zero asymptotically** — never actually zero, but tending to zero as x approaches −∞ or +∞. Values on the horizontal axis are the labels of X, representing outcomes the random variable holds. The **area under the curve represents the probability**, with 0 ≤ p ≤ 1. It is written X ~ N(μ_X, σ_X).

## Q062
**Status:** active
**Type:** true-false
**Difficulty:** advanced
**Topic:** normal-distribution
**Focus Area:** Probability of a single point
**Question:** True or false: for a continuous random variable, P(x₁ ≤ X ≤ x₂) and P(x₁ < X < x₂) can differ.
**Answer:** **False.** Since probability equals area, P(X = x) ≡ 0 — a point on the real line corresponds to a zero (infinitesimal) interval and thus zero area. Therefore P(x₁ ≤ X ≤ x₂) = P(x₁ ≤ X < x₂) = P(x₁ < X ≤ x₂) = P(x₁ < X < x₂); including or excluding the endpoints makes no difference.

## Q063
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** normal-distribution
**Focus Area:** The standard normal distribution
**Question:** What defines the standard Normal distribution, and what are z-scores and p-values?
**Answer:** The standard Normal distribution has **μ_X = 0** and **σ_X = 1**. By convention the random variable with this distribution is denoted **Z**, and its values are called **z-scores**. The area for a given z-score interval is called its **p-value** — e.g. P(Z < z) = p.

## Q064
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** normal-distribution
**Focus Area:** Converting to the standard normal
**Question:** Give the conversion formulas between a general Normal distribution and the standard Normal, and show how a probability transfers.
**Answer:** **z = (x − μ_X)/σ_X** and **x = μ_X + z σ_X**. Consequently P(X < x₁) = P(Z < z₁), and P(x₁ < X < x₂) = P(X < x₂) − P(X < x₁) = P(Z < z₂) − P(Z < z₁) = P(z₁ < Z < z₂).

## Q065
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** normal-distribution
**Focus Area:** Combining areas and symmetry
**Question:** How do you find P(z₁ < Z < z₂) from a cumulative table, and what does symmetry give you?
**Answer:** **P(z₁ < Z < z₂) = P(Z < z₂) − P(Z < z₁)** — subtract the smaller cumulative area from the larger. Due to symmetry around 0, for any z-score z: **P(Z ≤ −z) = P(Z ≥ z)**.

## Q066
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** normal-distribution
**Focus Area:** Critical values
**Question:** Define a critical value and give the two standard examples from the notes.
**Answer:** A **critical value** is a z-score that separates unlikely values from those that are likely to occur. We write z_α when P(Z ≥ z_α) = α and P(Z ≤ −z_α) = α. The two standard examples: α = 0.05 → **z₀.₀₅ = 1.645**, giving P(−1.645 < Z < 1.645) = 0.90; and α = 0.025 → **z₀.₀₂₅ = 1.96**, giving P(−1.96 < Z < 1.96) = 0.95.

## Q067
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** normal-distribution
**Focus Area:** Applying the z-table
**Question:** A bone density reading between −1.00 and −2.50 indicates osteopenia. Given that the area left of z = −2.50 is 0.0062 and the area left of z = −1.00 is 0.1587, find this probability.
**Answer:** The area between them is the difference of the two cumulative areas: 0.1587 − 0.0062 = **0.1525**.

## Q068
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** sampling-distributions-and-clt
**Focus Area:** Sampling distribution
**Question:** What is a sampling distribution, and how is it constructed?
**Answer:** Take a sample of size n from values of a random variable X, then compute a statistic of the sample like the mean x̄. Take a *different* sample of size n and repeat — the mean will most likely differ. Repeat many times and store the values of x̄ in a new random variable, **X̄ₙ**. X̄ₙ will typically have a different distribution than X, and **the distribution of X̄ is called the sampling distribution**.

## Q069
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** sampling-distributions-and-clt
**Focus Area:** Statement of the CLT
**Question:** State the Central Limit Theorem, including the formulas for the mean and standard deviation of the sampling distribution.
**Answer:** X can be **any** random variable — it need not be Normal, and need not even be continuous. If the sample sizes n are large, the sample distribution X̄ₙ will have approximately a Normal distribution: **X̄ₙ ~ N(μ_x̄, σ_x̄)** where **μ_x̄ = μ_X** and **σ_x̄ = σ_X / √n**.

## Q070
**Status:** active
**Type:** mcq
**Difficulty:** intermediate
**Topic:** sampling-distributions-and-clt
**Focus Area:** Sample size requirement
**Question:** For the Central Limit Theorem to be a good approximation when X is **not** itself Normal, how large must n be?
(a) n ≥ 5 (b) n ≥ 10 (c) n ≥ 30 (d) any size
**Answer:** **(c) n ≥ 30.** If X is itself Normal, n can be any size. If X is not Normal, then n ≥ 30 is required for the C.L.T. to be a good approximation.

## Q071
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** sampling-distributions-and-clt
**Focus Area:** What the CLT buys you
**Question:** Starting from an arbitrary, even multi-peaked, distribution for X, describe what the CLT tells you about the distribution of sample means.
**Answer:** Drawing many samples of size n ≥ 30 and collecting their means produces a **Normal** distribution for X̄ — regardless of the shape of X. It is centred at the **same mean** (μ_x̄ = μ_X) but is **narrower**, with σ_x̄ = σ_X/√n. The notes illustrate this convergence from three starting shapes — Normal, Uniform and U-shaped — showing that as n goes from 1 to 50, the distribution of sample means approaches a normal distribution in every case.

## Q072
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** sampling-distributions-and-clt
**Focus Area:** Single observation vs sample mean
**Question:** In the elevator problem, why are parts (a) and (b) different — the probability that one male weighs more than 156.25 lb versus the probability that a sample of 16 males has a mean weight greater than 156.25 lb?
**Answer:** Part (a) uses the distribution of a **single** observation, X ~ N(182.9, 40.8). Part (b) uses the **sampling distribution** of the mean, X̄₁₆, which by the CLT has the same mean (μ_x̄ = 182.9) but a standard deviation reduced by a factor of √n: σ_x̄ = 40.8/√16. The sample mean is far less spread out than a single observation, so the two probabilities differ.

## Q073
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** random-variables-and-distributions
**Focus Area:** Recovering a missing probability
**Question:** A random variable X has P(−4) = 0.65, P(2) = ?, P(3) = 0.10 and P(5) = 0.05. Determine the missing value P(X = 2).
**Answer:** **P(X = 2) = 0.20.** The probabilities of a valid distribution must sum to 1. The known entries total 0.65 + 0.10 + 0.05 = 0.80, so the missing entry is 1 − 0.80 = 0.20.

## Q074
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** expected-value-variance-standard-deviation
**Focus Area:** Expected value with negative outcomes
**Question:** For the distribution P(−4) = 0.65, P(2) = 0.20, P(3) = 0.10, P(5) = 0.05, compute the expected value E[X].
**Answer:** **E[X] = −1.65.** Applying μ = ∑ₓ [x · P(x)]: (−4)(0.65) + (2)(0.20) + (3)(0.10) + (5)(0.05) = −2.60 + 0.40 + 0.30 + 0.25 = −1.65. The heavy 0.65 weight on x = −4 pulls the mean below zero.

## Q075
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** expected-value-variance-standard-deviation
**Focus Area:** Variance via the shortcut formula
**Question:** For the distribution P(−4) = 0.65, P(2) = 0.20, P(3) = 0.10, P(5) = 0.05 with E[X] = −1.65, compute Var(X).
**Answer:** **Var(X) = 10.6275.** Using Var(X) = E[X²] − (E[X])²: E[X²] = 16(0.65) + 4(0.20) + 9(0.10) + 25(0.05) = 10.40 + 0.80 + 0.90 + 1.25 = 13.35. Then Var(X) = 13.35 − (−1.65)² = 13.35 − 2.7225 = 10.6275. (σ = √10.6275 ≈ 3.26.)

## Q076
**Status:** active
**Type:** true-false
**Difficulty:** intermediate
**Topic:** expected-value-variance-standard-deviation
**Focus Area:** Squaring a negative mean
**Question:** True or False: When the expected value is negative, the term (E[X])² in the shortcut variance formula is added rather than subtracted.
**Answer:** **False.** A negative mean squares to a positive number — (−1.65)² = +2.7225 — so it is still subtracted: Var(X) = E[X²] − (E[X])². The sign of the mean never changes the structure of the formula.

## Q077
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** expected-value-variance-standard-deviation
**Focus Area:** The mean need not be in the spectrum
**Question:** The distribution P(−4) = 0.65, P(2) = 0.20, P(3) = 0.10, P(5) = 0.05 has E[X] = −1.65, which is not one of the four possible values of X. Is this a problem? What constraint does the mean satisfy?
**Answer:** No — the mean need not be (and usually isn't) in the spectrum of X. The only constraint is **min x ≤ μ_X ≤ max x**, which holds here since −4 ≤ −1.65 ≤ 5.

## Q078
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** conditional-probability-and-bayes
**Focus Area:** Bayes' Theorem — reversing the conditioning
**Question:** AJ takes the train 70% of the time, otherwise an Uber. He is late 15% of the time when taking the train and 65% of the time when taking an Uber. Given that AJ is late, find the probability he took an Uber.
**Answer:** **P(U∣L) = 0.65.** By Bayes' Theorem, P(U∣L) = P(L∣U)P(U) / [P(L∣T)P(T) + P(L∣U)P(U)]. The joints are P(L∩U) = 0.65 × 0.30 = 0.195 and P(L∩T) = 0.15 × 0.70 = 0.105, so P(L) = 0.300. Then 0.195/0.300 = 0.65.

## Q079
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** conditional-probability-and-bayes
**Focus Area:** Why Bayes is needed
**Question:** In the AJ commute problem the answer P(U∣L) = 0.65 is numerically the same as the given P(L∣U) = 0.65. Does this mean the two are the same quantity? Explain.
**Answer:** No — the coincidence is an artefact of these particular numbers. P(L∣U) is the probability of being late given an Uber was taken; P(U∣L) is the probability an Uber was taken given lateness. They condition on different events and have different denominators. Treating P(A∣B) and P(B∣A) as interchangeable is the classic error that Bayes' Theorem exists to correct.

## Q080
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** conditional-probability-and-bayes
**Focus Area:** Completing a contingency table
**Question:** In a survey of 800 athletes: those who stretch had 295 with no injury; those who don't stretch had 231 injuries and total 450. Fill in the four missing entries of the contingency table.
**Answer:** Stretches total = 800 − 450 = **350**; Stretches/Had Injury = 350 − 295 = **55**; Doesn't Stretch/No Injury = 450 − 231 = **219**; column totals = Had Injury **286** (55 + 231) and No Injury **514** (295 + 219). Check: 286 + 514 = 800.

## Q081
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** conditional-probability-and-bayes
**Focus Area:** Conditional probability from a table
**Question:** Using the completed athletes table (Stretches 55/295/350; Doesn't Stretch 231/219/450; totals 286/514/800), find the probability that an athlete had an injury given that they did not perform stretches.
**Answer:** **231/450 ≈ 0.513.** Conditioning on "doesn't stretch" restricts the sample space to that row, so the denominator is the row total 450, not the grand total 800.

## Q082
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** conditional-probability-and-bayes
**Focus Area:** Direction of conditioning
**Question:** From the athletes table, P(injury ∣ doesn't stretch) = 231/450 while P(stretches ∣ no injury) = 295/514. Explain why the denominators differ.
**Answer:** Each conditional probability restricts the sample space to whatever is given. Conditioning on "doesn't stretch" restricts to that **row**, so the denominator is the row total 450. Conditioning on "no injury" restricts to that **column**, so the denominator is the column total 514. The given event always supplies the denominator, which is why P(A∣B) ≠ P(B∣A).

## Q083
**Status:** active
**Type:** mcq
**Difficulty:** intermediate
**Topic:** conditional-probability-and-bayes
**Focus Area:** Marginal probability from counts
**Question:** Of 210 patients, 75 were alcoholic (35 with cirrhosis) and 135 non-alcoholic (5 with cirrhosis). What is the probability that a randomly selected patient has cirrhosis?
(a) 35/210 (b) 40/210 (c) 35/75 (d) 5/135
**Answer:** **(b) 40/210 ≈ 0.190.** Total cirrhosis cases are 35 + 5 = 40 across all 210 patients — a marginal probability, so the denominator is the grand total.

## Q084
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** conditional-probability-and-bayes
**Focus Area:** Joint versus conditional probability
**Question:** In the 210-patient study, "the probability of an alcoholic with cirrhosis" is 35/210 ≈ 0.167, but P(cirrhosis ∣ alcoholic) is 35/75 ≈ 0.467. What distinguishes the two?
**Answer:** The first is a **joint** probability — of all 210 patients, how many are both alcoholic and cirrhotic — so the denominator is the grand total. The second is a **conditional** probability, which restricts the sample space to the 75 alcoholic patients, so the denominator is that subgroup. The wording ("an alcoholic with cirrhosis" versus "given that they are alcoholic") determines which denominator applies.

## Q085
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** addition-and-multiplication-rules
**Focus Area:** Addition rule with mutually exclusive events
**Question:** From the Titanic table (Men 332 survived/1360 died; Women 318/104; Boys 29/35; Girls 27/18; 2223 total), find the probability of selecting someone who is a woman or a child.
**Answer:** **531/2223 ≈ 0.239.** "Woman" and "child" are mutually exclusive — no passenger is both — so P(A∪B) = P(A) + P(B) with no overlap term. Women = 422, children = 64 + 45 = 109, giving (422 + 109)/2223.

## Q086
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** addition-and-multiplication-rules
**Focus Area:** Addition rule with overlap
**Question:** From the same Titanic table, find the probability of selecting a child or someone who survived the sinking.
**Answer:** **759/2223 ≈ 0.341.** These categories overlap — 29 + 27 = 56 children survived — so the full addition rule applies: P(A∪B) = P(A) + P(B) − P(A∩B) = (109 + 706 − 56)/2223. Omitting the subtraction would double-count the 56 surviving children.

## Q087
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** addition-and-multiplication-rules
**Focus Area:** When to subtract the overlap
**Question:** In the Titanic problem, "woman or child" needs no overlap subtraction but "child or survived" does. What determines which form of the addition rule you use?
**Answer:** Whether the two events can occur together. "Woman" and "child" are mutually exclusive categories in that table, so P(A∩B) = 0 and the rule simplifies to P(A) + P(B). "Child" and "survived" can both be true of the same passenger, so P(A∩B) ≠ 0 and the overlap must be subtracted once to avoid double-counting.

## Q088
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** complement-events
**Focus Area:** Applying the complement rule
**Question:** When a woman over 25 is randomly selected, there is a 0.218 probability that she has a bachelor's degree. Find the probability that she does not have one.
**Answer:** **0.782.** By the complement rule P(Aᶜ) = 1 − P(A) = 1 − 0.218 = 0.782.

## Q089
**Status:** active
**Type:** mcq
**Difficulty:** intermediate
**Topic:** addition-and-multiplication-rules
**Focus Area:** Identifying dependence
**Question:** Which of these pairs of consecutive events is **dependent**?
(a) Picking a black marble and placing it back, then picking another marble
(b) Picking a black marble and leaving it outside, then picking another marble
(c) Flipping a coin, then rolling a die
(d) None of these
**Answer:** **(b).** Leaving the marble out means the bag's contents change, so the first draw alters the probability of the second — the defining signature of a without-replacement draw. In (a) replacement restores the original state, so the draws are independent.

## Q090
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** addition-and-multiplication-rules
**Focus Area:** Why replacement matters
**Question:** Why does replacing a drawn marble make two consecutive draws independent, while leaving it out makes them dependent?
**Answer:** Independence means P(B∣A) = P(B) — the first event has no influence on the second. Replacing the marble restores the bag to its original composition, so the second draw faces exactly the same probabilities as the first. Leaving it out changes both the count of that colour and the total, so the second draw's probability depends on what was drawn first.

## Q091
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** addition-and-multiplication-rules
**Focus Area:** Multiplication rule with replacement
**Question:** A biologist has six plants: two vascular (V) and four nonvascular (N). Two are selected **with replacement**. Find the probability that both are nonvascular.
**Answer:** **4/9 ≈ 0.444.** With replacement the draws are independent, so P(N ∩ N) = P(N) × P(N) = 4/6 × 4/6 = 16/36 = 4/9.

## Q092
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** addition-and-multiplication-rules
**Focus Area:** Multiplication rule without replacement
**Question:** For the same six plants (two vascular, four nonvascular), find the probability both selections are nonvascular when made **without replacement**.
**Answer:** **2/5 = 0.400.** The draws are dependent, so P(N ∩ N) = P(N) × P(N∣N) = 4/6 × 3/5 = 12/30 = 2/5. It is smaller than the with-replacement answer because removing one nonvascular plant leaves proportionally fewer behind.

## Q093
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** addition-and-multiplication-rules
**Focus Area:** Repeated independent trials
**Question:** In a test of a gender-selection method, 12 couples try to have baby girls. If the method has no effect, what is the probability that all 12 babies will be girls?
**Answer:** **(0.5)¹² = 1/4096 ≈ 0.000244.** With no effect, each birth is independent with P(girl) = 0.5, so the multiplication rule for independent events gives 0.5 multiplied by itself 12 times. The binomial formula gives the same: ₁₂C₁₂ · (0.5)¹² · (0.5)⁰.

## Q094
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** addition-and-multiplication-rules
**Focus Area:** Interpreting a very small probability
**Question:** If all 12 babies in the gender-selection trial are girls, does the method appear to be effective? Justify your answer using the probability you computed.
**Answer:** Yes. Under the assumption that the method does nothing, the probability of that outcome is about 0.000244 — so small that it would almost never occur by chance. Observing it anyway is evidence against the "no effect" assumption, so the method does appear effective.

## Q095
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** permutations-and-combinations
**Focus Area:** Counting with repetition
**Question:** A home alarm code has four digits, each 0 through 9, entered in order. How many codes are possible if each digit can be repeated?
**Answer:** **10,000.** This is choosing from n distinct objects r times with repetition: nʳ = 10⁴ = 10,000.

## Q096
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** permutations-and-combinations
**Focus Area:** Counting without repetition
**Question:** For the same four-digit alarm code, how many are possible if no digit can be repeated?
**Answer:** **5,040.** Each position has one fewer option: 10 × 9 × 8 × 7 = 5,040. Equivalently P(10,4) = 10!/(10−4)! = 10!/6! = 5,040.

## Q097
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** permutations-and-combinations
**Focus Area:** Evaluating a factorial
**Question:** Evaluate 6!.
**Answer:** **720.** 6! = 6 × 5 × 4 × 3 × 2 × 1 = 720.

## Q098
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** permutations-and-combinations
**Focus Area:** Arranging distinct letters
**Question:** How many ways can the letters T A I S E R be arranged?
**Answer:** **720.** All six letters are distinct, so this is a straight permutation of n distinct objects: 6! = 720.

## Q099
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** permutations-and-combinations
**Focus Area:** Permutations with repeated letters
**Question:** Find the number of arrangements of the letters T T I R R R O G H E.
**Answer:** **302,400.** There are 10 letters with T appearing twice and R three times, so unique arrangements = 10!/(2! × 3!) = 3,628,800/12 = 302,400. Dividing by 2! and 3! removes rearrangements of the identical letters among themselves.

## Q100
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** permutations-and-combinations
**Focus Area:** Lottery odds when order matters
**Question:** In a lottery you select six numbers from 1 to 42 and win only if your numbers come up in the correct order. What is the probability of winning?
**Answer:** **1/3,776,965,920.** Order matters with no repetition, so the count is a permutation: ₄₂P₆ = 42 × 41 × 40 × 39 × 38 × 37 = 3,776,965,920. Exactly one arrangement wins.

## Q101
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** permutations-and-combinations
**Focus Area:** Lottery odds when order does not matter
**Question:** For the same lottery, you now win if you choose the right six numbers regardless of order. What is the probability of winning?
**Answer:** **1/5,245,786.** Order no longer matters, so the count is a combination: ₄₂C₆ = ₄₂P₆/6! = 3,776,965,920/720 = 5,245,786.

## Q102
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** permutations-and-combinations
**Focus Area:** Why the r! divisor appears
**Question:** Dropping the order requirement in the 6-from-42 lottery improves your odds by a factor of exactly 720. Where does that number come from?
**Answer:** 720 = 6!, the number of ways a single set of six chosen numbers can be arranged. When order matters each of those 720 orderings is a distinct losing-or-winning outcome; when order doesn't matter they all collapse into one selection. That collapse is precisely what the r! in the denominator of C(n, r) = n!/[r!(n−r)!] accounts for.

## Q103
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** permutations-and-combinations
**Focus Area:** Combinations used to test a claim
**Question:** A company cut its sales staff from 32 to 28, claiming the four terminated employees were randomly selected — but the four chosen were the four oldest. Find the probability that a random selection would produce this result, and say what it implies.
**Answer:** **1/35,960 ≈ 0.0000278.** Order doesn't matter in choosing a group of four, so the number of possible groups is ₃₂C₄ = (32 × 31 × 30 × 29)/(4 × 3 × 2 × 1) = 863,040/24 = 35,960. Exactly one of those groups is the four oldest. A probability that small means the outcome would almost never arise by chance, which is evidence against the company's claim of random selection.

## Q104
**Status:** active
**Type:** mcq
**Difficulty:** introductory
**Topic:** introduction-to-probability
**Focus Area:** Classical probability with a certain event
**Question:** If a person is randomly selected, what is the probability that they were born on a day of the week that ends with the letter "y"?
(a) 1/7 (b) 2/7 (c) 5/7 (d) 1
**Answer:** **(d) 1.** All seven days of the week end in "y", so all outcomes are favourable: 7/7 = 1. This is a sure event.

## Q105
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** permutations-and-combinations
**Focus Area:** Choosing between permutation and combination
**Question:** The alarm-code problem uses a permutation while the staff-termination problem uses a combination, yet both select a fixed number of items from a larger set. What single test tells you which to use?
**Answer:** Ask whether swapping two selected items creates a different outcome. For an alarm code, 1234 and 4321 are different codes, so order matters → permutation. For a group of four employees to terminate, picking them in any order yields the same group, so order is irrelevant → combination.
