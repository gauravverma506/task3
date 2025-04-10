# Task 3: SQL for Data Analysis – Fitness Trackers Products Ecommerce

##  Objective
To extract, manipulate, and analyze data using SQL queries from a structured relational database simulating an ecommerce store selling fitness tracker products.

##  Tools Used
- **Database Engine:** MySQL / PostgreSQL / SQLite (choose based on availability)
- **SQL IDE:** MySQL Workbench / pgAdmin / SQLite Browser / DBeaver / VS Code (with SQL plugin)

---

##  Dataset
**Dataset Name:** `Ecommerce_SQL_Database`  
**Type:** Relational Database  
**Structure:** Contains multiple tables related to ecommerce transactions, including customers, orders, products, categories, etc.

---

##  Key SQL Concepts Applied

###  1. Basic Queries
- `SELECT`, `WHERE`, `ORDER BY` for filtering and sorting data

###  2. Aggregations
- Using `SUM()`, `AVG()`, `COUNT()`, `MAX()`, `MIN()` to summarize data
- Grouping data with `GROUP BY`

###  3. Joins
- `INNER JOIN`, `LEFT JOIN`, `RIGHT JOIN` to merge data from related tables

###  4. Subqueries
- Nesting queries for complex filters and calculations

###  5. Views
- Creating reusable named queries for reporting and dashboards

###  6. Indexing
- Implementing indexes to optimize performance on large queries

---

##  Deliverables

### 1. `ecommerce_queries.sql`
- All SQL queries used in this analysis
- Well-commented and organized by section (Basic Queries, Joins, Aggregations, etc.)

### 2. `screenshots/`
- Folder containing screenshots of query outputs and results

---

##  Learning Outcomes

By completing this task, the following skills were strengthened:
- Writing efficient and structured SQL queries
- Understanding relational data relationships
- Aggregating and analyzing data to extract insights
- Creating views and indexes for better performance and readability

---

##  Sample Query Snippets

```sql
-- Total revenue per product category
SELECT c.category_name, SUM(o.total_amount) AS revenue
FROM orders o
JOIN products p ON o.product_id = p.product_id
JOIN categories c ON p.category_id = c.category_id
GROUP BY c.category_name
ORDER BY revenue DESC;
