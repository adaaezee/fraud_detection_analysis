# Credit Card Fraud Detection – WEKA Analysis

This project uses the well-known **Credit Card Fraud Detection** dataset from Kaggle to build and evaluate fraud prediction models using **WEKA**.  
It was completed as part of my MSc Artificial Intelligence coursework and demonstrates skills in:

- supervised learning  
- feature selection  
- model evaluation  
- working with highly imbalanced datasets  
- comparative analysis of classifiers  

---

## Dataset

- **Source:** Kaggle  
- **Link:** https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud  
- **Description:** 284,807 transactions with only 492 fraudulent cases (≈0.17%)  
- **Challenge:** Extreme class imbalance  

Dataset is not included in this repo due to licensing restrictions.  
Please download it directly from Kaggle.

---

## Feature Selection

To identify the most informative attributes, I used:

- **Evaluator:** `CorrelationAttributeEval`  
- **Search Method:** `Ranker`  
- **Outcome:** Produced a ranked list of features based on their correlation with the fraud class.  

*Screenshot included in the `/screenshots` folder.*

---

## Models Tested

I applied two supervised ML algorithms:

### **1. Logistic Regression**
- Interpretable  
- Good baseline  
- Performs well with linear relationships  
- High AUC  

### **2. Random Forest**
- Handles non-linear patterns  
- Robust to noise  
- Works well on imbalanced datasets  

---

## Evaluation Metrics (Class = 1 → Fraud)

| Metric | Logistic Regression | Random Forest |
|--------|----------------------|----------------|
| **Precision** | 0.872 | 0.957 |
| **Recall** | 0.624 | 0.776 |
| **F1-Score** | 0.727 | 0.857 |
| **ROC AUC** | 0.975 | 0.951 |

---

## Key Insights

- **Random Forest performed best overall**, achieving the highest precision and F1-score.  
- **Logistic Regression achieved the highest ROC AUC**, showing strong ability to separate classes, but struggled on recall.  
- **Fraud cases are extremely rare**, so metrics like recall and F1-score are more important than accuracy.  
- **Feature ranking provided useful insights** into which attributes contribute most to fraud prediction.  
- The imbalance makes precision/recall trade-offs crucial for real-world deployment.

---

## Tools Used

- **WEKA** (GUI-based machine learning toolkit)  
- Correlation-based feature selection  
- Logistic Regression  
- Random Forest  
- Evaluation: Precision, Recall, F1-Score, ROC AUC  

---

## Summary

This project strengthened my understanding of:

- model evaluation on imbalanced datasets  
- the importance of precision/recall for fraud detection  
- feature selection and attribute ranking  
- comparative model performance  
- interpreting WEKA outputs for real-world decision-making  

---

## Dataset Access  
Dataset must be downloaded from Kaggle due to licensing:  
https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud

---

If you have any questions about this project or would like to see the WEKA workflow, feel free to explore the screenshots folder.

