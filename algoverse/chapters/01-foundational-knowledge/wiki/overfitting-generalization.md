# Overfitting, Underfitting, and Generalization

## Definition
**Overfitting:** When a model learns the training data too well, it also learns the noise and outliers. It performs well on training data but poorly on unseen data.
> Source: Copy of Section 1 _ Introduction to AI and Algoverse.pdf

**Underfitting:** When a model cannot capture the underlying pattern of the data, it performs poorly on both the training data and unseen data.
> Source: Copy of Section 1 _ Introduction to AI and Algoverse.pdf

## Key Concepts

- **Goal of training:** Fit the underlying data, but not the noise. Generalization = good performance on unseen data.
  > Source: Copy of Section 1 _ Introduction to AI and Algoverse.pdf

- **Biggest tell of overfitting:** Low train loss, but high validation loss.
  > Source: Copy of Section 1 _ Introduction to AI and Algoverse.pdf

- **This doesn't tell the full story for modern deep neural networks** — see "Deep Double Descent."
  > Source: Copy of Section 1 _ Introduction to AI and Algoverse.pdf

### Train/Validation/Test Split
- **Why:** To prevent overfitting and ensure our model generalizes to new, unseen data.
- **Training Set:** Used to train the model (all the learning happens here). Typically 60–80% of data.
- **Validation Set:** Used to check how well the model is performing on unseen data *during training*. Unbiased gauge since the model isn't trained on it. Also used to tune hyperparameters. Typically 10–20% of data. Sometimes called "test" or "hold-out" (confusingly).
- **Test Set:** Final evaluation of the model. Should only be used once. Usually 10–20%.
- **Why a separate test set?** You can overfit on the validation set if you optimize on it too hard. Any time you optimize weights over a dataset you risk learning specific patterns and noise in it.
  > Source: Copy of Section 1 _ Introduction to AI and Algoverse.pdf, Copy of Section 3_ ML Learning Paradigms and Models, Neural Networks.pdf

### Cross-Validation
- Optimizing on a fixed validation set might overfit on that validation set.
- Solution: Divide data into partitions (folds) and rotate which partition is used for training vs. validation.
  > Source: Copy of Section 4_ Training and Gradient Descent, Pytorch intro.pdf

## Related Topics
- [ml-models-weights-training.md](ml-models-weights-training.md)
- [training-deep-dive.md](training-deep-dive.md)
