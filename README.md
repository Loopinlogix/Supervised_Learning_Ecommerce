# Supervised_Learning_Ecommerce
# E-Commerce Customer Classification — ML Assignment

[![Python](https://img.shields.io/badge/Python-3.10%2B-blue)](https://www.python.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-1.3%2B-orange)](https://scikit-learn.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

&gt; **Objective:** Predict whether an e-commerce customer is a **High Value** or **Low Value** customer based on behavioral and profile data using multiple classification models.

---

## 📋 Table of Contents

- [Project Overview](#-project-overview)
- [Dataset](#-dataset)
- [Models Evaluated](#-models-evaluated)
- [Requirements](#-requirements)
- [Setup & Installation](#-setup--installation)
- [How to Run](#-how-to-run)
- [Results](#-results)
- [Project Structure](#-project-structure)
- [Key Insights](#-key-insights)
- [Author](#-author)

---

## 🎯 Project Overview

This project addresses a binary classification problem in e-commerce analytics. Using synthetic customer data, we compare five machine learning algorithms to identify the best approach for segmenting customers by spending behavior.

**Business Value:**
- Enable targeted marketing campaigns
- Optimize resource allocation for high-value customers
- Reduce customer churn through early identification of at-risk high-value segments

**Target Variable:**
| Class | Label | Definition |
|-------|-------|------------|
| 0 | Low Value | Yearly spending ≤ median ($~500) |
| 1 | High Value | Yearly spending &gt; median ($~500) |

---

## 📊 Dataset

| Feature | Type | Description |
|---------|------|-------------|
| `Email` | Identifier | Customer email address |
| `Address` | Identifier | Customer shipping address |
| `Avatar` | Categorical | Color preference (Red, Blue, Green, Orange, Purple, Yellow) |
| `Avg Session Length` | Numeric | Average minutes per session |
| `Time on App` | Numeric | Total minutes spent on mobile app |
| `Time on Website` | Numeric | Total minutes spent on website |
| `Length of Membership` | Numeric | Years as a registered member |
| `Yearly Amount Spent` | Target (continuous) | Total annual spending in USD |

**Data Characteristics:**
- **Samples:** 500 customers
- **Features:** 6 input features (2 identifiers + 4 numeric + 1 categorical)
- **Class Balance:** 50/50 (median-split threshold)
- **Synthetic:** Generated with controlled noise for reproducibility

---

## 🤖 Models Evaluated

| Model | Scaling Required | Key Hyperparameters |
|-------|-----------------|---------------------|
| Logistic Regression | ✅ Yes | `max_iter=5000` |
| Random Forest Classifier | ❌ No | `n_estimators=200` |
| Support Vector Machine (SVM) | ✅ Yes | `probability=True` |
| Decision Tree | ❌ No | Default |
| K-Nearest Neighbors (KNN) | ✅ Yes | `n_neighbors=5` |

**Evaluation Metrics:** Accuracy, Precision, Recall, F1-Score, ROC-AUC

---

## ⚙️ Requirements

### Software
- Python 3.10 or higher
- Google Colab (recommended) or Jupyter Notebook

### Python Libraries
