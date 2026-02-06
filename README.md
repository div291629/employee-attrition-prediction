# HR Attrition Analysis and Prediction

## Problem Statement
Employee attrition creates direct hiring costs, productivity loss, and operational disruption.
However, HR teams often lack a structured way to identify which employees are at higher risk of leaving and which factors are realistically actionable.

This project uses historical HR data to address two decision-focused questions:

Which employees are most at risk of attrition?

What controllable factors are contributing to their decision to leave?

The objective is not just prediction, but risk ranking and insight generation to support HR decision-making.

---

## Dataset
IBM HR Analytics Employee Attrition & Performance dataset (Kaggle)  
- 1,470 employee records  
- ~40 HR-related attributes including age, department, income, job satisfaction, overtime, and years at company  

The dataset is largely pre-structured; the focus of this project is on analysis, preprocessing, modeling, and interpretation.

---

## Project Approach

### 1. Data Preprocessing
- Removed non-informative identifiers (e.g., Employee ID)
- Handled missing values using:
  - Median imputation for numerical variables
  - Mode imputation for categorical variables
- Encoded categorical features using one-hot encoding
- Standardized numerical features using StandardScaler to ensure comparable feature scales

### 2. Exploratory Data Analysis (EDA)
- Analyzed attrition distribution and key demographic patterns
- Studied relationships between attrition and variables such as:
  - Overtime
  - Job satisfaction
  - Monthly income
  - Work-life balance
  - Years at company and job role
- Used correlation analysis and visualizations to identify influential factors

### 3. Predictive Modeling
Two machine learning models were built and compared:
- **Logistic Regression** as an interpretable baseline model
- **Random Forest Classifier** to capture non-linear relationships and improve predictive performance

Models were evaluated using:
- Stratified train–test split
- Confusion matrix
- ROC-AUC score

### 4. Model Interpretation
- Logistic Regression coefficients and odds ratios were analyzed to understand the direction and strength of feature impact
- Random Forest feature importance was used to identify the most influential variables
- Employees were ranked by predicted attrition probability to highlight high-risk cases

---

## Power BI Dashboards
Interactive Power BI dashboards were created to support business interpretation and storytelling.  
The dashboards provide insights on:

- Overall attrition rate and employee distribution
- Attrition by department, job role, age group, and tenure
- Impact of overtime, income bands, and work-life balance
- Comparison between employees who left and those who stayed

These dashboards allow HR stakeholders to explore trends without interacting directly with the code.

---

## Key Insights
- Employees working overtime show significantly higher attrition rates
- Lower job satisfaction and lower income levels are strongly associated with attrition
- Attrition varies across departments, job roles, and tenure groups
- Random Forest achieved better predictive performance, while Logistic Regression offered clearer interpretability

---

## How This Can Be Used by HR

- Identify high-risk employees for early intervention
- Focus retention strategies on controllable factors (e.g., overtime, role design)
- Avoid over-reliance on non-actionable attributes such as age

---

## Tech Stack
- Python
- Pandas, NumPy
- Scikit-learn
- Power BI
- Matplotlib
- Jupyter Notebook

---

## Notes
This project is an analytical case study focused on understanding and predicting employee attrition using historical data.  
It is not intended as a deployed production system.
