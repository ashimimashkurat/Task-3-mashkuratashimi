# 📊 E-Commerce Sales Analysis Using SQL

## 📌 Project Overview

This project demonstrates how SQL can be used to analyze e-commerce sales data. It covers database creation, data insertion, filtering, sorting, aggregation, and reporting techniques commonly used in data analytics.

The goal is to gain practical experience with SQL queries while extracting meaningful business insights from sales transactions.

---

## 🛠️ Technologies Used

- SQL
- MySQL
- DB Browser for SQLite / MySQL Workbench

---

## 📂 Database Schema

### Table: `ecommerce_project`

| Column Name | Data Type |
|------------|------------|
| OrderID | VARCHAR(20) |
| CustomerID | VARCHAR(20) |
| Product | VARCHAR(100) |
| Category | VARCHAR(50) |
| Quantity | INT |
| UnitPrice | DECIMAL(10,2) |
| TotalPrice | DECIMAL(10,2) |
| PaymentMethod | VARCHAR(50) |
| OrderStatus | VARCHAR(50) |
| ItemsInCart | INT |
| CouponCode | VARCHAR(50) |
| ReferralSource | VARCHAR(50) |

---

## 📋 SQL Queries Performed

### 1. View All Records

```sql
SELECT *
FROM ecommerce_project;
```

### 2. Display Product Sales Details

```sql
SELECT OrderID, Product, Quantity, TotalPrice
FROM ecommerce_project;
```

### 3. Find High-Value Orders

```sql
SELECT OrderID, TotalPrice
FROM ecommerce_project
WHERE TotalPrice > 1000;
```

### 4. Sort Orders by Revenue

```sql
SELECT OrderID, TotalPrice
FROM ecommerce_project
ORDER BY TotalPrice DESC;
```

### 5. Analyze Payment Methods

```sql
SELECT PaymentMethod,
       COUNT(*) AS TotalOrders
FROM ecommerce_project
GROUP BY PaymentMethod;
```

### 6. Count Total Records

```sql
SELECT COUNT(*) AS TotalRecords
FROM ecommerce_project;
```

### 7. Calculate Total Sales

```sql
SELECT SUM(TotalPrice) AS TotalSales
FROM ecommerce_project;
```

### 8. Calculate Average Order Value

```sql
SELECT AVG(TotalPrice) AS AverageOrderValue
FROM ecommerce_project;
```

---

## 📈 Results

| Metric | Value |
|---------|---------|
| Total Records | 3 |
| Total Sales | 2551.00 |
| Average Order Value | 850.33 |
| Highest Order Value | 1200.00 |

### Payment Method Distribution

| Payment Method | Total Orders |
|---------------|--------------|
| Credit Card | 1 |
| Debit Card | 1 |
| Cash | 1 |

---

## 🔍 Key Insights

- Total revenue generated from all orders is **2551.00**.
- The average order value is **850.33**.
- The highest-value order was **1200.00**.
- Electronics products generated the highest sales revenue.
- All payment methods were used equally in the sample dataset.
- High-value orders can be easily identified using SQL filtering techniques.

---

## 🎯 Skills Demonstrated

- Database Design
- Data Insertion
- Data Retrieval
- Filtering Data with WHERE
- Sorting Data with ORDER BY
- Aggregation Functions (COUNT, SUM, AVG)
- Grouping Data with GROUP BY
- Business Data Analysis
- SQL Reporting

---

## 📁 Project Structure

```text
Ecommerce-Sales-Analysis/
│
├── ecommerce_sales_analysis.sql
├── README.md
└── screenshots/
    ├── sql_script.png
    └── results.png
```

---

## 🚀 Future Enhancements

- Add more sales records for deeper analysis
- Analyze sales by product category
- Track monthly revenue trends
- Customer segmentation analysis
- Coupon effectiveness analysis
- Build an interactive dashboard using Power BI or Tableau

---

## 👨‍💻 Author

--- Mashkurat Ashimi 

If you found this project helpful, consider giving it a ⭐ on GitHub.
