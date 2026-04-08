# Transformer-Based-Scientific-Document-Intelligence-Pipeline
# Smart Research Paper Domain Classification, Recommendation & Credibility Checker

An AI-powered research paper analysis system that classifies papers into academic domains, recommends semantically similar papers, and evaluates document credibility.

Built using **SciBERT, SBERT, and Hierarchical SBERT Classification**, this project helps researchers quickly identify **relevant, trustworthy, and domain-specific papers**.

---

## 🚀 Features

- 📚 **Research Domain Classification**
  - Uses **SciBERT** to classify papers into domains like:
    - Computer Science
    - Physics
    - Mathematics
    - Engineering

- 🔍 **Semantic Paper Recommendation**
  - Uses **Sentence-BERT (SBERT)** embeddings
  - Finds semantically similar papers using cosine similarity

- ✅ **Credibility Checker**
  - Predicts credibility using:
    - writing quality
    - structural consistency
    - category reliability
    - hierarchical domain classification

- 🧠 **Hierarchical Classification**
  - Level 1 → broad domains
  - Level 2 → fine-grained arXiv subcategories
  - rare/unusual domains mapped to lower credibility

---

## 🛠️ Tech Stack

- Python
- Google Colab
- Hugging Face Transformers
- SciBERT
- Sentence Transformers (SBERT)
- Scikit-learn
- Logistic Regression
- NumPy
- Pandas
- Matplotlib
- arXiv Dataset

---

## 📂 Project Structure

```bash
smart-research-paper-checker/
│
├── notebooks/
│   ├── domain_classification_scibert.ipynb
│   ├── recommendation_engine_sbert.ipynb
│   ├── credibility_checker_hierarchical_sbert.ipynb
│
├── dataset/
│   ├── arxiv_data.csv
│   └── credibility_data.csv
│
├── saved_models/
│   ├── scibert_model/
│   ├── sbert_embeddings.npy
│   └── credibility_classifier.pkl
│
├── outputs/
│   ├── confusion_matrix.png
│   └── recommendation_samples.csv
│
├── README.md
└── requirements.txt
⚙️ Methodology
1️⃣ Domain Classification

Fine-tuned SciBERT (allenai/scibert_scivocab_uncased)
for scientific abstract classification.

2️⃣ Recommendation Engine

Used SBERT (all-mpnet-base-v2)
to generate embeddings and cosine similarity scores.

3️⃣ Credibility Module

Hierarchical SBERT + Logistic Regression:

Level 1: main domain prediction
Level 2: subdomain prediction
rare labels grouped into OTHER_domain

Credibility is reduced when:

rare categories appear
domain mismatch occurs
linguistic consistency is poor
📊 Results
✅ SciBERT Classification
Accuracy: ~80%
Strong semantic understanding
Balanced precision/recall
✅ Credibility Checker
Score range: 0.0 to 1.0
High interpretability
Detects weak or suspicious scientific writing
✅ Recommendation Engine
Strong semantic relevance
Better than keyword matching
Credibility-aware ranking supported
🔮 Future Improvements
Citation network analysis
PDF upload support
plagiarism detection
explainable AI module
full research paper analysis
real-time web app deployment
📄 Research Motivation

With the rapid growth of scientific publications, manually identifying
relevant and trustworthy research papers is difficult.

This project solves that using:

SciBERT for classification
SBERT for recommendation
Hierarchical credibility analysis

making academic literature review faster and smarter.
