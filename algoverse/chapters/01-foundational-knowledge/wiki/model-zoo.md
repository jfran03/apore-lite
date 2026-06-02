# Model Zoo (Models by Modality)

## Definition
The model you choose first depends on the type of data (data modality), then other trade-offs.
> Source: Copy of Section 3_ ML Learning Paradigms and Models, Neural Networks.pdf

## Key Concepts

### Text Data
- **LLMs (e.g., GPT):** For text understanding and generation.
- **BERT-based models:** For understanding. Often used for classification (e.g., sentiment analysis).
  > Source: Copy of Section 3_ ML Learning Paradigms and Models, Neural Networks.pdf

### Visual Data
- **Image classification:** Convolutional Neural Networks (e.g., ResNet, VGG).
- **Object detection:** YOLO.
- **Segmentation:** SAM (Segment Anything Model), U-nets.
- **Generation:** Diffusion models, GANs.
- **VLM:** Vision-Language Models.
  > Source: Copy of Section 3_ ML Learning Paradigms and Models, Neural Networks.pdf

### Multimodal
- **Multimodal LLMs** (e.g., GPT-4o, LLaVA).
- **CLIP.**
  > Source: Copy of Section 3_ ML Learning Paradigms and Models, Neural Networks.pdf

### Tabular Data
- **Neural Networks:** MLPs, LSTMs.
- **Traditional ML models:** Linear/Logistic Regression, Decision Trees, Random Forests, Boosting Models.
  > Source: Copy of Section 3_ ML Learning Paradigms and Models, Neural Networks.pdf

### Key Distinction
- All the above model types are neural networks *except* the last bullet in tabular data (Linear/Logistic Regression, Decision Trees, Random Forests, Boosting Models).
- Text and visual data are **high-dimensional** (thousands of words, millions of pixels) and less structured — they require advanced neural networks. Tabular data is lower-dimensional and more structured, so traditional ML models can work well.
  > Source: Copy of Section 3_ ML Learning Paradigms and Models, Neural Networks.pdf

### ML Libraries
- **Language models:** HuggingFace Datasets and Transformers, APIs (GPT, Gemini, Claude).
- **Deep learning:** PyTorch (low-level, more customization, harder to use), Fastai (high-level, easier). Don't use: TensorFlow, Keras.
- **Machine learning:** pandas/numpy (data processing), scikit-learn (traditional ML), Matplotlib/plotly/seaborn (visualizations).
  > Source: Copy of Section 4_ Training and Gradient Descent, Pytorch intro.pdf

## Related Topics
- [neural-networks.md](neural-networks.md)
- [language-models.md](language-models.md)
- [encoder-models.md](encoder-models.md)
