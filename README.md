# Bank Customer Churn Analysis

## 📌 Project Overview

This project analyzes customer churn behavior in a banking dataset to identify factors associated with customer attrition and develop a classification model to predict churn.

The project covers the end-to-end data analysis process, including data preparation, exploratory data analysis, hypothesis testing, machine learning, and model evaluation.

## 🎯 Business Problem

Customer churn is an important business problem for banks because losing existing customers can affect revenue and increase the cost of acquiring new customers.

This project aims to answer the following questions:

- Which customer characteristics are associated with churn?
- Are there significant differences in churn rates across customer groups?
- Which factors are most relevant for identifying customers who are likely to churn?
- How well can a classification model identify customers at risk of churn?

The analysis combines exploratory data analysis, statistical hypothesis testing, and machine learning to investigate customer churn from both a business and predictive perspective.

## 📊 Dataset

The dataset contains customer-level information from a banking context, including demographic, financial, product, and activity-related features.

The target variable is:

- **Exited** — indicates whether a customer has churned (`1`) or remained with the bank (`0`).

The dataset includes variables such as:

- **CreditScore**
- **Geography**
- **Gender**
- **Age**
- **Tenure**
- **Balance**
- **NumOfProducts**
- **HasCrCard**
- **IsActiveMember**
- **EstimatedSalary**

## 🔍 Data Analysis

### 1. Data Understanding

The dataset was examined to understand its structure, data types, missing values, duplicate records, and the distribution of the target variable.

The original data consists of customer information and account-related information. These datasets were merged using `CustomerId` to create the final analytical dataset.

Key steps included:

- Inspecting dataset dimensions and data types
- Checking missing values
- Identifying duplicate records
- Reviewing categorical and numerical variables
- Examining the distribution of the target variable `Exited`

### 2. Data Cleaning

Several data preparation steps were performed before analysis:

- Merged customer and account information using `CustomerId`
- Handled missing values in relevant variables
- Removed duplicate records
- Converted `EstimatedSalary` from string format to numerical format
- Reviewed inconsistent or unsuitable values
- Created derived variables where appropriate for further analysis

The cleaned dataset was then used for exploratory analysis and statistical testing.

### 3. Exploratory Data Analysis

Exploratory Data Analysis (EDA) was conducted to investigate customer characteristics and identify patterns associated with churn.

The analysis examined the relationship between churn and variables including:

- Age
- Credit Score
- Balance
- Gender
- Geography
- Tenure
- Number of Products
- Credit Card Ownership
- Active Membership

Additional derived features and customer segments were also explored to investigate differences in customer behavior across groups.

### 4. Hypothesis Testing

Statistical hypothesis testing was performed to determine whether observed differences between churned and non-churned customers were statistically significant.

The analysis included appropriate statistical tests for numerical and categorical variables.

For categorical variables, the Chi-Square test of independence was used to examine whether customer characteristics were associated with churn.

The hypothesis testing results were used together with the EDA findings to distinguish between observed patterns and statistically supported relationships.

## 🤖 Machine Learning

### Data Preprocessing

Before model training, the dataset was prepared for machine learning.

Numerical and categorical variables were processed separately:

- Numerical features were standardized using `StandardScaler`
- Categorical features were encoded using `OneHotEncoder`
- The target variable was `Exited`
- The dataset was split into training and testing sets
- Stratified cross-validation was used to preserve the class distribution across folds

### Model Development

Classification models were evaluated to identify a suitable approach for predicting customer churn.

Model performance was evaluated using multiple metrics rather than accuracy alone, including:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC

Cross-validation was used during model evaluation to assess the consistency of model performance across different data splits.

### Classification Threshold

The classification threshold was also examined because the default threshold of 0.5 may not always provide the most appropriate balance between precision and recall.

ROC and Precision-Recall curves were used to understand how model performance changes as the classification threshold changes.

## 📈 Final Model Performance

| Metric | Final Model |
|---|---:|
| Accuracy | 78.75% |
| Precision | 47.90% |
| Recall | 50.37% |
| F1-score | 49.10% |

## 💡 Key Insights

The exploratory analysis and hypothesis testing revealed several patterns associated with customer churn:

- **Geography:** Customers in Germany showed a substantially higher churn rate compared with customers in France and Spain.
- **Gender:** Female customers had a higher churn rate than male customers in the dataset, and the association between gender and churn was statistically significant.
- **Credit Card Ownership:** Customers without a credit card showed a higher churn rate than customers with a credit card.
- **Age:** Churned customers tended to be older than customers who remained with the bank.
- **Balance:** Churned customers generally showed a higher median account balance.
- **Tenure:** No clear evidence of a strong relationship between tenure and churn was observed.
- **Customer Activity:** Customer activity and product-related characteristics were further investigated to understand differences between churned and retained customers.

## 📝 Conclusion

This project demonstrates an end-to-end approach to analyzing customer churn, from data preparation and exploratory analysis to statistical hypothesis testing and classification modeling.

The analysis identified several customer characteristics associated with churn and demonstrated how statistical testing can be used to validate patterns observed during exploratory analysis.

The final classification model provides a baseline approach for identifying customers who may be at risk of churn. The results also highlight the importance of selecting an appropriate classification threshold depending on the business objective and the relative cost of false positives and false negatives.
The original data was prepared and merged before being used for the subsequent analysis.

## 📝 Conclusion

This project demonstrates an end-to-end approach to analyzing customer churn, from data preparation and exploratory analysis to statistical hypothesis testing and classification modeling.

The analysis identified several customer characteristics associated with churn and demonstrated how statistical testing can be used to validate patterns observed during exploratory analysis.

The final classification model provides a baseline approach for identifying customers who may be at risk of churn. The results also highlight the importance of selecting an appropriate classification threshold depending on the business objective and the relative cost of false positives and false negatives.

## 🛠️ Tools & Technologies

- **Python**
- **Pandas** — data manipulation
- **NumPy** — numerical computing
- **Matplotlib** — data visualization
- **Seaborn** — statistical visualization
- **SciPy** — statistical hypothesis testing
- **Scikit-learn** — machine learning and model evaluation
- **Jupyter Notebook** — analysis and experimentation
- **GitHub** — version control and project documentation

## 📁 Project Structure

```
bank-customer-churn-analysis/
│
├── data/
│   ├── Bank_Churn.csv
│   ├── Bank_Churn_Data_Dictionary.csv
│   └── Bank_Churn_Merged.xlsx
│
├── notebooks/
│   └── 01_data_understanding.ipynb
│
└── README.md

```
## 👤 Author

**Phạm Phú Thanh Tuyền**

Financial Mathematics Graduate | Aspiring Data Analyst

Interested in Data Analysis, Business Analytics, Statistics, and Machine Learning.

