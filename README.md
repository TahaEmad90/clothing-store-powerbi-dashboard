# 👕 Clothing Store Sales & Business Performance Analysis Using Power BI

## 📌 Project Overview

This project analyzes clothing store sales data using **Power BI** to evaluate overall business performance, sales trends, category performance, customer behavior, store performance, profitability, and returned sales.

The project transforms raw transactional data into an interactive Business Intelligence solution using:

- **Power Query**
- **DAX**
- **Data Modeling**
- **KPIs**
- **Dynamic Parameters**
- **Interactive Slicers**
- **Conditional Formatting**
- **Dynamic Visualizations**

The dashboard is designed as an analytical story, allowing users to start from a high-level business overview and navigate through **categories, customers, and stores** to understand the main drivers of business performance.

---

# 🏠 Dashboard Navigation

<img width="1190" height="663" alt="Landing Page" src="https://github.com/user-attachments/assets/883241b8-2244-47eb-a567-9deabe2f2829" />

The Landing Page serves as the main navigation page of the report.

Users can navigate between the different analytical sections of the dashboard, allowing them to move through the analysis in a structured way.

The report includes the following main sections:

- **Overview**
- **Categories**
- **Category Details**
- **Category Performance**
- **Customers**
- **Customer Performance**
- **Stores**

---

# 🗂️ Data Model

<img width="746" height="643" alt="Data Model" src="https://github.com/user-attachments/assets/3b13c42a-e8d6-4902-bbac-ec385b0dfd4c" />

The project uses a **Star Schema** to organize the data model.

The model consists of one central fact table connected to multiple dimension tables.

## 📌 Fact Table

### `Fact(sales_data)`

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

## 📌 Dimension Tables

| Dimension Table | Description |
|---|---|
| `Dim(customer_data)` | Contains customer identification and demographic information |
| `Dim(product_data)` | Contains product, category, pricing, season, size, color, and supplier information |
| `Dim(Date)` | Contains calendar and time-related attributes |
| `Dim(store_data)` | Contains store, region, and store-related information |

The relationships between the fact and dimension tables allow the dashboard to analyze sales from multiple perspectives, including:

- Customer
- Product
- Category
- Date
- Store
- City
- Supplier
- Season
- Color
- Size

This structure supports efficient filtering, aggregation, and DAX calculations throughout the report.

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
- KPI Development
- Dynamic Parameters
- Conditional Formatting
- Interactive Slicers
- Data Visualization
- Business Intelligence

---

# 📊 Key Performance Indicators

The dashboard includes a set of KPIs designed to monitor **overall business performance, category performance, customer performance, and time-based performance**.

## 💼 Overall Business KPIs

The Overview page includes the following main business KPIs:

- **Total Sales**
- **Return Rate**
- **Total Cost**
- **Profit**
- **Profit Margin**

These KPIs provide a high-level view of the company's sales, cost, profitability, and return performance.

---

## 🏷️ Category KPIs

The Category Analysis page includes KPIs focused on orders, sales volume, category performance, and customer order behavior:

- **Total Orders**
- **Total Quantity**
- **Top Selling Category**
- **Average Order Value (AOV)**
- **Average Quantity per Order**

These KPIs provide a quick summary of category-related performance and help identify the strongest-selling category.

---

## 👥 Customer KPIs

The Customer Analysis page includes KPIs focused on customer base and customer value:

- **Total Customers**
- **Profit per Customer**
- **Net Sales for New Customers**

These metrics help evaluate the size of the customer base, customer profitability, and the contribution of newly acquired customers to sales.

---

## 📈 Performance & Time-Based KPIs

The dashboard evaluates performance across different time periods using:

- **Net Sales MTD** — Month-to-Date
- **Net Sales QTD** — Quarter-to-Date
- **Net Sales YTD** — Year-to-Date
- **Net Sales MoM%** — Month-over-Month Growth
- **Net Sales QoQ%** — Quarter-over-Quarter Growth
- **Net Sales YoY%** — Year-over-Year Growth

These KPIs are used in the **Category Performance** and **Customer Performance** pages to compare current performance with previous periods.

---

## 🎯 Target-Based KPIs

The Overview page includes three user-controlled target parameters:

- **Profit Target**
- **Profit Margin Target**
- **Net Sales Target**

Users can define their own target values using the parameter controls.

The KPI cards dynamically evaluate actual performance against the selected targets using conditional formatting:

- 🟢 **Green** → Target achieved
- 🔴 **Red** → Target not achieved

This allows users to evaluate business performance based on their own objectives instead of fixed benchmarks.

---

# 📈 1. Business Overview

<img width="1190" height="670" alt="Business Overview" src="https://github.com/user-attachments/assets/33a30a18-1267-4851-bb87-239c642dfb4d" />

The **Overview** page provides a high-level view of the company's overall sales and profitability performance.

The page includes:

- **Sales**
- **Return Rate**
- **Total Cost**
- **Profit**
- **Profit Margin**

For the dashboard context shown, total sales are approximately **11.19M**, with a **9.81% return rate**, **5.31M total cost**, **5.88M profit**, and a **52.56% profit margin**.

---

## 📊 Sales Trend Analysis

The dashboard includes a **Net Sales by Year and Quarter** trend that allows users to track sales performance over time.

The trend helps identify:

- Changes in sales across different years
- Quarterly sales patterns
- Periods of growth and decline
- Overall sales direction

This provides users with a clear view of how sales performance changes over time.

---

## 🏷️ Sales by Category

The **Net Sales by Category** visual compares sales performance across the main product categories.

The dashboard allows users to compare categories such as:

- Accessories
- Bottoms
- Dresses
- Shoes
- Tops

This helps identify which product categories contribute the most to total sales.

---

## 🌍 Geographic Sales Analysis

A geographic visual is used to display sales performance across different cities.

This provides a spatial view of the business and allows users to understand how sales are distributed across locations.

The analysis can be filtered using the available report slicers.

---

## 🎛️ Dynamic Axis Parameters

The Overview page includes two dynamic parameters:

- **X-Axis**
- **Y-Axis**

Users can select different dimensions and measures to dynamically change the analysis.

This allows users to explore different relationships within the data without requiring separate visuals for every possible scenario.

For example, users can change the dimensions displayed on the chart and dynamically explore different business perspectives.

---

## 🎯 Target-Based KPI Analysis

The dashboard includes three user-controlled target parameters:

- **Profit Target**
- **Profit Margin Target**
- **Net Sales Target**

Users can define their own target values.

The KPI cards then compare actual performance with the selected targets.

Conditional formatting provides an immediate visual indication:

- 🟢 **Green** → Performance meets or exceeds the target
- 🔴 **Red** → Performance is below the target

This makes the dashboard more flexible for performance monitoring.

---

## 🎛️ Interactive Filters

Users can filter the Overview page using:

- **Date**
- **Category**
- **City**

The selected filters dynamically update the KPIs and visualizations.

This allows users to analyze performance for specific periods, categories, or locations.

---

# 🏷️ 2. Category Analysis

<img width="1183" height="661" alt="Category Analysis" src="https://github.com/user-attachments/assets/b95e337a-fe47-4122-887b-0a52fed40905" />

The **Category Analysis** page provides a detailed overview of product category performance.

The analysis focuses on:

- Sales by Category
- Profit by Category
- Returned Sales by Product
- Average Discount by Category

---

## 📊 Category Overview

The Category page includes the following KPIs:

- **Total Orders**
- **Total Quantity**
- **Top Selling Category**
- **Average Order Value (AOV)**
- **Average Quantity per Order**

Based on the dashboard context shown:

- Total Orders: approximately **10K**
- Total Quantity: approximately **26K**
- Top Selling Category: **Accessories**
- Average Order Value: approximately **224**
- Average Quantity per Order: approximately **3**

These KPIs provide a quick overview of category-related sales performance.

---

## 📈 Sales by Category

Sales are compared across the different product categories.

The analysis helps identify which categories contribute the most to total sales and allows users to compare their relative performance.

---

## 💰 Profit by Category

Profit is analyzed across categories to identify which product groups generate the highest financial contribution.

Comparing **Sales and Profit** provides a more complete understanding of category performance.

A category with high sales does not necessarily have the highest profitability, making this comparison useful for business decision-making.

---

## 🔄 Returned Sales by Product

Returned sales are analyzed at the **product level** to identify products associated with higher return quantities.

This provides an additional perspective on product performance beyond sales and profit.

It can help identify products that may require further investigation regarding product quality, sizing, customer expectations, or other potential factors.

---

## 🏷️ Average Discount by Category

The dashboard calculates the **average discount percentage** for each category.

This allows users to compare discount levels between categories and understand how discounting varies across the product portfolio.

---

# 🔎 3. Category Details

<img width="1184" height="663" alt="Category Details" src="https://github.com/user-attachments/assets/a7c4d6a6-96d2-42d0-a6a1-3b1eff14a85b" />

The **Category Details** page provides a deeper analysis of category performance over time and across multiple product attributes.

---

## 📈 Sales by Year and Category

A **Sales by Year and Category** waterfall visualization is used to analyze changes in sales over different years.

The visualization highlights:

- 📈 Categories contributing to sales increases
- 📉 Categories contributing to sales decreases
- Total yearly changes
- Category-level contribution to sales movement

This helps explain not only whether sales changed, but also **which categories contributed to those changes**.

---

## 🔬 Product Attribute Analysis

The dashboard provides a hierarchical analysis that allows users to explore sales through multiple product dimensions.

The analysis follows the hierarchy:

**Supplier → Season → Category → Color → Size → Product**

This allows users to drill down from overall sales into increasingly detailed product attributes.

Users can analyze:

- Sales by Supplier
- Sales by Season
- Sales by Category
- Sales by Color
- Sales by Size
- Sales by Product

This provides a detailed view of the factors contributing to overall sales performance.

---

## 🏭 Supplier Analysis

Sales can be analyzed by supplier to compare supplier contribution to total sales.

This allows users to identify suppliers associated with higher sales and then drill down into the products and categories contributing to their performance.

---

## 🌦️ Seasonal Analysis

Sales performance can be analyzed across different seasons:

- Fall
- Spring
- Summer
- Winter

This helps identify differences in customer demand and product performance throughout the year.

---

## 🎨 Color Analysis

The dashboard allows sales to be analyzed by product color.

This helps identify which colors contribute most to sales and provides an additional dimension for understanding product demand.

---

## 📏 Size Analysis

Product performance can be further analyzed by size, including:

- XS
- S
- M
- L
- XL

This provides additional insight into customer purchasing patterns and product demand.

---

# 📊 4. Category Performance

<img width="1186" height="665" alt="Category Performance" src="https://github.com/user-attachments/assets/4c0b8c1e-0000-0000-0000-000000000000" />

The **Category Performance** page focuses on evaluating category performance across different time periods.

> 📸 **Replace the image above with the actual Category Performance screenshot URL.**

The page includes:

- **Net Sales MTD**
- **Net Sales QTD**
- **Net Sales YTD**
- **Net Sales MoM%**
- **Net Sales QoQ%**
- **Net Sales YoY%**

These metrics allow users to evaluate both current performance and growth compared with previous periods.

---

## 📅 Period-Based Performance

The dashboard provides three main time-based sales measures:

### MTD — Month-to-Date

Measures sales generated from the beginning of the current month up to the selected date.

### QTD — Quarter-to-Date

Measures sales generated from the beginning of the current quarter up to the selected date.

### YTD — Year-to-Date

Measures sales generated from the beginning of the current year up to the selected date.

---

## 📊 Growth Analysis

The dashboard also calculates:

- **MoM%**
- **QoQ%**
- **YoY%**

These metrics help identify whether category performance is improving or declining compared with previous periods.

Conditional formatting makes positive and negative performance easier to identify.

---

# 👥 5. Customer Analysis

<img width="1186" height="662" alt="Customer Analysis" src="https://github.com/user-attachments/assets/6724d0eb-d25b-48f1-a02e-6a62c776a26b" />

<img width="1186" height="665" alt="Customer Analysis Detail" src="https://github.com/user-attachments/assets/c5197ac2-a89d-4ade-8d63-063d67731ba2" />

The **Customer Analysis** section focuses on understanding customer behavior and contribution to the business.

The dashboard includes:

- Total Customers
- Profit per Customer
- Net Sales for New Customers
- Sales by City
- Sales by Gender
- Customer-level analysis

---

## 🌍 Customer Distribution by City

The dashboard analyzes the number of customers across different cities.

The main cities include:

- Lisbon
- Faro
- Braga
- Coimbra
- Porto

This provides insight into the geographic distribution of the customer base.

---

## 💰 Sales by City

Sales performance is analyzed across cities to identify differences in geographic contribution.

Users can compare sales across different locations and identify the strongest-performing markets.

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

This allows the dashboard to show the impact of missing customer information on:

- Customer analysis
- Sales
- Customer segmentation
- Demographic analysis

---

# 📊 6. Customer Performance

<img width="1186" height="665" alt="Customer Performance" src="https://github.com/user-attachments/assets/c5197ac2-a89d-4ade-8d63-063d67731ba2" />

The **Customer Performance** page evaluates customer-related sales performance across different time periods.

The page uses:

- **Net Sales MTD**
- **Net Sales QTD**
- **Net Sales YTD**
- **Net Sales MoM%**
- **Net Sales QoQ%**
- **Net Sales YoY%**

Customer performance can be compared across different cities to identify locations with stronger or weaker growth.

---

## 🌍 City-Level Customer Performance

The dashboard allows users to compare customer-related sales performance across cities such as:

- Braga
- Coimbra
- Faro
- Lisbon
- Porto

This helps identify differences in current performance and growth between locations.

---

# 🏪 7. Store Analysis

<img width="1184" height="661" alt="Store Analysis" src="https://github.com/user-attachments/assets/e1cdd2af-de33-47ff-bb84-c67232227171" />

The **Store Analysis** section evaluates the performance of different stores and sales channels.

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

Total sales are compared across different stores and sales channels.

This helps identify the strongest-performing locations and understand their contribution to total sales.

---

## 📊 Profit by Store & Category

Profit performance is analyzed by combining:

- Store
- Category

This provides a detailed view of how different categories contribute to profitability within each store.

It also allows users to compare category profitability across locations.

---

## 🏷️ Sales by Store & Category

Sales are analyzed by combining **Store and Category**.

This provides a detailed view of how each product category contributes to sales within each store.

The analysis can help identify differences in product demand between locations.

---

## 🔄 Returned Sales by Store

Returned sales are analyzed across stores to provide an additional perspective on store performance.

Comparing returned sales with total sales provides additional context when evaluating store performance.

---

# 🎛️ Interactive Features

The dashboard includes several interactive features that allow users to explore the data dynamically.

## 🎚️ Slicers

Users can filter the report using slicers such as:

- **Date**
- **Category**
- **City**
- **Year**
- **Quarter**
- **Month**

The selected filters dynamically update KPIs and visualizations throughout the report.

---

## 🔄 Dynamic Axis Parameters

The report includes dynamic parameters that allow users to control the dimensions and measures used in visualizations.

Users can dynamically select:

- **X-Axis**
- **Y-Axis**

This makes the dashboard more flexible and reduces the need to create multiple separate visuals for different analysis scenarios.

---

## 🎯 Target Parameters

The report includes three user-defined target parameters:

- **Profit Target**
- **Profit Margin Target**
- **Net Sales Target**

Users can select their own target values and immediately see whether actual performance meets the selected targets.

---

## 🎨 Conditional Formatting

Conditional formatting is used throughout the dashboard to make performance easier to interpret.

For target-based KPIs:

- 🟢 **Green** → Target achieved
- 🔴 **Red** → Target not achieved

Conditional formatting is also used in performance tables to highlight positive and negative changes.

---

# 📊 Dashboard Analysis Coverage

The project provides analysis across multiple business dimensions.

| Analysis Area | Key Metrics / Dimensions |
|---|---|
| Overall Business | Sales, Cost, Profit, Profit Margin, Return Rate |
| Time Analysis | Year, Quarter, Month, MTD, QTD, YTD |
| Category | Sales, Profit, Quantity, Discount |
| Product | Product ID, Size, Color, Category |
| Customer | Customer Count, Sales, Gender, Age, City |
| Store | Sales, Profit, Returns, Category |
| Geography | City, Store Location |
| Supplier | Supplier Sales Contribution |
| Season | Seasonal Sales Performance |
| Returns | Returned Sales by Product and Store |

---

# 💡 Key Business Insights

Based on the dashboard analysis:

1. The business generated approximately **11.19M in total sales** in the dashboard context shown.

2. The business recorded approximately **5.88M in profit**, representing a **52.56% profit margin**.

3. The dashboard shows a **9.81% return rate**, making returned sales an important metric for evaluating business performance.

4. The customer analysis includes approximately **4K customers**.

5. **Lisbon** has the highest customer count among the displayed cities.

6. **Accessories** appears as the top-selling category in the Category Analysis page based on the displayed KPI.

7. Category performance differs across sales, profit, discount, and returned sales, demonstrating the importance of evaluating multiple KPIs rather than relying on sales alone.

8. Store performance is relatively close across the displayed stores and channels, making detailed **Store + Category** analysis useful for identifying performance differences.

9. Returned sales vary across products and stores, providing an additional dimension for evaluating business performance.

10. Some transactions have missing customer information, and these records are retained rather than removed to preserve the completeness of the sales analysis.

11. The dashboard's dynamic axis parameters allow users to explore different business dimensions without creating separate visuals for every possible combination.

12. Target-based KPI parameters allow users to evaluate business performance against their own selected targets.

13. Time-based performance metrics such as **MoM%, QoQ%, and YoY%** provide additional context for understanding category and customer performance trends.

---

# 📂 Power BI Analysis

The project demonstrates practical Power BI analysis covering:

- KPI Development
- Sales Analysis
- Profit Analysis
- Return Analysis
- Category Analysis
- Product Analysis
- Customer Analysis
- Store Analysis
- Supplier Analysis
- Seasonal Analysis
- Geographic Analysis
- Time-Based Analysis
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
- Interactive Dashboard Design

---

# 🚀 Conclusion

This project demonstrates how **Power BI** can be used to transform raw transactional clothing store data into an interactive Business Intelligence solution.

The project combines:

- **Data Cleaning**
- **Power Query**
- **DAX**
- **Data Modeling**
- **Star Schema**
- **KPIs**
- **Sales Analysis**
- **Profitability Analysis**
- **Category Analysis**
- **Customer Analysis**
- **Store Performance**
- **Returned Sales Analysis**
- **Time-Based Analysis**
- **Dynamic Parameters**
- **Target-Based Performance Monitoring**
- **Interactive Visualizations**

The dashboard allows users to move from a high-level business overview to detailed analysis of **categories, products, customers, and stores**.

The use of dynamic parameters, interactive slicers, conditional formatting, and target-based KPIs makes the report more flexible and suitable for business performance monitoring.

Overall, this project demonstrates practical skills in **Power BI, Power Query, DAX, Data Modeling, Business Intelligence, Data Visualization, and Business-Oriented Data Analysis**.
