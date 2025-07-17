# SQL Data Warehouse Analytics Project

##  Overview

This project involves a structured analysis of sales data using SQL on a data warehouse designed with a **star schema**. The goal is to derive key business insights by exploring, querying, and summarizing transactional data. The focus is on sales performance, customer behavior, and product categorization.

---

##  Database Structure

The database follows a star schema model and contains:

- **Fact Table:**
  - `gold.fact_sales`: Core transactional data including order details, sales amount, quantity, product/customer keys, and date fields.

- **Dimension Tables:**
  - `gold.dim_products`: Metadata on products including name, category, and subcategory.
  - `gold.dim_customers`: Customer demographic and geographic information.

---

## Objectives

1. Explore and understand the structure and content of the database.
2. Perform temporal and categorical analysis using SQL.
3. Rank and evaluate customers and products based on sales metrics.
4. Apply SQL functions to answer business-driven analytical questions.

---

##  Key Analyses & Queries

### 1. **Database Metadata Exploration**
- List all tables using `INFORMATION_SCHEMA.TABLES`.
- Inspect column-level metadata with `INFORMATION_SCHEMA.COLUMNS`.

### 2. **Dimension Exploration**
- Extract unique countries from customer data.
- List all product categories, subcategories, and product names.

### 3. **Date-Based Exploration**
- Determine the range of sales orders (first vs last).
- Filter out invalid dates (`'0000-00-00'`) to avoid strict mode errors.

### 4. **Customer Age Profiling**
- Identify the oldest and youngest customers using `MIN()` and `MAX()` on `birthdate`.

### 5. **Performance Ranking**
- Identify top-performing products using `RANK()` and `SUM(sales_amount)`.
- Find the least active customers or products based on order count.

---

##  SQL Features Used

- **JOINs** (inner and left joins)
- **Aggregation** (`SUM`, `COUNT`, `AVG`)
- **Window Functions** (`RANK`, `ROW_NUMBER`)
- **Filtering** and **Grouping**
- **Date calculations** with `MIN()`, `MAX()`, and `DATEDIFF` (or manual logic for MySQL)

---

##  Sample Insights

- Products in specific categories consistently outperform others in revenue.
- A small subset of customers accounts for a large portion of total sales.
- There are irregularities in order dates that need cleansing before analysis.

---

## 🛠 Tools Used

- **SQL Engine**: MySQL Server 8.0
- **Interface**: MySQL Workbench
- **Data Format**: CSV files (imported via GUI)

---

## Project Structure

