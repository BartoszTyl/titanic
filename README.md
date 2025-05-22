# Titanic Classification Project 🚢

This project applies machine learning to the Titanic dataset to predict the survival of passengers based on various features. It was built as a complete data science pipeline, from cleaning and feature engineering to model training and evaluation.

## 📁 Dataset

- **train.csv**: Training data with survival labels.
- **test.csv**: Unlabelled data for prediction.

Data from the [Kaggle Titanic: Machine Learning from Disaster](https://www.kaggle.com/c/titanic) competition.

## 🔍 Problem Statement

Using passenger information (name, age, ticket class, fare, etc.), predict which passengers survived the Titanic disaster.

## 🛠 Features Engineered

- `Title`: Extracted from names and grouped by social class.
- `Age_Cut`: Age binned using `qcut`.
- `Family_Size`: Combined `SibSp` and `Parch`.
- `Cabin_Assigned`: Binary indicator for whether a cabin was assigned.
- `Name_Length`: Character length of the name, binned.
- `Ticket_Prefix`: Standardised ticket prefixes.

## 🧹 Missing Data Handling

- **Age**: Filled using title-specific mean age.
- **Embarked**: Imputed with most common value ("S").
- **Cabin**: Missing entries marked as 'X'; only deck letter retained.
- **Fare**: Filled with median.
- No missing values remain after processing.

## 🧪 Models Explored

- Logistic Regression
- Decision Tree
- Support Vector Machine (SVM)
- K-Nearest Neighbors (KNN)
- Naive Bayes
- Random Forest
- Gradient Boosting
- AdaBoost
- Extra Trees
- XGBoost
- Voting Classifier (Ensemble)

Cross-validation was used to evaluate model performance.

## 📊 Evaluation

Model performance was assessed using accuracy via stratified cross-validation. Feature importance and survival rates were analysed across all key features.

## 💡 Key Insights

- Titles and Cabin assignment were strong indicators of survival.
- Family size showed a non-linear relationship with survival likelihood.
- Female passengers and those in higher classes had higher survival rates.
