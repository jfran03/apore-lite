# Language Models

## Definition
A **language model** maintains some distribution over language. Nowadays, most language models are trained neural networks using the **transformer architecture**. The sources restrict discussion to **autoregressive language models**.
> Source: Copy of Section 3_ ML Learning Paradigms and Models, Neural Networks.pdf, Copy of Section 2_ Language Models, Alignment, Reasoning.pdf

## Key Concepts

### Probability Distributions
- A probability distribution pairs up events with a likelihood of them occurring.
- Key properties: probabilities cannot be negative and must add up to 1.
- **Sampling** from a distribution means picking one event according to how likely it is.
- Example: a fair die has distribution {(1, 1/6), (2, 1/6), ..., (6, 1/6)}.
  > Source: Copy of Section 1 _ Introduction to AI and Algoverse.pdf, Copy of Section 2_ Language Models, Alignment, Reasoning.pdf

### Probability Theory
- The two languages of machine learning are **probability theory** and **linear algebra**.
- Key identity: `P(x, y) = P(x|y) * P(y)` where P(x|y) is "probability of x given y."
- **Bayes' Rule:** `P(A|B) = P(B|A) * P(A) / P(B)`, if P(B) ≠ 0.
- **Chain Rule of Probability:** `P(X1, X2, ... Xn) = P(X1) * P(X2|X1) * P(X3|X1, X2) ... = Π P(Xi|X1,...,X_{i-1})`
  > Source: Copy of Section 2_ Language Models, Alignment, Reasoning.pdf

### Generative Models
- A **generative model** is a model (estimate) of a probability distribution.
- Rather than hand-specifying the distribution, we *learn* it from data.
- Generative models can take in **sequential data** — instead of assigning probability to single events, they assign it to *sequences* of events. Individual numbers in a sequence are called **tokens**.
  > Source: Copy of Section 1 _ Introduction to AI and Algoverse.pdf, Copy of Section 2_ Language Models, Alignment, Reasoning.pdf

### Autoregressive Models
- **Problem:** Once sequences get longer, there are exponentially many possible sequences — too many to fit explicitly. We need to simplify.
- **Autoregressive model:** A generative model that takes a sequence of input tokens and produces a **probability distribution over the next token** in the sequence.
- Sampling is easy: sample the first token, then sample the next token given the first, and so on — eventually producing a whole sequence.
- The reason this is equivalent to sampling from the complete distribution is the **probability chain rule**, a consequence of Bayes' rule.
  > Source: Copy of Section 1 _ Introduction to AI and Algoverse.pdf, Copy of Section 2_ Language Models, Alignment, Reasoning.pdf

### From Numbers to Language Models
- Replace tokens (numbers) with short sequences of letters and symbols.
- The task is just to predict the next token (autoregressively), and the model is optimized to get very good at this.
- If the model and dataset are big enough, we start to see **emergent behavior** — e.g., if enough math problems are in the dataset, the easiest way for the model to solve next-token prediction is to learn how to do math.
- If only 2 math problems are in the dataset, the model will just memorize them — a special case of overfitting.
- When we sample, the sequences form sentences and paragraphs.
- **Prompting:** The best way to control what we get is to manually specify the beginning of a sequence (called a **prefix** or **prompt**) and let the model finish it.
  > Source: Copy of Section 1 _ Introduction to AI and Algoverse.pdf, Copy of Section 2_ Language Models, Alignment, Reasoning.pdf

### Tokenization
- To plug text into a mathematical function, we must first turn text into numbers.
- A **tokenizer** finds commonly-occurring sequences of letters/symbols and assigns them numbers. (The algorithm used is Byte Pair Encoding (BPE) — out of scope.)
- Tokenizers have a fixed **vocabulary size** (typically 30k–60k tokens), referred to as V.
- Small words might only take one token; long or unusual words will be split up.
- **Special tokens** (not all tokenizers have all of these):
  - `<bos>` — beginning of sequence
  - `<eos>` — end of sequence
  - `<unk>` — unknown character
  - `<cls>` — used when training for classification
  > Source: Copy of Section 2_ Language Models, Alignment, Reasoning.pdf

### One-Hot Encoding
- Neural networks take in **vector** inputs (ordered lists of numbers).
- NNs generally do better with more, simpler dimensions.
- In **one-hot encoding**, a number (or numbered category) `i` is turned into a vector with a 1 at position `i` and 0 everywhere else.
- A OHE vector from a tokenizer with vocabulary size V will have dimension V.
  > Source: Copy of Section 2_ Language Models, Alignment, Reasoning.pdf

### Embeddings
- After one-hot encoding, each token transforms into a **learned embedding vector** — a lower-dimensional representation (often ~1k–3k dimensions).
- Similar tokens are typically assigned similar embedding vectors.
- How: the specific embedding is learned over the course of training.
  > Source: Copy of Section 2_ Language Models, Alignment, Reasoning.pdf

### Positional Embeddings
- In addition to the token embedding, a **positional embedding** is added to encode positional information. It does not depend on the token, only its position.
- Can be a vector of sinusoids or learned via training.
- **Absolute positional embeddings:** Different embedding for each position.
- **Relative positional embeddings:** Constructed so that when two tokens are compared/combined, only the *difference* in positions matters. Now more common.
  > Source: Copy of Section 2_ Language Models, Alignment, Reasoning.pdf

### LM Output Structure and Logits
- The output of an autoregressive Transformer LM has the same structure as its input: a sequence of dimension-V vectors, each representing **scores for each possible next output token**. These scores are called **logits**.
  > Source: Copy of Section 2_ Language Models, Alignment, Reasoning.pdf

### Softmax
- The **softmax function** normalizes a set of scores so they add to 1 (a valid probability distribution).
- Formula: `softmax(z_i) = e^z_i / Σ_j e^z_j`
- Properties:
  - Larger scores → larger probabilities.
  - Shift-invariant (adding a constant doesn't change it).
  - Maps everything to (0, 1).
  - All outputs sum to 1.
  > Source: Copy of Section 2_ Language Models, Alignment, Reasoning.pdf

### Temperature
- **Temperature (τ):** An extra term introduced by dividing logits by τ before applying softmax: `softmax(z_i; T) = e^(z_i/T) / Σ_j e^(z_j/T)`
- **High temperature:** Logits scaled down → distribution gets **flatter** (more random/chaotic output).
- **Low temperature:** Logits scaled up → the maximum logit dominates, everything else shrinks toward zero (less random, more deterministic).
  > Source: Copy of Section 2_ Language Models, Alignment, Reasoning.pdf

### Generating Text
- **Greedy Decoding:** Starting from a prefix, take the maximum-probability token and append it. Repeat until enough tokens are generated.
- **Sampling:** Instead of taking the max, sample a token according to the probability distribution. Temperature affects how random this sampling is.
  > Source: Copy of Section 2_ Language Models, Alignment, Reasoning.pdf

### Scoring Text
- Using the chain rule, we can compute the probability a model assigns to a sequence of text.
- This lets us score how "likely" an input text is — specifically, how likely it would be for the text to appear in the distribution the model was trained on.
- Probability is typically lower for longer sequences.
  > Source: Copy of Section 2_ Language Models, Alignment, Reasoning.pdf

### Autoregressive Language Modeling
- An autoregressive LM is just an estimate of the conditional probability term from the chain rule: `P(Xi | X1, ..., X_{i-1})`.
- In practice, this is a function that takes in a sequence of tokens and outputs estimated probabilities for the next token.
  > Source: Copy of Section 2_ Language Models, Alignment, Reasoning.pdf

### Surrogate Objective (Training LMs)
- At training time, the model outputs predicted scores for potential next tokens, normalized to a probability distribution.
- We don't have access to the true next-token probabilities, but the dataset *does* have the actual next token.
- As a surrogate, we use a **one-hot encoding** of the true next token and optimize the model's output to match it. This can lead to **miscalibration** — the model is encouraged to be confident in the next token.
- Using a large enough dataset, the model learns the general pattern (Monte Carlo sampling intuition).
  > Source: Copy of Section 4_ Training and Gradient Descent, Pytorch intro.pdf

## Common Misconceptions
- Language modeling is **not** the same as "foundational models" in the sense of large general-purpose models — it simply refers to the task of predicting the next token.
  > Source: Copy of Section 2_ Language Models, Alignment, Reasoning.pdf

## Related Topics
- [alignment.md](alignment.md)
- [prompting-reasoning.md](prompting-reasoning.md)
- [neural-networks.md](neural-networks.md)
- [encoder-models.md](encoder-models.md)
