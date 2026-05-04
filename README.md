# 📊 E-Commerce Store Analysis Dashboard (Power BI)

![Power BI](https://img.shields.io/badge/Tool-PowerBI-yellow)
![DAX](https://img.shields.io/badge/Language-DAX-blue)
![Status](https://img.shields.io/badge/Project-Completed-brightgreen)
![Domain](https://img.shields.io/badge/Domain-ECommerce-orange)

---

## 🧩 Problem Statement
The goal of this project is to build an interactive Power BI dashboard to analyze an e-commerce store’s performance. The dashboard answers key business questions related to sales, products, customers, and regional trends, enabling data-driven decision-making.

---

## 🎯 Objectives
- Track overall sales and profit performance  
- Identify top-performing products and categories  
- Analyze customer purchasing behavior  
- Understand regional sales distribution  
- Build an interactive and user-friendly dashboard  

---

## 📂 Dataset Description

### 1. Orders Table
Contains customer and order-related details:
- Order ID  
- Order Date  
- Customer Name  
- State  
- City  

### 2. Details Table
Contains transactional data:
- Order ID  
- Amount (Sales)  
- Profit  
- Quantity  
- Category  
- Sub-Category  
- Payment Mode  

---

## 🔗 Data Modeling
- Relationship: Orders → Details using **Order ID**
- Type: One-to-Many  
- Schema: Star Schema  
  - Orders → Dimension Table  
  - Details → Fact Table  

---

## 🧮 DAX Measures

```DAX
Total Sales = SUM(Details[Amount])

Total Profit = SUM(Details[Profit])

Total Quantity = SUM(Details[Quantity])

Total Orders = DISTINCTCOUNT(Details[Order ID])

Total Customers = DISTINCTCOUNT(Orders[CustomerName])

🧹 Data Cleaning & Preparation
Removed null and duplicate values
Standardized column names
Converted data types (Date, Numeric)
Created Month-Year column for trend analysis
Ensured proper relationships between tables
📊 Dashboard Overview
📈 Overview Dashboard
KPI Cards (Sales, Profit, Orders, Quantity)
Sales Trend (Line Chart)
Category-wise Sales (Bar Chart)
Payment Mode Distribution (Donut Chart)
State-wise Sales (Map)
📦 Product Analysis Dashboard
Top Products (Bar Chart with Top N filter)
Sales vs Profit (Scatter Plot)
Category Contribution (Donut Chart)
👤 Customer Analysis Dashboard
Top Customers by Sales
Customer Distribution by State
Orders Trend
Orders by Category
🌍 Region Analysis Dashboard
Sales by State (Map)
Top States by Sales
Regional Sales Trend
Category-wise Regional Contribution
🎨 Dashboard Design
Clean and consistent UI across all pages
Left-side navigation panel
Active page highlighting
White card containers with shadow
Blue-themed professional color palette
Dropdown slicers for better user experience
🎛️ Features
Interactive slicers (Category, State, Customer, etc.)
Cross-filtering between visuals
Drill-down capabilities
Dynamic data updates
💡 Key Insights
Certain categories contribute the majority of revenue
Some products generate high sales but low profit
A small group of customers contributes significantly to sales
Sales are concentrated in specific regions
🛠️ Tools & Technologies
Power BI
DAX (Data Analysis Expressions)
Power Query
Data Modeling

📁 Project Structure

E-Commerce-Store-Analysis/
│
├── dataset/
│   ├── Orders.csv
│   ├── Details.csv
│
├── dashboard/
│   └── ECommerce_Dashboard.pbix
│
├── images/
│   ├── overview.png
│   ├── products.png
│   ├── customers.png
│   ├── regions.png
│
└── README.md

🚀 Project Outcome

This project demonstrates:

End-to-end data analysis workflow
Dashboard design and storytelling
Business insight generation using data

📌 Conclusion

This project showcases the ability to transform raw data into meaningful insights using Power BI. It reflects real-world business intelligence practices and is suitable for a professional data analytics portfolio.

⭐ Support

If you found this project useful, consider giving it a ⭐ on GitHub!

Avg Order Value = DIVIDE([Total Sales], [Total Orders], 0)

Avg Sales per Customer = DIVIDE([Total Sales], [Total Customers], 0)
