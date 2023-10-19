# sleep_efficiency
Machine Learning Predictions for Sleep Efficiency Data Analysis

This project aims to make predictions on a sleep efficiency dataset. After performing data preprocessing techniques, machine learning algorithms were run pertaining to regression and classification. The primary objectives of this project are to determine which level of sleep patients are more likely to experience throughout their 8-hour sleep cycle.

Dataset:

The dataset used for this project can be found at:
https://www.kaggle.com/datasets/equilibriumm/sleep-efficiency

The following steps were performed for data preprocessing:
1. Imputed the Gender column to have Male mapped to 0, and Female mapped to 1.
2. The Smoking Status column was mapped to have 0 equal to No and 1 equal to Yes.
3. For the Awakenings, Alcohol consumption, Caffeine consumption, and Exercise frequency columns, N/A was replaced with 0 for the models to identify a better accuracy in the modified dataset.

REM Sleep Susceptibility Predictions:

A random over sampler was used for this prediction to improve resolution and signal-to-noise ratio. This is extremely helpful in avoiding phase distortion in the data. The following models were run:
1. Logistic Regression
2. K-Nearest Neighbors
3. Cross validation on K-Nearest Neighbors using Stratified K-Folds
4. Random Forest

Deep Sleep Susceptibility Predictions:
1. Gradient Boosting
2. Naive Bayes
3. Logistic Regression
4. Cross validation on Logistic Regression using Repeated K-Folds

Light Sleep Susceptibility Prediction
1. Support Vector Machine
2. Stacking Ensemble
3. Random Forest

Each model was followed with a confusion matrix to show how many predictions are correct and incorrect per class.

For the Random Forest models, a feature importance was conducted to understand which features for the X data frame are most important to the model. It can help with simplifying the models to make them more interpretable.

Results:

REM:
While Logistic Regression and Random Forest have a higher accuracy score (in the 90s percentile), K-Nearest had an accuracy of 85%. To assess the effectiveness of K-Nearest, a cross validation was done using Stratified K-Folds. This cross validation test generated an accuracy 83%.

Deep:
The Gradient Boosting and the Naive Bayes models had a high 90s accuracy. However, the Logistic Regression model calculated a 34% accuracy at the Light Sleep susceptibility. A cross validation on Logistic was done using Repeated K-Folds. This generated a 34% accuracy, same as the original model.

Light:
In the Support Vector Machine model, the accuracy was much lower compared to the other two models run (34%). The Stacking Ensemble model calculated a 98% accuracy while the Random Forest generated a 76% accuracy.

Conclusions:

While most of the models had a better accuracy compared to the rest, it is possible to note that there may be model complexities, imbalance within the data, outliers that can disproportionately affect certain models, and overfitting. Further research would need to be done in understanding hyperparameter tuning, data distribution, and feature engineering.  
