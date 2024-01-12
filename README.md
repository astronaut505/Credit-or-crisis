
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

#### Model 3: Decision Tree
-   **Training Set Accuracy:** 88.40%
-   **Validation Set Accuracy:** 79.97%
-   **Precision, Recall, and F1-Score for Each Class on the Validation Set:**
    -   Good: Precision - 82%, Recall - 88%, F1-Score - 85%
    -   Standard: Precision - 80%, Recall - 86%, F1-Score - 83%
    -   Poor: Precision - 77%, Recall - 66%, F1-Score - 71%

#### Model 1: Random Forest Classifier
-   **Training Set Accuracy:** 87.10%
-   **Validation Set Accuracy:** 82.26%
-   **Precision, Recall, and F1-Score for Each Class on the Validation Set:**
    -   Good: Precision - 78%, Recall - 93%, F1-Score - 85%
    -   Standard: Precision - 85%, Recall - 85%, F1-Score - 85%
    -   Poor: Precision - 84%, Recall - 69%, F1-Score - 75%

#### Model 2: LightGBM with SMOTE
-   **Training Set Accuracy:** 75.43%
-   **Validation Set Accuracy:** 74.88%
-   **Precision, Recall, and F1-Score for Each Class on the Validation Set:**
    -   Good: Precision - 73%, Recall - 88%, F1-Score - 80%
    -   Standard: Precision - 76%, Recall - 79%, F1-Score - 78%
    -   Poor: Precision - 76%, Recall - 58%, F1-Score - 66%


###The performance metrics reveal distinct strengths and weaknesses for each model.

-   The Random Forest Classifier demonstrates a strong balance across all classes with the highest validation accuracy of 82.26%, indicating robust generalization. Its precision and recall for the 'Good' class are particularly notable.
-   The LightGBM model, while slightly less accurate overall, shows commendable performance, especially in identifying the 'Good' class, but it struggles more with the 'Poor' class.
-   The Decision Tree has the highest training accuracy but a lower validation accuracy, suggesting some overfitting; however, it performs well in classifying the 'Good' and 'Standard' classes.

**Considering all metrics, the Random Forest Classifier emerges as the most performing model. Its superior balance in precision, recall, and F1-scores across all classes, coupled with the highest validation accuracy, makes it the most reliable choice for this specific dataset and task.**
