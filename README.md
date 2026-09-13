# 📊 Customer Churn Analysis Dashboard

An end-to-end interactive Power BI dashboard designed to analyze customer retention patterns, evaluate churn drivers, and provide actionable business recommendations to reduce customer attrition for a **Telecom Industry**.

---

## 📌 Project Overview
Customer churn directly impacts revenue growth in the **telecom industry**. This project analyzes **7,043 customer profiles** to identify key risk factors, highlight high-churn service segments, and offer data-driven strategies for long-term retention.

---
## 📊 Live Report & Visual Previews
![Dashboard Main View](https://github.com/kimsovannarong/Customer-Churn-Analysis/blob/f800900635aa209839209cdddccfcddbfae38c71/Asset/Customer%20Churn%20Analysis%20Dashboard.png)
> **[🔗 View Interactive Dashboard via Power BI Service](https://app.powerbi.com/links/r0iP-ndGKD?ctid=1e9461ec-5362-4329-ae46-61fa3e91c6d2&pbi_source=linkShare)**
---
## 📈 Key Metrics (KPIs)
* **Total Customers:** 7,043
* **Total Churned Customers:** 1,869
* **Overall Churn Rate:** 26.54%
* **Retained Risk Classification:** 4,541 Normal Risk | 633 High Risk

---

## 🔍 Key Insights & Findings

* **Insight 1 (Contract Type):** Most customers who leave are on Month-to-Month contracts (over 1,600 people)[cite: 1]. Customers on 1-Year or 2-Year contracts stay much longer[cite: 1].
* **Insight 2 (Tenure Risk):** New customers leave very fast. **52.94%** of churn happens in the first 0–6 months[cite: 1]. After 1 year, the churn rate drops to **17.13%**[cite: 1].
* **Insight 3 (Online Security):** Customers without Online Security leave more often ($157.44K monthly revenue lost without security vs. $64.72K lost with security)[cite: 1].
* **Insight 4 (Monthly Spend):** Churned customers pay a higher average monthly bill (**$74/month**) compared to retained customers (**$61/month**)[cite: 1].
* **Insight 5 (Customer Revenue):** Monthly charges from old/existing customers are high (**$0.38M**), but monthly charges from new customers drop to **$0.08M**[cite: 1].

* **Key Finding:** Customers leave mostly because they pay high monthly rates ($74/mo) on short Month-to-Month plans without Online Security during their first 6 months[cite: 1].

---

## 💡 Business Recommendations

* **Recommendation 1:** Give discounts to help Month-to-Month customers switch to 1-Year or 2-Year contracts[cite: 1].
* **Recommendation 2:** Offer special welcome deals, free setup, and check-ins during the first 6 months to stop early churn[cite: 1].
* **Recommendation 3:** Include Online Security and Backup in standard packages so every user gets protection automatically[cite: 1].
* **Recommendation 4:** Review high-price monthly plans and create cheaper options for price-sensitive users[cite: 1].

---
## 🏗️ Data Architecture & Technical Details

### 1. Data Source and ETL
* **Data Source:** Excel file.
* **ETL Process:** 
  * Loaded Excel file into Power Query.
  * Cleaned missing values and fixed column data types.
  * Created custom columns for tenure groups (0-6 months, 6-12 months, 12+ months)[cite: 1].
  * Grouped existing customers into Normal Risk (4,541) and High Risk (633)[cite: 1].

### 2. DAX Calculations & Key Measures
```dax
// Total Customers
Total Customers = COUNT(Telco_Data[CustomerID])

// Total Churned Customers
Total Churned Customers = CALCULATE(COUNT(Telco_Data[CustomerID]), Telco_Data[Churn] = "Yes")

// Churn Rate Percentage
Churn Rate % = DIVIDE([Total Churned Customers], [Total Customers], 0)

// Average Monthly Charges
Avg Monthly Charges = AVERAGE(Telco_Data[MonthlyCharges])

## 🛠️ Tools & Technologies
* **Business Intelligence:** Microsoft Power BI
* **Data Visualizations:** DAX KPI Cards, Stacked Bar Charts, Donut Charts, Line & Clustered Column Charts

---

## 📄 License
This project is open-source and available under the [MIT License](LICENSE).
