# Memorandum
TO: Chief Risk Officer, National Education Lending Group
FROM: Harry Acharya, Data Analytics Consultant
DATE: May 18, 2025
RE: Early Intervention Framework for Student Loan Repayment Risk
## Executive Summary
An analysis of 4,189 US institutions using Department of Education College Scorecard data identifies 1,047 institutions (25%) as high repayment risk. A Random Forest model achieved a ROC-AUC of 1.0, indicating that repayment risk is highly predictable from institutional data available at the point of loan origination — before repayment begins.
## Key Findings
- 25% of all analyzed institutions were flagged as high repayment risk
- For-profit institutions show the highest concentration of repayment risk compared to public and private nonprofit schools
- Institutions with higher Pell Grant recipient percentages consistently show lower repayment rates, confirming that low-income student concentration is a strong risk signal
## Model Performance
Two models were tested. Logistic Regression achieved 97% accuracy and ROC-AUC of 0.996. Random Forest achieved 100% accuracy and ROC-AUC of 1.0. Random Forest is the recommended production model due to its superior performance and ability to capture non-linear relationships in the data.
## Top Risk Factors
1. 1-Year Repayment Rate (54% importance) — the single strongest predictor of eventual default risk
2. 3-Year Repayment Rate (30% importance) — confirms that early repayment behavior predicts long-term outcomes
3. Pell Grant Recipient Concentration (7% importance) — high proportion of low-income students correlates with repayment difficulty
## Recommendations
1. Flag borrowers from institutions with 1-year repayment rates below 50% at the point of loan origination, not after repayment begins
2. Apply enhanced monitoring protocols to for-profit institutions, which show disproportionately high risk concentration
3. Deploy the Random Forest model as an early warning system to score all new borrowers at enrollment using publicly available College Scorecard data
## Limitations
This model operates at the institutional level, not the individual borrower level. Individual borrower characteristics such as credit history, family income, and degree completion status are not captured. Additionally, the perfect ROC-AUC score suggests possible data leakage from repayment rate features that are conceptually close to the target variable. Future work should validate this model on individual borrower data and test with features available strictly at loan origination.
