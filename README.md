# Loan-Approval
# Credit Risk Classification Model

## Project Overview
This project aims to develop a robust machine learning model to predict loan default probabilities based on financial, demographic, and credit-related features. Using the Credit Risk Prediction Dataset, the project explores risk factors influencing loan repayment behavior and enhances decision-making in loan approvals.

---

## Data Source
- [Kaggle Dataset](https://www.kaggle.com/datasets/rizqi01/ps4e9-original-data-loan-approval-prediction)

---

## Dataset Description
The dataset contains detailed information to assess credit risk and predict loan defaults.

### Features:
- **person_age**: Age of the individual.
- **person_income**: Annual income in dollars.
- **person_home_ownership**: Type of home ownership (e.g., RENT, OWN).
- **person_emp_length**: Employment length in months.
- **loan_intent**: Loan purpose (e.g., PERSONAL, EDUCATION).
- **loan_grade**: Risk grade assigned (A to D).
- **loan_amnt**: Loan amount requested in dollars.
- **loan_int_rate**: Loan interest rate.
- **loan_status**: Binary indicator of repayment status (0: Repaid, 1: Defaulted).
- **loan_percent_income**: Loan amount as a percentage of income.
- **cb_person_default_on_file**: History of default (Y/N).
- **cb_person_cred_hist_length**: Credit history length in years.

### Dataset Overview:
- **Total Records**: 32,581
- **Missing Values**: Present in `person_emp_length` and `loan_int_rate`.

---

## Project Objectives
1. Identify key factors affecting loan repayment.
2. Build predictive models to classify loans into default or non-default categories.
3. Provide actionable insights for credit risk management.

---

## Exploratory Data Analysis (EDA)
### Key Findings:
- **Feature Distributions**:
  - Loan amounts are concentrated at lower values.
  - Income distribution shows a right skew, with a few high-income outliers.
- **Correlations**:
  - Positive: Age and credit history length (0.86), loan amount and income (0.27).
  - Negative: Income and loan percent income (-0.25).
- **Loan Intent**:
  - Higher loan amounts observed for home improvement and ventures.

### Potential Issues:
- Outliers in `person_income` and `loan_amnt`.
- Missing values in key features.

---

## Machine Learning Pipeline
### Workflow:
1. Data Preprocessing:
   - Handled missing values.
   - Encoded categorical variables.
   - Standardized numerical features.
2. Modeling:
   - Algorithms: Logistic Regression, Decision Tree, Random Forest, Gradient Boosting, Neural Networks.
   - Addressed class imbalance using oversampling.
3. Feature Selection:
   - Techniques: Recursive Feature Elimination (RFE), SelectKBest.

### Model Performance:
- Evaluated models using accuracy, precision, recall, and F1-score.
- Best performance achieved with Random Forest after hyperparameter tuning.

---

## Insights
1. Homeowners and mortgage holders tend to receive higher loan amounts than renters.
2. Debt consolidation and home improvement loans are associated with higher amounts.
3. Strong correlation between age and credit history length highlights the importance of credit experience.

---

## Limitations & Future Work
### Limitations:
- Outliers may affect model performance.
- Limited exploration of advanced sampling techniques.

### Future Enhancements:
1. Implement advanced feature engineering techniques.
2. Add cross-validation for robust model evaluation.
3. Develop a monitoring system to track model performance over time.
4. Enhance the pipeline with detailed logging and error handling.

---

## Deployment Considerations
- Create an API for real-time predictions.
- Set up a retraining schedule to adapt to new data.
- Monitor feature drift and update models accordingly.

---

## Conclusion
This project successfully implemented a comprehensive machine learning pipeline for credit risk classification. With modular design, robust preprocessing, and high-performing models, the solution provides actionable insights and supports effective risk management. Further enhancements can make the system scalable and adaptable for real-world applications.
