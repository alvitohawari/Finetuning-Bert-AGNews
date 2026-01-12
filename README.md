# Fine-tuning BERT for News Topic Classification (AG News)

## 👥 Team Information
**Course**: Deep Learning  
**Institution**: Telkom University  

| Name | NIM |
|------|-----|
| Alvito Kiflan Hawari | 1103220235 |
| Nafal Rifky Atsilah Maulana | 1103223106 |

---

## 🎯 Purpose
This repository contains the implementation of a **news topic classification** project using **BERT**.

The objective of this project is to fine-tune a pre-trained **BERT** model on the **AG News** dataset to classify news articles into predefined topic categories.

---

## 🔍 Project Overview

### The Task: News Topic Classification
News topic classification is a **multi-class text classification task** where the goal is to automatically assign a topic label to a news article based on its content.

---

## 📰 Dataset: AG News
**AG News** is a popular benchmark dataset for topic classification, collected from news articles.

- **Input**: News headline and short description
- **Output Labels**:
  - World
  - Sports
  - Business
  - Science / Technology
- **Number of Classes**: 4
- **Task Type**: Multi-class text classification

---

## 🤖 Model Description

### The Model: BERT-base
- **Base Model**: `bert-base-uncased`
- **Architecture**: Encoder-only Transformer
- **Pre-training Objectives**:
  - Masked Language Modeling (MLM)
  - Next Sentence Prediction (NSP)

### Fine-tuning Strategy
- A classification head is added on top of BERT’s `[CLS]` token
- The entire model is fine-tuned end-to-end
- Cross-entropy loss is used for optimization

---

## 📊 Technical Approach

### Model Configuration
- **Base Model**: `bert-base-uncased`
- **Tokenizer**: `BertTokenizerFast`
- **Framework**: PyTorch & Hugging Face Transformers
- **Task Type**: Multi-class text classification

### Training Configuration
- **Batch Size**: 16
- **Learning Rate**: 2e-5
- **Epochs**: 3
- **Optimizer**: AdamW
- **Loss Function**: Cross-Entropy Loss
- **Evaluation Metrics**:
  - Accuracy
  - Precision
  - Recall
  - F1-score

---

## 📁 Repository Structure
finetuning-bert-agnews/
│
├── notebooks/
│ └── Finetuning-Bert-AGNews.ipynb # Main Jupyter Notebook
│
├── models/
│ └── bert-agnews.pt # Saved fine-tuned model
│
└── README.md # Project documentation
