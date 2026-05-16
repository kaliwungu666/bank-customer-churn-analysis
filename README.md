Bank Customer Churn Prediction Using Machine Learning
Project Overview

This project aims to analyze and predict customer churn in the banking sector using Machine Learning techniques. Customer churn prediction is important for banks to identify customers who are likely to leave the service so that retention strategies can be implemented effectively.

The project was developed using Python in Google Colab and follows the standard Data Science workflow, including:

Data Understanding
Data Validation
Data Cleaning
Data Transformation
Exploratory Data Analysis (EDA)
Machine Learning Modeling
Model Evaluation
Dataset

The dataset used in this project contains information about bank customers, including demographic data, account information, and customer activity.

Features:
CreditScore
Geography
Gender
Age
Tenure
Balance
NumOfProducts
HasCrCard
IsActiveMember
EstimatedSalary
Target Variable:
Exited
0 = Customer stays
1 = Customer churns
Tools & Libraries

This project was built using:

Python
Google Colab
Pandas
NumPy
Matplotlib
Seaborn
Scikit-learn
Data Preprocessing

The preprocessing steps include:

Removing irrelevant columns
Handling categorical variables
Encoding text variables into numerical format
Checking missing values and duplicate data

Example preprocessing code:

df = df.drop(['CustomerId', 'Surname'], axis=1)

from sklearn.preprocessing import LabelEncoder

le = LabelEncoder()
df['Gender'] = le.fit_transform(df['Gender'])

df = pd.get_dummies(df, columns=['Geography'], drop_first=True)
Exploratory Data Analysis (EDA)

EDA was performed to understand customer behavior patterns and relationships between variables.

Visualization includes:

Customer churn distribution
Correlation heatmap
Customer demographic analysis
Machine Learning Model

The model used in this project:

Logistic Regression
Train-Test Split:
80% Training Data
20% Testing Data

Example model code:

model = LogisticRegression(max_iter=5000)
model.fit(X_train, y_train)
Model Evaluation

The model was evaluated using:

Accuracy Score
Classification Report
Confusion Matrix
Result:
Accuracy: 81%

The model performs well in predicting non-churn customers but still has limitations in detecting churn customers accurately.

Key Insights
Inactive customers are more likely to churn.
Older customers tend to have higher churn probability.
Customer activity significantly influences retention.
Conclusion

This project demonstrates how Machine Learning can be applied to predict customer churn in the banking industry. Logistic Regression achieved a satisfactory performance with an accuracy score of 81%.

Further improvements may include:

Random Forest
XGBoost
SMOTE for imbalanced data handling
Hyperparameter tuning
Author

Dimas Fahmi

Project Status

Completed ✔️



