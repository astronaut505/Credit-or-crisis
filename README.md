
# Credit Score Classification: Credit or Crisis

## Project Overview

The "Credit Score Classification" project was prepared for Machine Learning course assignment and aims to develop a machine learning model to classify credit scores of individuals based on a variety of financial indicators. This project is crucial for understanding creditworthiness, which can impact lending decisions in financial institutions.

## Dataset

The dataset `train.csv` consists of 100,000 records with 28 features, including customer ID, monthly income, number of bank accounts, number of loans, type of loans, credit history, and more. The target variable is `Credit_Score`.

Dataset can be found here:
https://www.kaggle.com/datasets/parisrohan/credit-score-classification/
Further dataset details can also be found there. Dataset there is well-documented.

## Methodology

The project involves several key stages:

1.  **Data Cleaning and Preprocessing:** Focused on handling missing values and ensuring data quality.

2.  **Exploratory Data Analysis (EDA):** Conducted small analysis to understand the distribution and relationship between various financial indicators. Removing outliers, errors and placeholders.

3.  **Feature Engineering:** Dataset was extremely large, having more than enough self explanatory columns, so I decided only add few simple Financial ratios. Further engineered features would double the computational cost for training and feature selection.

4.  **Model building:** Prepared the data for model training and validation by splitting it into appropriate subsets and also balancing the target. Since there were too many outliers, given the nature of data, I decided use tree-based, outlier-resistant models. So I decided to use tree based models. Decision trees, Random Forest Classifier, and LightGBM. Which would also allow me to skip scaling steps.



## Achievements

-   Successfully handled missing and unrealistic data points in the dataset, ensuring robustness and reliability of the models.
-   Conducted comprehensive exploratory analysis, gaining valuable insights into factors influencing credit scores.
-   Employed feature engineering strategies that significantly improved the predictive power of the models.
-   Prepared the dataset effectively for model training and testing, ensuring proper data splitting.
-   Applied advanced techniques like Random Forest and LightGBM classifiers for credit score prediction.


### Performance Metrics


#### Model 1: Logistic Regression

-   **Training Accuracy**: 71.47%
-   **Validation Accuracy**: 71.02%
-   Precision, Recall, F1-Score for each class:
    -   **Good**: Precision - 70%, Recall - 86%, F1-Score - 77%
    -   **Standard**: Precision - 74%, Recall - 68%, F1-Score - 71%
    -   **Poor**: Precision - 69%, Recall - 59%, F1-Score - 64%

#### Model 2: Decision Tree

-   **Training Accuracy**: 88.09%
-   **Validation Accuracy**: 80.54%
-   Precision, Recall, F1-Score for each class:
    -   **Good**: Precision - 81%, Recall - 89%, F1-Score - 85%
    -   **Standard**: Precision - 82%, Recall - 85%, F1-Score - 83%
    -   **Poor**: Precision - 77%, Recall - 66%, F1-Score - 71%

#### Model 3: Random Forest Classifier

-   **Training Accuracy**: 87.16%
-   **Validation Accuracy**: 82.19%
-   Precision, Recall, F1-Score for each class:
    -   **Good**: Precision - 79%, Recall - 92%, F1-Score - 85%
    -   **Standard**: Precision - 85%, Recall - 86%, F1-Score - 85%
    -   **Poor**: Precision - 84%, Recall - 68%, F1-Score - 75%

#### Model 4: LightGBM with SMOTE

-   **Training Accuracy**: 75.38%
-   **Validation Accuracy**: 75.04%
-   Precision, Recall, F1-Score for each class:
    -   **Good**: Precision - 73%, Recall - 88%, F1-Score - 80%
    -   **Standard**: Precision - 76%, Recall - 79%, F1-Score - 78%
    -   **Poor**: Precision - 76%, Recall - 58%, F1-Score - 66%


**The performance metrics reveal distinct strengths and weaknesses for each model.**

-   The Random Forest model shows the best overall performance with the highest validation accuracy and a good balance between precision, recall, and F1-score across all classes. This model appears to be the most suitable for your dataset.
-   The Decision Tree model also performs well, especially in handling the 'Poor' class, but it's slightly inferior to Random Forest in overall accuracy and balance.
-   Logistic Regression and LightGBM offer similar levels of accuracy, but Logistic Regression is simpler and might be preferred if interpretability is a key factor.
-   The LightGBM model, while not outperforming Random Forest or Decision Tree in accuracy, provides a more balanced classification across classes


Our models achieved promising results, but additional feature engineering could potentially enhance their performance, especially reducing the overfitting. The size and complexity of our dataset allowed for the creation of more features. However, we balanced this against the significant computational resources already required, with models taking up to 3 hours to run.

Given these computational constraints, we focused on optimizing existing features rather than extensively expanding them.

## Sumarry

**Considering all metrics, the Random Forest Classifier emerges as the most performing model. Its superior balance in precision, recall, and F1-scores across all classes, coupled with the highest validation accuracy, makes it the most reliable choice for this specific dataset and task.**

It's also important to consider the context of our application: If interpretability is important for the given task, Logistic Regression might be preferred despite its lower performance. If the highest possible accuracy on our validation set is the priority, Random Forest is the best choice.

P.s Notebook takes around 3 hours to run.
