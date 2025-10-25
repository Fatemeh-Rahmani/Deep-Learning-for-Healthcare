# Deep Learning for Healthcare

[![Python](https://img.shields.io/badge/python-3.10-blue)](https://www.python.org/)
[![PyTorch](https://img.shields.io/badge/pytorch-2.0-red)](https://pytorch.org/)
[![License](https://img.shields.io/badge/license-MIT-green)](LICENSE)

This repository contains multiple healthcare-focused deep learning projects built using PyTorch.

---

## 1. Pneumonia Detection (CNN on Chest X-Ray Images)

**Objective:** Classify chest X-ray images as *Normal* or *Pneumonia*.  

**Models Used:**  
- Custom CNN  
- ResNet18 (Transfer Learning)

**Evaluation Metrics:**  
- Accuracy  
- Precision  
- Recall  
- F1-score  
- ROC-AUC  
 

---

## 2. Heart Failure Prediction (Bi-directional RNN)

**Objective:** Predict the risk of heart failure using patient diagnosis sequences.  

**Techniques Used:**  
- Diagnosis code embeddings  
- Bi-directional GRU  
- Masking for variable-length visit sequences  

**Evaluation Metrics:**  
- Precision  
- Recall  
- F1-score  
- ROC-AUC  
 

---

## 3. RETAIN – Reverse Time Attention Model

**Objective:** Predict heart failure while providing interpretability by identifying important visits and diagnosis codes.  

**Key Ideas:**  
- Uses a **reverse-time RNN with attention mechanism** (RETAIN model from Choi et al.).  
- Two-level attention:  
  - **α (alpha)** → visit-level importance (scalar attention for each visit)  
  - **β (beta)** → feature-level importance (vector attention for diagnosis codes)  
- Generates a context vector by weighting visit embeddings with α and β.  

**Why RETAIN?**  
- Provides both **high prediction accuracy** and **interpretability**, showing which past visits and diagnoses contributed most to the prediction.  

**Evaluation Metrics:**  
- Precision  
- Recall  
- F1-score  
- ROC-AUC  
 

---
 
