# Advance Bank Term Deposit — Predictive Analysis 📊🤖

A deeper analysis of the Bank Marketing dataset, going beyond initial inspection into **customer demographics, campaign effectiveness, and a logistic regression model** to predict whether a client will subscribe to a term deposit.

## 📁 Repository Structure

```
├── Advance_Bank_Term_Deposit.ipynb   # Main analysis + modeling notebook (with outputs)
├── data.csv                          # Dataset used in the analysis
├── screenshots/                      # Key visualizations from the notebook
│   ├── age_dist.png
│   ├── job_dist.png
│   ├── duration_by_y.png
│   ├── contact_method.png
│   ├── campaign_by_y.png
│   ├── corr_matrix.png
│   ├── confusion_matrix.png
│   └── feature_importance.png
└── README.md
```

## 📌 About the Dataset

The dataset contains **41,188 records** and **21 columns** from a Portuguese bank's telemarketing campaigns — client demographics, campaign contact details, previous campaign outcomes, macroeconomic indicators, and the target `y` (subscribed to a term deposit: yes/no).

> **Note:** This is the `bank-additional-full` version of the UCI Bank Marketing dataset, which does not include an account **balance** column. Where the analysis called for it, **call duration** was used instead as the comparable continuous variable.

## 🔍 What the Notebook Covers

1. **Data loading** — reading the CSV and previewing its structure
2. **Customer demographics** — age distribution and job category breakdown
3. **Balance & deposit trends** — average call duration by subscription outcome (in place of balance)
4. **Campaign effectiveness** — subscription rate by contact method, and number of contacts vs. subscription
5. **Correlation heatmap** — relationships between numerical features
6. **Predictive modeling** — a Logistic Regression model (with class-balanced weighting to handle the imbalanced target) to predict subscription, including a confusion matrix and classification report
7. **Feature importance** — coefficient-based ranking of the strongest predictors

## 📈 Key Findings

- Clients who subscribed had a much **higher average call duration** (~553s) than those who didn't (~221s).
- **Cellular contact** produced a noticeably higher subscription rate than telephone contact.
- Clients who subscribed were, on average, **contacted fewer times** (~2.1) than those who didn't (~2.6) — repeated calling shows diminishing returns.
- Macroeconomic indicators (`emp.var.rate`, `euribor3m`, `nr.employed`, `cons.price.idx`) are **strongly correlated** with each other.
- The logistic regression model reached **~85.7% accuracy**, with **90% recall** on subscribers — useful for a marketing context where catching most likely subscribers matters more than avoiding false positives.
- The strongest predictors of subscription were `euribor3m`, `emp.var.rate`, `nr.employed`, and `duration`.

### Age Distribution
![Age Distribution]https://github.com/kavinirfan/Advance_Bank_Term_Deposit_/blob/main/age_dist.png

### Job Distribution
![Job Distribution]https://github.com/kavinirfan/Advance_Bank_Term_Deposit_/blob/main/job_dist.png

### Call Duration by Subscription
![Duration by Subscription]https://github.com/kavinirfan/Advance_Bank_Term_Deposit_/blob/main/duration_by_y.png

### Subscription Rate by Contact Method
![Contact Method]https://github.com/kavinirfan/Advance_Bank_Term_Deposit_/blob/main/contact_method.png

### Correlation Matrix
![Correlation Matrix]

### Model Confusion Matrix
![Confusion Matrix]

### Feature Importance
![Feature Importance]]

- Python
- Pandas
- Seaborn / Matplotlib
- Scikit-learn (Logistic Regression)
- Jupyter Notebook

## 🚀 How to Run

1. Clone this repository
2. Install dependencies: `pip install pandas seaborn matplotlib scikit-learn`
3. Open `Advance_Bank_Term_Deposit.ipynb` in Jupyter Notebook or Google Colab
4. Run all cells

## 🎯 Next Steps

Future improvements could include trying tree-based models (Random Forest, XGBoost) for comparison, hyperparameter tuning, and applying SMOTE or other resampling techniques to further address class imbalance.

---
*This project was completed as part of a data analysis internship task.*
