# Employee Performance Prediction

A machine learning project that analyzes employee data and predicts whether employees meet the KPI threshold of 80%, using exploratory data analysis, preprocessing, feature encoding, scaling, and classification models.

## Project Overview

| Item                    | Details                   |
| ----------------------- | ------------------------- |
| Dataset                 | Employee Performance Data |
| Records                 | 23,490                    |
| Original Features       | 13                        |
| Features After Cleaning | 12                        |
| Target                  | `KPIs_met >80%`           |
| Problem Type            | Binary Classification     |
| Train/Test Split        | 75% / 25%                 |
| Best Model              | LightGBM                  |
| Best Scaler             | StandardScaler            |
| Best Accuracy           | 70.78%                    |

## Objectives

* Analyze employee characteristics and performance patterns.
* Clean and prepare the dataset for machine learning.
* Explore categorical and demographic distributions.
* Predict whether an employee meets the 80% KPI threshold.
* Compare different scaling techniques and classification models.
* Select the best-performing model based on test accuracy.

## Data Preprocessing

* Filled missing `education` values using the mode.
* Filled missing `previous_year_rating` values using the median.
* Removed duplicate records.
* Removed `employee_id` as an identifier with no predictive value.
* Encoded categorical variables using one-hot encoding.
* Used stratified train-test splitting.

## Exploratory Data Analysis

The analysis examined:

* Department distribution
* Gender distribution
* Education levels
* Recruitment channels
* Employee performance-related features

Key observations included department imbalance, uneven gender distribution, skewed education categories, and dominance of a particular recruitment channel.

## Model Comparison

Four scaling techniques were evaluated with three tree-based classification models.

| Model    |   Standard | MinMax | Robust | MaxAbs |
| -------- | ---------: | -----: | -----: | -----: |
| XGBoost  |     69.30% | 69.30% | 69.30% | 69.30% |
| CatBoost |     70.51% | 70.51% | 70.51% | 70.51% |
| LightGBM | **70.78%** | 70.51% | 70.51% | 70.51% |

## Final Model

**LightGBM + StandardScaler**

The combination achieved the highest test accuracy of **70.78%** among the evaluated model-scaler combinations. The project therefore selected LightGBM with StandardScaler as the final model based on the comparison performed.

## Technologies Used

**Python | Pandas | NumPy | Matplotlib | Seaborn | Scikit-learn | XGBoost | CatBoost | LightGBM | Jupyter Notebook**

## Repository Structure

```text
Employee-Performance-Prediction/
├── EDA Ashish Chaudhari.ipynb
├── EDA Model - Ashish Chaudhari.ipynb
├── Model - Ashish Chaudhari.ipynb
└── README.md
```

## Skills Demonstrated

**Data Cleaning | EDA | Feature Engineering | Categorical Encoding | Data Scaling | Binary Classification | Model Evaluation | Model Comparison**

## Outcome

The project demonstrates an end-to-end machine learning workflow for employee performance prediction, from data preparation and exploratory analysis to model comparison and final model selection.
