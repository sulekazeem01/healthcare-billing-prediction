# Healthcare Billing Classification Using Python and Logistic Regression

## Project Overview

This project analyzes 900 healthcare billing records to explore patient characteristics associated with high and low billing categories.

Using Python and Logistic Regression, the project develops a classification model to predict whether a patient's billing amount falls above the dataset's median billing amount.

The analysis demonstrates data cleaning, exploratory data analysis, feature preprocessing, predictive modeling, model evaluation, and interpretation.

## Business Objectives

- Explore healthcare billing patterns across patient characteristics.
- Identify relationships between age, gender, medical conditions, insurance providers, and billing categories.
- Prepare healthcare data for machine learning.
- Develop a Logistic Regression classification model.
- Evaluate performance using accuracy, precision, recall, F1-score, and a confusion matrix.
- Compare model performance against a majority-class baseline.
- Communicate findings and potential business applications.

## Tools and Technologies

- **Python:** Data analysis and predictive modeling
- **Pandas and NumPy:** Data cleaning and manipulation
- **Matplotlib and Seaborn:** Data visualization
- **Scikit-learn:** Preprocessing, Logistic Regression, and model evaluation
- **Jupyter Notebook:** Analysis documentation and reporting

## Dataset Description

The analysis uses 900 healthcare billing records retained after removing observations with missing billing amounts.

The selected predictors are:

- Age
- Gender
- Medical Condition
- Insurance Provider

**Target Variable:** `High_Billing`

Patients with billing amounts above the dataset median are classified as High Billing (1), while the remaining patients are classified as Low Billing (0).

The dataset is used for educational and portfolio practice. Findings should not be interpreted as validated real-world hospital billing relationships.

## Data Preparation and Modeling

1. Inspected and cleaned the healthcare dataset.
2. Addressed missing values and prepared relevant variables.
3. Created the binary `High_Billing` target variable.
4. Selected predictors while excluding billing amount to prevent direct target leakage.
5. Split the dataset into 70% training and 30% testing data.
6. Applied median imputation and StandardScaler to Age.
7. Applied categorical imputation and OneHotEncoder to categorical predictors.
8. Trained a Logistic Regression model.
9. Evaluated classification performance and examined model coefficients.

## Model Performance

| Evaluation Metric | Result |
|---|---:|
| Logistic Regression Accuracy | 68.89% |
| Majority-Class Baseline Accuracy | 51.85% |
| Improvement Over Baseline | 17.04 percentage points |
| Training Records | 630 |
| Testing Records | 270 |
| High-Billing Precision | 71% |
| High-Billing Recall | 59% |
| High-Billing F1-Score | 65% |

The Logistic Regression model outperformed the majority-class baseline, although its ability to identify high-billing cases remains limited.

## Key Findings

- The model correctly classified 186 of 270 testing records.
- Cancer, Stroke, and Heart Disease had the largest positive coefficients among the selected encoded features.
- Hypertension and Asthma had negative coefficients relative to their reference category.
- The model identified approximately 59% of actual high-billing cases.
- Coefficients describe associations with predicted log-odds, not causal effects or direct changes in billing amounts.

## Business Recommendations

- Investigate patient characteristics associated with higher billing categories to support further financial analysis.
- Explore relationships between medical conditions, resource utilization, and billing patterns.
- Monitor billing trends and evaluate additional predictors before considering operational applications.

## Model Limitations

- The dataset is intended for educational practice and may not reflect real hospital billing patterns.
- The model achieved moderate accuracy and missed approximately 41% of actual high-billing cases.
- Only four patient characteristics were used as predictors.
- Additional validation using representative real-world data would be necessary before operational deployment.
- The model is not intended for clinical decision-making.

## Conclusion

This project demonstrates an end-to-end machine-learning classification workflow using Python and Scikit-learn.

The Logistic Regression model achieved **68.89% accuracy**, outperforming the majority-class baseline of **51.85%**.

Future improvements could include additional relevant predictors, alternative classification algorithms, and further model validation.

## Project Files

- **Healthcare Billing Classification Using Logistic Regression.ipynb** — Updated Jupyter Notebook containing the analysis, model, evaluation, and visualizations.
- **README.md** — Project overview, methodology, results, and recommendations.
