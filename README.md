# 🔁 Retention Insights – Churn & Value Drop Prediction

This project uses machine learning to predict customer churn based on behavioral, transactional, and service interaction data. The goal is to identify high-risk customers and guide proactive retention strategies.

---

## 🧠 Project Summary

- 📊 **Problem**: Binary classification – churned vs. retained customers
- 🏗️ **Tech Stack**: Python, scikit-learn, XGBoost, SHAP, Seaborn
- 🎯 **Objective**: Predict which customers are likely to churn and understand the "why" using explainable AI

---

## 📁 Files

| File | Description |
|------|-------------|
| `01_generate_churn_data.ipynb` | Creates a realistic, labeled churn dataset |
| `02_churn_classification.ipynb` | ML model with class weighting, SHAP explainability |
| `data/retention_insights_fake_customers.csv` | The generated dataset |

---

## 🔍 Features Used

- `tenure_months`: How long they've been with the company
- `monthly_spend`: Average billing amount
- `num_complaints`: Count of service complaints
- `is_on_promo_plan`: Whether the customer is on a discount plan
- `used_app_this_week`: Recent digital engagement
- `segment`: Customer tier (Basic, Plus, Premium)

---

## ✅ Model Performance

- Trained using **XGBoost** with `scale_pos_weight` to handle imbalance
- Achieved ~70% accuracy
- **Churn recall** improved from 29% ➜ 36% after class balancing

---

## 🔬 Explainability with SHAP

SHAP is used to:

- Understand global feature importance (e.g. complaints, tenure)
- Explain individual churn predictions
- Build trust and transparency for business users

---

## 📈 Use Cases

- Targeted churn prevention campaigns
- Personalized offers for at-risk segments
- Trigger alerts based on SHAP-driven decision rules

---

## 🔮 Next Steps

- Test SMOTE vs. `scale_pos_weight`
- Simulate marketing impact with campaign scoring
- Deploy lightweight API for live scoring

---
