# Alignment

## Definition
**Alignment** refers to the process of taking a base (pretrained) language model and making it helpful, harmless, and honest — training it to behave in ways that users and operators want.
> Source: Copy of Section 2_ Language Models, Alignment, Reasoning.pdf

## Key Concepts

### Base (Unaligned) Models vs. Instruct (Aligned) Models
- **Base models:** Trained from scratch with an autoregressive objective on a large corpus of data (called **pretraining**). They learn to reproduce the distribution of data. No notion of helpfulness, harmlessness, etc.
- **Instruct (aligned) models:** Have 1 or 2 "alignment" steps after pretraining.
  > Source: Copy of Section 2_ Language Models, Alignment, Reasoning.pdf

### RLHF — Reinforcement Learning from Human Feedback
- One major form of alignment training.
- **How it works:**
  1. Humans rate or rank model outputs to train a **reward model**.
  2. The language model is then trained via reinforcement learning to maximize this reward model.
- RLHF is not the only form of alignment training.
  > Source: Copy of Section 2_ Language Models, Alignment, Reasoning.pdf

### SFT — Supervised Fine-Tuning
- A labeler demonstrates desired output behavior for a given prompt.
- This data is used to fine-tune the base model with supervised learning.
- SFT typically comes before RLHF in the alignment pipeline: **Base model → SFT → RLHF**.
  > Source: Copy of Section 2_ Language Models, Alignment, Reasoning.pdf

### Other Alignment Approaches
- **LIMA:** Shows that you can train on a small dataset of carefully chosen examples and get similar results to full RLHF.
- **RLAIF (Constitutional AI, Anthropic):** Uses AI feedback instead of human feedback.
- **DPO (Direct Preference Optimization):** A recent seminal work in alignment, an alternative to PPO (the RL algorithm used in RLHF).
  > Source: Copy of Section 2_ Language Models, Alignment, Reasoning.pdf

### Superficial Alignment Hypothesis
- Most researchers subscribe to this hypothesis.
- All of the "heavy lifting" learning is done in **pretraining**.
- The alignment phase just teaches the model **how to apply** what it has already learned.
  > Source: Copy of Section 2_ Language Models, Alignment, Reasoning.pdf

### How Alignment Affects Behavior
- An aligned model's behavior depends on its alignment data.
- For example, it might be aligned to follow certain templates and thus answer questions better zero-shot than few-shot.
- Most customer-facing models are aligned (GPT-*, Bard/Gemini, Meta Assistant).
  > Source: Copy of Section 2_ Language Models, Alignment, Reasoning.pdf

### RLVR — Reasoning Models
- Models like o1 and DeepSeek use **RLVR (Reinforcement Learning with Verifiable Rewards)**.
- The reward function is verifiable: `r = γ` if correct, `0` otherwise.
- Loop: sample a mini-batch of prompts → generate completions → compute reward → use rewards to compute a policy update.
- This is a general framework for **online RL** and related to RLHF in structure but uses verifiable rewards instead of human ratings.
  > Source: Copy of Section 2_ Language Models, Alignment, Reasoning.pdf

## Related Topics
- [language-models.md](language-models.md)
- [prompting-reasoning.md](prompting-reasoning.md)
- [training-deep-dive.md](training-deep-dive.md)
