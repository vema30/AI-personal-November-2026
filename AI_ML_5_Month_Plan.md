# 5-Month AI / ML Learning Plan

**Assumed time:** about 10–15 hours a week (1.5–2 hours on weekdays, plus 3–4 hours on weekends).
**Goal:** finish with solid Python and math basics, a working knowledge of classical ML, deep learning, and modern LLM/GenAI development, and 4–5 portfolio projects on GitHub.

---

## Overview

| Month | Focus | Main outcome |
|-------|-------|--------------|
| 1 | Python for data + math foundations | Comfortable with NumPy, pandas, plotting, and basic linear algebra, statistics and calculus |
| 2 | Classical Machine Learning | Can build, evaluate and tune scikit-learn models end to end |
| 3 | Deep Learning (PyTorch) | Can build and train neural nets, CNNs and simple sequence models |
| 4 | NLP, Transformers and LLMs | Understands transformers; uses Hugging Face; builds LLM apps (prompting, RAG) |
| 5 | MLOps, specialization and capstone | Deploys a model or API; finishes a capstone; has a portfolio ready |

---

## Setup (Week 0, 1–2 days)

- Install **Python 3.11+** (already on your machine), **VS Code** with the Python and Jupyter extensions, and **Git**.
- Create a virtual environment in this folder:
  ```powershell
  python -m venv .venv
  .\.venv\Scripts\Activate.ps1
  pip install numpy pandas matplotlib seaborn scikit-learn jupyter
  ```
- Create free accounts on **GitHub**, **Kaggle** and **Google Colab** (Colab gives you a free GPU for Month 3 onward).
- Folder layout: `month1/`, `month2/`, … and `projects/`.

---

## Month 1 – Python and Math Foundations

### Week 1: Python refresher
- Data types, lists, dicts, sets, comprehensions, functions, `*args/**kwargs`, classes, modules, exceptions, file I/O.
- Practice: 20–30 easy problems on HackerRank or LeetCode (Python track).
- **Mini-task:** a CLI script that reads a CSV and prints summary statistics using only plain Python.

### Week 2: NumPy and pandas
- NumPy: arrays, indexing, broadcasting, vectorization, `reshape`, aggregations.
- pandas: `Series`/`DataFrame`, `read_csv`, filtering, `groupby`, `merge`, missing values, `apply`.
- Resource: Kaggle Learn "Pandas" (free), the official pandas "10 minutes to pandas" guide.

### Week 3: Visualization and EDA
- Matplotlib and Seaborn: line, bar, histogram, scatter, box and heatmap plots.
- Exploratory Data Analysis workflow: look at distributions, correlations and outliers.
- **Project 1 – EDA notebook:** pick a Kaggle dataset (Titanic, House Prices or similar) and publish a clean EDA notebook on GitHub.

### Week 4: Math for ML (only what you need)
- **Linear algebra:** vectors, dot product, matrices, matrix multiplication, transpose, inverse, eigenvalues (intuition). Resource: 3Blue1Brown, "Essence of Linear Algebra".
- **Calculus:** derivatives, partial derivatives, chain rule, gradients. Resource: 3Blue1Brown, "Essence of Calculus".
- **Probability and statistics:** mean, variance, distributions (normal, binomial), Bayes' theorem, hypothesis testing basics. Resource: StatQuest (YouTube).
- Practice: implement the dot product, matrix multiplication and gradient descent on `y = x²` in NumPy.

**Month 1 checkpoint:** you can load, clean, analyze and plot any CSV dataset, and you can explain what a gradient is.

---

## Month 2 – Classical Machine Learning

**Main resources:** Andrew Ng's *Machine Learning Specialization* (Coursera; you can audit it for free) and the book *Hands-On Machine Learning with Scikit-Learn, Keras & TensorFlow* by Aurélien Géron (chapters 1–7).

### Week 5: ML fundamentals and regression
- Supervised vs. unsupervised learning, train/test split, overfitting vs. underfitting, the bias–variance trade-off.
- Linear regression: cost function and gradient descent. **Code it from scratch in NumPy**, then use `sklearn`.
- Metrics: MAE, MSE, RMSE, R².

### Week 6: Classification
- Logistic regression, k-NN, Decision Trees, Naive Bayes, SVM (intuition).
- Metrics: accuracy, precision, recall, F1, confusion matrix, ROC-AUC.
- Handling class imbalance.

### Week 7: Ensembles, feature engineering and tuning
- Random Forest, Gradient Boosting, **XGBoost / LightGBM**.
- Feature scaling, encoding (one-hot, ordinal), feature selection, `Pipeline` and `ColumnTransformer`.
- Cross-validation, `GridSearchCV` / `RandomizedSearchCV`.

### Week 8: Unsupervised learning and the Month 2 project
- K-Means, hierarchical clustering, DBSCAN, PCA.
- **Project 2 – End-to-end ML project:** for example, house price prediction or customer churn. Cover EDA, preprocessing pipeline, several models, tuning, evaluation and a README that explains your results. Submit it to a Kaggle competition.

**Month 2 checkpoint:** given a tabular dataset, you can build a tuned, cross-validated model and justify your choice of metric.

---

## Month 3 – Deep Learning with PyTorch

**Main resources:** Andrej Karpathy's *Neural Networks: Zero to Hero* (YouTube), the official PyTorch tutorials, and the fast.ai *Practical Deep Learning for Coders* course (free). Use Google Colab for the GPU.

### Week 9: Neural network basics
- Perceptron, activation functions (ReLU, sigmoid, softmax), loss functions, backpropagation.
- Build a tiny autograd engine (follow Karpathy's "micrograd" video).
- Build an MLP in NumPy for MNIST, then in PyTorch.

### Week 10: PyTorch in depth
- Tensors, `autograd`, `nn.Module`, `Dataset`/`DataLoader`, the training loop, optimizers (SGD, Adam).
- Regularization: dropout, weight decay, batch norm, early stopping.
- Learning-rate schedules; saving and loading models.

### Week 11: Computer vision with CNNs
- Convolutions, pooling, CNN architectures (LeNet, ResNet intuition).
- Data augmentation, **transfer learning** with pretrained models (`torchvision`).
- **Project 3 – Image classifier:** fine-tune a ResNet on a custom dataset (plants, food, X-rays, or similar).

### Week 12: Sequence models
- RNNs, LSTMs and GRUs (concepts), embeddings.
- Build a character-level language model (Karpathy's "makemore" series).
- Introduction to attention: why RNNs struggle with long sequences.

**Month 3 checkpoint:** you can write a PyTorch training loop from memory, and you can explain backpropagation and transfer learning.

---

## Month 4 – NLP, Transformers and LLMs

**Main resources:** the Hugging Face NLP/LLM Course (free), Karpathy's "Let's build GPT" video, and the paper *Attention Is All You Need*.

### Week 13: NLP basics and Transformers
- Tokenization (BPE/WordPiece), word embeddings (Word2Vec intuition).
- Self-attention, multi-head attention, positional encoding, encoder vs. decoder models (BERT vs. GPT).
- Build a mini-GPT from scratch (follow Karpathy's video).

### Week 14: Hugging Face ecosystem
- `transformers`, `datasets`, `tokenizers`; the `pipeline` API.
- Fine-tune a BERT or DistilBERT model for text classification (sentiment, spam, intent).
- Efficient fine-tuning: **LoRA / PEFT** concepts, quantization basics.

### Week 15: Building LLM applications
- Prompt engineering: zero-shot, few-shot, chain-of-thought, structured (JSON) output.
- Using LLM APIs (OpenAI, Anthropic, Gemini) or local models (Ollama).
- Embeddings and vector databases (FAISS, Chroma).
- **RAG (Retrieval-Augmented Generation):** chunking, retrieval, re-ranking, evaluation.

### Week 16: Agents and the Month 4 project
- Tool / function calling, simple agents, frameworks (LangChain, LlamaIndex). Learn the concepts first; you can build a simple agent without a framework.
- **Project 4 – RAG chatbot:** a "chat with your PDFs or docs" app using Streamlit or Gradio, with source citations.

**Month 4 checkpoint:** you can explain how a transformer works, fine-tune a model, and build a working RAG application.

---

## Month 5 – MLOps, Specialization and Capstone

### Week 17: Deployment and MLOps basics
- Serve a model with **FastAPI**; containerize it with **Docker**.
- Experiment tracking with **MLflow** or Weights & Biases.
- Deploy a free demo to Hugging Face Spaces, Render or Streamlit Community Cloud.
- Basics: model versioning, monitoring, data drift, CI with GitHub Actions.

### Week 18: Choose one specialization and go deeper

| Track | What to learn |
|-------|---------------|
| **GenAI / LLM Engineer** (most in demand) | Advanced RAG, LLM evaluation, agents, fine-tuning with LoRA, guardrails |
| Computer Vision | Object detection (YOLO), segmentation, OpenCV |
| Data Science / Analytics | Time series (Prophet, ARIMA), A/B testing, SQL, dashboards |
| Classical ML Engineering | Feature stores, batch pipelines, model monitoring at scale |

### Weeks 19–20: Capstone project
- **Project 5 – Capstone:** solve a real problem, ideally from your own work domain (for example, insurance: claim fraud detection, document or policy Q&A with RAG, or premium prediction).
- It must include: a problem statement, data, a model or LLM pipeline, evaluation, a deployed demo, and a detailed README with architecture diagram and results.
- Write a blog post (Medium, LinkedIn or Hashnode) about it.

### Final week: Portfolio and next steps
- Clean up the GitHub repos for all 5 projects (README, requirements.txt, screenshots, demo links).
- Update your résumé and LinkedIn; add a "Projects" section.
- Practice ML interview questions (metrics, bias/variance, regularization, transformers, system design for ML).

---

## Weekly Routine (Template)

| Day | Activity (about 1.5–2 h) |
|-----|------------------------|
| Mon–Wed | Learn: course videos or book chapters, with notes |
| Thu–Fri | Code: re-implement the concepts in a notebook |
| Sat | Build: work on the weekly mini-project |
| Sun | Review: revise notes, push to GitHub, plan the next week (1 h) |

**Rule of thumb:** spend 30% of your time watching or reading and 70% coding. Don't get stuck watching tutorials without building anything.

---

## Projects Summary (Portfolio)

1. **EDA notebook** – data cleaning and visualization (Month 1)
2. **End-to-end ML model** – tabular prediction with a tuned pipeline (Month 2)
3. **Image classifier** – CNN with transfer learning (Month 3)
4. **RAG chatbot** – chat with documents using an LLM (Month 4)
5. **Deployed capstone** – real-world problem, API plus UI, Dockerized (Month 5)

---

## Core Resource List (mostly free)

- **Python:** official Python tutorial; Kaggle Learn (Python, Pandas, Intro to ML)
- **Math:** 3Blue1Brown (Linear Algebra, Calculus, Neural Networks); StatQuest; Khan Academy
- **ML:** Andrew Ng's ML Specialization (Coursera); *Hands-On ML* by Aurélien Géron; scikit-learn docs
- **Deep Learning:** Karpathy's "Zero to Hero"; fast.ai; PyTorch tutorials; *Dive into Deep Learning* (d2l.ai, free)
- **LLMs:** Hugging Face Course; DeepLearning.AI short courses (free); provider docs (OpenAI, Anthropic)
- **Practice:** Kaggle competitions and datasets; LeetCode (easy/medium Python)

---

## Progress Tracker

- [ ] Week 0 – Environment set up
- [ ] Month 1 – Python, NumPy, pandas, visualization, math → Project 1
- [ ] Month 2 – Regression, classification, ensembles, unsupervised → Project 2
- [ ] Month 3 – Neural nets, PyTorch, CNNs, sequence models → Project 3
- [ ] Month 4 – Transformers, Hugging Face, prompting, RAG, agents → Project 4
- [ ] Month 5 – FastAPI, Docker, MLflow, specialization, capstone → Project 5
- [ ] Portfolio, résumé and blog published

---

## Tips for Success

1. **Consistency beats intensity:** 1.5 hours every day is better than 10 hours once a week.
2. **Build from scratch once, then use libraries:** for example, linear regression, an MLP and attention.
3. **Learn in public:** post weekly progress on LinkedIn or GitHub.
4. **Don't wait to master math:** learn it alongside the ML topics as you need it.
5. **Use AI assistants to explain things, not to write everything:** write the code yourself first.
6. **Join communities:** Kaggle discussions, Hugging Face Discord, r/learnmachinelearning.