# -Predicting-Credit-Card-Defaults
Built and evaluated supervised learning models (Random Forest, Logistic Regression, SVM) to predict loan defaults, with a focus on minimizing false negatives. Recommended ensemble-based Random Forest for robust, high-recall performance in credit risk modeling.
# 📊 Predicting Credit Card Defaults

## 🔍 Project Overview
This project explores predictive modelling techniques to forecast system resource usage (or financial risk / defaults in your adjusted case).
We built and compared multiple supervised learning models (Random Forest, Logistic Regression, SVM) to minimize **false negatives**, a key metric in credit risk prediction.

The final recommended model was an **ensemble-based Random Forest**, chosen for its robust, high-recall performance.

---

## 🗂️ Dataset
- **Source:** Historical system activity dataset (or financial transaction dataset if renamed for credit card defaults).
- **Records:** ~8,192 rows, 23 columns
- **Target Variable:**  
  - `usr`: Portion of time (%) CPUs run in user mode *(analogous to default flag for financial dataset)*

**Features included:**
- Reads, writes, system calls
- Page ins, page outs
- Memory and swap metrics
- Process run queue size, free memory, etc.

---

## 🚀 Process & Methodology
- **Data Preprocessing:**
  - Imputed missing values (mean strategy).
  - Removed duplicates.
  - Handled outliers via boxplots & IQR filtering.

- **Exploratory Data Analysis:**
  - Generated correlation matrices & heatmaps.
  - Created pairplots to inspect feature relationships.

- **Feature Engineering:**
  - One-hot encoded categorical variables.
  - Calculated Variance Inflation Factors (VIF) to handle multicollinearity.

- **Modeling:**
  - Built multiple linear regression models, iteratively removing high-VIF variables.
  - Compared adjusted R² and RMSE across models.
  - Evaluated on a 70:30 train-test split.

---

## 🏆 Results & Insights
- **Best Model:** Initial OLS regression with all features  
  - Adjusted R²: **0.793**  
  - RMSE: **4.45 (train)**, **4.66 (test)**
- Dropping high-VIF features reduced performance, highlighting their predictive contribution.
- Key influential features included:
  - `lread`, `lwrite`, `scall`, `sread` — strongly linked to CPU user mode.

**Business Implications:**
- Even a simpler model captured ~79% of variance, enabling resource allocation planning and potential cost savings.

---

## 📈 Sample Visualizations

![Correlation Heatmap](images/correlation_heatmap.png)
*Example: Heatmap showing feature correlations*

![Pair Plot](images/pairplot.png)
*Example: Pairplot of selected features*

![Regression Results](images/regression_plot.png)
*Example: Regression fit plot showing model predictions vs actuals*

---

## 🛠️ Tech Stack
- **Python**: pandas, numpy, seaborn, matplotlib, scikit-learn, statsmodels
- **Jupyter Notebooks** for experimentation
- **Excel** for raw data storage

---

## ⚙️ How to Run
1. Clone the repo:
   ```
   git clone https://github.com/yourusername/Predicting-Credit-Card-Defaults.git
   cd Predicting-Credit-Card-Defaults
   ```
2. Install dependencies (you can create `requirements.txt`):
   ```
   pip install -r requirements.txt
   ```
3. Open and run the notebook:
   ```
   jupyter notebook analysis.ipynb
   ```

---

## 💡 Future Work
- Explore ensemble techniques like Gradient Boosting or XGBoost for potentially higher recall.
- Implement hyperparameter tuning (GridSearchCV) to improve model generalization.
