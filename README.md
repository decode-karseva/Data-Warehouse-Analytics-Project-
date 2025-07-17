# 📊 Data Warehouse Analytics Project (SQL-Based)

## 🔍 Overview

This project presents a structured data analysis pipeline using SQL on a simulated data warehouse. The dataset consists of a typical star schema with fact and dimension tables. The goal is to extract meaningful insights from transactional sales data through querying, exploration, and reporting.

---

## 🧱 Database Structure

The database is designed following a **star schema**:

- **Fact Table:**
  - `gold.fact_sales`: Stores transactional-level data including sales amount, product key, customer key, and date fields.

- **Dimension Tables:**
  - `gold.dim_products`: Product metadata such as name, category, and subcategory.
  - `gold.dim_customers`: Customer information including demographics and geography.
  - `gold.dim_date`: Calendar table for time-based analysis.

---

## 🎯 Objectives

1. **Explore** the structure of the data warehouse.
2. **Analyze** temporal patterns in order placements and customer age distribution.
3. **Rank** products and customers based on sales and order activity.
4. **Extract** key business insights using SQL window functions and aggregation logic.

---

## 📌 Key Analyses & Queries

### 1. **Database Exploration**
- Listing all tables and columns using `INFORMATION_SCHEMA`.

### 2. **Date-Based Analysis**
- Calculating the time range between first and last order.
- Determining the age of oldest and youngest customers using `DATEDIFF`.

### 3. **Dimension Exploration**
- Listing unique product categories and customer countries.

### 4. **Ranking & Performance**
- Top 5 products by revenue using `RANK()` and aggregate functions.
- Bottom 5 products and least active customers using `COUNT(DISTINCT ...)` and sorting.

---

## ⚙️ SQL Features & Techniques Used

- **Joins** (`INNER JOIN`, `LEFT JOIN`)
- **Aggregation** (`SUM`, `COUNT`, `AVG`)
- **Window Functions** (`RANK`, `ROW_NUMBER`)
- **Filtering & Sorting** (`WHERE`, `ORDER BY`, `GROUP BY`)
- **Information Schema Queries** to explore metadata
- **Date Calculations** using `DATEDIFF`, `MIN()`, `MAX()`

---

## 💡 Sample Insights

- Identified top-grossing products by analyzing revenue distribution.
- Ranked customers based on total revenue and number of distinct orders.
- Explored customer base by age and geography.
- Assessed order volume over time and potential seasonality (where applicable).

---

## 🛠️ Tools Used

- **Database**: MySQL Server 8.0
- **Query Editor**: MySQL Workbench
- **Data Format**: CSV files (imported via GUI)

---

## 📁 Project Folder Structure


