# 📊 Customer Segmentation & Retention Analytics

![Power BI](https://img.shields.io/badge/PowerBI-F2C811?style=for-the-badge&logo=Power%20BI&logoColor=black)
![Power Query](https://img.shields.io/badge/Power_Query-50E6FF?style=for-the-badge&logo=Microsoft&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-0078D4?style=for-the-badge&logo=Microsoft&logoColor=white)

**[View High-Resolution Dashboard Preview](Dashboard%20Preview/Customer_Retention_Dashboard.png)**

## 🚀 The Business Problem
Companies across e-commerce and retail struggle to maximize Customer Lifetime Value (CLV) without clear visibility into purchasing behaviors. The objective of this project was to engineer a dynamic Business Intelligence tool that segments 100+ customers based on profitability and flags accounts at high risk of churning.

## 💡 Solution & Executive Impact
I developed an automated, end-to-end Power BI dashboard that transforms raw transactional data into an executive-ready model. 
* **Targeted Interventions:** Segmented customers into actionable tiers (VIP, High Value, Mid Value, Low Value), enabling targeted marketing strategies.
* **Churn Mitigation:** Engineered a visual "Traffic Light" retention matrix to instantly isolate "At Risk" and "Churned" revenue.
* **Automated Logic:** Replaced manual reporting with Power Query transformations and dynamic DAX metrics.

## 📸 Executive View
*(Click to enlarge)*
![Dashboard Preview](Dashboard%20Preview/Customer_Retention_Dashboard.png)

## 🧠 Core Technical Skills Applied

### 1. Data Engineering (Power Query)
* Ingested unstructured `.csv` files and modeled them into a relational schema.
* Executed data cleaning protocols: handled nulls, removed duplicates, standardized data types, and built conditional grouping columns.

### 2. Advanced DAX Calculations
Developed robust measures to bypass circular dependencies and provide dynamic KPI tracking.

```dax
// Core Retention Metric
Retention Rate % = 
DIVIDE(
    CALCULATE(
        [Total Customers], 
        Customer_Data[Retention Status] = "Retained"
    ), 
    [Total Customers], 
    0
)

// Dynamic Revenue Calculation
Total Revenue = SUM(Customer_Data[Total Spend])
