# 📚 Bookstore Customer Analytics & Customer Spending Prediction

## Project Overview

This project presents an end-to-end data analytics and machine learning workflow using a bookstore customer dataset. The objective was to clean and prepare raw customer data, explore customer behaviour through Exploratory Data Analysis (EDA), engineer meaningful features, and develop predictive models capable of estimating customer spending.

The project demonstrates the complete data science process, from data cleaning and visualization to predictive modeling and business recommendations, with the goal of supporting data-driven decision-making within the business.

---

## Business Problem

Understanding customer purchasing behaviour is essential for improving customer retention, increasing revenue, and optimizing business operations. This project aims to answer questions such as:

* Who are the company's most valuable customers?
* How do customer behaviours differ across stores and regions?
* What factors influence customer spending?
* Can customer spending be predicted using historical customer data?
* What actionable insights can support better business decisions?

---

## Project Objectives

* Clean and prepare a real-world customer dataset.
* Perform exploratory data analysis to identify trends and customer behaviour.
* Engineer additional features to improve predictive performance.
* Train and compare multiple machine learning regression models.
* Evaluate model performance using appropriate regression metrics.
* Generate business insights and practical recommendations.

---

## Dataset

The dataset contains customer information collected from a bookstore, including customer demographics, purchasing behaviour, engagement metrics, store information, and customer service records.

### Target Variable

* **Total Spent** – The total amount spent by each customer.

### Key Features

* Home Store
* Region
* Annual Visits
* Visits in 2023
* Online Purchase Ratio
* Customer Rating
* Loyalty Membership
* Escalation Status
* Escalation Reason
* Lifetime Value Estimate (LTV)
* Total Purchases

---

# Project Workflow

## 1. Data Cleaning

The raw dataset was cleaned to improve data quality before analysis.

Cleaning tasks included:

* Standardizing inconsistent categorical values.
* Handling missing numerical values using the regional median.
* Filling missing categorical values with meaningful labels.
* Converting date columns to the appropriate datetime format.
* Correcting data types.
* Removing duplicate records.

---

## 2. Exploratory Data Analysis (EDA)

EDA was performed to understand customer behaviour and identify patterns within the data.

The analysis included:

### Univariate Analysis

* Distribution of categorical variables
* Distribution of numerical variables
* Customer engagement metrics
* Customer ratings
* Online purchasing behaviour

### Bivariate Analysis

* Numerical vs Numerical relationships
* Categorical vs Numerical comparisons
* Categorical vs Categorical relationships
* Correlation analysis

---

## 3. Feature Engineering

Additional variables were created to capture customer behaviour more effectively.

Engineered features include:

* Customer Tenure
* Purchase Lifespan
* High Value Customer (created for analysis but excluded from modeling to prevent target leakage)

---

## 4. Data Preprocessing

Prior to modeling:

* Unnecessary columns were removed.
* Categorical variables were encoded using One-Hot Encoding.
* Numerical variables were standardized using StandardScaler.
* The dataset was split into training and testing sets (80:20).
* Data leakage was prevented by fitting the scaler only on the training data.

---

## 5. Predictive Modeling

Four regression models were developed and evaluated:

* Linear Regression
* Decision Tree Regression
* Random Forest Regression
* Gradient Boosting Regression

Model performance was evaluated using:

* R² Score
* Mean Squared Error (MSE)
* Root Mean Squared Error (RMSE)

---

# Model Performance

| Model                            |  R² Score |             MSE |        RMSE |
| -------------------------------- | --------: | --------------: | ----------: |
| **Random Forest Regression**     | **0.638** | **911,058.849** | **954.494** |
| **Gradient Boosting Regression** |     0.635 |     918,359.924 |     958.311 |
| **Linear Regression**            |     0.624 |     947,688.294 |     973.493 |
| **Decision Tree Regression**     |     0.264 |   1,853,507.352 |   1,361.436 |

Among the evaluated models, **Random Forest Regression** achieved the best overall performance, closely followed by **Gradient Boosting Regression**. The ensemble models outperformed the individual models by capturing more complex relationships within the data while producing lower prediction errors.

---

# Key Business Insights

The analysis revealed several important findings:

* Calgary Downtown and the YYC-DT home store account for the largest share of customers.
* Most customers are not enrolled in the loyalty program, suggesting opportunities to improve customer retention.
* Customer Lifetime Value (LTV) is positively skewed, with most customers contributing relatively modest long-term value and a smaller group generating substantially higher value.
* Customer spending follows a similar pattern, with most customers making relatively small purchases while a limited number contribute significantly higher spending.
* Most customers experience no service escalations, although **Late Delivery** is the most frequently reported complaint and represents an opportunity for operational improvement.
* Only a small proportion of customers rely heavily on online purchasing, indicating potential to expand digital engagement.
* Customer ratings average approximately **3.95**, suggesting generally positive customer satisfaction while highlighting opportunities to further enhance service quality.
* Average customer spending and purchasing behaviour remain relatively consistent across regions and home stores despite differences in customer volume.
* Random Forest Regression demonstrated that customer spending can be predicted with moderate accuracy using customer behavioural and transactional data.

---

# Business Recommendations

Based on the findings, the following recommendations are proposed:

* Strengthen the loyalty program through targeted promotions and customer incentives.
* Improve delivery operations to reduce late delivery complaints.
* Expand the company's online presence through enhanced digital marketing and website improvements.
* Develop retention strategies for high-value customers using personalized offers and exclusive benefits.
* Continue improving customer service to increase customer satisfaction and long-term loyalty.
* Deploy the Random Forest model as a decision-support tool for forecasting customer spending and identifying valuable customer segments.

---

# Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook

---

# Repository Structure

```text
Bookstore-Customer-Analytics/
│
├── data/
│   ├── bookstore_customers_expanded_raw.csv
│   └── bookstore_customers_cleaned.csv
│
├── notebooks/
│   ├── 01_Data_Cleaning.ipynb
│   └── 02_EDA_Feature_Engineering_Modeling.ipynb
│
├── images/
│
├── requirements.txt
│
└── README.md
```

---

# Future Improvements

Potential improvements for future work include:

* Hyperparameter tuning using GridSearchCV or RandomizedSearchCV.
* Cross-validation for more robust model evaluation.
* Exploring additional ensemble algorithms such as XGBoost or LightGBM.
* Incorporating customer demographics, marketing interactions, and seasonal purchasing patterns to improve predictive performance.
* Developing an interactive dashboard for business stakeholders.

---

# Author

**Mary Olalere**

Data Analyst | Data Scientist

This project was developed as part of my data science portfolio to demonstrate practical skills in data cleaning, exploratory data analysis, feature engineering, machine learning, and business insight generation.
