# Customer Churn Prediction Using Machine Learning - Individual Project

Machine learning project predicting customer churn using customer behaviour and service data. Includes data preprocessing, exploratory analysis, feature engineering and classification modelling.

---  

## Overview
Customer churn is a major challenge for businesses, particularly in industries such as telecommunications, banking, and subscription services, where retaining existing customers is often more cost-effective than acquiring new ones.

This project aims to develop a machine learning model that predicts whether a customer is likely to leave a service and analyses the factors contributing to churn behaviour.

The project follows a complete data science workflow:
- Data preparation
- Exploratory data analysis
- Feature engineering
- Machine learning modelling
- Model evaluation
- Business insights

## Project Report
A polished, end-to-end report covering data preparation, exploratory analysis, feature engineering, predictive modelling and business recommendations is available below.

- [Customer Churn: End-to-End Data Science Report](https://github.com/rohan-sajeesh/Customer-Churn-Analysis-and-Prediction/blob/main/report/Customer_Churn_Final_Report_Rohan_Sajeesh.pdf)

An earlier report, produced at the end of the exploratory analysis stage before feature engineering and modelling began, is also available for reference.

- [Customer Churn: Exploratory Data Analysis Report](https://github.com/rohan-sajeesh/Customer-Churn-Analysis-and-Prediction/blob/main/report/Customer_Churn_EDA_Report_Rohan_Sajeesh.pdf) *(milestone report — superseded by the Final Report above)*

The accompanying Jupyter notebooks contain the full technical implementation and analysis.

---

## Business Problem

Customer churn directly impacts revenue, customer relationships, and long-term business growth.

The objectives of this project are to:

- Predict customers who are likely to churn.
- Identify important factors influencing customer churn.
- Provide insights that support customer retention strategies.

This project simulates a real-world analytics workflow used by organisations to understand customer behaviour and improve retention outcomes.

---

## Dataset

**Dataset:** Customer Churn Prediction Dataset

**Source** [Kaggle - Customer Churn Prediction Dataset](https://www.kaggle.com/datasets/isandeep06/customer-churn-prediction-dataset-1m)

The dataset contains customer demographic, account, service usage, and behavioural information.

Key features include:

- Customer demographics
- Account information
- Contract details
- Payment methods
- Service usage
- Customer satisfaction metrics
- Complaint history

**Target variable:**

- Churn (Yes/No)

---

## Technologies Used

**Programming**

- Python

**Data Analysis and Visualisation**

- Pandas
- NumPy
- Matplotlib
- Seaborn

**Machine Learning**

- Scikit-learn
- Logistic Regression
- Decision Tree
- Random Forest
- Gradient Boosting
- XGBoost

**Development**

- Jupyter Notebook
- Git/GitHub

---
## Repository Structure

```
Customer-Churn-Analysis-and-Prediction/
│
├── data/
│   └── README.md
│       Dataset information, feature descriptions and preprocessing summary
│
├── notebooks/
│   ├── customer_churn_data_preprocessing.ipynb
│   │   Data cleaning and preprocessing
│   │
│   ├── Customer_Churn_EDA_Notebook_Rohan_Sajeesh.ipynb
│   │   Exploratory data analysis and business insights
│   │
│   ├── Feature Engineering and Machine Learning Modelling (1).ipynb
│   │   Feature engineering, model training, evaluation and interpretation
│   │
│   └── README.md
│       Notebook workflow documentation
│
├── report/
│   ├── Customer_Churn_EDA_Report_Rohan_Sajeesh.pdf
│   │   Exploratory analysis milestone report
│   │
│   ├── Customer_Churn_Final_Report_Rohan_Sajeesh.pdf
│   │   Final end-to-end data science report
│   │
│   └── README.md
│
├── .gitignore
├── LICENSE
└── README.md

```
## Project Workflow

### 1. Data Preparation

Completed:

- Loaded and inspected raw dataset
- Analysed missing values
- Checked for duplicate records
- Converted data types
- Processed categorical variables
- Prepared features for modelling
- Created training and testing datasets

---

### 2. Exploratory Data Analysis

The project investigates relationships between customer characteristics and churn behaviour.

Analysis includes:

- Overall churn distribution
- Customer demographic patterns
- Contract type and churn relationship
- Payment behaviour
- Service usage patterns
- Customer satisfaction factors

Visualisations include:

- Churn distribution plots
- Feature comparisons
- Correlation analysis
- Customer behaviour analysis

---

### 3. Machine Learning Modelling

Five classification models were trained and compared using a stratified 80/20 train-test split.

Models:

| Model               | Purpose / Role                         |
| ------------------- | -------------------------------------- |
| Logistic Regression | Interpretable linear baseline          |
| Decision Tree       | Non-linear rule-based model            |
| Random Forest       | Ensemble learning approach             |
| Gradient Boosting   | Sequential boosted-tree model          |
| XGBoost             | Regularised boosted-tree model         |

Because the dataset was imbalanced, with approximately 9.92% of customers classified as churned, model performance was evaluated using metrics beyond accuracy. 

Evaluation metrics:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC

### Model Performance

| Model               | Accuracy | Precision | Recall | F1-score | ROC-AUC |
| ------------------- | -------- | --------- | ------ | -------- | ------- |
| XGBoost             | 62.76%   | 15.85%    | 63.91% | 25.40%   | 0.6850  |
| Logistic Regression | 62.76%   | 15.86%    | 63.95% | 25.42%   | 0.6849  |
| Gradient Boosting   | 61.30%   | 15.49%    | 65.05% | 25.02%   | 0.6808  |
| Random Forest       | 64.18%   | 15.90%    | 60.86% | 25.21%   | 0.6776  |
| Decision Tree       | 60.67%   | 15.14%    | 64.32% | 24.51%   | 0.6704  |

XGBoost achieved the highest ROC-AUC at **0.6850**, while Gradient Boosting achieved the highest recall at **65.05%**. Logistic Regression performed almost identically to XGBoost, indicating that additional model complexity produced only limited gains with the available feature set.

XGBoost was selected as the final model for interpretation because it achieved the highest ROC-AUC. The model identified contract type, customer satisfaction, complaint history, technical support, service calls, online security, number of services and late payments as the strongest predictors of churn.

---

## Current Progress

This project is complete. All stages of the data science workflow — data preparation, exploratory analysis, feature engineering, predictive modelling, model evaluation, and business recommendations — have been carried out and documented in the accompanying notebooks and reports.

---

## Future Improvements

Potential extensions include:

- Threshold optimisation using retention costs and customer value
- Precision-recall analysis for improved evaluation under class imbalance
- Cross-validation and separate validation data for model selection
- Explainable AI techniques such as SHAP
- Deployment-safe preprocessing using scikit-learn pipelines
- Interaction feature engineering
- Temporal validation and testing on real or independent datasets

---


## Author

**Rohan Sajeesh**

Bachelor of Applied Data Science  
Monash University
