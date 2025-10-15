# 💳 Sparkflows Fraud Detection

End-to-end **Credit Card Fraud Detection** project built on **Sparkflows**, combining **SMOTE balancing**, **Random Forest**, **XGBoost (H2O)**, and **SHAP explainability** to detect fraudulent transactions with high accuracy and interpretability.

---

## 📘 Project Overview

This project was developed during my **AI Internship at Treomind** (Istanbul) as part of my work in the **AI Department**.  
It demonstrates how to design, train, and evaluate machine learning workflows in **Sparkflows**, a low-code data science platform for building scalable ML pipelines.

The goal was to **detect fraudulent transactions** in a highly imbalanced credit card dataset, while ensuring **model transparency** using **SHAP values**.

---

## 🧠 Key Objectives

- Perform **data profiling** and exploratory analysis inside Sparkflows  
- Handle **class imbalance** using **SMOTE oversampling**  
- Train multiple models:
  - Decision Tree Classifier  
  - Random Forest Classifier  
  - H2O XGBoost  
- Evaluate performance using **ROC-AUC**, **PR-AUC**, and **Confusion Matrices**  
- Extract and visualize **SHAP feature contributions** for interpretability  
- Document every **Sparkflows node configuration** and workflow step

---

## ⚙️ Workflows Included

| Workflow | Purpose |
|-----------|----------|
| **1️⃣ Data Profiling** | Correlation matrix, histograms, outlier analysis |
| **2️⃣ Decision Tree (Baseline)** | Initial model without balancing |
| **3️⃣ Decision Tree + SMOTE** | Oversampling minority (fraud) class |
| **4️⃣ Random Forest + SMOTE** | Ensemble method for better generalization |
| **5️⃣ H2O XGBoost + SHAP** | Gradient boosting with feature explainability |
| **6️⃣ SHAP Extract** | SQL transformation & CSV export of SHAP values |
| **7️⃣ Score Workflow** | Load model, predict on new data, and save results |

---

## 📊 Results Summary

| Model | Balancing | Accuracy | ROC-AUC | PR-AUC | Key Notes |
|--------|------------|-----------|----------|----------|------------|
| Decision Tree | ❌ None | 99.92% | 0.731 | 0.596 | Misleading accuracy due to imbalance |
| Decision Tree | ✅ SMOTE | 98.80% | 0.8596 | 0.8719 | Big recall improvement |
| Random Forest | ✅ SMOTE | 98.66% | **0.991** | **0.978** | Best model – balanced precision & recall |
| H2O XGBoost | ✅ SMOTE + SHAP | — | — | — | Used for interpretability & SHAP extraction |

> 💡 *High accuracy alone isn’t meaningful for imbalanced data — AUC and precision-recall tell the real story.*

---

## 🔍 Explainability (SHAP Values)

To make the model interpretable, the project used **H2O XGBoost** with `With Contributions = true` to compute **SHAP (SHapley Additive exPlanations)**.  
Then, using SQL Transformer nodes, all SHAP contributions were extracted per feature and exported as a CSV file for visualization and analysis.

This step reveals **which variables most influence fraud predictions**, improving transparency and trust.

---

## 🧩 Tech Stack

- **Sparkflows** – Low-code data science platform  
- **Apache Spark** – Distributed processing backend  
- **H2O.ai Integration** – For XGBoost + SHAP explainability  
- **Python / SQL Nodes** – Data transformation and feature engineering  
- **CSV / Parquet** – Data storage and SHAP export

---


## 🧾 Documentation

Full step-by-step workflow documentation is available in  
[`FRAUD_DETECTION_MODEL_DOCUMENTATION.pdf`](./FRAUD_DETECTION_MODEL_DOCUMENTATION.pdf)

This document includes:
- Node configurations  
- Workflow connections  
- Visualization samples  
- Evaluation results  
- Final SHAP extraction pipeline  

---

## 🧑‍💻 Author

**Kutay Demir**  
AI & Data Science Intern @ Treomind  
🎓 Computer Engineering Student, MEF University  
🌐 [GitHub Profile](https://github.com/kutaydemir462)

---

## 🏷️ Keywords

`Sparkflows` • `Machine Learning` • `SMOTE` • `Random Forest` • `XGBoost` • `H2O` • `SHAP` • `Credit Card Fraud Detection` • `Data Science` • `Explainable AI`

---

⭐ **If you found this project insightful, consider giving it a star — it helps others discover explainable AI workflows built on Sparkflows.**
