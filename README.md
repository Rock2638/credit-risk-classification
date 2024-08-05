# Credit Risk Analysis Report 
## Overview of the Analysis
* In this Challenge, various techniques to train and evaluate a model based on loan risk were used. A dataset of historical lending activity from a peer-to-peer lending services company was used. Then a model that can identify the creditworthiness of borrowers was built.

* The dataset comprises various features that provide a comprehensive view of a borrower’s financial status and the specifics of the loan. The prediction models utilise these features to classify loans into two categories: healthy or high-risk. This classification helps in understanding the potential risk associated with each loan, thereby assisting in better financial decision-making.

* The 'loan_status` column in the dataset contains two classes: 0 (healthy loans) and 1 (high-risk loans). There are in total 75,036 healthy loans and 2,500 high-risk loans.

* As part of this analysis, the following stages of the machine learning process were completed: 
  - The 'lending_data.csv' data from the 'Resources' folder was read into a Pandas DataFrame.
  - The labels set 'y' from the 'loan_status' column was created, and then the features 'x' DataFrame was created from the remaining columns.
  - The data was split into training and testing datasets by using 'train_test_split'. 
  - The following **models** were considered: ***Linear Regression / Logistic Regression / Decision Tree / Randon Forest***

## Results
**1. Linear Regression Model**:
A linear regression model **would not be suitable** for this analysis because the target variable `loan_status` is categorical, not continuous. Linear regression is typically used for predicting continuous numerical outcomes. In this case, the `loan_status` column indicates categorical classes (0 for healthy loans and 1 for high-risk loans), which is a binary classification problem.

 **2. Logistic Regression Model**
The classification report that was generated summarises the performance of the **logistic regression model** for predicting the two classes: 0 (healthy loan) and 1 (high-risk loan). The high accuracy of 99% indicates that the model handles the data very well. 
#### *Healthy Loan*
-   **Precision**: 1.00 - This means that all the loans predicted as healthy loans are actually healthy loans. 
-   **Recall**: 0.99 - This indicates that 99% of the actual healthy loans are correctly identified as healthy. There is a very small percentage of healthy loans that are incorrectly classified as high-risk.
#### *High-Risk Loan*
-   **Precision**: 0.85 - Out of all the loans predicted as high-risk, 85% are actually high-risk. 
-   **Recall**: 0.91 - 91% of the actual high-risk loans are correctly identified. There is a 9% miss rate where high-risk loans are classified as healthy.

**3. Decision Tree Model**
The classification report that was generated summarises the performance of the **decision tree model** for predicting the two classes: 0 (healthy loan) and 1 (high-risk loan). The high accuracy of 99% indicates that the model handles the data very well. 
#### *Healthy Loan*
-   **Precision**: 1.00 - This means that all the loans predicted as healthy loans are actually healthy loans. 
-   **Recall**: 0.99 - This indicates that 99% of the actual healthy loans are correctly identified as healthy. There is a very small percentage of healthy loans that are incorrectly classified as high-risk.
#### *High-Risk Loan*
-   **Precision**: 0.84 - Out of all the loans predicted as high-risk, 84% are actually high-risk. 
-   **Recall**: 0.85 - 85% of the actual high-risk loans are correctly identified. There is a 15% miss rate where high-risk loans are classified as healthy.

**4. Random Forest model**
The classification report that was generated summarises the performance of the **Random forest model** for predicting the two classes: 0 (healthy loan) and 1 (high-risk loan). The high accuracy of 99% indicates that the model handles the data very well. 
#### *Healthy Loan*
-   **Precision**: 1.00 - This means that all the loans predicted as healthy loans are actually healthy loans. 
-   **Recall**: 0.99 - This indicates that 99% of the actual healthy loans are correctly identified as healthy. There is a very small percentage of healthy loans that are incorrectly classified as high-risk.
#### *High-Risk Loan*
-   **Precision**: 0.85 - Out of all the loans predicted as high-risk, 85% are actually high-risk. 
-   **Recall**: 0.90 - 90% of the actual high-risk loans are correctly identified. There is a 10% miss rate where high-risk loans are classified as healthy.

## Summary
#### 1. Linear Regression Model
Not suitable for this analysis as explained above.

#### 2. Logistic Regression Model
The logistic regression model performs exceptionally well for the healthy loan (0) with perfect precision and very high recall. The model also performs well for the high-risk loan (1) with strong precision and recall, though not as perfectly as for the healthy loans. The high accuracy indicate that the model handles the data well, but there is a slight imbalance in performance between the two classes, with slightly less accuracy in predicting high-risk loans. 

#### 3. Decision Tree Model
The decision tree model performed well overall, particularly in classifying healthy loans with near-perfect precision and recall. While the performance for high-risk loans is good, there is room for improvement, especially if the focus is on minimising financial risks associated with misclassified high-risk loans.

#### 4. Random Forest Model
The random forest model, according to the classification report, demonstrates excellent performance, especially in detecting healthy loans with near-perfect precision and recall, and fairly strong metrics for high-risk loans.  There is still room for improvement, especially if the focus is on minimising financial risks associated with misclassified high-risk loans.

## Recommendations
Based on the classification reports, I would recommend using the **Random Forest** model for this analysis. 
The Random Forest model has shown strong performance:
-   **High accuracy** (0.99)
-   **Excellent precision and recall for both classes**, particularly a high recall of 0.90 for the high-risk loans (1). This is crucial in identifying potential default risks.

Also, Random Forests provide insights into **feature importance**, helping identify which factors most influence the loan status. It provides clarity on which features are driving predictions and enables informed decisions to be made based on the model's output.
