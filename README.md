# CropYieldPrediction
This project aims to design, develop and implement the training model by using different inputs data. The machine will able to learn the features and extract the crop yield from the data by using data mining and data science techniques.

Algorithms used in this project:
1. Gradient Boosting Regression, validated by 5 Folds Cross Validation (for crop yield prediction)
Gradient boosting is a machine learning technique for regression and classification problems, which produces a prediction model in the form of an ensemble of weak prediction models, typically decision trees.

2. Multi-variate Regression (for Fertilizer Recommendation)
Multivariate Regression is a method used to measure the degree at which more than one independent variable (predictors) and more than one dependent variable (responses), are linearly related.

References to Dataset (column wise):
1. State - Name of the 14 states in USA
2. Year - Data from 1964-2017 (Historical occurences and records)
3. _Name of Fertilizer_ (%) - Acreage receiving the particular fertilizer
4. _Name of Fertilizer_ (Pounds/Acre) - Amount of the fertilizer being given to that acreage
5. Area Planted - As mentioned
6. Harvested Area - As mentioned
7. Lint Yield - Yield of the cotton crop

# Data pre-processing
1. As part of pre-processing, the missing values were replaced with the mean values. Further to increase accuracy, the values were later replaced with the mean values of that feature, corresponding to the state; since states were showing varied values that weren’t in correlation with each other. 
2. Unique values of States have been noted and were mapped to corresponding integral values, to get a dataset that was capable to be trained on the regression model used. 
3. Pearson’s correlation used to check for redundant features. Fortunately, all the features show a value greater than |0.2| which shows a medium-high relation between the features and the target variable (Lint Yield)

# Key Metrics
Accuracy of 90.1% for Test set and 98% for Train set (no case of underfit/overfit). Still to rule out the possibility, 5 Folds Cross Validation is being used to re-check the accuracy score. After validation, 82.5% is accuracy.
1. MAE=  71.42171078565305
2. MSE=  9318.895794593871
3. R2 value=  0.9072612517186169
4. Adjusted R2 value=  0.906016436305444
5. RMSE (train)=  44.51231769473379
6. RMSE (test)=  96.53442802748599
