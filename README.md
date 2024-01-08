
# Credit Score Classification

## Project Overview

The "Credit Score Classification" project aims to develop a machine learning model to classify credit scores of individuals based on a variety of financial indicators. This project is crucial for understanding creditworthiness, which can impact lending decisions in financial institutions. 

## Dataset

The dataset `train.csv` consists of 100,000 records with 28 features, including customer ID, monthly income, number of bank accounts, number of loans, type of loans, credit history, and more. The target variable is `Credit_Score`.

Dataset can be found here:
https://www.kaggle.com/datasets/parisrohan/credit-score-classification/

## Methodology

The project involves several key stages:

1.  **Data Cleaning and Preprocessing:** Focused on handling missing values and ensuring data quality. 
    
2.  **Exploratory Data Analysis (EDA):** Conducted small analysis to understand the distribution and relationship between various financial indicators. Removing outliers, errors and placeholders.
    
3.  **Feature Engineering:** Dataset was extremely large, having more than enough self explanatory columns, so I decided only add few Financial ratios. 
    
4.  **Model building:** Prepared the data for model training and validation by splitting it into appropriate subsets. Since there were too many outliers, given the nature of data, I decided use tree-based, outlier-resistant models. So I decided to use Random Forest Classifier, and LightGBM. Which these also allowed me to skip scaling steps.
    


## Achievements

-   Successfully handled missing and unrealistic data points in the dataset, ensuring robustness and reliability of the models.
-   Conducted comprehensive exploratory analysis, gaining valuable insights into factors influencing credit scores.
-   Employed feature engineering strategies that significantly improved the predictive power of the models.
-   Prepared the dataset effectively for model training and testing, ensuring proper data splitting.
-   Applied advanced techniques like Random Forest and LightGBM classifiers for credit score prediction.

## Performance Metrics

### Model 1: Random Forest Classifier

-   **Training Set Accuracy**: 86.86%
-   **Validation Set Accuracy**: 79.18%
-   **Cross-validation Score (Mean)**: 78.46%
-   Precision, Recall, and F1-score for each class (Good, Poor, Standard) on the Validation Set:
    -   **Good**: Precision - 72%, Recall - 76%, F1-Score - 74%
    -   **Poor**: Precision - 78%, Recall - 80%, F1-Score - 79%
    -   **Standard**: Precision - 82%, Recall - 80%, F1-Score - 81%

### Model 2: LightGBM with SMOTE

-   **Training Set Accuracy**: 75.83%
-   **Validation Set Accuracy**: 75.74%
-   **Macro Average Metrics** on the Validation Set:
    -   **Precision**: 75.99%
    -   **Recall**: 75.71%
    -   **F1 Score**: 75.27%
-   Precision, Recall, and F1-score for each class (Good, Poor, Standard) on the Validation Set:
    -   **Good**: Precision - 74%, Recall - 88%, F1-Score - 80%
    -   **Poor**: Precision - 77%, Recall - 79%, F1-Score - 78%
    -   **Standard**: Precision - 77%, Recall - 60%, F1-Score - 68%

These metrics indicate a strong performance by both models, with the Random Forest Classifier showing slightly better accuracy and balance across precision, recall, and F1-score compared to the LightGBM model.
