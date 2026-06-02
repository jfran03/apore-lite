# Encoder Models (BERT)

## Definition
Encoder models (like BERT) are distinct from autoregressive, decoder-only language models. Rather than generating text, they produce rich representations of input text useful for understanding tasks.
> Source: Copy of Section 4_ Training and Gradient Descent, Pytorch intro.pdf

## Key Concepts

### Motivation: Why Encoder Models?
- Autoregressive, decoder-only models are not ideal for all tasks.
- They are trained to output text, which isn't ideal for every task.
- If you don't need to generate text, it helps to be able to **look both ways** (both past and future tokens in a sentence).
  - Example: "April went to the store." vs. "April is the windiest month of the year." — "April" means different things; you need future context to disambiguate.
- Use cases where encoders excel: text classification, feature visualization, named-entity recognition.
  > Source: Copy of Section 4_ Training and Gradient Descent, Pytorch intro.pdf

### Encoder-Decoder Structure
- Older models have an **encoder-decoder** structure.
- The input is encoded into a vector. That vector is fed into a decoder. The decoder predicts the next token autoregressively.
- **Pros:** Encoding can be used for other tasks; don't have to re-predict tokens for the input.
- **Cons:** Training data must be input/output pairs (not just a block of text); generally not as effective once you scale up.
  > Source: Copy of Section 4_ Training and Gradient Descent, Pytorch intro.pdf

### BERT
- **Bidirectional Encoder Representations from Transformers** (2018).
- Got incorporated into Google search — one of the first commercial uses of large language models.
- **Key differences from autoregressive LMs:**
  - Self-attention is **not causal** — it's allowed to refer to future tokens (bidirectional).
  - Trained on two different tasks (not next-token prediction):
    1. **Masked Language Modeling (MLM):** Randomly mask out some tokens and predict those.
    2. **Next-Sentence Prediction (NSP):** Given two sentences, predict whether the second follows the first.
- Cannot easily be used for text generation. Useful for text **understanding**.
  > Source: Copy of Section 4_ Training and Gradient Descent, Pytorch intro.pdf

### BERT Variants
- **RoBERTa:** Trained BERT more carefully and got better results.
- **ELECTRA**
- Many fine-tuned BERT models available on HuggingFace.
  > Source: Copy of Section 4_ Training and Gradient Descent, Pytorch intro.pdf

### Using BERT: Downstream Tasks
- The encoding of the `[CLS]` token should contain global information about the sentence.
- A **classification head** (usually just a matrix multiplication) is placed on top of the `[CLS]` encoding to map to as many output categories as needed.
- Two ways to use pre-trained BERT:
  1. **Freeze** the model and train a tiny model on top of the frozen BERT sentence representations.
  2. **Fine-tune** the whole model on the target task.
- Example: Predict star rating (sentiment) from a Yelp review.
  > Source: Copy of Section 4_ Training and Gradient Descent, Pytorch intro.pdf

### BERT for Retrieval
- The **dot product** can measure similarity between vectors. Normalizing by vector lengths gives **cosine similarity**.
- If BERT vectors represent what a sequence is like, then higher cosine similarity → more similar sequences.
- Simple retriever: Given a query q and documents d1, d2, ..., dn, take the dot product of q with all documents to get relevance scores, then sort by score.
- In practice, retrievers are trained in more complex ways, but ultimately rely on similarity of encodings.
  > Source: Copy of Section 4_ Training and Gradient Descent, Pytorch intro.pdf

## Related Topics
- [language-models.md](language-models.md)
- [neural-networks.md](neural-networks.md)
- [training-deep-dive.md](training-deep-dive.md)
