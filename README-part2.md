# CharityML: S-learning P2 

# README.md

## Project: CharityML - Finding Donors for Charity

This project aims to build a supervised machine learning model that can accurately identify individuals who are likely to donate more than $50,000 to CharityML, a fictitious charity organization. The model will help CharityML effectively target potential donors and maximize their fundraising efforts.

### Dataset

The dataset used for this project is the UCI Census Income dataset, which contains information about individuals and their income level. The dataset has 46,000 rows and 13 columns, including features such as age, education level, occupation, capital gains, and more. The target variable is the income class, which is binary and indicates whether an individual earns more than $50,000 or not.

### Data Preprocessing

Before building the model, the data is preprocessed via one-hot encode categorical features, and scalin (log and maxmin norm.) numerical features. 
The dataset is then split into training and testing sets (80/20 split) to train and evaluate the model's performance.

### Model Selection and Evaluation

Three models are evaluated for this task: Logistic Regression, Random Forest Classifier, and Support Vector Classifier - eventually dropped owing to its costs. 
The RF and LR models are optimized using GridSearchCV with 5-fold cross-validation to find the best hyperparameters.

### Results and Conclusion

The final model selected for CharityML is the Random Forest Classifier, as it achieved the highest accuracy (86.17%) and F-score (0.7329) on the testing data. This model outperformed the unoptimized version and the other models, including Logistic Regression.

The final Random Forest Classifier was trained w/ the following hyperparameters: max_depth=None, min_samples_leaf=2, min_samples_split=10, and n_estimators=200.

In addition, feature importance analysis was conducted to identify the five most important features for prediction. 
The performance slightly decreased with an accuracy of 84.28% and an F-score of 0.6881, compared to the full feature set of 13. 
However, this reduction in data significantly reduced the training time, making it a suitable option for real-time applications.

Overall, the optimized Random Forest Classifier model is recommended for CharityML's task of identifying potential donors. It offers a good balance of accuracy, interpretability, and prediction time while effectively identifying individuals likely to donate more than $50,000.
