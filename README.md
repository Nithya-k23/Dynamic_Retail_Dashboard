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
Contains transactional details of orders, including customer information, product details, sales, and profit.
| Order ID | Returned | Order Date | Ship Date | Ship Mode | Customer ID | Customer Name | Segment | City | State | Country | Postal Code | Market | Region | Product ID | Category | Sub-Category | Product Name | Sales | Quantity | Discount | Profit | Profit Margin | Shipping Cost |
|----------|----------|------------|-----------|-----------|-------------|--------------|---------|------|-------|---------|-------------|--------|--------|------------|----------|--------------|--------------|-------|----------|----------|--------|--------------|--------------|
| MX-2011-131688 | Yes | 22-12-2019 | 26-12-2019 | Standard Class | BP-11230 | Benjamin Patterson | Consumer | Toluca | México | Mexico | LATAM | North | OFF-BI-10002799 | Office Supplies | Binders | Acco Binder Covers, Recycled | 36.48 | 4 | 0 | 3.28 | 0.039 | Medium |

### 2. People Table (Sample Data)
Contains details of personnel associated with different regions.
| Person | Region |
|--------|--------|
| Anna Andreadi | Central |
| Chuck Magee | South |
| Kelly Williams | East |

### 3. Return Table (Sample Data)
Contains information about returned orders.
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
- Goal: Compute total sales, total profit, quantity, number of orders, and profit margin.

**Steps:**
1. Create a Pivot Table using the Orders Table.
2. Use `SUM` functions to calculate total sales, profit, and quantity.
3. Count unique Order IDs to get the number of orders.
4. Calculate profit margin as: `Profit Margin = (Profit / Sales) * 100`.
5. Store these metrics in the **KPI Table**.

![kpi visual](https://github.com/user-attachments/assets/bb713537-db36-4bd9-bcdf-4d6e37afd6b0)



---

### 2. Sales and Profit Analysis
- Goal: Analyze overall sales and profit trends

**Steps:**
1. Use the Orders Table to create a new scatter plot.

2. Set the X-axis as "Sales" and Y-axis as "Profit".

3. Apply conditional formatting to highlight profit/loss zones.

4. Add dynamic slicers for Segment, Country, and Year.

5. Ensure filters allow switching between time periods dynamically.


![sales profit analysis](https://github.com/user-attachments/assets/4f61b8f8-c9b4-4c53-b0ec-5fce15702090)



---

### 3. Category-wise Profit
- Goal: Identify profitable product categories.

**Steps:**
1. Load the Orders Table into Power Query.

2. Group data by Category and calculate Total Profit per Category.

3. Insert a Pie Chart to display the share of each category in overall profit.

4. Add labels and percentages for better visualization.

5.Implement slicers for filtering by year, region, and segment.


![3 category wise profit](https://github.com/user-attachments/assets/137415f9-d860-4409-a54b-2f6e2f07f857)


---

### 4. Segment-wise Sales Share %
- Goal: Analyze contribution of each customer segment.

**Steps:**
1. Group data by `Segment`.
2. Calculate segment-wise `Total Sales`.
3. Compute percentage share: `(Segment Sales / Total Sales) * 100`.
4. Use a **Donut chart** for visualization.

![4 segmentwise total sales](https://github.com/user-attachments/assets/6a0b41fa-fa47-4696-9bb2-f46245824b84)


---

### 5. Sales by Country
- Goal: Compare sales performance across different countries.

**Steps:**
1. Group sales data by `Country`.
2. Create a **geographical heatmap** using Excel’s map chart.
3. Highlight countries with the highest and lowest sales.


![5 countrywise sales](https://github.com/user-attachments/assets/951be99a-e096-47b6-83aa-9ffc24b878e9)



---

### 6. Top 5 Subcategories by Sales
- Goal: Identify the best-performing subcategories.

**Steps:**
1. Sort the data by `Total Sales` in descending order.
2. Filter the **top 5 subcategories**.
3. Create a **bar chart** for visualization.

![6 top 5 sub category](https://github.com/user-attachments/assets/c4138ba6-64a8-4f4e-a184-1f772bc85469)



---

### 7. Bottom 5 Subcategories by Sales
- Goal: Identify the least-performing subcategories.

**Steps:**
1. Sort the data by `Total Sales` in ascending order.
2. Filter the **bottom 5 subcategories**.
3. Create a **bar chart** to visualize.

![7 bottom sub category](https://github.com/user-attachments/assets/421e69e5-a800-4263-b7bb-c3a80de49475)



---

### 8. Yearly Sales Trend
- Goal: Show sales growth trends over time.

**Steps:**
1. Extract the `Year` from `Order Date` using Power Query.
2. Summarize sales by year.
3. Create a **line chart** to show the trend over time.
4. Apply Trendlines for forecasting future sales.
   
![yearly](https://github.com/user-attachments/assets/a378ffd0-9b01-4df5-9428-50d898240673)



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

- Download the Excel file with Power Query integration.

- Ensure data connection is enabled to fetch the latest updates from GitHub.

- Use slicers & filters to explore insights interactively.

- Leverage KPIs & charts to drive business decisions.

---
## Visuals
This repository includes:

 - Visual examples for each solved problem statement.
 - Snapshots of the final dashboard with all components.

![dashb](https://github.com/user-attachments/assets/8b8a2f56-b6e4-4a81-b3a3-e3b625fd1c4e)

---

## Conclusion
The **Dynamic Retail Dashboard** provides powerful insights into sales and profitability. Using **Power Query** for transformations and **dynamic charts**, it offers an interactive experience for users to explore key metrics. Future enhancements will include **return analysis** and **customer segmentation**.

---

