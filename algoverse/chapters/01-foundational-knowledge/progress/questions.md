# Question Bank

> Generated from `wiki/` during the compile step. Extended on wrong-answer targeting and graduation.
> Do not edit manually — all changes are made by Claude during compile and session flows.

---

<!-- Question format (do not delete this comment):

## Q{NNN}
**Status:** active | retired
**Type:** mcq | short-answer | conceptual | true-false
**Difficulty:** introductory | intermediate | advanced
**Topic:** {topic-slug}
**Focus Area:** {specific concept or sub-topic}
**Question:** {question text}
**Answer:** {model answer — sourced from wiki only}

-->

## Q001
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** ai-ml-overview
**Focus Area:** AI/ML/Deep Learning hierarchy
**Question:** What is the hierarchical relationship between AI, Machine Learning, and Deep Learning?
**Answer:** Deep Learning ⊂ Machine Learning ⊂ Artificial Intelligence. AI is any technique enabling computers to mimic human intelligence. ML is a subset of AI — statistical techniques that enable computers to improve with experience. Deep Learning is a subset of ML that makes computations using neural networks. (Source: ai-ml-overview.md)

## Q002
**Status:** active
**Type:** conceptual
**Difficulty:** introductory
**Topic:** ai-ml-overview
**Focus Area:** Why ML instead of traditional programming
**Question:** Why do we use Machine Learning instead of traditional programming for tasks like recognizing dogs vs. cats in photos?
**Answer:** Traditional programming requires telling the computer the exact steps, which is infeasible for complex perceptual tasks (how would you write rules for "what makes a dog?"). ML instead shows the computer examples (labeled data) and uses an algorithm to learn the pattern from that data — a process called training. (Source: ai-ml-overview.md)

## Q003
**Status:** active
**Type:** mcq
**Difficulty:** introductory
**Topic:** ml-models-weights-training
**Focus Area:** Prediction problem types
**Question:** Which of the following is a classification problem? (A) Predicting a house's sale price. (B) Predicting whether an email is spam or not spam. (C) Predicting tomorrow's temperature in Celsius. (D) Predicting the number of units a product will sell.
**Answer:** (B). Classification is used when the output variable is categorical (e.g., "spam" or "not spam"). All other options have continuous outputs and are regression problems. (Source: ml-models-weights-training.md)

## Q004
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** ml-models-weights-training
**Focus Area:** Weights/parameters
**Question:** What are weights (parameters) in a machine learning model, and what role do they play?
**Answer:** Weights are adjustable numbers (knobs) that dictate the model's prediction on a given input. They parameterize the model's internal representations of its data. You can think of them as coefficients in a very high-dimensional space. During training they are updated; at inference the final weights are used to make predictions. (Source: ml-models-weights-training.md)

## Q005
**Status:** active
**Type:** conceptual
**Difficulty:** introductory
**Topic:** ml-models-weights-training
**Focus Area:** Training vs. Inference
**Question:** What is the difference between training and inference in machine learning?
**Answer:** Training is the process of iteratively updating the model's weights by comparing its predictions with the actual answers across the training dataset. Inference is using the final trained weights to make predictions on new inputs — the model acts as a function that takes an input and returns an output. (Source: ml-models-weights-training.md)

## Q006
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** overfitting-generalization
**Focus Area:** Overfitting definition and diagnosis
**Question:** What is overfitting, and what is the most reliable signal that a model is overfitting?
**Answer:** Overfitting is when a model learns the training data too well — including its noise and outliers — so it performs well on training data but poorly on unseen data. The biggest tell is low training loss but high validation loss. (Source: overfitting-generalization.md)

## Q007
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** overfitting-generalization
**Focus Area:** Train/Validation/Test split rationale
**Question:** Why do we need a separate test set if we already have a validation set?
**Answer:** Because you can overfit on the validation set if you optimize on it too hard. Any time you optimize weights over a dataset, you risk learning its specific patterns and noise. The test set is a held-out final evaluation that is used only once — it provides an unbiased estimate of generalization performance after all model selection and hyperparameter tuning is done. (Source: overfitting-generalization.md)

## Q008
**Status:** active
**Type:** mcq
**Difficulty:** introductory
**Topic:** overfitting-generalization
**Focus Area:** Split proportions and roles
**Question:** What is the primary purpose of the validation set during training? (A) To train the model's weights. (B) To provide a final unbiased evaluation after training. (C) To check model performance on unseen data during training and tune hyperparameters. (D) To increase the size of the training set.
**Answer:** (C). The validation set is an unbiased gauge of how well the model is doing during training since it's not being trained on. It is also used to tune hyperparameters. (Source: overfitting-generalization.md)

## Q009
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** learning-paradigms
**Focus Area:** Supervised vs. Unsupervised vs. RL
**Question:** Describe the key difference in the data structure required by supervised learning vs. unsupervised learning.
**Answer:** Supervised learning requires labeled data — each data point x has a corresponding ground-truth label y (the target to predict). Unsupervised learning only has the features x, with no labels — the goal is to discover interesting structure (like clusters or lower-dimensional representations) without any ground-truth supervision. (Source: learning-paradigms.md)

## Q010
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** learning-paradigms
**Focus Area:** Reinforcement Learning
**Question:** What is the goal of Reinforcement Learning and how does it differ from supervised learning in terms of data?
**Answer:** The goal of RL is to learn a policy that maximizes reward from an environment. Unlike supervised learning where a fixed labeled dataset is provided upfront, in RL the agent itself can collect data by interacting with the environment. RL is more general but also more complicated and less stable to train. (Source: learning-paradigms.md)

## Q011
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** learning-paradigms
**Focus Area:** Self-supervised learning
**Question:** What is self-supervised learning, and how does it turn unlabeled data into a supervised signal?
**Answer:** Self-supervised learning aims to learn interesting representations from unlabeled data by having the model predict one part of the input from another. For example, in masked language modeling, tokens are randomly masked and the model must predict them. This creates a supervised-like signal (the masked tokens become the labels) without any human annotation. (Source: learning-paradigms.md)

## Q012
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** neural-networks
**Focus Area:** Activation functions and non-linearity
**Question:** Why do neural networks need activation functions? What would happen without them?
**Answer:** Activation functions introduce non-linearity between layers. Without them, stacking multiple linear layers is mathematically equivalent to a single linear transformation — no matter how deep the network, it could only learn linear functions. Non-linear activation functions allow neural networks to model complex, non-linear relationships in the data. The most popular today is ReLU (or its variants). (Source: neural-networks.md)

## Q013
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** neural-networks
**Focus Area:** Weights vs. biases
**Question:** What is the role of a bias term in a neural network neuron, and why is it needed?
**Answer:** A bias is an additive offset (like the `b` in `y = mx + b`) that helps with generalization. The biological analogy: neurons have an activation threshold; the bias represents that threshold (as a negative offset). Without biases, a neuron can only produce outputs proportional to its inputs, limiting what functions the network can represent. All weights and biases are learned through gradient descent. (Source: neural-networks.md)

## Q014
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** neural-networks
**Focus Area:** What neurons learn / feature hierarchies
**Question:** Conceptually, what do neurons at different layers of a trained neural network represent, and how does this change with depth?
**Answer:** Each trained neuron represents a feature, with an activation indicating how "present" that feature is in the input. In early layers, neurons represent simple, low-level features (e.g., edges or lines). As the network progresses deeper, neurons represent increasingly complete, high-level parts of the class being predicted (e.g., from horizontal lines → partial shapes → full digit). (Source: neural-networks.md)

## Q015
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** neural-networks
**Focus Area:** Scaling / why NNs work
**Question:** Why have neural networks (and specifically transformers) become the dominant approach in modern ML?
**Answer:** Neural networks scale very well. You can make them very large by adding more weights, and if you feed a lot of data, they learn very effectively. Large neural networks can solve tasks that simpler models cannot — like generating arbitrary images (DALL-E) or segmenting objects in pictures (Segment Anything). Transformers are a specific type of NN that has proven especially effective and scalable. (Source: neural-networks.md)

## Q016
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** language-models
**Focus Area:** Autoregressive LM core idea
**Question:** What does an autoregressive language model do, and how does it generate a full sequence?
**Answer:** An autoregressive LM takes a sequence of input tokens and produces a probability distribution over the next token in the sequence. To generate a full sequence: first sample a token, then feed that token back in and sample the next one, and so on — autoregressively building up the full sequence. This is valid because of the probability chain rule (a consequence of Bayes' rule). (Source: language-models.md)

## Q017
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** language-models
**Focus Area:** Tokenization
**Question:** What is a tokenizer and what is "vocabulary size"? Why can't we just use individual characters as tokens?
**Answer:** A tokenizer maps text to numbers by finding commonly-occurring sequences of characters and assigning each a unique ID. Vocabulary size (V) is the number of distinct tokens the tokenizer recognizes (typically 30k–60k). Using individual characters would create very long sequences and make it hard for the model to learn meaningful patterns. Using subword tokens (via BPE) is a balance — common words get one token, rare ones are split. (Source: language-models.md)

## Q018
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** language-models
**Focus Area:** Embeddings vs. one-hot encoding
**Question:** Why do we use learned embeddings instead of simply passing one-hot encoded tokens directly into the LM?
**Answer:** A one-hot encoding of a token with vocabulary size V is a V-dimensional sparse vector (all zeros except one 1). This is too high-dimensional and contains no semantic information — "cat" and "kitten" would be totally unrelated. Embeddings map each token to a lower-dimensional dense vector (often ~1k–3k dimensions) learned during training, so that similar tokens end up with similar vectors. This enables the model to generalize across related concepts. (Source: language-models.md)

## Q019
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** language-models
**Focus Area:** Temperature in softmax
**Question:** What is temperature in the context of language model generation, and what happens at high vs. low temperature?
**Answer:** Temperature (τ) is a scalar by which logits are divided before softmax. High temperature scales logits down → the probability distribution becomes flatter (more uniform) → more random/creative outputs. Low temperature scales logits up → the maximum logit dominates → the distribution becomes very peaked → more deterministic, repetitive outputs. Temperature = 1 is standard softmax. (Source: language-models.md)

## Q020
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** language-models
**Focus Area:** Greedy decoding vs. sampling
**Question:** What is the difference between greedy decoding and sampling in language model generation?
**Answer:** Greedy decoding always picks the highest-probability (argmax) token at each step — deterministic and fast but can miss better sequences. Sampling instead draws a token from the probability distribution at each step — stochastic and introduces diversity. Temperature affects sampling (high T → more random; low T → near-greedy). (Source: language-models.md)

## Q021
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** language-models
**Focus Area:** Emergent behavior
**Question:** How does emergent behavior arise in large language models trained on next-token prediction?
**Answer:** The model is trained only on the objective of predicting the next token. If the dataset is large and the model is large enough, the easiest strategy to minimize prediction loss is to internalize the underlying patterns in the data — including skills like math, reasoning, or code. For example, if enough math problems appear in training, the model learns math because that helps predict the next token in math contexts. This is called emergent behavior. (Source: language-models.md)

## Q022
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** language-models
**Focus Area:** Surrogate objective / training LMs
**Question:** What is the surrogate objective used to train autoregressive language models, and why is it a "surrogate"?
**Answer:** The model is trained to maximize the probability it assigns to the actual next token in the training corpus. This uses a one-hot encoding of the true next token as the "target distribution." It's a surrogate because we don't have access to the true distribution over all possible next tokens — we only observe one sample from it. Over a large dataset, the model learns the general pattern. A side effect is miscalibration: the model is encouraged to be overconfident in the next token. (Source: language-models.md)

## Q023
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** alignment
**Focus Area:** Base vs. instruct model
**Question:** What is the difference between a base model and an instruct (aligned) model?
**Answer:** A base model is pretrained from scratch on a large corpus with an autoregressive objective — it learns to reproduce the distribution of the training data but has no notion of helpfulness or harmlessness. An instruct model has additional alignment steps after pretraining (typically SFT + RLHF) that teach it to follow instructions, be helpful, and avoid harmful outputs. (Source: alignment.md)

## Q024
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** alignment
**Focus Area:** RLHF mechanism
**Question:** Describe the two steps of RLHF and what each step achieves.
**Answer:** Step 1 (SFT — Supervised Fine-Tuning): A labeler demonstrates desired output behavior for a given prompt; this data fine-tunes the base model to start behaving helpfully. Step 2 (RLHF): Humans rate or rank model outputs; these ratings train a reward model. The language model is then trained via RL to maximize the reward model's scores. Together, SFT teaches the model the format/style, and RLHF aligns it with human preferences. (Source: alignment.md)

## Q025
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** alignment
**Focus Area:** Superficial alignment hypothesis
**Question:** What does the superficial alignment hypothesis claim, and what are its implications for alignment research?
**Answer:** The hypothesis claims that all the "heavy lifting" learning happens during pretraining — the model already develops its capabilities there. The alignment phase (SFT + RLHF) just teaches the model *how to apply* what it has already learned (formatting, helpfulness style), not new capabilities. Implication: alignment is mostly a style adjustment on top of a capable pretrained model, which is why small datasets (like LIMA) can get similar results to full RLHF. (Source: alignment.md)

## Q026
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** alignment
**Focus Area:** RLVR for reasoning models
**Question:** How do reasoning models like o1 and DeepSeek differ from standard RLHF in their training approach?
**Answer:** Reasoning models use RLVR (Reinforcement Learning with Verifiable Rewards) instead of human ratings. The reward is verifiable: the model gets a positive reward only if its answer is correct (r = γ), and 0 otherwise. The training loop: sample prompts → generate completions → compute verifiable reward → update the policy. This avoids the need for human raters, but requires tasks with objectively correct answers. (Source: alignment.md)

## Q027
**Status:** active
**Type:** conceptual
**Difficulty:** introductory
**Topic:** prompting-reasoning
**Focus Area:** K-shot prompting
**Question:** What is k-shot prompting and why is it useful?
**Answer:** K-shot prompting means providing the model with K input-output examples in the prompt before the actual question. It's useful because it helps the model understand the expected format and reasoning style for the task — especially for base (unaligned) models that haven't been fine-tuned to follow specific instructions. Zero-shot gives no examples; k-shot (e.g., 8-shot) gives k examples. (Source: prompting-reasoning.md)

## Q028
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** prompting-reasoning
**Focus Area:** Chain-of-Thought prompting
**Question:** What is Chain-of-Thought prompting and why does it improve performance on reasoning tasks?
**Answer:** CoT prompting asks the model to output a full reasoning chain before its final answer — decomposing the task into intermediate steps. It improves performance because reasoning tasks are easier when broken into smaller subproblems. It also makes models more explainable. You can trigger zero-shot CoT by appending "Let's think step by step." to the prompt. (Source: prompting-reasoning.md)

## Q029
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** prompting-reasoning
**Focus Area:** Self-consistency
**Question:** How does self-consistency work, and what is its key limitation?
**Answer:** Self-consistency samples multiple full reasoning chains from the model independently, then aggregates the final answers (in practice via majority vote). The intuition is that multiple different reasoning paths might all reach the correct answer. Key limitation: it only works for closed-form problems where answers can be compared and grouped. It also requires 5–100× more compute at generation time. (Source: prompting-reasoning.md)

## Q030
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** training-deep-dive
**Focus Area:** Loss functions
**Question:** What is the purpose of a loss function in machine learning, and what are two common examples?
**Answer:** A loss function measures the difference between the model's predictions and the true labels — it quantifies how wrong the model is. The goal of training is to minimize it. Two common examples: (1) Mean Squared Error (MSE) — average of squared differences, good for regression; (2) Cross-entropy — sum of -p_i * log(p̂_i), better for classification. (Source: training-deep-dive.md)

## Q031
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** training-deep-dive
**Focus Area:** MSE — why square errors
**Question:** Why does Mean Squared Error square the errors rather than use absolute values?
**Answer:** Squaring makes all errors positive (so overshooting and undershooting are penalized equally) and gives higher weight to large errors (so MSE is useful when large errors are particularly undesirable). Mean Absolute Error (MAE) is also valid — absolute value — but MSE's squaring penalizes outlier predictions more heavily. (Source: training-deep-dive.md)

## Q032
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** training-deep-dive
**Focus Area:** Gradient descent intuition
**Question:** Explain gradient descent in plain terms. Why does moving opposite to the gradient minimize the loss?
**Answer:** Gradient descent works by computing the slope (gradient) of the loss function at the current weight position and then moving a small step in the *opposite* direction of that slope. If the slope is positive, increasing the parameter increases loss — so we decrease it. If the slope is negative, decreasing it would increase loss — so we increase it. By repeatedly taking steps opposite the gradient, we iteratively move toward a minimum of the loss. (Source: training-deep-dive.md)

## Q033
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** training-deep-dive
**Focus Area:** Learning rate effects
**Question:** What happens when the learning rate is too small or too large during training?
**Answer:** Too small: the model converges very slowly or effectively never converges in a reasonable time. Too large: the weight updates overshoot — the model "flops" back and forth across the minimum, potentially never converging and oscillating wildly. A well-chosen learning rate is crucial. In practice, people try many values, and modern optimizers (like Adam) adapt the effective learning rate per parameter. (Source: training-deep-dive.md)

## Q034
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** training-deep-dive
**Focus Area:** Batch vs. SGD trade-offs
**Question:** What is the difference between batch gradient descent, stochastic gradient descent, and mini-batch? What is the main trade-off?
**Answer:** Batch GD: compute gradient over the full dataset before each update — accurate gradient, slow per step. SGD: update after each single data point — fast per step, noisy gradient. Mini-batch: in between (e.g., 32 data points) — most common in practice. Main trade-off: efficiency vs. accuracy of the gradient estimate. SGD's noise can also help escape local minima. (Source: training-deep-dive.md)

## Q035
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** training-deep-dive
**Focus Area:** Fine-tuning vs. training from scratch
**Question:** When and why would you fine-tune a pretrained model rather than train from scratch?
**Answer:** Fine-tune when: (1) you have a specialized task/distribution (e.g., clinical notes with specific jargon) that differs from general data, AND (2) you don't have enough data to train from scratch (large models would just memorize it; small ones aren't powerful enough). Fine-tuning reuses the pretrained weights as a strong initialization — the model already knows language, you just adjust it for the target distribution. Training from scratch requires massive data and compute. (Source: training-deep-dive.md)

## Q036
**Status:** active
**Type:** short-answer
**Difficulty:** intermediate
**Topic:** training-deep-dive
**Focus Area:** Catastrophic forgetting
**Question:** What is catastrophic forgetting in the context of fine-tuning?
**Answer:** Catastrophic forgetting is when a model loses its previously learned general capabilities while being optimized for a new, specific task. If you fine-tune for too long, the model overwrites prior knowledge to minimize the new task's loss, making it worse at general language modeling. This is why fine-tuning is done for only a few epochs on the target dataset. (Source: training-deep-dive.md)

## Q037
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** training-deep-dive
**Focus Area:** Hyperparameters
**Question:** What are hyperparameters, and how do they differ from model weights?
**Answer:** Hyperparameters are parameters set *before* training begins (e.g., learning rate, number of layers, batch size). They cannot be learned directly from the training data — they must be set by the practitioner. Model weights, by contrast, are learned automatically during training via gradient descent. Hyperparameters control the training process and model architecture; weights are what the model "knows." (Source: training-deep-dive.md)

## Q038
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** data-features
**Focus Area:** Why feature selection / why scale data
**Question:** Why might you scale (normalize/standardize) features before training an ML model?
**Answer:** If features have very different scales (e.g., one feature ranges 0–1 and another 0–1,000,000), gradient descent may take very uneven steps — moving quickly in the direction of large-valued features and slowly in the direction of small-valued ones. Normalizing (min-max to 0–1) or standardizing (z-score to μ=0, σ=1) puts all features on a comparable scale, making optimization more stable and often faster. (Source: data-features.md)

## Q039
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** data-features
**Focus Area:** One-hot encoding of categories
**Question:** Why do we one-hot encode categorical variables rather than simply assigning integer labels (e.g., cat=1, dog=2, bird=3)?
**Answer:** Assigning integers implies an ordering (dog > cat) and magnitude (bird is 3× cat) that doesn't exist in the data. A model may incorrectly learn that "bird" is numerically closer to "dog" than to "cat." One-hot encoding gives each category its own binary dimension, making all categories equidistant — the model can't infer false ordinal relationships. (Exception: label encoding is valid for truly ordinal variables.) (Source: data-features.md)

## Q040
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** model-zoo
**Focus Area:** Neural networks vs. traditional ML for different data types
**Question:** Why are neural networks typically preferred over traditional ML models (like linear regression or decision trees) for text and image data, but not necessarily for tabular data?
**Answer:** Text and image data are high-dimensional (millions of pixels, thousands of words) and highly unstructured — traditional ML requires manual feature engineering to extract useful representations, which doesn't scale. Neural networks do **automatic feature extraction**, handling raw inputs and learning hierarchical representations. Tabular data is already low-dimensional and structured, so traditional models (which are simpler, faster, and more interpretable) often perform comparably or better. (Source: model-zoo.md)

## Q041
**Status:** active
**Type:** short-answer
**Difficulty:** introductory
**Topic:** encoder-models
**Focus Area:** BERT vs. autoregressive LMs
**Question:** What is the key architectural difference between BERT and autoregressive language models like GPT, and what does this enable?
**Answer:** BERT uses **bidirectional** self-attention — it can look at tokens both before and after the current token. GPT-style autoregressive models are **causal** — they can only look at previous tokens. Bidirectionality allows BERT to build richer contextual representations of the entire input sequence, making it better for understanding tasks (classification, NER, retrieval) rather than generation. (Source: encoder-models.md)

## Q042
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** encoder-models
**Focus Area:** BERT training tasks
**Question:** What are the two pre-training tasks for BERT, and why were they chosen?
**Answer:** (1) **Masked Language Modeling (MLM):** Random tokens are masked; the model must predict them. This forces the model to use bidirectional context. (2) **Next-Sentence Prediction (NSP):** Given two sentences, predict whether the second follows the first. This teaches the model sentence-level relationships. These tasks are challenging, don't require autoregressive ordering, and encourage a rich global sentence representation in the [CLS] token. (Source: encoder-models.md)

## Q043
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** encoder-models
**Focus Area:** Using BERT for downstream tasks
**Question:** How is a pre-trained BERT model adapted for a text classification task like sentiment analysis?
**Answer:** The encoding of the [CLS] token is used as a global sentence representation. A **classification head** (typically a simple linear layer / matrix multiplication) is placed on top of this [CLS] encoding, mapping it to as many output classes as needed. The model can then be either (1) frozen — only the classification head is trained — or (2) fine-tuned — the entire BERT model is further trained on the labeled classification dataset. (Source: encoder-models.md)

## Q044
**Status:** active
**Type:** true-false
**Difficulty:** introductory
**Topic:** language-models
**Focus Area:** Language modeling as next-token prediction
**Question:** True or False: Language modeling is the task of directly generating the most likely complete sentence given a prompt, in one forward pass.
**Answer:** False. Language modeling (specifically autoregressive LM) is the task of predicting the **next token** at each step. A full sentence is generated autoregressively — one token at a time — not in a single forward pass. Each new token is sampled or selected from the predicted distribution and then appended to the context for the next prediction step. (Source: language-models.md)

## Q045
**Status:** active
**Type:** true-false
**Difficulty:** intermediate
**Topic:** alignment
**Focus Area:** RLHF vs. pretraining
**Question:** True or False: According to the superficial alignment hypothesis, alignment training (SFT + RLHF) is where the model acquires most of its capabilities (e.g., reasoning, knowledge).
**Answer:** False. The superficial alignment hypothesis holds that the "heavy lifting" — acquiring capabilities — happens in **pretraining**. Alignment only teaches the model how to *apply* what it has already learned, adjusting its style and behavior to be helpful and safe, but not adding fundamentally new capabilities. (Source: alignment.md)

## Q046
**Status:** active
**Type:** short-answer
**Difficulty:** advanced
**Topic:** language-models
**Focus Area:** Positional embeddings — absolute vs. relative
**Question:** What is the difference between absolute and relative positional embeddings, and why have relative embeddings become more common?
**Answer:** Absolute positional embeddings assign a different embedding for each absolute position in the sentence. Relative positional embeddings are constructed so that when two tokens are compared/combined, only the *difference* in their positions matters. Relative embeddings are more common today because they generalize better to sequence lengths not seen during training — absolute PEs can struggle if the model is applied to longer sequences than it was trained on. (Source: language-models.md)

## Q047
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** training-deep-dive
**Focus Area:** Gradient descent — local vs. global minima
**Question:** Why does gradient descent only guarantee finding a local minimum rather than the global minimum, and is this a major problem in practice for deep learning?
**Answer:** Gradient descent follows the local slope — it moves downhill from wherever it starts. If the loss landscape has multiple valleys, it will settle in the nearest one (local minimum) rather than necessarily finding the deepest one (global minimum). In practice for deep learning, this is often less problematic than it sounds — the loss landscape of large networks tends to have many good local minima, and modern optimizers (with momentum) can escape shallow local minima. (Source: training-deep-dive.md)

## Q048
**Status:** active
**Type:** mcq
**Difficulty:** intermediate
**Topic:** language-models
**Focus Area:** Softmax properties
**Question:** Which of the following is NOT a property of the softmax function? (A) All outputs sum to 1. (B) Larger input scores produce larger output probabilities. (C) It is shift-invariant (adding a constant to all inputs doesn't change the output). (D) It maps inputs to the range [-1, 1].
**Answer:** (D). Softmax maps all inputs to the range (0, 1) — not [-1, 1]. All other statements are correct properties of softmax. (Source: language-models.md)

## Q049
**Status:** active
**Type:** conceptual
**Difficulty:** advanced
**Topic:** encoder-models
**Focus Area:** BERT for retrieval / cosine similarity
**Question:** How can BERT embeddings be used for retrieval, and what mathematical operation underlies the similarity comparison?
**Answer:** BERT encodes a query and all documents into dense vectors. The similarity between query and each document is computed using the **dot product** (or **cosine similarity** — the dot product normalized by vector lengths). Documents with higher cosine similarity to the query are ranked higher. This works because BERT's training encourages similar sequences to have similar embedding vectors. In practice, retrievers are trained with more specialized objectives, but cosine similarity of encodings remains the core mechanism. (Source: encoder-models.md)

## Q050
**Status:** active
**Type:** conceptual
**Difficulty:** intermediate
**Topic:** learning-paradigms
**Focus Area:** Clustering (unsupervised)
**Question:** What is the goal of clustering in unsupervised learning, and why is it considered a hard problem?
**Answer:** The goal is to group together similar items into classes based on their features, without any labeled ground truth. K-means is a common algorithm. It's considered hard because there's no gold standard to train toward — "similarity" must be defined by the practitioner, different initializations can lead to different results, and the number of clusters (k) must be chosen upfront. (Source: learning-paradigms.md)
