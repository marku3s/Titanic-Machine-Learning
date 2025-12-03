🚢 Titanic Survival Prediction: Machine Learning Workflow
1. Project Objective

The goal of this project is to predict the survival of passengers aboard the Titanic using historical data. The workflow transitions from Exploratory Data Analysis (EDA) to Feature Engineering, and finally to Supervised Machine Learning models to classify passengers as Survivors (1) or Deceased (0).

2. Data Processing & Engineering
Exploratory Analysis

- Analyzed survival rates by Class, Sex, and Age.

- identified that Women and First Class passengers had significantly higher survival rates.

- Identified missing data in Age, Cabin, and Embarked.

Feature Engineering

FamilySize: Created a new feature combining SibSp (Siblings/Spouses) and Parch (Parents/Children) to understand family dynamics.

IsAlone: Created a binary feature indicating if a passenger was traveling solo.

FareNormalized: Normalized fare distribution for better visualization.

Data Cleaning & Imputation

Missing Ages: Imputed missing values in the Age column using the Median to preserve the distribution without being influenced by outliers.

Missing Fares: Filled missing Fare values with the Median.

Categorical Encoding:

Note: The Sex column was already encoded numerically (0 = Male, 1 = Female) in the dataset/preprocessing steps, so no further One-Hot Encoding was required for this feature.

3. Machine Learning Models

Two different classification algorithms were trained on the processed data:

Logistic Regression: Used as a baseline model for binary classification.

Random Forest Classifier: A powerful ensemble method used to capture non-linear relationships.

4. Evaluation & Results

The models were evaluated using Accuracy, Precision, and Recall.

Model	Accuracy	Precision	Recall
Logistic Regression	~80.4%	0.78	0.73
Random Forest	~81.6%	0.86	0.66
Key Findings:

Random Forest achieved the highest overall accuracy (~81.6%).

Feature Importance Analysis: The Random Forest model identified Age and Fare as the most critical features for predicting survival, followed by Class and Sex.

Precision vs. Recall: The Random Forest model had higher Precision (fewer false positives) but lower Recall compared to Logistic Regression, indicating it was more "conservative" in predicting survival.
