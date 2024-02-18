# Predictive Modeling for Multiclass Obesity Risk
## PROJECT GOALS
- Develop a predictive model aimed at identifying obesity risk across multiple classes with high accuracy.
- Ensure the model achieves a high level of accuracy in identifying obesity risk on a multi-class level.

## Data Information
- Dataset Source from Kaggle : Multi-Class Prediction of Obesity Risk
- The Train Dataset ('train.csv') consists of 18 columns and 20758 rows of data.
- The Test Dataset ('test.csv') consists of 17 columns and 13840 rows of data.
- There are no null values or duplicate data in the dataset.

## Data Pre-processing
As null values and duplicates were not found, and the dataset has been pre-normalized, preprocessing entails feature encoding. 
Binary columns utilize label encoding, while others employ one-hot encoding, and for the target column, mapping is conducted.

## Modeling
I have employed various algorithms including Decision Tree, Random Forest, AdaBoost, Gradient Boosting, XGBoost, CatBoost, and LGBM. 
After thorough evaluation based on accuracy rates and ROC-AUC scores, I've identified LGBM as the top-performing algorithms. 
Consequently, these algorithms will undergo a hyperparameter tuning process to determine the optimal parameters.

## Predictions on Data Test
I proceeded to perform predictions on the 'test.csv' data using the pre-tuned LGBM model. The structure of the columns in the 'test.csv' data 
is identical to that of the 'train.csv' data,except that it lacks the target variable ("Nobeyesdad").
The pre-processing steps used for the 'test.csv' data are the same as those used for the 'train.csv' data.

## Conclusion
With a high ROC AUC (0.99) on both testing and training data, as well as relatively stable accuracy (0.97 on training data and 0.91 on testing data), 
it can be concluded that the model exhibits excellent predictive capability for the target classes in the testing data. A ROC AUC approaching 1 indicates the model's 
outstanding ability to distinguish between positive and negative classes. 

Despite a slight decrease in accuracy from the training to testing data, this difference remains small and can be considered a sign of the model's strong 
generalization ability on previously unseen data. Therefore, the conclusion drawn is that the model demonstrates exceptional performance in predicting 
the target classes in the multiclass dataset.













