📌 Overview

<img width="1287" height="667" alt="image" src="https://github.com/user-attachments/assets/7a4874a2-5bb4-47c6-82f3-99f72866a24c" />


🛠️ Tools & Technologies


<img width="1393" height="735" alt="image" src="https://github.com/user-attachments/assets/85f48a68-7656-400a-a92f-9b6a47db856c" />



📂 Dataset


| Business Entity      | Description                                                                                             |
| ---------------- | ----------------------------------------------------------------------------------------------------------- |
| Customer         | Contains customer information used for customer behavior and sales analysis.                                |
| Product          | Contains product details used to analyze product and category performance.                                  |
| Store            | Contains store information used to evaluate branch-level performance.                                       |
| Sales Fact Table | Contains sales transactions and measures such as quantity, price, cost, discount, and returns.              |
| Date Dimension   | Dedicated date table created to support Time Intelligence calculations such as MTD, QTD, YTD, MoM, and YoY. |




🧹 Data Cleaning



| Table          | Data Quality Issue                         | Action Taken                                 |
| -------------- | ------------------------------------------ | -------------------------------------------- |
| Customer   | Invalid Gender values (`???`)              | Replaced with **Unknown Gender**                 |
| Customer   | Missing Email values                       | Replaced with **Unknown Email**                  |
| Product    | Invalid Category values                    | Replaced with **Unknown Category**               |
| Product    | Missing Color values                       | Replaced with **Unknown Color**                  |
| Sales      | Product IDs not found in Product Dimension | Replaced with **Unknown Product ID**             |
| Sales      | Store IDs not found in Store Dimension     | Replaced with **Unknown Store ID**               |
| Sales      | Missing Customer IDs                       | Replaced with **Unknown Customer ID**            |
| Sales      | Missing Discount values                    | Replaced with **0**                              |
| Sales      | Missing Cost Price & List Price            | Preserved as **NULL** to maintain data integrity |
| All Tables | Duplicate records                          | Removed duplicate records                        |



🏗️ Data Model


The project follows a Star Schema design.
Dimension Tables
Customer
Product
Store
Date
Fact Table
Sales
This structure improves query performance and simplifies report development.


<img width="710" height="609" alt="image" src="https://github.com/user-attachments/assets/be4dd36b-b968-4953-8194-2a4779464801" />

📈 DAX Measures


The dashboard includes a comprehensive set of business measures such as:

<img width="1377" height="651" alt="image" src="https://github.com/user-attachments/assets/f1af4934-47aa-4a66-aa13-21fb507c42fa" />

<img width="1341" height="553" alt="image" src="https://github.com/user-attachments/assets/31e99254-52a3-4e07-abac-67a9bbe6b91e" />

🎨 Dashboard Features


🏠 Landing Page


<img width="1172" height="607" alt="image" src="https://github.com/user-attachments/assets/d058fd88-df8e-4ce1-af9b-e24f08fa0e27" />


Sales Analysis – Overview

The **Overview** page provides a comprehensive view of sales performance through interactive KPIs and dynamic analysis.

* **KPIs:** Sales, Return Rate, Total Cost, Profit, and Profit Margin.
* **Dynamic Targets:** Users can set targets for Net Sales, Profit, and Profit Margin, with KPI colors changing based on target achievement.
* **Sales Trend:** Date is fixed on the X-axis, while users can select the Y-axis measure.
* **Dynamic Analysis:** Users can select both X-axis and Y-axis fields for flexible analysis.
* **Category & City Analysis:** Analyzes Net Sales by category and city.
* **Interactive Filters:** Date, Category, and City slicers allow users to customize the analysis.


<img width="1197" height="683" alt="image" src="https://github.com/user-attachments/assets/0895e950-e2a8-4f77-aaa7-07e0573d640e" />


Product & Time Analysis

The Product Analysis page evaluates category performance across sales, profitability, margins, and discount strategies, helping identify high-performing categories and data quality issues such as Unknown Category.

The Time Intelligence analysis tracks MTD, QTD, and YTD performance alongside MoM, QoQ, and YoY growth, while Waterfall and Decomposition Tree visuals highlight sales changes and key drivers across different business dimensions.

<img width="1189" height="670" alt="image" src="https://github.com/user-attachments/assets/0fd8277f-16e0-4eab-97c8-efa60cd241ca" />
<img width="1194" height="668" alt="image" src="https://github.com/user-attachments/assets/40086419-1364-4d05-9191-f6188315c411" />



💡 Key Insights

-Shoes is the top-selling category by order count, with an average order value of 226.57 and ~3 items per order.

-Profit is nearly even across categories (1.15M–1.18M); Dresses generates the highest profit despite not being the top seller — indicating strong margin efficiency.

-Product P000528 has notably higher returns (1,948) than any other product — a candidate for quality investigation.
Shoes carries the highest average discount (5.68%), which may be compressing its margin relative to Dresses.

-YoY growth is strong across all categories (~24–26%), and Net Sales last month (11.00M) is already close to total sales (11.2M), showing accelerating recent momentum.


📉 Sales detial


Advanced analysis using:
Waterfall Chart
Decomposition Tree
Time Intelligence Matrix
Allows users to drill into yearly sales changes and identify business drivers.

<img width="1192" height="672" alt="image" src="https://github.com/user-attachments/assets/a77b43c9-ee4a-4615-9ddb-6837bb32d42e" />



💡 Key Insights


-Sales show a clear cyclical pattern: growth in 2021, decline in 2022, sharp recovery in 2023, then a pullback in 2024 — suggesting market-driven volatility rather than steady linear growth.

-2023 stands out as the strongest growth year across almost all categories, making it a useful benchmark for what drove performance.

-The decomposition tree shows Supplier D as the top contributor to total sales, followed by Suppliers A, B, and C  supplier concentration is fairly balanced but Supplier D leads.

-Fall and Winter seasons drive slightly higher sales than Spring and Summer, useful for inventory and promotion planning.

-At the most granular level, size XL and the color White lead within the Tops category  useful for merchandising decisions.




👥 Customer Analysis


The Customer Analysis page evaluates customer distribution, geographic sales performance, demographics, and new customer acquisition. It compares customer counts and Net Sales by city analyzes sales by gender and highlights Net Sales generated by new customers across cities, helping identify key markets and acquisition opportunities.

<img width="1198" height="673" alt="image" src="https://github.com/user-attachments/assets/4a7ebd6e-b610-4ea4-b370-35c98b9d4bad" />



💡 Key Insights


-Customer base is fairly evenly distributed across cities (Faro, Lisbon, Coimbra, Braga, Porto each 4.1K–4.4K), with no single city dominating.

-Lisbon generates the highest sales (2.24M) despite Faro having the largest customer count indicating higher average spend per customer in Lisbon.

-Gender split is nearly balanced between Male (32.47%), Female (31.69%), and Other (30.96%) — a notably diverse customer base with minimal skew.

-New customer sales mirror the overall city ranking (Lisbon > Faro > Braga > Coimbra > Porto), suggesting consistent acquisition performance across markets rather than one city driving growth.

-Profit per customer stands at 148.45, with 2M in new customer sales, showing new customers are a meaningful revenue contributor.


📈Customer Sales & Growth Analysis

This page provides an in-depth analysis of customer Net Sales using a Decomposition Tree and Time Intelligence metrics. It enables drill-down by Gender, City, Age, and Customer ID, while MTD, QTD, YTD, MoM, QoQ, and YoY metrics highlight sales performance and growth trends across cities.

<img width="1190" height="668" alt="image" src="https://github.com/user-attachments/assets/25543961-718d-4cf7-a2e6-5086d0be814f" />


💡 Key Insights

-Male customers generate the highest sales (3.63M), closely followed by "Other" (3.55M) and Female (3.46M) — confirming the balanced gender contribution seen in the Customer Analysis page.

-Lisbon leads MTD net sales (43,356) and shows the highest QTD/YTD figures among cities, reinforcing it as the top-performing market.

-Porto posts the strongest YoY growth (26.79%) among cities, even though it isn't the top city in absolute sales — a market worth watching for future potential.

-Records with a blank/missing city consistently underperform (lowest MTD, QTD, YTD, and YoY), tying back to the data quality gaps noted in the cleaning stage.

-Overall city-level YoY growth (25.07% total) is consistent with category-level growth, showing broad-based growth rather than one segment driving results.


🏪 Store Analysis:

The Store Analysis page evaluates store performance across Net Sales, Profit, Product Categories, and Returned Sales. It compares store and category performance to identify top and underperforming branches, analyze category profitability and sales contribution, and highlight stores with high return values that may require further investigation.

<img width="1190" height="670" alt="image" src="https://github.com/user-attachments/assets/a841340d-0a7e-420d-a8e0-1ed497a44426" />



💡 Key Insights

-Sales are well-balanced across all five stores/channels (2.2M–2.3M), with Lisbon Flagship and Faro Outlet slightly ahead — no single store dominates.

-Porto Center has the highest returned sales value (254K) despite not being the top-selling store, flagging it as a priority for return-reduction investigation.

-Profit margin by category is fairly consistent across stores (~19–20%), though Faro Outlet stands out with a notably higher Shoes profit share (18.97%) and stronger Unknown Category margin (20.30%).

-The Online channel performs on par with physical stores in both sales and returns, confirming it's a fully competitive channel rather than a secondary one.

-Category sales distribution is nearly identical across all stores, suggesting a consistent merchandising/assortment strategy rather than store-specific specialization.
