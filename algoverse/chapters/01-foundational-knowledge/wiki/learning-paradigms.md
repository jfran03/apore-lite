# ML Learning Paradigms

## Definition
There are different ways to structure the process of how we learn from data. Three main paradigms: Supervised Learning, Unsupervised Learning, and Reinforcement Learning.
> Source: Copy of Section 3_ ML Learning Paradigms and Models, Neural Networks.pdf

## Key Concepts

### Supervised Learning
- **Goal:** Predict some quantity **y** from **x**, where x are the features and y is the label.
- If y is a discrete category → **classification** (e.g., predict city from house info).
- If y is a continuous value → **regression** (e.g., predict house price).
- This is the most common paradigm, and fundamentally the easiest problem.
  > Source: Copy of Section 3_ ML Learning Paradigms and Models, Neural Networks.pdf

### Unsupervised Learning
- **Goal:** Given unlabeled data, learn something interesting.
- **Clustering:** Group similar items into classes based on similarity. K-means is a typical algorithm. Generally a hard problem.
- **Dimensionality Reduction:** Project down from a high-dimensional space to a low-dimensional space — learns to throw away redundant data. Two common algorithms: PCA, t-SNE.
- **Manifold Hypothesis:** High-dimensional data "in the wild" usually lies on low-dimensional manifolds. Visualize as a wavy blanket in 3-D space; if we can "flatten it out" we can visualize the true distribution.
  > Source: Copy of Section 3_ ML Learning Paradigms and Models, Neural Networks.pdf

### Reinforcement Learning
- **Goal:** Learn a policy to maximize reward from an environment. Data can be collected by the agent.
- More complicated and general than other paradigms. Training is much less stable.
- Reward function can be anything; doesn't need to be differentiable.
- Used for: robotics, games (e.g., AlphaGo), optimization problems (e.g., traffic control, trading). Recently used in NLP on top of standard methods (e.g., RLHF).
  > Source: Copy of Section 3_ ML Learning Paradigms and Models, Neural Networks.pdf

### Self-Supervised Learning
- **Goal:** Learn something interesting from unlabeled data.
- **Method:** Learn to predict one part of the input from another — turns unlabeled data into labeled data (kind of).
- **Example:** Masked language modeling.
  > Source: Copy of Section 4_ Training and Gradient Descent, Pytorch intro.pdf

## Common Misconceptions
- (None explicitly stated in the sources.)

## Related Topics
- [ai-ml-overview.md](ai-ml-overview.md)
- [alignment.md](alignment.md)
- [language-models.md](language-models.md)
