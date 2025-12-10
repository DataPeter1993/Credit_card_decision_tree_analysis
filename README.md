# 🏦 Credit Card Decision Tree Data Analysis

## 📖 Project Overview

This project explores and models credit card application data using a Decision Tree algorithm. The goal is to build a predictive model that helps financial institutions make informed decisions on credit card approvals based on applicant information. The project covers the complete data science workflow, from data loading and cleaning to exploratory data analysis (EDA), feature engineering, model training, evaluation, and prediction.

---

## 📚Table of Contents

- [Project Overview](#project-overview)
- [Dataset Description](#dataset-description)
- [Project Workflow](#project-workflow)
- [Requirements](#requirements)
- [How to Run](#how-to-run)
- [Results](#results)
- [License](#license)

---

## 🧩 Dataset Description

- **Dataset:** Credit card application records from 30,000 applicants, including demographic, financial, and repayment information,etc.
- **Features include:**  
    - Age  
    - Marital status  
    - Employment status  
    - Credit score  
    - Education Level
    - Gender
- **Target variable:** Y (sometimes named default.payment.next.month): Credit card approval or default status (1 = approved/good, 0 = not approved/defaulted)

---

## 📋Project Workflow

1. **Data Loading & Initial Exploration:**  
   Import data, check for missing values, and perform basic descriptive statistics.

2. **Data Cleaning:**  
   Handle missing data, outliers, and encode categorical variables as needed.

3. **Exploratory Data Analysis (EDA):**  
   Analyze feature distributions, visualize relationships, and uncover data patterns.

4. **Feature Engineering:**  
   Select, transform, or create new features to improve model performance.

5. **Model Building:**  
   Build a Decision Tree classifier to predict application outcomes.

6. **Hyperparameter Tuning:**  
   Optimize model parameters to achieve better performance.

7. **Model Evaluation:**  
   Assess model accuracy, plot confusion matrix, and review other relevant metrics.

8. **Prediction:**  
   Predict outcomes for new samples and analyze the results.

---
## 📊Exploratory Data Analysis (EDA)

The EDA section explores key distributions and relationships:

1. **Credit Limit Distribution**

A histogram shows:As credit limit increases, the number of clients decreases. Most credit limits concentrate below 500,000.

2. **Gender Distribution**

Using SEX:

1 = Male

2 = Female

The histogram indicates that female clients slightly outnumber male clients.

3. **Education Level Distribution**

EDUCATION is encoded as:

1 = Graduate school

2 = University

3 = High school

4 = Others

5, 6 = Unknown

Most clients have university-level education or above.

4. **Marital Status Distribution**

MARRIAGE is encoded as:

1 = Married

2 = Single

3 = Others

Single and married clients appear relatively balanced in count.

5. **Age Distribution**

A histogram for AGE shows:Most clients fall between 20 and 50 years old. Client base is dominated by working-age adults.

6. **Default Distribution**

The distribution of Y shows: The majority of clients do not default. Around 20–25% of clients default (positive class).

7. **Bill vs. Repayment Amounts**

Scatterplots of (PAY_AMTn, BILL_AMTn) for n = 1…6 illustrate the relationship between:

Monthly bill statements and Corresponding repayment amounts.This helps visualize repayment behavior over time.

8. **Correlation Heatmap**

A correlation heatmap (sns.heatmap(data.corr(), annot=True)) shows:

- Strong correlations among bill amounts across months.

- Strong correlations among repayment amounts across months.

- Clear relationships between past payment status (PAY_0–PAY_6) and the target Y.

9. **Top 10 Correlated Features with Y**

The code selects the 10 features with the highest correlation with Y and visualizes their correlation matrix, focusing on the most influential predictors of default.

10. **Decision Tree**
    <img width="2852" height="566" alt="image" src="https://github.com/user-attachments/assets/b463ab84-30fa-4870-85a1-204f3f481222" />


---
## 🏆 Results

- Decision tree model achieves strong classification accuracy on the test set.

- Key features influencing approval decisions are identified and visualized.

- The project demonstrates a reproducible workflow for similar tabular classification tasks.
