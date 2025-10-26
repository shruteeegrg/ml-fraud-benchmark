# 🔐 Credit Card Fraud Detection with Machine Learning

> **Catching the bad guys, one transaction at a time.** 💳✨

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/scikit--learn-ML-orange.svg)](https://scikit-learn.org/)

---

## 🎯 The Challenge

Imagine searching for 492 needles in a haystack of 284,807 pieces of hay. That's **0.173%** - the percentage of fraudulent transactions in our dataset. Welcome to the world of extreme class imbalance!

This project tackles one of the most challenging problems in financial technology: **detecting fraudulent credit card transactions**. Using cutting-edge machine learning techniques and smart feature engineering, we've built a system that can spot fraud with remarkable accuracy.

---

##  What Makes This Special?

- **Advanced Feature Engineering**: We don't just use raw data - we craft intelligent features that capture temporal patterns and transaction behaviors
- **Smart Imbalance Handling**: SMOTE isn't just a technique here; it's our secret weapon against the tyranny of imbalanced data
- **Battle of the Models**: Five heavyweight ML algorithms duke it out - may the best model win!
- **Real-World Simulation**: Trained on balanced data, tested on real-world imbalanced scenarios - just like production

---

## 📈 The Results Are In!

Our champion model? **Random Forest** takes the crown! 

### 🥇 Leaderboard

| Model | F1-Score | Precision | Recall | Why It Matters |
|:---|:---:|:---:|:---:|:---|
**Random Forest** | **0.8216** | 0.8837 | 0.7677 | Perfect balance - catches fraudsters without annoying customers |
**XGBoost** | 0.8148 | 0.8556 | 0.7778 | Speed demon with excellent PR-AUC |
**Decision Tree** | 0.4873 | 0.3807 | 0.6768 | Simple but struggles with precision |
**Gradient Boosting** | 0.2309 | 0.1339 | 0.8384 | Catches fraud but cries wolf too often |
**Logistic Regression** | 0.1034 | 0.0550 | 0.8586 | High recall, but at what cost? |

### What These Numbers Mean

- **Random Forest caught 76 out of 99 fraudulent transactions** while only incorrectly flagging 10 legitimate ones
- That's a **77% fraud detection rate** with **88% precision** - industry-leading performance!
- **XGBoost** is hot on its heels with the best PR-AUC score (0.8101) - perfect for highly imbalanced scenarios


---

## Quick Start

### Get Up and Running in 3 Steps

**1. Clone & Enter**
```bash
git clone git@github.com:shruteeegrg/ml-fraud-benchmark.git
```

**2. Power Up**
```bash
pip install -q imbalanced-learn scikit-learn pandas numpy matplotlib seaborn opendatasets xgboost
```

**3. Launch**
```bash
jupyter notebook Fraud_Detection_Model.ipynb
```

You'll need your Kaggle API credentials (`kaggle.json`) to download the dataset. Place it in `~/.kaggle/` and you're golden!

---

## 📊 The Dataset

**Source**: [Kaggle's Credit Card Fraud Detection Dataset](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)

**The Stats**:
-  Time period: September 2013 (2 days)
-  Total transactions: 284,807
-  Fraudulent cases: 492
-  Features: 28 PCA-transformed features (V1-V28) + Time + Amount
-  Origin: European cardholders

**Why PCA?** Privacy matters! All original features were transformed to protect sensitive information while preserving patterns.

---

## 🎓 Key Takeaways

 **Class imbalance is real** - and ignoring it means your model will just predict "not fraud" every time and call it a day
 
 **F1-Score > Accuracy** - When classes are imbalanced, accuracy is a liar. F1-Score tells the truth.
 
 **SMOTE for the win** - Synthetic oversampling is your best friend when you have rare events
 
 **Ensemble methods** - Random Forest and XGBoost dominate simpler models in complex scenarios
 
 **Feature engineering is an art** - The right features can make or break your model

---
