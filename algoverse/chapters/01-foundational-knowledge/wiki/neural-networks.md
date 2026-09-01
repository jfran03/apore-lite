# Neural Networks

## Definition
Neural networks are complicated functions, like other ML models, with weights (parameters) which are automatically learned to solve a task. They are distinct from other ML models in three ways: automatic feature extraction (rather than manual feature engineering), better scalability in terms of data and model size, and better at modeling complex non-linear relationships.
> Source: Copy of Section 3_ ML Learning Paradigms and Models, Neural Networks.pdf

## Key Concepts

### High-Level Goal
- **Input:** e.g., each pixel value. **Output:** the desired class.
- Each neuron, after training, represents a **feature**, with an **activation** that describes how "present" the feature is.
  - Example: a neuron in layer 3 might represent the horizontal line in a "7."
- As the network progresses deeper, neurons represent more and more complete parts of the desired class.
  > Source: Copy of Section 3_ ML Learning Paradigms and Models, Neural Networks.pdf

### Components of a Neural Network
- **Weights:** Parameters that determine the strength of the connection between pairs of neurons. These are what the model "learns."
- **Biases:** Also model weights (despite the name). One per neuron in the hidden layers. Serves as an additive offset — analogous to the `b` in `y = mx + b`. The biological analogy: neurons have an activation threshold; bias is the negative offset of that threshold.
- **Activation:** How active a neuron is ↔ how present the feature is in the given input.
- **Activation function:** A function applied after the linear combination to introduce **non-linearity**, which is necessary for generalization. Sigmoid is an example. The most popular activation function today is **ReLU** (or its variants), not sigmoid.
- All weights and biases start randomly initialized and are learned through **gradient descent**.
  > Source: Copy of Section 3_ ML Learning Paradigms and Models, Neural Networks.pdf, Copy of Section 4_ Training and Gradient Descent, Pytorch intro.pdf

### Forward Pass (MLP)
- In a vanilla neural network (MLP), each neuron communicates with all neurons in the previous layer.
- **Step 1 — Linear Combination (Pre-Activation):** Each neuron computes a weighted sum of its inputs from the previous layer plus a bias:
  `z_i^(l) = Σ_j w_ij^(l) * a_j^(l-1) + b_i^(l)`
- **Step 2 — Nonlinear Activation:** The pre-activation is passed through a nonlinear activation function σ:
  `a_i^(l) = σ(z_i^(l))`
- **Combined formula:** `a_i^(l) = σ(Σ_j w_ij^(l) * a_j^(l-1) + b_i^(l))`
  > Source: Copy of Section 3_ ML Learning Paradigms and Models, Neural Networks.pdf, Copy of Section 4_ Training and Gradient Descent, Pytorch intro.pdf

### Scaling
- The reason ML has taken off is a specific type of model called a **neural network** (and more specifically, **transformers**).
- At an abstract level, a neural network takes in a list of numbers (a vector) and outputs a list of numbers (another vector).
- The reason NNs are good: they **scale** very well. You can make them very large (adding more weights), and if you feed a lot of data they learn very effectively.
- Large NNs can solve tasks like generating arbitrary images (DALL-E) or segmenting objects in a picture (Segment Anything).
  > Source: Copy of Section 1 _ Introduction to AI and Algoverse.pdf, Copy of Section 3_ ML Learning Paradigms and Models, Neural Networks.pdf

### Transformers
- A Transformer is a type of neural network used for LLMs (and others).
- Transformers ⊂ Neural Networks.
  > Source: Copy of Section 3_ ML Learning Paradigms and Models, Neural Networks.pdf

### Abstraction
- The single most important concept in computer science is **abstraction** — treating certain things as a "black box," intentionally ignoring how something works and focusing on how to use it. Essential for understanding AI systems.
  > Source: Copy of Section 3_ ML Learning Paradigms and Models, Neural Networks.pdf

## Examples
- Given a neural network trained on handwritten digits: if the input is a "6," a neuron representing the horizontal line in a "7" would have low activation (that feature isn't present). If the input is a "5" with a top horizontal line in the same position, that neuron would activate (the feature is present regardless of the final class).
  > Source: Copy of Section 3_ ML Learning Paradigms and Models, Neural Networks.pdf

## Related Topics
- [ml-models-weights-training.md](ml-models-weights-training.md)
- [training-deep-dive.md](training-deep-dive.md)
- [language-models.md](language-models.md)
- [encoder-models.md](encoder-models.md)
