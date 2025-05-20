# Elevate-labs-Task-6
# task6
#  Sales Trend Analysis Using SQL Aggregations
# Objective
This project analyzes **monthly revenue** and **order volume** from an `online_sales` database using SQL aggregation functions. The goal is to extract useful business insights such as which months had the highest sales and order volumes.
# Tools & Technologies
**SQL Database**: PostgreSQL / MySQL / SQLite
 **Tables Used**: `orders` (with `order_date`, `amount`, `product_id`, `order_id`)
# Analysis Performed
Extracted **month** and **year** from `order_date`.
 Calculated:
  Total Revenue` → `SUM(amount)`
  Order Volume` → `COUNT(DISTINCT order_id)`
 Grouped data by `year` and `month`.
 Sorted results in chronological or descending order.
  Limited results to specific time periods (e.g., past year).

---

# SQL Query (Sample)
```sql
SELECT
    EXTRACT(YEAR FROM order_date) AS year,
    EXTRACT(MONTH FROM order_date) AS month,
    SUM(amount) AS total_revenue,
    COUNT(DISTINCT order_id) AS order_volume
FROM
    orders
GROUP BY
    year, month
ORDER BY
    year, month;



[Screenshot 2025-04-29 111111.pdf](https://github.com/user-attachments/files/20349251/Screenshot.2025-04-29.111111.pdf),
[task 6 .zip](https://github.com/user-attachments/files/20349272/task.6.zip)



    
    
    

