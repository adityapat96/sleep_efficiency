Machine Learning Predictions for Sleep Efficiency Data Analysis

This project aims to make predictions on a sleep efficiency dataset. After performing data preprocessing techniques, machine learning algorithms were applied for regression and classification tasks. The primary objectives of this project are to determine the levels of sleep that patients are more likely to experience throughout their 8-hour sleep cycle.

Dataset:

The dataset used for this project can be found at: Kaggle Sleep Efficiency Dataset.

The following steps were performed for data preprocessing:

Imputed the Gender column to have 'Male' mapped to 0 and 'Female' mapped to 1.
The Smoking Status column was mapped to have 0 for 'No' and 1 for 'Yes'.
For the 'Awakenings', 'Alcohol consumption', 'Caffeine consumption', and 'Exercise frequency' columns, 'N/A' was replaced with 0 to improve model accuracy in the modified dataset.
REM Sleep Susceptibility Predictions:

A random oversampler was used to enhance resolution and signal-to-noise ratio, preventing phase distortion in the data. The following models were employed:

Logistic Regression
K-Nearest Neighbors
Cross-validation on K-Nearest Neighbors using Stratified K-Folds
Random Forest
Deep Sleep Susceptibility Predictions:

Gradient Boosting
Naive Bayes
Logistic Regression
Cross-validation on Logistic Regression using Repeated K-Folds
Light Sleep Susceptibility Prediction:

Support Vector Machine
Stacking Ensemble
Random Forest
Each model was assessed using a confusion matrix to indicate the number of correct and incorrect predictions per class.

For the Random Forest models, a feature importance analysis was conducted to understand which features in the X data frame are most significant for the model. This can aid in simplifying the models to make them more interpretable.

Results:

REM:
While Logistic Regression and Random Forest achieved higher accuracy scores in the 90th percentile, K-Nearest Neighbors had an accuracy of 85%. To evaluate the effectiveness of K-Nearest Neighbors, cross-validation was performed using Stratified K-Folds, resulting in an accuracy of 83%.

Deep:
The Gradient Boosting and Naive Bayes models achieved high 90s accuracy. However, the Logistic Regression model had an accuracy of 34% for Light Sleep susceptibility. Cross-validation on Logistic Regression using Repeated K-Folds also yielded a 34% accuracy, consistent with the original model.

Light:
In the Support Vector Machine model, the accuracy was considerably lower compared to the other two models (34%). The Stacking Ensemble model achieved a 98% accuracy, while the Random Forest model had a 76% accuracy.

Conclusions:

While most of the models demonstrated better accuracy compared to the rest, it's important to note that model complexities, data imbalances, outliers that may disproportionately affect certain models, and overfitting could be factors at play. Further research is needed to understand hyperparameter tuning, data distribution, and feature engineering.
