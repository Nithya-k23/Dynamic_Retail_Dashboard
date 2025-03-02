# Dynamic_Retail_Dashboard
Dynamic Retail Dashboard in Excel.
Dynamic Retail Dashboard

Overview

The Dynamic Retail Dashboard is an interactive Excel-based dashboard that provides insightful retail analytics using data transformation and visualization techniques. The dashboard connects to a GitHub-hosted dataset, performs transformations in Power Query Editor, and dynamically visualizes key retail metrics.

Significance

This dashboard is designed to help businesses analyze their sales, profitability, and order trends efficiently. By leveraging Power Query, Excel formulas, and dynamic charts, it enables data-driven decision-making for retail performance optimization.

Data Sources

The dashboard integrates data from three primary tables:

Orders Table: Contains transactional details such as order date, customer name, category, subcategory, sales, profit, and order region.

People Table: Stores information about individuals and their respective regions.

Return Table: Identifies returned orders.

Sample Data:

Orders Table:

Order ID       | Returned | Order Date  | Ship Date  | Ship Mode     | Customer ID | Customer Name         | Segment   | City      | State        | Country       | Postal Code | Region | Category         | Sub-Category | Product Name                                     | Sales | Quantity | Discount | Profit | Profit Margin | Priority
MX-2011-131688 | Yes      | 22-12-2019  | 26-12-2019 | Standard Class | BP-11230    | Benjamin Patterson    | Consumer  | Toluca    | México       | Mexico        | LATAM       | North  | Office Supplies | Binders      | Acco Binder Covers, Recycled                    | 36.48 | 4        | 0        | 3.28   | 0.039        | Medium
...

People Table:

Person                 | Region
Anna Andreadi         | Central
Chuck Magee          | South
Kelly Williams       | East
Matt Collister       | West
...

Return Table:

Returned | Order ID         | Region
Yes      | US-2013-122917   | LATAM
Yes      | ES-2014-2439745  | EU
Yes      | CA-2012-134075   | United States
...
Steps to Create the Dashboard

Load Data into Excel

Connect the Orders, People, and Returns tables from the GitHub repository.

Use Power Query to clean and transform the data.

Transform Data Using Power Query

Remove duplicates and inconsistencies.

Standardize date formats and column names.

Merge the Orders and Returns tables using Order ID.

Create KPI Metrics

Calculate Total Sales, Profit, Quantity, Order Count, and Profit Margin.

Store these in a separate KPI Table with icons for visual clarity.

Build Visualizations & Interactivity

Use Pivot Tables and Pivot Charts for dynamic reports.

Apply slicers to filter data based on Region, Category, and Segment.

Finalize Dashboard Design

Arrange charts and tables in an intuitive layout.

Add headers, tooltips, and conditional formatting for better readability.

Problem Statements & Step-by-Step Solutions

1. KPI Metrics Calculation

Goal: Compute total sales, total profit, quantity, number of orders, and profit margin.
Steps:

Create a Pivot Table using the Orders Table.

Use SUM function to calculate Total Sales, Total Profit, and Total Quantity.

Use COUNT function to count Order IDs.

Compute Profit Margin = (Total Profit / Total Sales) * 100.

![image](https://github.com/user-attachments/assets/3670d554-3e90-410c-8cea-c774c723c723)


2. Sales & Profit Analysis

Goal: Analyze overall sales and profit trends.
Steps:

Insert a Pivot Chart to visualize sales and profit.

Apply a slicer for Year, Region, and Category to filter data dynamically.

Use Conditional Formatting to highlight positive and negative trends.

![image](https://github.com/user-attachments/assets/d868d5e1-e3fb-449a-9ce8-bf59a1c421da)



3. Category-Wise Profit

Goal: Identify profitable product categories.
Steps:

Create a Pivot Table with Category as Row and Sum of Profit as Values.

Sort categories from highest to lowest profit.

Use a bar chart for better visualization.

![image](https://github.com/user-attachments/assets/aff99556-d090-49d7-a868-382ed963eb98)


4. Segment-Wise Sales Share

Goal: Analyze contribution of each customer segment.
Steps:

Create a Pie Chart using Segment-wise Sum of Sales.

Use Data Labels to show percentage share.

![image](https://github.com/user-attachments/assets/4b52c1ea-d219-4cc2-aabd-7f6ebf92f9a3)


5. Sales by Country

Goal: Compare sales performance across different countries.
Steps:

Use a Geo Map Chart in Excel (Power BI alternative).

Plot Sum of Sales by Country.

Use color coding to highlight high and low sales regions.

![image](https://github.com/user-attachments/assets/f46c553d-3f73-4a0a-99d7-c5290d4a0741)


6. Top 5 Subcategories

Goal: Identify the best-performing subcategories.
Steps:

Create a Pivot Table with Sub-Category as Row and Sum of Sales as Values.

Sort data in descending order and select the top 5.

Visualize using a bar chart.

![image](https://github.com/user-attachments/assets/360484f6-6285-4b55-ae8a-2ee2beff2479)


7. Bottom 5 Subcategories

Goal: Identify the least-performing subcategories.
Steps:

Follow the same steps as above but sort in ascending order.

Highlight negative profit margins using Conditional Formatting.

![image](https://github.com/user-attachments/assets/da1298c5-4736-4fe0-beb7-32968756f191)


8. Yearly Sales Trend

Goal: Show sales growth trends over time.
Steps:

Create a Pivot Table with Order Date (Year) as Rows and Sum of Sales as Values.

Plot a Line Chart to show yearly trends.

Apply Trendlines for forecasting future sales.

![image](https://github.com/user-attachments/assets/861daa42-9e13-41eb-82a3-c6c459e126ba)


Dynamic Features

✅ Interactive slicers for filtering by Year, Region, Segment, and Category.
✅ KPI Table with icons for quick insights.
✅ Conditional Formatting for profitability trends.
✅ Dynamic Charts that update with data changes.

Future Enhancements

Return Analysis to understand product return trends.

Top & Bottom Customers to identify loyal and at-risk customers.

Market Analysis for country-wise performance.

Product Analysis for identifying fast-moving items.

Integration with Power BI for advanced visualization.

Conclusion

The Dynamic Retail Dashboard is a powerful tool for retail analytics, offering deep insights into sales, profit, and customer behavior. By integrating data from various sources and applying Power Query transformations, this dashboard provides real-time analysis, helping businesses make data-driven decisions.

