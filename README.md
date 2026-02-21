# neuro-disease-nlp-classifier
NLP-based classification of neurodegenerative diseases using PubMedBERT / 93.23% accuracy
# 🧠 NLP for Analyzing Neurological Disease Paths

An NLP project that classifies neurodegenerative diseases based on clinical symptom timelines using a fine-tuned **PubMedBERT** model, achieving **93.23% accuracy**.

---

## 📌 Project Overview

This project applies Natural Language Processing to analyze the clinical progression of neurodegenerative diseases such as Alzheimer's, Parkinson's, and related conditions. Each patient's symptom history is transformed into a chronological text timeline, which is then classified by disease type.

---

## 🎯 Key Features

- 🔬 Classifying symptoms according to disease type
- 📅 Analyzing temporal progression and chronological sequences
- 🧪 Comparing clinical and pathological diagnoses to reduce diagnostic error
- 🔍 Identifying disease subtypes and progression patterns
- 💊 Future: Treatment recommendations with a chatbot for medication reminders
- 🔗 Future: Extracting causal relationships between symptoms
- 🎙️ Future: Voice analysis to detect speech changes as biomarkers
- 📋 Future: Summarizing clinical histories for physician decision-making

---

## 🗂️ Dataset

- **Source:** Clinical records of brain donors with confirmed neuropathological diagnoses
- **Patients:** 1,329 unique patients
- **Features:** DonorID, Age, Sex, Diagnosis, Symptoms, Years before death, Type

### Disease Distribution

| Disease | Patients |
|--------|----------|
| Alzheimer's Disease | 703 |
| Control Brain | 341 |
| Parkinson's Disease | 133 |
| Progressive Supranuclear Palsy | 91 |
| Multiple System Atrophy | 61 |

---

## 🤖 Model

- **Base Model:** `microsoft/BiomedNLP-PubMedBERT-base-uncased-abstract-fulltext`
- **Task:** Multi-class sequence classification (5 classes)
- **Input:** Patient timeline text including sex, age, type, and chronological symptoms
- **Framework:** HuggingFace Transformers + PyTorch

### Training Configuration

| Parameter | Value |
|-----------|-------|
| Learning Rate | 2e-5 |
| Batch Size | 8 |
| Epochs | 20 (early stopping) |
| Early Stopping Patience | 6 |
| FP16 | True |

---

## 📊 Results

**Final Accuracy: 93.23%**

| Class | Precision | Recall | F1-Score |
|-------|-----------|--------|----------|
| Alzheimer's Disease | 0.96 | 0.98 | 0.97 |
| Control Brain | 1.00 | 1.00 | 1.00 |
| Multiple System Atrophy | 0.73 | 0.67 | 0.70 |
| Parkinson's Disease | 0.74 | 0.93 | 0.82 |
| Progressive Supranuclear Palsy | 1.00 | 0.50 | 0.67 |

---

## 🚀 How to Run

1. Clone the repository
```bash
git clone https://github.com/alaareda121/neuro-disease-nlp-classifier.git
```

2. Install dependencies
```bash
pip install transformers datasets accelerate scikit-learn openpyxl pandas torch
```

3. Run the notebook on Kaggle or locally with GPU support

---

## 🛠️ Tech Stack

- Python
- HuggingFace Transformers
- PyTorch
- scikit-learn
- pandas
- Kaggle (GPU environment)
