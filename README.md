# Lending Club Loan Charge-Off Prediction

## Project Overview

This project applies supervised machine learning to Lending Club loan data to investigate the financial and credit characteristics associated with loan charge-offs. Using Python, the analysis incorporates data cleaning, exploratory data analysis, decision tree classification, and random forest modeling to evaluate loan outcomes.

The primary objective is to determine how effectively machine learning algorithms can identify charged-off loans and assess the influence of class imbalance on predictive performance.

## Research Objectives

- Examine relationships between borrower characteristics and loan outcomes.
- Identify patterns in credit scores, annual income, debt-to-income ratios, and credit history.
- Develop decision tree and random forest classification models.
- Evaluate model performance using accuracy, precision, and recall.
- Investigate how class imbalance affects the identification of charged-off loans.

## Dataset

**Dataset:** `lending_club.csv`

The dataset contains approximately 104,858 loan records with financial and credit-related information.

Key variables include:

- Annual income
- Debt-to-income ratio
- Credit score ranges
- Credit inquiries
- Previous delinquencies
- Revolving credit balances
- Revolving credit utilization
- Total credit accounts
- Loan status

A binary target variable, `charge_off`, was created to distinguish charged-off loans from other recorded loan statuses.

## Methodology

### 1. Data Cleaning and Preparation

The dataset was imported into Python using pandas. Data preparation included reviewing missing values, standardizing column names, and applying median imputation to selected numerical variables.

### 2. Exploratory Data Analysis (EDA)

Descriptive statistics, correlation matrices, and heatmaps were used to investigate relationships among financial variables.

The analysis examined the distribution of loan outcomes and identified a class imbalance between charged-off and non-charged-off loans.

### 3. Decision Tree Classification

A decision tree classifier was developed using a maximum tree depth of four.

The dataset was divided into 60% training and 40% validation samples.

Decision trees were used to evaluate how borrower characteristics contributed to loan classification.

### 4. Random Forest Classification

A random forest model consisting of four decision trees was developed to classify loan outcomes.

The model was evaluated using accuracy, precision, and recall to assess its overall performance and its ability to identify charged-off loans.

## Model Performance

The notebook's written results reported the following random forest performance:

| Evaluation Metric | Result |
|---|---|
| Accuracy | 87% |
| Precision | 18% |
| Recall | 2% |

### Interpretation

Although the random forest achieved 87% accuracy, its recall of 2% indicated that it correctly identified only a small percentage of charged-off loans.

Approximately 12.26% of the dataset consisted of charged-off loans, creating a class imbalance that affected the model's performance.

These findings demonstrate that high classification accuracy does not necessarily indicate strong predictive performance when the primary objective is identifying a minority class.

The reported metrics should be verified by rerunning the notebook.

## Key Findings

1. Borrower financial and credit characteristics provide a foundation for analyzing loan outcomes.
2. Class imbalance significantly affects the interpretation of classification accuracy.
3. Decision trees offer an interpretable method for examining loan classification.
4. Random forest classification can achieve relatively high accuracy while failing to identify most charged-off loans.
5. Precision and recall are essential measures when evaluating models designed to identify financial risk.

## Technologies Used

- **Python:** Data processing and predictive modeling
- **Jupyter Notebook:** Interactive analysis and documentation
- **pandas:** Data cleaning and manipulation
- **NumPy:** Numerical operations
- **Matplotlib:** Data visualization
- **seaborn:** Correlation heatmaps
- **scikit-learn:** Decision trees, random forests, and model evaluation
- **dmba:** Data mining utilities

## Conclusion

This project demonstrates the application of supervised machine learning to credit risk analysis using historical Lending Club loan data.

The results highlight the importance of evaluating classification models beyond overall accuracy, particularly when identifying relatively uncommon financial outcomes.

Although the random forest achieved high overall accuracy, its low recall demonstrated substantial limitations in identifying charged-off loans.

The project emphasizes the importance of data preparation, model selection, and appropriate performance metrics when developing predictive models for financial decision-making.

## Limitations and Future Improvements

- The dataset contains historical loan information and may not represent current lending conditions.
- Class imbalance limits the model's ability to identify charged-off loans.
- The binary outcome represents recorded charge-offs rather than confirmed future defaults.
- Model performance requires additional validation before operational use.
- Future improvements could include class weighting, hyperparameter tuning, alternative classification thresholds, and cross-validation.
- Additional model evaluation could incorporate ROC-AUC, precision-recall curves, and confusion matrices.

## Repository Contents

- `loan_chargeoff_classification.ipynb` — Python analysis and machine learning models
- `lending_club.csv` — Lending Club loan dataset, subject to redistribution permissions
- `README.md` — Project documentation

## How to Run

1. Download or clone this repository.
2. Install Python and Jupyter Notebook.
3. Install the required Python libraries: pandas, NumPy, Matplotlib, seaborn, scikit-learn, and dmba.
4. Place `lending_club.csv` in the same directory as the Jupyter notebook.
5. Open `loan_chargeoff_classification.ipynb`.
6. Execute the notebook cells in sequence to reproduce the analysis.

**Note:** The original assignment notebook requires minor code formatting and column-name corrections before it can run successfully from beginning to end.

## Academic Context

Developed as part of ANA615 graduate-level Data Science coursework, emphasizing exploratory data analysis, supervised machine learning, decision tree classification, random forests, and predictive model evaluation.
