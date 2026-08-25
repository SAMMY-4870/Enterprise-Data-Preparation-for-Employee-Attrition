# Enterprise-Data-Preparation-for-Employee-Attrition


## Project Overview

This project focuses on preparing and preprocessing an HR employee dataset for employee attrition analysis.

The project performs data cleaning, duplicate handling, outlier detection, feature engineering, categorical encoding, numerical scaling, and preprocessing pipeline creation.

## Dataset

The dataset contains **5,000 employee records and 22 columns**.

The target variable is:

- `LeftCompany`

The dataset contains employee-related information such as salary, age, department, designation, education, overtime, leaves taken, training hours, distance from home, and years with the company.

## Project Activities

The following activities were performed:

1. Import HR dataset
2. Clean missing values
3. Handle duplicate records
4. Detect and handle outliers using the IQR method
5. Encode categorical variables using One-Hot Encoding
6. Scale numerical variables using StandardScaler
7. Create derived HR features
8. Create a preprocessing pipeline using Pipeline and ColumnTransformer
9. Export the processed dataset

## Feature Engineering

The following derived features were created:

- `AnnualSalary`
- `SalaryPerYearExperience`
- `LeaveRate`
- `TrainingIntensity`
- `LongDistanceEmployee`
- `OvertimeFlag`
- `JoiningYear`
- `JoiningMonth`

These features provide additional information that can be useful for employee attrition analysis.

## Data Preprocessing

### Numerical Data

Numerical variables were processed using:

- Median imputation
- StandardScaler

### Categorical Data

Categorical variables were processed using:

- Most-frequent imputation
- One-Hot Encoding

### Outlier Handling

Outliers were detected using the **Interquartile Range (IQR)** method and handled using value capping.

## Preprocessing Pipeline

A Scikit-learn preprocessing pipeline was created using:

- `Pipeline`
- `ColumnTransformer`
- `SimpleImputer`
- `StandardScaler`
- `OneHotEncoder`

This provides a consistent and reproducible preprocessing workflow.

## Project Structure

```text
Enterprise_Data_Preparation_Employee_Attrition/
│
├── README.md
├── requirements.txt
├── Enterprise_Data_Preparation_Employee_Attrition.ipynb
│
├── data/
│   └── employee_attrition_raw.csv
│
├── outputs/
│   ├── clean_employee_attrition_dataset.csv
│   └── processed_employee_attrition_dataset.csv
│
└── reports/
    ├── data_cleaning_report.md
    ├── feature_engineering_report.md
    └── pipeline_documentation.md
