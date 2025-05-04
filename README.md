# Task 7 - Basic Sales Summary Using SQLite and Python

## 🧠 Objective
Analyze basic sales data using SQLite and Python to get:
- Total quantity sold per product
- Total revenue generated per product
- A bar chart showing revenue by product

---

## 🛠️ Tools & Libraries Used
- **Python**
- **SQLite** (via `sqlite3` module)
- **Pandas** for data handling
- **Matplotlib** for chart visualization

---

## 📂 Files in this Repository
- `task7_script.py` — Main Python script for the task
- `sales_data.db` — SQLite database file created by the script
- `sales_chart.png` — Bar chart output image showing revenue per product
- `README.md` — This file

---

## 📝 SQL Query Used
```sql
SELECT 
    product, 
    SUM(quantity) AS total_qty, 
    SUM(quantity * price) AS revenue 
FROM sales 
GROUP BY product;
