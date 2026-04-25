# 🧠 Employee Attrition Prediction & HR Analytics

## 📌 Project Overview

Employee attrition is one of the most critical challenges in HR. High attrition leads to increased hiring costs, productivity loss, and knowledge drain.

This project aims to:

* Predict which employees are likely to leave
* Identify key drivers of attrition
* Provide actionable insights for HR decision-making

---

## 🎯 Problem Statement

Organizations often react to attrition **after employees leave**.
This project builds a **predictive model** to proactively identify at-risk employees and enable early intervention.

---

## 🛠️ Tools & Technologies

* **Python** (Pandas, NumPy, Scikit-learn)
* **Machine Learning** (Logistic Regression, Random Forest)
* **Power BI** (for visualization)
* **SQL** (for data analysis – optional extension)

---

## 📂 Dataset

* Source: IBM HR Analytics Dataset (Kaggle)
* Records: ~1,400 employees
* Target Variable: `Attrition` (Yes/No)

### Key Features:

* Demographics: Age, Gender, Marital Status
* Job Info: Department, Job Role, Years at Company
* Compensation: Monthly Income, Salary Structure
* Behavior: Overtime, Work-Life Balance, Job Satisfaction
* Performance: Performance Rating

---

## 🔍 Data Preprocessing

* Handled missing values using **department-wise median imputation**
* Converted categorical variables using **one-hot encoding**
* Dropped irrelevant columns (EmployeeNumber, Over18, StandardHours)
* Addressed class imbalance using:

  * Class weighting
  * Threshold tuning

---

## 📊 Exploratory Data Analysis (EDA)

Key patterns observed:

* Employees working overtime show higher attrition
* Early tenure employees (0–3 years) are more likely to leave
* Lower income is associated with higher attrition
* Manager stability impacts retention

---

## 🤖 Model Building

### Models Used:

1. Logistic Regression
2. Random Forest Classifier

---

## 📈 Model Performance

### 🔹 Random Forest (Default Threshold)

* Accuracy: 0.85
* Precision: 1.00
* Recall: 0.04 ❌
* ROC-AUC: 0.83

👉 Issue: Model was too conservative and missed most attrition cases

---

### 🔹 Improved Model (Threshold = 0.3)

* Recall: **0.36** ✅
* Precision: **0.85** ✅

👉 Improvement:

* Increased ability to detect at-risk employees
* Maintained strong prediction reliability

---

## 📉 Confusion Matrix (After Optimization)

* True Positives: Increased significantly
* False Negatives: Reduced (critical for HR use case)

---

## 🔑 Key Insights

### 1. 💰 Compensation Matters

* Monthly Income is the strongest predictor
* Lower salary → higher attrition risk

---

### 2. ⏳ Early Tenure Risk

* Employees with fewer years at the company are more likely to leave

---

### 3. 🔥 Overtime = Burnout

* Employees working overtime show significantly higher attrition

---

### 4. 👨‍💼 Manager Stability

* Lower `YearsWithCurrManager` correlates with higher attrition

---

### 5. 🏠 Commute Impact

* Greater distance from home increases likelihood of leaving

---

## 💼 Business Recommendations

* **Reduce Overtime Load**

  * Monitor workload distribution
  * Introduce work-life balance initiatives

* **Compensation Optimization**

  * Identify underpaid employees
  * Adjust salary bands strategically

* **Focus on Early Tenure Employees**

  * Strengthen onboarding
  * Conduct regular engagement check-ins

* **Manager Effectiveness**

  * Improve leadership training
  * Ensure stable reporting structures

* **Target High-Risk Employees**

  * Use prediction scores to prioritize retention efforts

---

## 🚀 Business Impact

This solution enables organizations to:

* Predict employee attrition proactively
* Reduce hiring and replacement costs
* Improve employee retention strategies
* Make data-driven HR decisions

---

## 📁 Project Structure

```
Attrition-Prediction/
│
├── data/
├── notebook.ipynb
├── attrition_predictions.csv
├── README.md
```

## 🙌 Conclusion

This project demonstrates how machine learning can be applied to solve real-world HR problems by combining:

* Data analysis
* Predictive modeling
* Business interpretation

👉 The focus is not just prediction, but **actionable insights that drive retention strategies**.
