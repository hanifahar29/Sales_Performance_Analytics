# 📊 Sales Performance Dashboard (Excel)

![Excel](https://img.shields.io/badge/Microsoft%20Excel-217346?style=flat-square&logo=microsoft-excel&logoColor=white)
![Power Query](https://img.shields.io/badge/Tool-Power_Query-orange?style=flat-square)
![Pivot Table](https://img.shields.io/badge/Feature-Pivot_Table-blue?style=flat-square)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=flat-square)

## 🧾 Overview

The **Sales Performance Dashboard** is a business analytics project built using **Microsoft Excel**, combining **Power Query**, **Data Model**, and **Pivot Table** features. It visualizes key metrics such as revenue, profit, orders, and product performance across different countries, age groups, and time periods.

> 🖼️ **Dashboard Preview**  
> *(Includes KPIs, monthly trends, top-selling products, and sales breakdowns.)*

---

## 📌 Key Metrics

- **Total Revenue**: $170,542,016  
- **Total Profit**: $64,442,200  
- **Total Orders**: 226,072  
- **Total Quantity Sold**: 2,690,632  
- **Average Order Value**: $754.37  
- **Profit Margin**: 38%

---

## 🧩 Data Model

This project uses a **star schema** built in Excel’s **Data Model**, powered by **Power Query**. Below is a simplified structure:

### 🔹 Fact Table:
- **Sales**  
  Contains transactional data: Product ID, Quantity, Revenue, Cost, Profit, etc.

### 🔸 Dimension Tables:
- **Products** – Product details, category, subcategory  
- **Customers** – Customer demographic (e.g., age group)  
- **Date** – Month, year  
- **Region / Country** – Sales location  
- **Shipping Type** – Shipping method  

All tables are cleaned and transformed using **Power Query** before loading into the model.

---

## 📈 Dashboard Features

- 📅 Revenue & Profit by Month  
- 👤 Orders by Age Group  
- 🌍 Sales & Profit by Country/Region  
- 🛍️ Top 10 Selling Products  
- 📦 Orders by Shipping Type  
- 📊 KPI Overview with Dynamic Metrics

---

## ⚙️ Tools & Techniques

| Category          | Tools / Methods                        |
|-------------------|-----------------------------------------|
| Data Cleaning     | Power Query (Get & Transform)           |
| Data Modeling     | Excel Data Model & Relationships        |
| Analysis Engine   | Pivot Tables                            |
| Visualization     | Pivot Charts, Slicers, Conditional Formatting |
| File Format       | `.xlsx`                                 |

---

## 🗂️ Dataset Source

This project uses publicly available data from **Kaggle**:  
🔗 [Kaggle - Bike Sales Dataset](https://www.kaggle.com/)  
> *(Replace with actual dataset link if available.)*

---

## 🎯 Objective

To create a dynamic and interactive Excel dashboard that helps:
- Track sales and profit performance  
- Identify top products and customer segments  
- Support data-driven business decisions  
- Showcase data modeling and visualization skills in Excel  

---

## 📁 Notes

> 📌 All data used in this project is **sample data** from Kaggle and is intended for **educational and portfolio purposes only**.
