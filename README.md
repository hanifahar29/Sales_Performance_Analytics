# 📊 Sales Performance Dashboard 

![Excel](https://img.shields.io/badge/Microsoft%20Excel-217346?style=flat-square&logo=microsoft-excel&logoColor=white)
![Power Query](https://img.shields.io/badge/Tool-Power_Query-orange?style=flat-square)
![Pivot Table](https://img.shields.io/badge/Feature-Pivot_Table-blue?style=flat-square)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=flat-square)

![EXCEL_E3Aq2iCuwU](https://github.com/user-attachments/assets/b13c6028-0685-49eb-97ad-85419511eb55)

## 🧭 Overview

This dashboard was created to help business managers and sales analysts track sales and profitability trends over the last 10 years (2013–2023). By using interactive filters for year, gender, product category, and country, users can analyze key metrics, identify top-performing products, and assess sales performance by geography and customer demographics.

It presents insights on:
- Total sales and profit over time
- Profit margin and total orders
- Monthly sales vs. profit trends
- Best-selling products and top countries by sales
- Profit distribution by product category
- Revenue contribution by customer age group

▶️ [Sales_Performance_Dashboard.xlsx](sales_bike2.xlxs) — this is the main file containing the interactive dashboard.


## 🗂️ Dataset Source

This project uses publicly available data from **Kaggle**:  
🔗 [Kaggle - Bike Sales Dataset](https://www.kaggle.com/code/sadiqshah/bike-store-sales-in-europe/data) 

### 📄 Dataset Description
The dataset contains sales transaction data from 2013–2023, including:
- 📅 Year — sales year for analysis
- 🧍 Gender — customer gender
- 🛍 Product Categories — Accessories, Bikes, Clothing
- 🌍 Countries — includes Australia, US, UK, France, Germany, and more
- 💰 Revenue — total sales revenue
- 📈 Profit — net profit from sales
- 📦 Orders — total number of orders
- 👥 Customer Age Groups — Youth, Young Adult, Adults, Seniors

## 📌 Excel Skills Use
This dashboard integrates PivotTables, Power Query, Data Model, and DAX Measures to produce dynamic KPIs and visual insights.
- **📊 PivotTables & PivotCharts** — to summarize and visualize KPIs  
- **🖱️ Slicers** — for interactive filtering by year and category  
- **📉 Chart Types**: Column, bar, line, KPI cards, and filled map charts  
- **📦 Data Model** — for efficient storage and relationship management
- **🧮 DAX Measures**: SUM(), DIVIDE(), calculated fields for margin, top N filtering
- **🔢 Formula** — for Map Chart compatibility

## 📊 Dashboard BUild Details

📌 **KPI Section**

<img width="463" height="260" alt="image" src="https://github.com/user-attachments/assets/f39e0156-b3ad-4c44-8d4b-3a5b68702f67" />

- **Metrics shown**: Total Revenue, Total Profit, Profit Margin %, Total Orders
- **Source**: Calculated via PivotTables from the Data Model
- **Purpose**: Provide at-a-glance performance indicators for the selected period.
  
📅 **Yearly Profit Trend**

<img width="629" height="244" alt="image" src="https://github.com/user-attachments/assets/cd232793-b7d8-4b36-97d6-543d6ab6398d" />

- **Type**: Bar Chart
- **Insight**: Annual profit has remained relatively stable, peaking in 2016 at $6.1M, with other years fluctuating between $5.7M and $6.0M. The steady performance suggests consistent market demand despite occasional dips.
-  **Logic**: Uses Date hierarchy in the PivotTable (Year grouping).

💰**Revenue vs. Profit per Month**

<img width="536" height="288" alt="image" src="https://github.com/user-attachments/assets/66f3b511-236c-4bdd-94dd-01ca3bc91ac5" />

- **Type**: Combination column & line chart
- **Insight**: Sales are highest in December, May, and July, indicating strong seasonal spikes likely tied to holiday demand and mid-year promotions. Profit trends follow a similar pattern, though with smaller fluctuations.
- **Logic**: Uses Date hierarchy in the PivotTable (Month-Year grouping).

📈**Profit by Category**

<img width="271" height="288" alt="image" src="https://github.com/user-attachments/assets/8021faea-31e3-4659-9364-b10108fdf99c" />

- **Type**: Pie Chart
- **Insight**: Bikes dominate profit generation, contributing 63.68% of total profit, while Clothing (27.50%) and Accessories (8.81%) provide smaller yet steady revenue streams, diversifying the sales portfolio.
- **Purpose**: Helps prioritize high-margin product categories.

🛍 **Best-Selling Products**

<img width="536" height="293" alt="image" src="https://github.com/user-attachments/assets/3803acbc-b39d-4b24-b0be-2d468bc4c119" />

- **Type**: Horizontal bar chart
- **Insight**: The Mountain-200 bike leads sales with $13.5M, followed by Road-150 and Sport-100 Helmet. High-value bikes consistently outperform accessories and apparel, showing strong demand in the premium cycling segment.
- **Sorting**: Highest to lowest revenue for quick comparison.

👥 **Revenue by Age Group**

<img width="269" height="284" alt="image" src="https://github.com/user-attachments/assets/32646f25-1055-45ae-8c70-fd5852bbb119" />

- **Type**: Donut chart
- **Insight**: Adults (49.39%) generate nearly half of total revenue, followed by Seniors (34.20%). Young Adults (15.77%) and Youth (0.64%) contribute less, highlighting opportunities for growth through targeted marketing toward younger demographics.
- **Purpose**: Identify top sales performers by group.

🌍 **Top Sales-Generating Country (Map)**

<img width="543" height="285" alt="image" src="https://github.com/user-attachments/assets/bacf7fe5-143a-4f34-8eee-8d6d74697475" />

- Type: Filled Map Chart
- Insight: The United States ($55.9M) and Australia ($42.6M) lead in sales revenue, followed by the United Kingdom, Germany, and France. Smaller markets may benefit from localized sales strategies to increase their share.
- Special Note: Requires helper table with IFERROR + MATCH + INDEX formula to ensure only valid country names and revenues appear after slicer filtering.
```excel
=IFERROR(
   IF(
      ISNUMBER(MATCH(J37, $J$3:$J$33, 0)),
      INDEX($K$3:$K$33, MATCH(J37, $J$3:$J$33, 0)),
      NA()
   ),
   NA()
)
```
## 🧩 Data Modeling Approach
Despite only using a single table, the Excel Data Model is employed to:
- Reduce workbook size via internal compression
- Enable dynamic PivotTables without duplicating tables
- Support potential future use of advanced DAX if needed

## 🎯 Conclusion

This Excel dashboard transforms raw sales data into actionable insights with interactive filters, clean visualizations, and KPI tracking.
Its mix of Data Model-driven PivotTables and formula-based map compatibility ensures both performance and visual clarity.
It’s ideal for executives and analysts who need to monitor revenue, profit trends, product performance, and regional contributions in one place.


## 📁 Notes

> 📌 All data used in this project is **sample data** from Kaggle and is intended for **portfolio purposes only**.
