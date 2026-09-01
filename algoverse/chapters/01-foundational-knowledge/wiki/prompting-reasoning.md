# Prompting and Reasoning

## Definition
**Prompting** is a general term for controlling a language model by the text we feed into it. The prompt (also called a prefix) is the fixed sequence of characters we feed to the model, which the model then completes.
> Source: Copy of Section 1 _ Introduction to AI and Algoverse.pdf, Copy of Section 2_ Language Models, Alignment, Reasoning.pdf

## Key Concepts

### K-Shot Prompting
- **Challenge:** How do we ensure a language model follows a standard format so we can extract an answer?
- **Answer:** Use a prompting strategy.
- **K-shot prompting:** Give the model K question-answer examples in the prompt to help it follow the desired format.
- **8-shot prompting:** Give 8 examples before the actual question.
- **Zero-shot prompting:** Give no previous examples, just the question.
  > Source: Copy of Section 2_ Language Models, Alignment, Reasoning.pdf

### Chain-of-Thought (CoT) Prompting
- **Motivation:** Decomposing tasks into intermediate steps makes them easier.
- **Idea:** Prompt a model to output a full reasoning chain before its final answer.
- **Results:**
  - Performance soars, almost universally.
  - Models become more explainable.
  - Outputs are longer.
- **Zero-shot CoT trick:** Adding "Let's think step by step." to the end of a zero-shot prompt gets some of these benefits.
- A paper found even better performance with "Take a deep breath."
- **Note:** CoT is less important for aligned models, which tend to explain their reasoning regardless of how they're prompted.
  > Source: Copy of Section 2_ Language Models, Alignment, Reasoning.pdf

### Self-Consistency
- **Motivation:** Multiple reasoning paths could take you to the right answer.
- **Idea:** Sample multiple full generations from a model, then aggregate the final answers.
- **Aggregation methods:**
  - Principled: Marginalize out reasoning paths — score each path using the LM and weigh each answer by its aggregate normalized score.
  - In practice: **Majority vote** — it does just as well.
- **Limitations:**
  - Only works for closed-solution problems that can be grouped.
  - Takes much more compute (typically 5–100 reasoning paths = 400% to 9,000% more compute at generation time).
- **Results:** Super reliably improves performance. Used in many papers to get an upper bound for benchmarks.
  > Source: Copy of Section 2_ Language Models, Alignment, Reasoning.pdf

### GSM8K (Example Benchmark)
- Grade School Math — 8,000 questions. A very standard benchmark.
- Nearly solved by GPT-4 + a verifier, but not by other models (at time of writing).
  > Source: Copy of Section 2_ Language Models, Alignment, Reasoning.pdf

## Related Topics
- [language-models.md](language-models.md)
- [alignment.md](alignment.md)
