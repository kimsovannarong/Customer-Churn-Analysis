# 📊 Customer Churn Analysis Dashboard

An interactive Power BI dashboard designed to analyze customer churn patterns, identify high-risk segments, and uncover key revenue drivers to improve customer retention.

---

## 📌 Executive Summary

* **Total Customers:** 7,043
* **Overall Churn Rate:** 26.54% (1,869 Churned Customers)
* **Retained Customers:** 5,174 (73.46%)

---

## 🎯 Key Insights & Analysis

### 1. Risk Segmentation
* **Normal Risk:** 4,541 retained customers.
* **High Risk:** 633 customers at immediate risk of churning.

### 2. Contract & Tenure Drivers
* **Contract Type:** Month-to-Month contracts account for the overwhelming majority of churned customers compared to One-Year or Two-Year plans.
* **Tenure Band:** New customers have a significantly higher churn risk:
  * **0–6 Months:** 52.94% Churn Rate
  * **6–12 Months:** 35.89% Churn Rate
  * **12+ Months:** 17.13% Churn Rate

### 3. Financials & Add-on Services
* **Monthly Charges:** Customers without Online Security generate higher monthly charge totals among churned groups, indicating that missing value-added security services correlates with attrition.
* **Customer Segment Spend:** Old/existing customers generate the vast majority of monthly charges ($0.38M) compared to new onboarded customers ($0.08M).

---

## 🛠 Tech Stack & Tools

* **Business Intelligence:** Power BI Desktop
* **Data Processing:** Power Query (ETL, Data Cleaning, Data Modeling)
* **Data Language:** DAX (Data Analysis Expressions)

---


1. Clone this repository:
   ```bash
   git clone [https://github.com/kimsovannarong/Customer-Churn-Analysis.git](https://github.com/kimsovannarong/Customer-Churn-Analysis.git)
