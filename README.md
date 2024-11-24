# Credit EDA & Scoring

## Project Overview
This project focuses on performing Exploratory Data Analysis (EDA) and building a credit scoring model using a dataset with various financial and demographic features. The goal is to analyze customer credit profiles, identify key risk factors, and develop a predictive model to estimate a hypothetical credit score based on the dataset.
---
## Project Overview
This project focuses on performing Exploratory Data Analysis (EDA) and building a credit scoring model using a dataset with various financial and demographic features. The goal is to analyze customer credit profiles, identify key risk factors, and develop a predictive model to estimate a hypothetical credit score based on the dataset.

Project link: [Credit EDA & Scoring Project](https://colab.research.google.com/drive/1861CsbKxc3uuSpLnYEFTj5wduqj0Lre3?usp=sharing)


---

## Key Objectives
1. **Exploratory Data Analysis (EDA)**: Analyze and visualize the dataset to uncover patterns and trends in customer credit behavior.
2. **Feature Engineering**: Create new features and modify existing ones to improve the accuracy and performance of the credit scoring model.
3. **Credit Scoring Model**: Build a model to predict a credit score for customers, providing a risk assessment of creditworthiness.
4. **Risk Mitigation**: Identify key risk factors influencing loan approval and provide strategies to mitigate these risks.
5. **Model Evaluation**: Evaluate model performance using appropriate metrics (e.g., AUC, accuracy, precision, recall).

---

## Insights and Findings

### 1. Data Overview
- **Dataset**: The dataset contains 100,000 rows and 27 columns, including demographic and financial information such as income, loan type, credit score, and payment behavior.
- **Key Features**:
  - `Age`: Age of the customer.
  - `Income`: Annual income of the customer.
  - `Credit_Mix`: Types of credit accounts (e.g., revolving credit, installment credit).
  - `Outstanding_Debt`: Total outstanding debt across accounts.
  - `Credit_Utilization_Ratio`: Ratio of current debt to available credit.
  - `Payment_Behavior`: Historical payment behavior indicating on-time or delayed payments.

### 2. Exploratory Data Analysis (EDA)
- **Missing Data**: Identified and imputed missing values using mean, median, or forward/backward fill as appropriate.
- **Correlation Analysis**: Key correlations were found between `Credit_Utilization_Ratio`, `Outstanding_Debt`, and `Credit_Score`.
- **Visualizations**: Used histograms, box plots, and heatmaps to visualize distributions and relationships between features.
- **Outliers**: Detected outliers in certain financial features like `Outstanding_Debt` and `Income`, which were handled using Z-score and IQR methods.

### 3. Feature Engineering
- **Debt-to-Income Ratio (DTI)**: Created a new feature combining `Outstanding_Debt` and `Income` to better assess customer debt risk.
- **Loan-to-Value (LTV)**: Created an `LTV` ratio based on the customer's loan amount and property value, which was found to be a strong predictor of default.
- **Credit History Age**: Converted the `Credit_History_Age` feature to categorize customers based on how long they've had a credit history.

### 4. Credit Scoring Model
- **Model Selection**: Various machine learning algorithms were tested, including Logistic Regression, Random Forest, and Gradient Boosting.
- **Hyperparameter Tuning**: Used Grid Search and Cross-Validation to optimize model parameters.
- **Evaluation Metrics**: The Random Forest model showed the best performance with an AUC of 0.85 and accuracy of 80%.

### 5. Risk Mitigation Strategies
- **High Risk Indicators**: Customers with high `Debt-to-Income (DTI)` ratios and `Credit_Utilization_Ratio` above 80% were identified as high risk.
- **Recommendations**:
  - Implement stricter approval processes for applicants with high DTI and low credit scores.
  - Provide financial counseling for individuals showing high credit utilization ratios.

---

## Methodology
1. **Data Collection**: The dataset used includes financial and demographic information of 100,000 customers, with relevant columns for credit scoring analysis.
2. **Preprocessing**: Data cleaning, feature engineering, and transformation were performed to prepare the data for modeling.
3. **Model Building**: Various machine learning models were trained, including decision trees, ensemble models, and logistic regression.
4. **Model Evaluation**: Evaluated models using metrics like ROC-AUC, F1 score, precision, recall, and confusion matrix to select the best-performing model.

---

## Technologies Used
- **Python**: For data cleaning, feature engineering, and building machine learning models.
- **Libraries**: Pandas, Numpy, Scikit-learn, Matplotlib, Seaborn, XGBoost
- **Jupyter Notebooks**: For analysis and model building.

