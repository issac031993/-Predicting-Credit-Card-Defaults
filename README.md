# 🏦 Predicting Credit Card Defaults: A Supervised Learning Approach

👋 **Hi, I'm Issac Abraham.**  
This project was independently designed and executed by me as a capstone, applying machine learning to tackle a real-world financial risk problem.

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
![Age Histogram](images/histogram_age.png)
![Default Status Histogram](images/histogram_default.png)
![Correlation Heatmap](images/correlation_heatmap.png)
![Boxplot Recovery Debt](images/boxplot_recovery.png)
![ROC Curve](images/roc_curve.png)

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
