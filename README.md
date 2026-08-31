# 👕 Clothing Store Sales & Business Performance Analysis Using Power BI

## 📌 Project Overview

This project analyzes clothing store sales data using **Power BI** to evaluate overall business performance, sales trends, category performance, customer behavior, store performance, profitability, and returned sales.

The project transforms raw transactional data into an interactive Business Intelligence solution using **Power Query, DAX, data modeling, KPIs, parameters, interactive slicers, and dynamic visualizations**.

The dashboard is designed as an analytical story, allowing users to start from a high-level business overview and drill into **categories, customers, and stores** to understand the main drivers of business performance.

---

# 🏠 Dashboard Navigation


<img width="1190" height="663" alt="image" src="https://github.com/user-attachments/assets/883241b8-2244-47eb-a567-9deabe2f2829" />



The Landing Page serves as the main navigation page of the report.

Users can navigate between the different analytical sections of the dashboard, allowing them to move through the analysis in a structured way.

The report includes the following main sections:

-Overview
-Categories
-Category Details
-Category Performance
-Customers
-Customer Performance
-Stores

---

# 🗂️ Data Model


<img width="746" height="643" alt="image" src="https://github.com/user-attachments/assets/3b13c42a-e8d6-4902-bbac-ec385b0dfd4c" />



The project uses a **star schema** to organize the data model.

The model consists of one central fact table surrounded by multiple dimension tables.

### Fact Table

**`Fact(sales_data)`**

The fact table contains transactional sales information, including:

- `customer_id`
- `product_id`
- `store_id`
- `date`
- `quantity`
- `list_price`
- `cost_price`
- `discount`
- `returned`

### Dimension Tables

| Dimension Table | Description |
|---|---|
| `Dim(customer_data)` | Contains customer demographic and identification information |
| `Dim(product_data)` | Contains product, category, pricing, season, size, color, and supplier information |
| `Dim(Date)` | Contains calendar and time-related attributes |
| `Dim(store_data)` | Contains store, region, and store-related information |

The relationships between the fact and dimension tables allow the dashboard to analyze sales from multiple perspectives, including **customer, product, date, and store**.

This structure also supports efficient filtering, aggregation, and DAX calculations throughout the report.

---

# 🛠️ Tools & Technologies

- **Power BI**
- **Power Query**
- **DAX**
- Data Cleaning & Transformation
- Data Modeling
- Star Schema
- Relationships
- Calculated Measures
- KPIs
- Parameters
- Conditional Formatting
- Interactive Slicers
- Data Visualization
- Business Intelligence

---

# 📊 Key Performance Indicators

The dashboard includes a set of KPIs designed to monitor overall business performance, category performance, and customer performance.

## 💼 Overall Business KPIs

These KPIs provide a high-level view of the company's sales performance:

- **Total Sales**
- **Net Sales Last Month**
- **Net Sales Last Quarter**
- **Net Sales Last Year**

These metrics allow users to quickly compare current sales performance with previous time periods and understand the overall direction of the business.

---

## 🏷️ Category KPIs

The Category Analysis page includes KPIs focused on orders, sales volume, category performance, and customer order behavior:

- **Total Orders**
- **Total Quantity**
- **Top Selling Category**
- **Average Order Value (AOV)**
- **Average Quantity per Order**

These KPIs provide a quick summary of category-related business performance and help identify the strongest-selling category.

---

## 👥 Customer KPIs

The Customer Analysis page includes KPIs focused on customer base and customer value:

- **Total Customers**
- **Profit per Customer**
- **Net Sales for New Customers**

These metrics help evaluate the size of the customer base, the average profit generated per customer, and the contribution of newly acquired customers to sales.

---

## 📈 Performance & Time-Based KPIs

The dashboard also evaluates performance across different time periods using:

- **Net Sales MTD** — Month-to-Date
- **Net Sales QTD** — Quarter-to-Date
- **Net Sales YTD** — Year-to-Date
- **Net Sales MoM%** — Month-over-Month Growth
- **Net Sales QoQ%** — Quarter-over-Quarter Growth
- **Net Sales YoY%** — Year-over-Year Growth

These KPIs are used in the **Category Performance** and **Customer Performance** pages to compare current performance with previous periods.

---

## 🎯 Target-Based KPIs

The dashboard also includes user-defined target parameters.

Users can select their own targets, and the KPI cards dynamically evaluate performance against those targets using conditional formatting:

- 🟢 **Green** → Target achieved
- 🔴 **Red** → Target not achieved

This allows users to evaluate business performance based on their own selected targets rather than fixed benchmarks.
---

# 📈 1. Business Overview


<img width="1190" height="670" alt="image" src="https://github.com/user-attachments/assets/33a30a18-1267-4851-bb87-239c642dfb4d" />



The Overview page provides a high-level view of the business performance.

It includes:

- Total Sales
- Net Sales Last Month
- Net Sales Last Quarter
- Net Sales Last Year
- Sales Trend Analysis
- Dynamic analytical visuals
- Target-based KPI evaluation

The page is designed to give users a quick understanding of the current business performance before moving into more detailed analysis.

---

## 🎛️ Dynamic Analysis Parameters

The Overview page includes **five user-controlled parameters** that make the dashboard more interactive.

### Parameters 1 & 2 — Dynamic Axes

The first two parameters allow users to dynamically select the dimensions displayed on:

- X-Axis
- Y-Axis

This allows users to explore different relationships between business dimensions without requiring multiple separate visuals.

For example, users can change the analytical dimensions and explore different views of the business using the same visual.

---

## 🎯 Target-Based KPI Analysis

The remaining three parameters allow users to define their own performance targets.

The KPI formatting dynamically changes based on the selected target.

- 🟢 **Green** → Target achieved
- 🔴 **Red** → Target not achieved

This allows users to evaluate performance against their own selected targets instead of relying only on fixed benchmarks.

---

# 🏷️ 2. Category Analysis


<img width="1186" height="663" alt="image" src="https://github.com/user-attachments/assets/d4c8b8d2-7f06-4a7f-9c70-2d83c00fc2ea" />

<img width="1186" height="660" alt="image" src="https://github.com/user-attachments/assets/963d21d7-1a66-4715-affd-7c728eb62196" />



The Category Analysis section focuses on understanding the performance of different product categories.

The analysis examines category performance from multiple perspectives, including:

- Sales
- Profit
- Revenue contribution
- Category comparisons
- Store-level category performance

Users can apply filters such as **Date, Category, and City** to investigate category performance under different conditions.

---

## 📊 Detailed Category Performance

<img width="1185" height="669" alt="image" src="https://github.com/user-attachments/assets/05482219-1677-4444-a518-396ebf359d7f" />


A deeper analysis is performed to understand differences between categories.

The dashboard helps identify:

- High-performing categories
- Lower-performing categories
- Sales differences
- Profit contribution
- Category performance across different locations

Analyzing both sales and profitability provides a more complete view of category performance.

---

# 👥 3. Customer Analysis

<img width="1186" height="662" alt="image" src="https://github.com/user-attachments/assets/6724d0eb-d25d-48f1-a02e-6a62c776a26b" />  <img width="1186" height="665" alt="image" src="https://github.com/user-attachments/assets/c5197ac2-a89d-4ade-8d63-063d67731ba2" />



The Customer Analysis section focuses on understanding customer behavior and contribution to the business.

The dashboard includes customer KPIs such as:

- **Total Customers**
- **Profit per Customer**
- **Net Sales for New Customers**

Customer performance can also be analyzed using:

- City
- Gender
- Age
- Customer ID
- Category

This allows users to investigate customer behavior from multiple perspectives.

---

## 🌍 Customer Distribution by City

The dashboard analyzes the number of customers across different cities.

The main cities include:

- Lisbon
- Faro
- Braga
- Coimbra
- Porto

This analysis provides insight into the geographic distribution of the customer base.

---

## 💰 Sales by City

Sales performance is analyzed across different cities to understand geographic differences in business performance.

This allows users to compare sales contribution between locations and identify the strongest-performing markets.

---

## 👤 Sales by Gender

Customer sales are analyzed by gender to understand the distribution of sales across customer segments.

The analysis includes:

- Male
- Female
- Other
- Blank / Missing

This provides visibility into customer composition and missing demographic information.

---

## ⚠️ Missing Customer Information

Some sales transactions are associated with customers whose registration information is missing.

These records appear as **Blank** in customer-related analysis.

Instead of removing these transactions, the dashboard keeps them visible to preserve the completeness of the sales analysis.

This makes it possible to understand the impact of missing customer information on:

- Customer counts
- Sales
- Customer segmentation
- Demographic analysis

---

# 🏪 4. Store Analysis


<img width="1184" height="661" alt="image" src="https://github.com/user-attachments/assets/e1cdd2af-de33-47ff-bb84-c67232227171" />


The Store Analysis section evaluates the performance of different stores and sales channels.

The analysis includes:

- Sales by Store
- Profit by Store & Category
- Sales by Store & Category
- Returned Sales by Store

The stores and channels analyzed include:

- Lisbon Flagship
- Faro Outlet
- Online
- Coimbra Boutique
- Porto Center

---

## 💰 Sales by Store

Total sales are compared across the different stores and sales channels.

This helps identify the strongest-performing locations and understand their contribution to overall sales.

---

## 📊 Profit by Store & Category

Profit performance is analyzed by combining:

- Store
- Category

This provides a detailed view of how different categories contribute to profitability within each store.

It also allows users to compare category profitability across locations.

---

## 🏷️ Sales by Store & Category

Sales are analyzed by combining store and category.

This provides a detailed view of how each category contributes to sales within each store.

The analysis can help identify differences in product demand between locations.

---

## 🔄 Returned Sales by Store

Returned sales are analyzed across stores to provide an additional perspective on store performance.

Comparing returned sales with total sales helps provide more context when evaluating store performance.

---

# 🎛️ Interactive Features

The dashboard includes several interactive features designed to allow users to explore the data dynamically.

## Slicers

Users can filter the report using different slicers, including:

- Date
- Category
- City
- Other available dimensions

The selected filters dynamically update the KPIs and visualizations.

---

## Dynamic Parameters

The report includes five parameters that improve dashboard flexibility.

### Dynamic Axis Parameters

The first two parameters allow users to select the dimensions used on the:

- X-Axis
- Y-Axis

### Target Parameters

The remaining three parameters allow users to define business targets.

The KPI cards then dynamically evaluate performance against those targets using conditional formatting.

---

# 📊 Dashboard Structure

The report follows an analytical story structure:

### 🏠 Landing Page

Main navigation page for accessing the different sections of the report.

### 📈 Overview

Provides:

- Main KPIs
- Sales trends
- Dynamic analysis
- Target-based KPI evaluation

### 🏷️ Category Analysis

Provides:

- Category performance
- Sales analysis
- Profitability analysis
- Category comparisons

### 👥 Customer Analysis

Provides:

- Customer KPIs
- Customer distribution
- Sales by gender
- Sales by city
- Customer-level analysis
- Missing customer information analysis

### 🏪 Store Analysis

Provides:

- Sales by store
- Sales by category and store
- Profit by store and category
- Returned sales analysis

---

# 💡 Key Business Insights

Based on the dashboard analysis:

1. The business generated approximately **11.19M in total sales** based on the report context shown in the dashboard.

2. The customer analysis includes approximately **4K customers**.

3. **Lisbon** has the highest customer count among the displayed cities.

4. Customer sales are distributed across multiple gender segments, with missing gender records also visible in the analysis.

5. Sales performance across the main stores and sales channels is relatively close, making detailed store-level analysis important.

6. Category performance varies across stores, highlighting the importance of analyzing **Store + Category** together.

7. Returned sales differ between stores, providing an additional metric for evaluating store performance.

8. Missing customer registration information is retained in the analysis rather than removing those transactions.

9. Dynamic parameters allow users to explore different business dimensions without creating separate visuals for every scenario.

10. Target-based KPI formatting allows users to quickly identify whether selected KPIs are meeting their defined targets.

---

# 📂 Power BI Analysis

The project demonstrates practical Power BI analysis covering:

- KPI Development
- Sales Analysis
- Customer Analysis
- Category Analysis
- Store Analysis
- Profit Analysis
- Returned Sales Analysis
- Time-Based Analysis
- Geographic Analysis
- Customer Segmentation
- Missing Data Analysis
- Dynamic Parameters
- Target-Based KPI Analysis
- Conditional Formatting
- Interactive Slicers
- Data Modeling
- Star Schema
- DAX Measures
- Power Query Transformations

---

# 🚀 Conclusion

This project demonstrates how **Power BI** can be used to transform raw transactional clothing store data into an interactive Business Intelligence solution.

The project combines **data modeling, Power Query transformations, DAX measures, KPIs, trend analysis, category analysis, customer analysis, store performance, profitability, returned sales, dynamic parameters, and target-based performance monitoring**.

The interactive dashboard allows users to explore business performance from multiple perspectives and evaluate KPIs based on their own selected dimensions and targets.

Overall, the project demonstrates practical skills in:

- **Power BI**
- **Power Query**
- **DAX**
- **Data Modeling**
- **Star Schema**
- **Data Visualization**
- **Interactive Dashboard Design**
- **Business-Oriented Data Analysis**
