# Bank Marketing ML Project

## 📌 Problem Statement
Banks often run marketing campaigns to encourage customers to subscribe to term deposits.  
However, the dataset is highly imbalanced — only about **11%** of customers actually subscribe.  

**Goal:**  
Build and compare multiple machine learning models that can predict whether a customer will subscribe, while handling class imbalance using **SMOTE**.

---

## 📊 Dataset
- **Source:** UCI Machine Learning Repository (Bank Marketing Dataset)  
- **Features:** Customer demographics, financial details, contact methods, previous campaign outcomes  
- **Target (`y`):** Subscription to term deposit (Yes = 1, No = 0)  

---

## ⚙️ Methodology
1. Data preprocessing & categorical encoding  
2. Class imbalance handling using **SMOTE**  
3. Model training on 4 classifiers:  
   - Logistic Regression  
   - Random Forest  
   - XGBoost  
   - Neural Network (MLPClassifier)  
4. Evaluation using metrics: **Accuracy, Precision, Recall, F1-score, ROC-AUC**

---

## 📈 Results

| Model               | Accuracy | Precision (class=1) | Recall (class=1) | F1-score (class=1) | ROC-AUC |
|----------------------|----------|----------------------|------------------|---------------------|---------|
| Logistic Regression  | 0.888    | 0.502                | 0.670            | 0.574               | 0.907   |
| Random Forest        | 0.915    | 0.619                | 0.637            | 0.628               | 0.948   |
| XGBoost              | 0.914    | 0.611                | 0.653            | 0.631               | 0.945   |
| Neural Net (MLP)     | 0.899    | 0.693                | 0.192            | 0.300               | 0.916   |

---

## ✅ Conclusion
- **Random Forest and XGBoost** performed best overall, achieving **ROC-AUC ≈ 0.95**.  
- Logistic Regression is a strong interpretable baseline.  
- Neural Network struggled with recall, indicating it missed many positive cases.  
- **SMOTE successfully balanced the dataset** and improved recall across most models.  

---

## 🚀 How to Run
1. Clone this repo  
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
