# Student Loan Default Predictor
## Business Problem
Which US institutions produce borrowers most at risk of student loan repayment failure, and what institutional factors drive that risk?
## Why I Built This
As an international student from Nepal who navigated the US student loan system firsthand, I wanted to understand what data can tell us about repayment risk — and what institutions and lenders should do about it.
## Data
US Department of Education College Scorecard — 4,189 institutions, 9 features, binary classification target
## Tools
Python | pandas | scikit-learn | matplotlib | seaborn | Jupyter
## Results
- Random Forest ROC-AUC: 1.0
- Logistic Regression ROC-AUC: 0.996
- Top predictor: 1-Year Repayment Rate (54% importance)
- 25% of institutions flagged as high repayment risk
## Project Structure
- notebooks/01_data_cleaning.ipynb
- notebooks/02_exploratory_analysis.ipynb
- notebooks/03_model_building.ipynb
- memo/recommendation_memo.md
## Business Recommendation
See memo/recommendation_memo.md for full analysis and recommendations directed to a student loan servicer risk team.
