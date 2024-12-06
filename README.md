# Titanic
Titanic 
# Model Card for [Tapiwanashe Emmanuel Matare]

## Basic Information
- **Email Address**: tapiwanashe.matare@gwmail.gwu.edu
- **Date**: [4 December 2024]
- **Model Version**: 1.0
- **License**:License
MIT License

Copyright (c) 2021 jphall@gwu.edu

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE
- **Model Implementation Code**: [Link to Colab](https://colab.research.google.com/drive/1hM_9FXe61U-6uMEgViwE-vmaZCpdamYh#scrollTo=qV1AOzzGyK7h) 
  
### Intended Use
- **Intended Uses**: This model is intended for predicting survival on the Titanic based on passenger characteristics.
- **Intended Users**: Data scientists, researchers, and educators interested in machine learning applications.
- **Out-of-Scope Uses**: This model should not be used for real-time decision-making in critical situations.
- 
## Training Data
- **Source of Training Data**: The Titanic dataset from Kaggle.
- **Training Data Division**: The training data was divided into 70% training and 30% validation.
- **Number of Rows**:
  - Training Data: [623 rows]
  - Validation Data: [134 rows]
- **Data Dictionary**:
  | Column Name | Modeling Role | Measurement Level | Description |
  |-------------|---------------|-------------------|-------------|
  | Pclass      | Input         | Nominal           | Passenger class (1st, 2nd, or 3rd) |
  | Sex         | Input         | Nominal           | Gender of the passenger |
  | Age         | Input         | Continuous        | Age of the passenger |
  | SibSp       | Input         | Discrete          | Number of siblings/spouses aboard |
  | Parch       | Input         | Discrete          | Number of parents/children aboard |
  | Fare        | Input         | Continuous        | Fare paid by the passenger |
  | Embarked    | Input         | Nominal           | Port of embarkation (C = Cherbourg; Q = Queenstown; S = Southampton) |
  | Survived    | Target        | Binary            | Survival status (0 = No, 1 = Yes) |

## EDA (Exploratory Data Analysis)
- **Engaging in Exploratory Data Analysis (EDA), I embark on a journey of understanding my dataset deeply. Through various visualization techniques, I:**

- **Visualize distributions of key numerical features like age, number of siblings/spouses (SibSp), number of parents/children (Parch), and fare. This helps me uncover trends and identify outliers.**
- **Explore relationships between different variables, potentially revealing correlations that could impact survival predictions.**

## Data Cleaning
- **Data cleaning is a pivotal stage in my analysis. In this phase, I:**
- **Address missing values meticulously, strategically choosing methods like imputation to fill in the gaps in my data.**
- **Drop irrelevant columns such as "PassengerId," "Cabin," "Name," and "Ticket," which don't significantly contribute to my analysis.**
- **Engage in feature engineering, crafting new features or transforming existing ones to enrich my dataset. This can lead to improved predictive performance.**

## Test Data
- **Source of Test Data**: The Titanic dataset from Kaggle.
- **Number of Rows in Test Data**: [134 rows]
- **Differences in Columns**: The test data does not include the 'Survived' column.

## Model Details
- **Input Columns**: Pclass, Sex, Age, SibSp, Parch, Fare, Embarked
- **Target Column**: Survived
- **Type of Model**: Decision Tree Classifier
- **Software Used**: Python with scikit-learn
- **Version of Software**: scikit-learn version [1.5.2]
- **Hyperparameters**:
  - Max Depth: [5]
  - Min Samples Split: [2]

## Quantitative Analysis
- **Metrics Used for Evaluation**:
  - AUC (Area Under the Curve)
  - AIR (Accuracy Improvement Rate)
  
## Ethical Considerations
### Potential Negative Impacts
- **Math or Software Problems**:
  - The model may produce biased predictions if trained on non-representative data.
  
- **Real-world Risks**:
  - Misclassification could lead to incorrect assumptions about passenger safety.

### Potential Uncertainties
- **Math or Software Problems**:
  - Variability in model performance due to changes in input data quality.
  
- **Real-world Risks**:
  - Decisions based on model predictions could affect public perception and safety measures.

### Unexpected Results
- The model's performance may vary significantly between different demographic groups (e.g., gender, age).
### Conclusion 
-At a predictive accuracy of 76.6%, my model demonstrates its potential to forecast Titanic passenger survival effectively. This project not only illustrates the practical application of machine learning techniques on historical data but also provides insights into the influential factors behind survival rates during the Titanic disaster.
