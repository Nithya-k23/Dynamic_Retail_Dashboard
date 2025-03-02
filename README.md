## Dynamic Retail Dashboard

## Overview
The **Dynamic Retail Dashboard** is an interactive Excel dashboard that provides key insights into retail sales, profitability, and customer trends. The dataset is sourced from **GitHub-hosted tables** and transformed using **Power Query Editor**. The dashboard features **dynamic charts and KPI indicators**, allowing users to analyze sales trends, profit margins, and category-wise performance efficiently.

## Significance
- **Real-time Data Integration**: Fetches data from GitHub and updates dynamically.
- **Power Query Transformations**: Cleans and structures data for better analysis.
- **Dynamic KPI Table**: Enables interactive visualization of key performance indicators.
- **Comprehensive Analysis**: Covers sales, profit, product categories, and customer segmentation.

## Data Sources
The dataset consists of three tables:

### 1. Orders Table (Sample Data)
| Order ID | Returned | Order Date | Ship Date | Ship Mode | Customer ID | Customer Name | Segment | City | State | Country | Postal Code | Market | Region | Product ID | Category | Sub-Category | Product Name | Sales | Quantity | Discount | Profit | Profit Margin | Shipping Cost |
|----------|----------|------------|-----------|-----------|-------------|--------------|---------|------|-------|---------|-------------|--------|--------|------------|----------|--------------|--------------|-------|----------|----------|--------|--------------|--------------|
| MX-2011-131688 | Yes | 22-12-2019 | 26-12-2019 | Standard Class | BP-11230 | Benjamin Patterson | Consumer | Toluca | México | Mexico | LATAM | North | OFF-BI-10002799 | Office Supplies | Binders | Acco Binder Covers, Recycled | 36.48 | 4 | 0 | 3.28 | 0.039 | Medium |

### 2. People Table (Sample Data)
| Person | Region |
|--------|--------|
| Anna Andreadi | Central |
| Chuck Magee | South |
| Kelly Williams | East |

### 3. Return Table (Sample Data)
| Returned | Order ID | Market |
|----------|----------|--------|
| Yes | US-2013-122917 | LATAM |
| Yes | ES-2014-2439745 | EU |

---

## KPI Table
This table is used to create dynamic charts and metrics.

| KPI | Names | Symbols |
|----|-------|--------|
| Sum of Sales | Total Sales | 💰 |
| Sum of Profit | Total Profit | 📈 |
| Sum of Quantity | Total Quantity | 📦 |
| Count of Order ID | Total Orders | 🛒 |
| Sum of Profitability | Profitability | 💹 |

---
## Dashboard Development Steps

1.Connected GitHub repository to Excel using Power Query.

2.Loaded & cleaned data (handled missing values, transformed date formats, and removed duplicates).

3.Created relationships between Orders, People, and Returns tables.

4.Developed calculated fields for sales, profit, and performance metrics.

5.Designed an interactive dashboard with charts, slicers, and filters.

6.Incorporated dynamic KPIs using a KPI reference table.

---
## Steps to Solve Each Problem Statement

### 1. KPIs - Total Sales, Total Profit, Quantity, Number of Orders, Profit Margin
**Steps:**
1. Use `SUM` functions to calculate total sales, profit, and quantity.
2. Count unique Order IDs to get the number of orders.
3. Calculate profit margin as: `Profit Margin = (Profit / Sales) * 100`.
4. Store these metrics in the **KPI Table**.

### 2. Sales and Profit Analysis
**Steps:**
1. Create a **Pivot Table** with `Sales` and `Profit`.
2. Add `Region` and `Segment` as row fields.
3. Use **Conditional Formatting** to highlight high/low profit regions.
4. Create a **line chart** to analyze trends.

### 3. Category-wise Profit
**Steps:**
1. Group data by `Category`.
2. Calculate total `Profit` for each category.
3. Create a **bar chart** to visualize category-wise profit.

### 4. Segment-wise Sales Share %
**Steps:**
1. Group data by `Segment`.
2. Calculate segment-wise `Total Sales`.
3. Compute percentage share: `(Segment Sales / Total Sales) * 100`.
4. Use a **pie chart** for visualization.

### 5. Sales by Country
**Steps:**
1. Group sales data by `Country`.
2. Create a **geographical heatmap** using Excel’s map chart.
3. Highlight countries with the highest and lowest sales.

### 6. Top 5 Subcategories by Sales
**Steps:**
1. Sort the data by `Total Sales` in descending order.
2. Filter the **top 5 subcategories**.
3. Create a **bar chart** for visualization.

### 7. Bottom 5 Subcategories by Sales
**Steps:**
1. Sort the data by `Total Sales` in ascending order.
2. Filter the **bottom 5 subcategories**.
3. Create a **bar chart** to visualize.

### 8. Yearly Sales Trend
**Steps:**
1. Extract the `Year` from `Order Date` using Power Query.
2. Summarize sales by year.
3. Create a **line chart** to show the trend over time.

---

## Next Steps
Additional analysis can be performed on:
- **Return Analysis**: Identify frequently returned products.
- **Top Customers**: Find the highest spending customers.
- **Bottom Customers**: Identify customers with the lowest purchases.
- **Segment Analysis**: Compare different customer segments.
- **Market Analysis**: Assess sales performance across different markets.
- **Product Performance**: Analyze best and worst-performing products.

---

## How to Use This Dashboard

Download the Excel file with Power Query integration.

Ensure data connection is enabled to fetch the latest updates from GitHub.

Use slicers & filters to explore insights interactively.

Leverage KPIs & charts to drive business decisions.

---
## Visuals
This repository includes:

Visual examples for each solved problem statement.
Snapshots of the final dashboard with all components.

---

Conclusion

This Dynamic Retail Dashboard provides a comprehensive retail business analysis with interactive features and automated data updates. By leveraging Power Query and Excel visualizations, businesses can gain valuable insights and make informed decisions to improve performance and profitability.

## Conclusion
The **Dynamic Retail Dashboard** provides powerful insights into sales and profitability. Using **Power Query** for transformations and **dynamic charts**, it offers an interactive experience for users to explore key metrics. Future enhancements will include **return analysis** and **customer segmentation**.

---

📌 *Visuals for each problem statement will be added separately.*

