Retail Sales Data Analysis Dashboard
📌 Overview
This project is an end-to-end Retail Sales Data Analysis solution built using Power BI. The project focuses on transforming raw transactional data into meaningful business insights through data cleaning, dimensional modeling, DAX calculations, and interactive dashboards.

The dashboard enables decision-makers to analyze sales performance, profitability, customer behavior, product performance, and store operations using interactive visualizations and advanced analytics.

🎯 Project Objectives
Clean and transform raw retail data.
Build a scalable Star Schema data model.
Create business KPIs using DAX.
Perform Time Intelligence analysis.
Analyze Customers, Products, Stores, and Sales.
Build an interactive Power BI dashboard for business users.

🛠️ Tools & Technologies
Microsoft Power BI
Power Query
DAX
Data Modeling
Star Schema
Time Intelligence
Navigation
Q&A Visual

📂 Dataset
The dataset contains four main business entities:
Customer
Product
Store
Sales Fact Table
Additionally, a dedicated Date Dimension was created to support Time Intelligence calculations.

🧹 Data Cleaning
Several data quality issues were identified and resolved before building the dashboard.
Customer Table
Replaced invalid Gender values (???) with Unknown Gender
Replaced missing Email values with Unknown Email
Product Table
Replaced invalid Category values with Unknown Category
Replaced missing Color values with Unknown Color
Sales Table
Replaced invalid Product IDs with Unknown Product ID
Replaced invalid Store IDs with Unknown Store ID
Replaced missing Customer IDs with Unknown Customer ID
Replaced missing Discounts with 0
Preserved missing Cost Price and List Price values as NULL to maintain data integrity
Removed duplicate records
These transformations improved data consistency while preserving analytical accuracy.

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
Gross Sales
Net Sales
Returned Sales
Total Cost
Profit
Profit Margin %
Return Rate %
Total Orders
Total Customers
Average Order Value (AOV)
Profit per Customer
Profit per Order
Average Discount
Average Quantity per Order
Time Intelligence Measures
MTD
QTD
YTD
MoM
QoQ
YoY
Net Sales Last Month
Net Sales Last Quarter
Net Sales Last Year
Quick Measures were also implemented for business comparison and trend analysis.

🎨 Dashboard Features
🏠 Landing Page
Landing Page
The Landing Page serves as the main entry point to the dashboard, providing users with quick and organized navigation to all analysis sections.
The page includes navigation buttons for:
•Dashboard Overview 
•Category Overview 
•Category Details 
•Category Performance 
•Customer Overview 
•Customer Performance 
•Store Overview
•Home Button 
Returns the user to the Landing Page from any report page, providing quick access to all dashboard sections. 
•Help Button 
Opens a Q&A visual, allowing users to ask business questions using natural language (for example: "Show sales by city" or "Top selling category"). The visual automatically generates charts and insights based on the user's query. 

Product Analysis:

The Product Analysis page focuses on evaluating category performance from multiple business perspectives, including sales, profitability, operational efficiency, and discount strategy. Together, these visualizations help identify high-performing categories and highlight potential data quality issues such as Unknown Category.
Sales by Category
The visualization highlights top-performing categories while also revealing categories with low sales, such as Unknown Category, which indicates missing product classification that should be investigated as part of data quality analysis.
Profit by Category

Comparing profit across categories helps evaluate business performance beyond sales volume, as a category with high sales may not necessarily generate the highest profit.
Profit Margin by Category
Profit Margin provides a better understanding of operational efficiency by measuring how much profit is generated from each unit of sales.
Average Discount  by Category
Analyzing average discounts helps identify categories receiving higher promotional offers and evaluate their impact on sales and profitability.

This page provides a detailed analysis of sales performance using Waterfall and Decomposition Tree visualizations. It helps users understand yearly sales changes and drill down through multiple business dimensions to identify the key factors driving sales performance.

Time Intelligence Analysis:
This table presents cumulative sales performance (MTD, QTD, and YTD) alongside sales growth metrics (MoM, QoQ, and YoY). Conditional formatting was applied to quickly highlight high and low-performing categories.


📉 Sales Performance
Advanced analysis using:
Waterfall Chart
Decomposition Tree
Time Intelligence Matrix
Allows users to drill into yearly sales changes and identify business drivers.

👥 Customer Analysis

Insights include:
The Customer Analysis page focuses on understanding customer distribution, geographical sales performance, customer demographics, and new customer acquisition.
Total Customers by City
This visualization compares the number of customers across different cities, helping identify locations with the largest customer base and supporting market coverage analysis.
Sales by City
Displays Net Sales generated from each city, allowing comparison of regional sales performance and identification of the highest and lowest revenue-generating locations.
Sales by Gender
Analyzes the distribution of Net Sales across customer gender groups. This visualization provides insights into customer purchasing behavior and highlights any missing demographic information such as Unknown Gender.
Net Sales for New Customers by City
Shows the contribution of newly acquired customers to Net Sales across different cities. This helps evaluate customer acquisition performance and identify cities generating the highest revenue from new customers.

📈 Customer Performance

Includes:
This page provides a detailed analysis of customer sales performance using Time Intelligence metrics and Decomposition Tree analysis.
Decomposition Tree
The Decomposition Tree enables interactive drill-down analysis to identify the factors contributing to Net Sales. Users can explore sales performance across multiple business dimensions, including:
•Gender 
•City 
•Age 
•Customer ID 
This visualization helps uncover customer segments that generate the highest sales and supports deeper business analysis.
Time Intelligence Analysis
The first matrix displays cumulative sales performance across different cities using:
•Month-to-Date (MTD) 
•Quarter-to-Date (QTD) 
•Year-to-Date (YTD) 
Conditional formatting was applied to quickly distinguish high and low sales performance across cities.
Sales Growth Analysis
The second matrix evaluates sales growth using key comparison metrics:
•Month-over-Month (MoM) 
•Quarter-over-Quarter (QoQ) 
•Year-over-Year (YoY) 
Conditional formatting highlights growth trends, making it easier to identify cities with improving or declining sales performance over time.


🏪 Store Analysis:

The Store Analysis page evaluates store performance by comparing sales, profitability, product distribution, and returned sales across all store locations.
Sales by Store
This visualization compares Net Sales across all stores, helping identify the highest and lowest performing branches while highlighting stores with missing or invalid references.
Profit by Store and Category
The heatmap visualizes profit distribution across product categories within each store. It enables quick comparison of category profitability and helps identify which categories contribute the most profit in every branch.

Sales by Store and Category
The stacked column chart shows how Net Sales are distributed across product categories for each store. This visualization provides insights into the sales contribution of each category and allows easy comparison of category performance between stores.

Returned Sales by Store
This visualization compares the value of Returned Sales across stores, helping identify branches with higher return volumes. Monitoring returned sales supports operational improvements and helps evaluate product quality and customer satisfaction.

