# ML Models, Weights, and Training

## Definition
An ML model is composed of a lot of numbers called **weights/parameters**, and rules to do computations with those numbers. All of CS is ultimately just data and algorithms applied to that data.
> Source: Copy of Section 1 _ Introduction to AI and Algoverse.pdf

## Key Concepts

- **Weights:** Adjustable knobs that dictate the model's prediction on a given input. They parameterize the model's internal representations of its data. You can think of them as coefficients (but in a very high-dimensional space).
  > Source: Copy of Section 1 _ Introduction to AI and Algoverse.pdf

- **Scale of weights:**
  - Traditional ML models may have just a handful.
  - Deep neural nets may have thousands, millions, even billions.
  - GPT-3.5 has 175 billion parameters, taking 350 GB of storage.
  > Source: Copy of Section 1 _ Introduction to AI and Algoverse.pdf

- **ML models learn internal representations** of their data, which they use to predict things.
  > Source: Copy of Section 1 _ Introduction to AI and Algoverse.pdf

- **ML is prediction:** Broadly speaking, ML is used to solve prediction problems. Many real-world problems can be framed as prediction problems.
  > Source: Copy of Section 1 _ Introduction to AI and Algoverse.pdf

- **Types of prediction problems:**
  - **Classification:** Used when the output variable is categorical (e.g., "spam" or "not spam").
  - **Regression:** Used when the output variable is a continuous value (e.g., salary, price).
  > Source: Copy of Section 1 _ Introduction to AI and Algoverse.pdf

- **Training as fitting a mathematical function:** Inputs are transformed into numbers; the output is also a number. The model can be graphed as a function (the "red line"). Weights define that function. The goal is generalization — fit the underlying data but not the noise. Prevent overfitting.
  > Source: Copy of Section 1 _ Introduction to AI and Algoverse.pdf

- **Training:** Iteratively update the model weights by comparing the model's predictions with the actual answer for all the data in the training dataset.
  > Source: Copy of Section 1 _ Introduction to AI and Algoverse.pdf

- **Inference:** After training, use the final set of weights to make predictions. Similar to a regular algorithm, a model is just a function that takes an input and returns an output.
  > Source: Copy of Section 1 _ Introduction to AI and Algoverse.pdf

## Related Topics
- [ai-ml-overview.md](ai-ml-overview.md)
- [overfitting-generalization.md](overfitting-generalization.md)
- [training-deep-dive.md](training-deep-dive.md)
- [neural-networks.md](neural-networks.md)
