# Data and Features

## Definition
Real-world data is almost always noisy, messy, and not in an optimal structure to directly use for prediction. Feature engineering and data transformation are essential preparation steps.
> Source: Copy of Section 4_ Training and Gradient Descent, Pytorch intro.pdf

## Key Concepts

### Data Matrix Formulation
- An entire dataset is represented mathematically as a **matrix** — rows are data points, columns are features (e.g., pixel values).
- Example: `X[3][4]` is the 4th pixel value for the 3rd image in the dataset.
- All ML libraries store data this way: pandas, numpy, pytorch.
  > Source: Copy of Section 4_ Training and Gradient Descent, Pytorch intro.pdf

### Features
- **Feature:** Any piece of data that helps the model make the prediction.
- Features are either engineered or built into the data.
- For traditional ML, features are manually engineered to increase model performance.
  > Source: Copy of Section 4_ Training and Gradient Descent, Pytorch intro.pdf

### Data Transformations

**Handling Missing Values:**
- **Deleting Rows:** Works well when the number of missing values is small.
- **Imputation:** Replace missing values with statistical measures (mean, median, or mode).

**Scaling:**
- **Min-max normalization:** Rescales features to a fixed range, usually 0–1.
- **Standardization (Z-score normalization):** Rescales to have μ=0 and σ=1 (standard normal distribution).
- **Log Transform:** Helps balance a skewed distribution by taking the log.

**Encoding Categorical Variables:**
- **One-hot Encoding:** Each category value is converted into a new column, assigned 1 or 0.
- **Label Encoding:** Each category assigned a unique integer. Used for "ordinal" variables.

**Removing Outliers:**
- Outliers can skew model learning. Techniques: capping, flooring, or using algorithms robust to outliers.
  > Source: Copy of Section 4_ Training and Gradient Descent, Pytorch intro.pdf

### Exploratory Data Analysis (EDA)
- **Univariate analysis:** Analyze one feature at a time. Use histograms or box plots; measure central tendency and dispersion.
- **Bivariate/Multivariate analysis:** Analyze relationships between features. Use correlation matrices, scatter plots, cross-tabulation.
- Libraries: **pandas**, **Matplotlib** (static/animated/interactive visualizations), **Seaborn** (high-level statistical graphics), **Plotly** (interactive).
  > Source: Copy of Section 4_ Training and Gradient Descent, Pytorch intro.pdf

### Feature Engineering (Traditional ML)
- Adding new columns to the data. Allows incorporating domain knowledge and hidden insights to help the model understand patterns.
- Called "an art, not a science."
- Techniques:
  - **Interaction features:** New features representing the interaction between two existing features (e.g., day of week × time of day).
  - **Temporal/Geospatial features:** Encode domain knowledge based on time and location (e.g., seasonality, YoY/MoM, rural vs. urban).
  > Source: Copy of Section 4_ Training and Gradient Descent, Pytorch intro.pdf

### Feature Extraction and Selection
- **Purpose:** Reduce the number of features.
- **Why:**
  - Less redundant data → less opportunity for noise-driven decisions.
  - Improved accuracy (less misleading data).
  - Reduced training time (fewer features → less complexity).
- **How:**
  - **PCA:** A linear algebraic technique to reduce dimensionality.
  - **Regularization:** Adding a penalization to model complexity.
  > Source: Copy of Section 4_ Training and Gradient Descent, Pytorch intro.pdf

### ML Lifecycle
The full ML lifecycle: (1) Frame the problem → (2) Gather data → (3) Data preprocessing → (4) EDA → (5) Feature engineering and selection → (6) Model training, evaluation, selection → (7) Model deployment → (8) Testing → (9) Optimize (repeat).
> Source: Copy of Section 4_ Training and Gradient Descent, Pytorch intro.pdf

## Related Topics
- [ml-models-weights-training.md](ml-models-weights-training.md)
- [training-deep-dive.md](training-deep-dive.md)
