# telecom-churn-prediction-EDA-project

# Telecom Churn Prediction - EDA & ML Project

## 📌 Project Description
This project focuses on **analyzing customer churn** in a telecom company using **Exploratory Data Analysis (EDA)** and **Machine Learning**. The aim is to:
- Understand what factors influence customer churn.
- Visualize behavioral patterns.
- Build a predictive model that can **accurately identify customers at risk of leaving** the company.

The dataset consists of 7,043 customer records with various attributes such as demographic details, service subscriptions, and billing information.

---

## 👩‍💼 Roles & Responsibilities

### 🔹 Data Analyst
- Performed data cleaning, feature engineering, and outlier handling.
- Conducted univariate, bivariate, and multivariate EDA using seaborn & matplotlib.
- Created interactive and interpretable visualizations to understand churn patterns.

### 🔹 Machine Learning Engineer
- Built a robust classification pipeline using **Random Forest Classifier**.
- Handled class imbalance using **SMOTEENN**.
- Evaluated the model using accuracy, precision, recall, F1-score, and confusion matrix.

---

## 📊 Key Findings (EDA Insights)

- **Tenure**: Customers with shorter tenure (<12 months) churn the most.
- **Contract Type**: Month-to-month contracts have the highest churn rate.
- **Internet Service**: Fiber optic users churn more than DSL users.
- **Payment Method**: Customers using electronic checks are most likely to churn.
- **Monthly Charges**: Higher charges correlate with increased churn.
- **Services**: Customers without security, backup, or tech support are more prone to churn.

---

## 📈 Metrics and Measures

| Metric              | Score     |
|---------------------|-----------|
| Accuracy            | 95.3%     |
| Precision (Class 1) | 95%       |
| Recall (Class 1)    | 96%       |
| F1-score            | 96%       |

Model Used: **Random Forest Classifier**  
Class Imbalance Handled with: **SMOTEENN (oversampling + undersampling)**

---

## 📊 Visualizations Used & Their Purpose

| Visualization Type             | Purpose                                                                 |
|-------------------------------|-------------------------------------------------------------------------|
| Bar Plot (Churn Distribution) | Shows proportion of churn vs. non-churn customers                       |
| Pie Chart                     | Visualizes churn percentage (Yes/No)                                    |
| Countplots (Categorical)      | Compare churn across different categories (gender, contract, etc.)      |
| KDE Plot (Density)            | Compare Monthly/Total Charges distribution between churn groups         |
| Scatter Plot                  | Relationship between Total Charges & Monthly Charges                    |
| Box Plot                      | Distribution of Charges across Churn status                             |
| Violin Plot                   | Monthly Charges across Contract types and churn                         |
| Stacked Bar Chart             | Churn distribution across multiple categories (Internet, Contract, etc.)|
| Heatmap                       | Correlation matrix to identify most influential features                |

---

## ⚙️ Step-by-Step Execution Guide

### Step 1: Data Cleaning
- Dropped `customerID` column.
- Converted `TotalCharges` to numeric and handled missing values.
- Standardized categorical formatting and grouped tenure into bins.

### Step 2: Exploratory Data Analysis
- Performed univariate, bivariate, and multivariate analysis.
- Used seaborn/matplotlib for clear insights and comparison.
- Created custom plots by gender, seniority, and services.

### Step 3: Feature Engineering
- Encoded binary features using **LabelEncoder**.
- Applied **One-Hot Encoding** for multi-class columns.
- Created `tenure_group` feature for better segmentation.

### Step 4: Handling Imbalanced Data
- Used **SMOTEENN** to oversample churn and undersample non-churn classes.

### Step 5: Model Building
- Built model using **Random Forest Classifier**.
- Trained with 80% data and tested with 20%.

### Step 6: Model Evaluation
- Evaluated using accuracy, precision, recall, F1-score.
- Final Accuracy: **95.3%**

---

## ✅ Conclusion

This project demonstrates a complete **EDA-to-model pipeline** for customer churn analysis. By combining statistical analysis with visual storytelling, we identified key churn drivers such as:
- **Contract type**
- **Monthly charges**
- **Payment method**
- **Tenure**

Using this knowledge, a **Random Forest model** was trained to predict churn with high accuracy (95.3%). This model can help telecom providers **proactively retain customers**, improve service quality, and reduce churn.

---

## 📁 Project Structure

```bash
├── data/
│   └── Telco-Customer-Churn-classification.csv
├── notebooks/
│   └── churn_EDA_model.ipynb
├── images/
│   └── charts, heatmaps, and visual assets
├── model/
│   └── rf_model.pkl
├── README.md
└── requirements.txt
