# 🏦 Predicting Credit Card Defaults: A Supervised Learning Approach for Risk Assessment and Management

This project develops and evaluates predictive models for credit card defaults, with a focus on achieving **high recall** to minimize false negatives — critical for effective risk management.  
Models explored include **Logistic Regression, Random Forest, SVM, and LDA**. The **Random Forest model demonstrated perfect initial performance**, and boosted & bagged ensembles were also assessed to ensure robustness.  
Final recommendations include adopting Random Forest, implementing regular monitoring, exploring ensemble methods for additional resilience, and balancing model interpretability to support informed decision-making. This ultimately helps enhance **operational efficiency and financial stability**.

---

## 🚀 Skills & Tools Covered
- 🔥 **Random Forest**, Logistic Regression, SVM, LDA
- 📊 **Classification & Ensemble Techniques**
- 🧠 **Machine Learning**
- 🕵️ **Exploratory Data Analysis (EDA)**
- 🐍 Python (pandas, numpy, seaborn, matplotlib, scikit-learn)

---


---
## 🔍 Project Overview
Credit card companies face substantial risk from customer defaults. This project builds predictive models to identify customers likely to default, enabling proactive risk management and protecting financial stability.

---

## 🗂️ Dataset Highlights
- **Rows:** ~100,000 customers
- **Columns:** 36 features including account activity, repayment patterns, merchant categories, and age.
- **Target:** `default` (1 = defaulted, 0 = did not default).

The dataset was highly imbalanced (88,688 non-default vs. 1,288 default), so careful upsampling was used to balance classes for effective learning.

---

## 🚀 Exploratory Data Analysis & Preprocessing
✅ Dropped irrelevant columns (`userid`, `name_in_email`, `time_hours`) to streamline the model.  
✅ Handled missing values by removal or imputation to ensure data integrity.  
✅ Used MinMaxScaler to normalize numerical features.  
✅ Label encoded categorical variables.

### 📊 Key Visuals from EDA
![Histogram of Age vs Frequency](https://github.com/user-attachments/assets/895fcf45-2273-4361-be05-fc0ee260d844)
![Histogram of Default vs Not Default Status](https://github.com/user-attachments/assets/7da54b9b-2dcc-4fed-9163-bdf220998775)
![Correlation Heatmap](https://github.com/user-attachments/assets/101f1d19-6084-4d43-8e51-f461b3850485)
![Stacked bar chart of Merchant group vs Default Status](https://github.com/user-attachments/assets/7649a902-f267-4d52-9899-db72197f42d7)
![Boxplot of Recovery Debt vs Default Status](https://github.com/user-attachments/assets/aa648681-ae98-48bd-9b50-918d62450b06)

Business insight: Features like **`acct_days_in_rem_12_24m`**, `recovery_debt`, and account activity status had strong influence on defaults.

---

## 🧠 Machine Learning Models & Results
Focused on **maximizing recall** to minimize false negatives (missing potential defaulters).

| Model                          | Accuracy | Precision | Recall | F1-Score |
|---------------------------------|----------|-----------|--------|----------|
| Logistic Regression             | 98.97%   | 1.00/0.98 | 0.98/1.00 | 0.99 |
| Random Forest                   | 100%     | 1.00      | 1.00   | 1.00 |
| SVM                             | 95.68%   | 1.00/0.92 | 0.91/1.00 | 0.96 |
| LDA                             | 96.76%   | 1.00/0.94 | 0.93/1.00 | 0.97 |
| **Boosted Logistic Regression** | 99.95%   | 1.00      | 1.00   | 1.00 |
| **Tuned Random Forest**         | 100%     | 1.00      | 1.00   | 1.00 |

✅ **Best model:** Tuned Random Forest (via GridSearchCV) achieved **perfect classification on test data**, catching **all defaults (recall = 1.0)** — critical for financial risk management.
![Confusion matrix for the Best Model](https://github.com/user-attachments/assets/d29e30a2-9f25-49c4-9c0b-ff1f2102b19c)
![Roc Curve for the best model(Tuned Random forest)](https://github.com/user-attachments/assets/ad420a61-3dfe-4b67-afa6-2df13154e297)

---

## 💼 Business Value & Recommendations
- Helps credit card companies **identify high-risk customers early**, reducing losses.
- Allows **dynamic credit limits & tailored financial guidance** for at-risk customers.
- Builds **trust in the financial ecosystem** by promoting responsible lending.

---

## ⚙️ How to Run
📌 This repository includes Jupyter notebooks with the complete workflow.
- Clone the repo, install the packages (`pip install -r requirements.txt`), and explore the notebooks.

---

## 🛠️ Tech Stack
- **Python:** pandas, numpy, seaborn, matplotlib, scikit-learn
- **Jupyter Notebook** for iterative data science workflows

---

## 🤝 About Me
I completed this project entirely on my own, showcasing my ability to handle everything from data wrangling and EDA to advanced machine learning tuning and interpretation.

🔗 [LinkedIn](https://linkedin.com/in/yourprofile)

---

✅ **Thank you for checking out my project!**
