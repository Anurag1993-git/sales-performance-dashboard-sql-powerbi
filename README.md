# sales-performance-dashboard-sqlserver-powerbi

Developed an interactive Sales Performance Dashboard using SQL and Power BI to analyze revenue, product trends, and regional performance, enabling data-driven business decisions.

## 📑 Table of Contents
- [Project Overview](#-project-overview)  
- [Business Problem](#-business-problem)  
- [Objectives](#-objectives)  
- [Dataset](#-dataset)  
- [Tools & Technologies](#-tools--technologies)  
- [Project Structure](#-project-structure)  
- [Data Model](#-data-model)  
- [SQL Queries](#-sql-queries)  
- [Dashboard Features](#-dashboard-features)  
- [Insights & Recommendations](#-insights--recommendations)  
- [Conclusion](#-conclusion)  

---

## 📝 Project Overview
The Sales Performance Dashboard provides insights into revenue, profit, customer behavior, and product performance using **SQL Server** for data cleaning/extraction and **Power BI** for visualization.  

---

## 💡 Business Problem
Businesses often lack **real-time visibility** into sales trends, top-performing products, and underperforming regions, which limits their ability to make **data-driven decisions**.  

---

## 🎯 Objectives
- Extract, clean, and transform sales data using SQL.  
- Design an interactive Power BI dashboard.  
- Track KPIs: revenue, profit, top products, and regional trends.  

---

## 📂 Dataset
The dataset includes transactional sales records with details on orders, customers, products, and sales teams.  

**Tables used**:  
- **Orders**: OrderID, CustomerID, ProductID, OrderDate, SalesAmount, Profit, Quantity  
- **Customers**: CustomerID, CustomerName, Region, Segment  
- **Products**: ProductID, Category, SubCategory, ProductName  
- **Salespersons**: SalespersonID, Name, Territory  

*(📌 You can add a link to your dataset here if it’s open-source or anonymized)*  

---

## 🛠️ Tools & Technologies
- **SQL Server** → Data cleaning, transformation, extraction  
- **Power BI** → Dashboard building & visualization  
- **Excel/CSV** → Dataset storage and import  

---

## 📂 Project Structure
📦 sales-performance-dashboard
┣ 📂 data # Dataset files (CSV/Excel)
┣ 📂 sql-scripts # SQL queries for cleaning & extraction
┣ 📂 Power BI # Power BI dashboard files
┣ 📂 images # Screenshots of dashboards
┗ 📜 README.md # Documentation

---

## 🗂️ Data Model
![Data Model](images/data_model.png)  

---

## 🧹 SQL Queries

### Data Cleaning
```sql
UPDATE Orders
SET SalesAmount = 0
WHERE SalesAmount IS NULL;
Data Extraction
sql
Copy
Edit
SELECT c.Region, SUM(o.SalesAmount) AS TotalSales
FROM Orders o
JOIN Customers c ON o.CustomerID = c.CustomerID
GROUP BY c.Region
ORDER BY TotalSales DESC;
📊 Dashboard Features
KPI Cards → Total Sales, Profit, Quantity

Time Analysis → Monthly revenue & profit trends

Regional Insights → Sales by region & customer segment

Product Analysis → Best vs. worst performing categories/products

Customer Insights → Top customers & contribution

Sales Team Performance → Territory and salesperson KPIs

🔎 Insights & Recommendations
Region A leads in revenue; Region C underperforms and improved sales reporting speed by 40%.

Category X dominates sales → prioritize stocking & promotion.

Top 10 customers generate ~40% revenue → diversify base.

Q4 shows seasonal spikes → align marketing campaigns.

✅ Conclusion
This project demonstrates how SQL + Power BI can turn raw sales data into actionable insights, empowering businesses to make smarter, data-driven decisions.

📫 Let's Connect
Anurag Kaushik (anuragkdatanalyst@gmail.com)
https://www.linkedin.com/in/anuragkaushik-analytics/
https://github.com/Anurag1993-git
https://www.datascienceportfol.io/anuragkaushik867

























