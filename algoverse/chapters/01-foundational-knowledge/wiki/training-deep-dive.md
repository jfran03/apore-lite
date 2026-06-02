# Training Deep Dive

## Definition
Training a ML model = finding the best weights in order to **minimize a loss function**. This is done via gradient descent.
> Source: Copy of Section 4_ Training and Gradient Descent, Pytorch intro.pdf

## Key Concepts

### Loss Functions
Loss functions measure the difference between model predictions and the true labels (performance signal).

- **Mean Squared Error (MSE):** The average of the squares of the errors between predictions and actual values.
  - Formula: `Loss = Σ(ŷ_i - y_i)²`
  - Why square (not absolute value)? Squaring makes all errors positive — overshooting and undershooting are penalized equally. MSE gives high weight to large errors, making it useful when large errors are particularly undesirable. But this can backfire with outliers.
  - Good for regression.
  - **Mean Absolute Error (MAE)** is also an option (absolute value instead of square).

- **Cross-Entropy:** `Loss = Σ(-p_i * log(p̂_i))`
  - Better for classification probabilities. Encourages the model's distribution to match the ground-truth distribution.

- Lower loss = better fit to the data.
  > Source: Copy of Section 4_ Training and Gradient Descent, Pytorch intro.pdf

### Gradient Descent
- **Core idea:** Iteratively move in the direction opposite to the slope (derivative/gradient) at the current point to minimize the loss.
- **Steps:**
  1. Start at a random place (random weight initialization).
  2. Compute the gradient (slope) of the loss at that point.
  3. Update: `x_1 = x_0 - lr * slope * x_0` — move opposite to slope.
- **Why this works:**
  - Positive slope → the direction of increase is right → move left (decrease x).
  - Negative slope → the direction of increase is left → move right (increase x).
- **In multiple dimensions:** The multi-dimensional version of slope is called the **gradient**.
- **Caveat:** Gradient descent finds a **local minimum**, not necessarily a global one.
  > Source: Copy of Section 4_ Training and Gradient Descent, Pytorch intro.pdf

### Foggy Mountain Analogy for Gradient Descent
- You're on a foggy mountain and want to get down. You can only see locally.
- **You** = the algorithm. **Path down** = sequence of weights. **Steepness** = gradient. **Instrument to measure steepness** = differentiation. **Distance traveled before next measurement** = step size (lr × gradient).
  > Source: Copy of Section 4_ Training and Gradient Descent, Pytorch intro.pdf

### Learning Rate
- A scalar that scales how much you move each iteration.
- **Too small:** Never converges.
- **Too large:** Flops back and forth, possibly never converging.
- In practice, try many different values. People often use learning rates that scale with the gradient (e.g., momentum-based variants).
  > Source: Copy of Section 4_ Training and Gradient Descent, Pytorch intro.pdf

### Batch Gradient Descent vs. Stochastic Gradient Descent
- **Batch Gradient Descent:** Make the weight update only after looking at *all* data and averaging.
- **Stochastic Gradient Descent (SGD):** Make the update after looking at only *one* data point.
- **Mini-batch:** In between — e.g., 32 data points per update (most common in practice).
- **Trade-off:** Efficiency vs. accuracy. SGD also sometimes escapes local minima better due to randomness.
  > Source: Copy of Section 4_ Training and Gradient Descent, Pytorch intro.pdf

### Backpropagation
- How gradients are actually computed for neural networks.
- **High-level idea:** Calculate the derivative of the loss with respect to each weight, working backwards through the network, applying the chain rule.
- Very efficient. In PyTorch, called with `loss.backward()`.
- Out of scope in detail, but approachable with a calculus background (recommended: 3Blue1Brown series).
  > Source: Copy of Section 4_ Training and Gradient Descent, Pytorch intro.pdf

### Optimizers
- The algorithm used to update weights is called an **optimizer**.
- Modern optimizers are all variants of gradient descent: Gradient descent w/ momentum, RMSProp, **Adam** (most commonly used in practice).
  > Source: Copy of Section 4_ Training and Gradient Descent, Pytorch intro.pdf

### Hyperparameters
- **Hyperparameters:** Parameters set *prior* to the learning process. Unlike model weights, they cannot be learned directly from training data.
- Examples: learning rate, number of hidden layers, number of clusters in K-Means, depth of a Decision Tree, number of neighbors in KNN.
- **Strategies to tune:**
  - **Manual tuning**
  - **Grid Search:** Try a predefined list.
  - **Random Search:** Sample from a predefined space.
  - **Bayesian Optimization:** Constructs a posterior distribution of functions to find best hyperparameters.
  > Source: Copy of Section 4_ Training and Gradient Descent, Pytorch intro.pdf

### Pretraining
- Grab a large amount of data from the Internet. Do basic filtering to remove toxic/useless content.
- Train the model on this directly.
- The model will learn general, emergent behavior.
  > Source: Copy of Section 4_ Training and Gradient Descent, Pytorch intro.pdf

### Fine-Tuning (Transfer Learning)
- Nowadays, you almost never train a model from scratch.
- Instead, start with a pre-trained model and **fine-tune** it.
- Fine-tuning = take the final weights of an existing model, then train for a few more epochs on a specialized dataset.
- Think of it as a better initialization scheme — start from weights that are already good at general recognition/language.
- This is also called **transfer learning**.
- **Catastrophic forgetting:** If you fine-tune for too long, the model will throw away previous learnings while optimizing for the new task, becoming worse at general language modeling.
- **When to use:** When you have a task that requires a different distribution than general language (e.g., clinical notes with specialized acronyms), and not enough data to train from scratch.
  > Source: Copy of Section 4_ Training and Gradient Descent, Pytorch intro.pdf

### Practical Fine-Tuning Considerations
- Try different learning rates and number of epochs; also different optimizers and batch sizes.
- For optimizer, probably use Adam.
- Monitor your validation loss (use wandb to visualize).
- Use a GPU (T4 or A100).
- Save model weights per epoch in case the runtime dies.
  > Source: Copy of Section 4_ Training and Gradient Descent, Pytorch intro.pdf

## Related Topics
- [ml-models-weights-training.md](ml-models-weights-training.md)
- [neural-networks.md](neural-networks.md)
- [overfitting-generalization.md](overfitting-generalization.md)
- [alignment.md](alignment.md)
