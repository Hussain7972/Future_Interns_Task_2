# 📊 Customer Retention & Churn Analysis

### Future Interns – Data Science & Analytics Internship | Task 2

> An end-to-end customer churn analysis project using Python and Power BI to identify churn patterns, high-risk customers, and actionable retention strategies.

---

## 📌 Project Overview

Customer churn is an important business problem because losing existing customers can reduce revenue and increase customer acquisition costs.

This project analyzes a telecommunications customer dataset to understand:

- Why customers may leave
- Which customer segments have higher churn
- How contract type affects churn
- How tenure relates to churn
- How internet service and payment methods relate to churn
- How technical support affects customer retention
- Which active customers can be considered high-risk

The analysis was performed using **Python** for data cleaning and exploratory analysis and **Microsoft Power BI** for interactive dashboard development.

---

## 🎯 Project Objectives

- Clean and preprocess the customer churn dataset
- Analyze overall customer churn
- Identify important factors associated with churn
- Analyze churn by contract type and customer tenure
- Analyze churn by internet service and payment method
- Analyze the relationship between technical support and churn
- Identify a practical high-risk customer segment
- Build an interactive Power BI dashboard
- Provide business recommendations for improving customer retention

---

## 📂 Dataset

The project uses the **Telco Customer Churn Dataset**.

### Dataset Statistics

| Metric | Value |
|---|---:|
| Total Customers | 7,043 |
| Churned Customers | 1,869 |
| Overall Churn Rate | 26.54% |
| Average Monthly Charges | $64.76 |

### Important Features

| Feature | Description |
|---|---|
| `customerID` | Unique customer identifier |
| `gender` | Customer gender |
| `SeniorCitizen` | Senior citizen indicator |
| `Partner` | Whether customer has a partner |
| `Dependents` | Whether customer has dependents |
| `tenure` | Number of months with the company |
| `InternetService` | Type of internet service |
| `Contract` | Customer contract type |
| `PaymentMethod` | Customer payment method |
| `MonthlyCharges` | Monthly customer charges |
| `TotalCharges` | Total customer charges |
| `TechSupport` | Technical support subscription |
| `Churn` | Whether the customer left |

---

## 🛠️ Tools & Technologies

- 🐍 Python
- 🐼 Pandas
- 🔢 NumPy
- 📈 Matplotlib
- 📓 Jupyter Notebook
- 📊 Microsoft Power BI

---

## 🧹 Data Cleaning & Preparation

The following preprocessing steps were performed:

1. Loaded the dataset using Pandas.
2. Checked the number of rows and columns.
3. Examined column names and data types.
4. Checked missing values.
5. Converted `TotalCharges` into numeric format.
6. Handled invalid and blank values.
7. Removed records with missing `TotalCharges`.
8. Checked for duplicate customer IDs.
9. Created customer tenure groups.
10. Created monthly charge groups for analysis.

---

## 🔍 Exploratory Data Analysis

![dashboard](<Dashboard Image-1.png>)
Several factors were analyzed to understand customer churn.

### 1. Overall Churn


The dataset contains **7,043 customers**, of which **1,869 customers churned**.

The overall churn rate is approximately:

**26.54%**

---

### 2. Churn by Contract Type

Contract type is one of the strongest factors associated with customer churn.

Customers with **month-to-month contracts** show considerably higher churn compared with customers on one-year and two-year contracts.

**Business Insight:**  
Encouraging suitable month-to-month customers to move to longer contracts may improve retention.

---

### 3. Churn by Customer Tenure

Customers with shorter tenure are more vulnerable to churn.

The first year of the customer relationship is therefore an important period for retention activities.

**Business Insight:**  
Companies should provide better onboarding, engagement and support during the early customer lifecycle.

---

### 4. Churn by Monthly Charges

Customers were grouped according to their monthly charges to understand the relationship between billing levels and churn.

This helps identify whether higher monthly charges may be associated with increased customer churn.

---

### 5. Churn by Internet Service

Customer churn was compared across different internet-service categories.

The analysis helps identify service groups that may require additional investigation regarding pricing, service quality and customer experience.

---

### 6. Churn by Payment Method

Different payment methods were analyzed to identify payment-related churn patterns.

Electronic check customers showed a higher historical churn tendency compared with several other payment groups.

---

### 7. Churn by Technical Support

Customers with and without technical support were compared.

Customers without technical support showed higher historical churn, indicating that customer assistance and service support may contribute to retention.

---

## ⚠️ High-Risk Customer Analysis

A practical rule-based high-risk segment was created using:

```text
Contract = Month-to-month
AND
Tenure ≤ 12 months
AND
Churn = No