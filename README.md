# Employee Attrition Prediction using Machine Learning

## Overview

Employee attrition is a major challenge for organizations because losing skilled employees results in increased recruitment costs, training expenses, productivity loss, and operational disruption.

This project develops a Machine Learning-based Employee Attrition Prediction System using the IBM HR Analytics Dataset. The objective is to identify employees who are likely to leave the organization and uncover the key factors driving employee turnover.

The project combines data analysis, visualization, machine learning, and business intelligence techniques to generate actionable HR insights.

---

## Project Objectives

* Analyze employee attrition patterns.
* Identify factors influencing employee turnover.
* Perform exploratory data analysis (EDA).
* Build predictive machine learning models.
* Compare model performance.
* Determine the most important attrition drivers.
* Generate actionable HR recommendations.

---

## Dataset Information

Dataset: IBM HR Analytics Employee Attrition Dataset

Source:
https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset

### Dataset Statistics

| Metric            | Value     |
| ----------------- | --------- |
| Total Records     | 1470      |
| Features          | 35        |
| Missing Values    | 0         |
| Duplicate Records | 0         |
| Target Variable   | Attrition |
| Attrition Rate    | 16.12%    |

---

## Business Problem

Employee attrition negatively impacts organizational performance through:

* Recruitment costs
* Training expenses
* Knowledge loss
* Productivity reduction
* Workforce instability

By predicting attrition before employees leave, HR teams can implement proactive retention strategies and improve workforce stability.

---

## Exploratory Data Analysis

The following analyses were performed:

### Department Analysis

| Department             | Attrition Rate |
| ---------------------- | -------------- |
| Sales                  | 20.63%         |
| Human Resources        | 19.05%         |
| Research & Development | 13.84%         |

### Job Role Analysis

Highest attrition rates:

| Job Role              | Attrition Rate |
| --------------------- | -------------- |
| Sales Representative  | 39.76%         |
| Laboratory Technician | 23.94%         |
| Human Resources       | 23.08%         |

### Overtime Analysis

| Overtime Status | Attrition Rate |
| --------------- | -------------- |
| No              | 10.44%         |
| Yes             | 30.53%         |

Employees working overtime were nearly three times more likely to leave the organization.

### Work-Life Balance Analysis

Employees with poor work-life balance exhibited significantly higher attrition rates compared to employees reporting better work-life balance.

---

## Data Preprocessing

The following preprocessing steps were performed:

* Removed EmployeeCount column
* Removed Over18 column
* Removed StandardHours column
* Removed EmployeeNumber column
* Encoded Attrition target variable
* Applied One-Hot Encoding to categorical variables
* Performed train-test split (80:20)
* Applied StandardScaler for Logistic Regression

---

## Machine Learning Models

Three classification algorithms were developed and evaluated:

### Logistic Regression

Advantages:

* Highly interpretable
* Strong recall performance
* Suitable for HR decision-making

### Random Forest Classifier

Advantages:

* Handles non-linear relationships
* Robust ensemble method
* Good overall accuracy

### Gradient Boosting Classifier

Advantages:

* Strong predictive performance
* Handles complex patterns
* Best overall model in this project

---

## Model Performance

| Model               | Accuracy | Precision | Recall | ROC-AUC |
| ------------------- | -------- | --------- | ------ | ------- |
| Logistic Regression | 0.75     | 0.35      | 0.62   | 0.798   |
| Random Forest       | 0.84     | 0.57      | 0.09   | 0.781   |
| Gradient Boosting   | 0.85     | 0.59      | 0.21   | 0.804   |

### Best Model

Gradient Boosting achieved the highest overall predictive performance with:

* Accuracy: 85%
* ROC-AUC: 0.804

---

## Top Factors Driving Attrition

Feature Importance Analysis identified the following key drivers:

1. Monthly Income
2. Age
3. Total Working Years
4. OverTime
5. Number of Companies Worked
6. Stock Option Level
7. Years With Current Manager
8. Daily Rate
9. Environment Satisfaction
10. Job Involvement

---

## Key Business Insights

### Finding 1

Sales Department recorded the highest attrition rate among all departments.

### Finding 2

Sales Representatives experienced the highest employee turnover rate.

### Finding 3

Overtime emerged as one of the strongest predictors of attrition.

### Finding 4

Lower-income employees demonstrated higher attrition tendencies.

### Finding 5

Employees with lower tenure showed increased attrition risk.

---

## HR Recommendations

### Recommendation 1

Reduce excessive overtime through workload balancing and workforce planning.

### Recommendation 2

Prioritize retention initiatives for Sales Representatives and Sales teams.

### Recommendation 3

Improve compensation competitiveness for high-risk employee groups.

### Recommendation 4

Strengthen employee engagement and satisfaction programs.

### Recommendation 5

Provide mentoring and career development opportunities for early-career employees.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-Learn
* Jupyter Notebook

---

## Project Structure

```text
EmployeeAttrition_PALAKURTHI_VENKATESH_GOUD
│
├── analysis.ipynb
├── HR_Attrition.csv
├── summary.pdf
├── README.md
│
├── charts/
│   ├── attrition_by_department.png
│   ├── overtime_attrition.png
│   ├── model_comparison.png
│   ├── confusion_matrix.png
│   ├── roc_curve.png
│   ├── top10_feature_importance.png
│
└── reports/
```

---

## Conclusion

This project successfully developed an Employee Attrition Prediction System capable of identifying employees at risk of leaving the organization.

The analysis revealed that compensation, overtime, experience, satisfaction, and career progression factors significantly influence employee attrition.

The findings provide actionable insights that HR departments can use to improve retention, reduce turnover costs, and support long-term workforce planning.
