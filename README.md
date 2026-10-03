# Churn Analysis Project

## Overview
This project is designed to analyze customer churn data from a telecommunications company. The analysis involves exploratory data analysis (EDA) and building a logistic regression model to predict customer churn based on various features.

## Data Description
The dataset used in this project is `Telco-Customer-Churn.csv`, which includes information about each customer such as tenure, contract type, internet service, payment method, monthly charges, total charges, and more. The target variable is `Churn`, indicating whether a customer has churned or not.

## analysis.ipynb
This Jupyter notebook performs the following tasks:
1. **EDA**:
   - Loads the dataset and prints its shape, information, null values, and value counts for the 'Churn' column.
   - Converts the `TotalCharges` column to numeric type, handling missing values by coercing errors.
   - Calculates churn rates by different contract types, tenure groups, internet service types, and payment methods.
   - Computes the correlation matrix between the `tenure`, `MonthlyCharges`, `TotalCharges`, and `ChurnFlag` columns.

2. **Visualization**:
   - Generates several bar charts to visualize churn rates by various customer attributes such as contract type, tenure group, internet service type, and tech support status.
   - Creates a histogram to compare monthly charges distribution between retained and churned customers.
   - Visualizes the top 10 most significant features affecting churn likelihood using a horizontal bar chart.

## Regression Model.ipynb
This Jupyter notebook focuses on building a logistic regression model to predict customer churn:
1. **Data Preparation**:
   - Loads the dataset and copies it for modeling purposes.
   - Drops columns that are not useful predictors.
   - Encodes the target variable and all remaining categorical columns using `LabelEncoder`.

2. **Model Training**:
   - Splits the data into training and testing sets with stratified sampling to ensure an equal distribution of churned customers in both sets.
   - Trains a logistic regression model with various configurations:
     - Default parameters
     - Balanced class weight to handle class imbalance
     - Custom threshold for prediction

3. **Model Evaluation**:
   - Evaluates the performance of each model using accuracy, classification reports, and confusion matrices.
   - Prints detailed metrics and saves bar charts showing feature importance.

## Visualizations
The notebooks generate several PNG files that are saved in the project directory (`02-churn-analysis`):
- `churn_overall.png`: Overall churn distribution
- `churn_by_contract.png`: Churn rate by contract type
- `churn_by_tenure.png`: Churn rate by tenure group
- `churn_by_internet.png`: Churn rate by internet service type
- `churn_by_monthly_charges.png`: Monthly charges distribution: churned vs retained
- `churn_by_techsupport.png`: Churn rate by tech support status
- `churn_feature_importance.png`: Top 10 churn predictors

These visualizations help in understanding customer churn patterns and the effectiveness of different models.

## Getting Started
To run these notebooks, you need:
- Python environment (Python 3.x)
- Jupyter Notebook or any other compatible IDE
- Pandas, Matplotlib, Scikit-Learn libraries installed

You can install the required libraries using pip:

```bash
pip install pandas matplotlib scikit-learn
```

## Conclusion
This project provides a comprehensive analysis and modeling approach to understanding customer churn in a telecommunications company. The visualizations generated help in making data-driven decisions to improve retention strategies.

---

Feel free to modify this README according to your specific needs and the actual contents of your notebooks!
