# Amazon Review Defect Mining

This project extracts and groups product defects from Amazon customer reviews using sentiment analysis and natural language processing (NLP).

The approach identifies negative review sentences, extracts defect-related terms, and clusters similar complaints to discover common product issues automatically.

---

## Overview

The pipeline consists of:

1. Review extraction and sentence segmentation
2. Sentiment analysis using VADER
3. Selection of negative review sentences
4. NLP preprocessing:
   - Tokenization
   - Stop-word removal
   - Lemmatization
   - Noun extraction
5. TF-IDF feature generation
6. Defect clustering using DBSCAN
7. Visualization of discovered defect groups

---

## Dataset

The project uses a shoe review dataset obtained from Kaggle.

Dataset source:

🔗 https://www.kaggle.com/code/sargisiskandaryan/shoes-review-sentiment-analysis

---

## Methodology

### Sentiment Analysis

Negative review sentences are identified using the VADER sentiment analyzer.

A sentence is considered negative when:

- Compound sentiment score < 0
- Neutral score < 0.9

### Text Preprocessing

The extracted negative sentences undergo:

- Lowercasing
- Tokenization
- English vocabulary filtering
- POS tagging
- Lemmatization
- Noun extraction
- Stop-word removal
- Punctuation removal
- Number removal

### Feature Extraction

Text is converted into numerical representations using:

- TF-IDF Vectorization
- Unigrams and Bigrams

### Defect Discovery

Similar complaints are grouped using:

- DBSCAN clustering
- Automatic epsilon estimation using a k-distance graph and KneeLocator

### Visualization

Cluster results are projected to two dimensions using PCA for visualization.

---

## Technologies

- Python
- NLTK
- VADER Sentiment Analysis
- Scikit-learn
- TF-IDF
- DBSCAN
- PCA
- Pandas
- Matplotlib

---

## Results

The output consists of clusters of semantically similar negative customer comments that can be interpreted as recurring product defects.

Examples include:

- Material defects
- Durability issues
- Comfort problems
- Sizing complaints

---

## Reference

This implementation is based on the methodology described in:

🔗 https://ieeexplore.ieee.org/document/9377851

---
Isfahan University of Technology - IT Fundamentals - Course Project