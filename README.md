# Customer Segmentation & Retention Analytics in Power BI

## 📌 Project Objective
To create a Power BI dashboard that segments customers based on purchasing behavior and analyzes retention rates, helping businesses design loyalty programs and reduce churn.

## 🛠️ Tools Used
* **Power BI Desktop:** For data modeling, DAX calculations, and interactive visualizations.
* **Power Query:** For data cleaning and transformation.

## 🗂️ Dataset Description
The dataset contains 100+ rows of customer transaction records including: Customer ID, Age, Region, Join Date, Total Spend, Purchase Frequency, and Engagement Score.

## ⚙️ Power Query Steps
* Removed null and duplicate values to ensure data integrity.
* Formatted date columns appropriately (Join Date, Last Purchase).
* Created custom conditional columns to structure loyalty tiers.

## 🧮 Key DAX Measures
* **Retention Rate %:** `DIVIDE(CALCULATE([Total Customers], Customer_Data[Retention Status] = "Retained"), [Total Customers], 0)`
* **Churn Rate %:** `DIVIDE(CALCULATE([Total Customers], Customer_Data[Retention Status] = "Churned"), [Total Customers], 0)`
* **Average Order Value (AOV):** `DIVIDE([Total Revenue], [Total Customers], 0)`

## 📊 Dashboard Features & Layout
* **Top KPIs:** Total Customers, Revenue, AOV, Retention Rate, Churn Rate.
* **Visuals:** Bar charts for segment comparison, Donut charts with traffic-light color coding for retention status, and Line charts for time-series trends.
* **Matrix Table:** Detailed breakdown of Customer Segment vs. Revenue vs. Retention.
* **Interactive Slicers:** Region, Gender, Loyalty Tier, and Purchase Channel.

## 💡 Key Business Insights
1. **High-Value Segments:** Identified which specific customer cohorts drive the majority of Total Revenue.
2. **Churn Risk:** Highlighted the "At Risk" customer percentage to allow for targeted marketing interventions.
3. **Retention Trends:** Tracked long-term loyalty via retention percentage over time.

## 📸 Dashboard Screenshot
![Dashboard Preview](Screenshots/Dashboard_Preview.png)

## 🏁 Conclusion
This dashboard provides a robust, automated solution for marketing and CRM teams to monitor customer health, reduce churn, and allocate resources efficiently toward high-value retention strategies.
