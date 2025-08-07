
# Task 7S – Online Sales Data Analysis (MySQL)

This repository contains the SQL scripts and output related to analyzing an **online_sales** dataset using **MySQL Workbench**.

## 🗃️ Database Used
**Database Name:** `sales_db`

### 📦 Table: `online_sales`
This table stores order data including the date, amount, and product ID.

#### Table Schema:
```sql
CREATE TABLE online_sales (
    order_id INT,
    order_date DATE,
    amount DECIMAL(10,2),
    product_id INT
);
```

### 📝 Sample Data Inserted
```sql
INSERT INTO online_sales (order_id, order_date, amount, product_id)
VALUES 
(1, '2023-01-15', 100.50, 101),
(2, '2023-01-25', 250.00, 102),
(3, '2023-02-10', 120.75, 103),
(4, '2023-02-20', 135.00, 104),
(5, '2023-03-05', 300.00, 105);
```

---

## 📊 Query Used

To extract and summarize data, the following SQL was used:

```sql
SELECT 
    EXTRACT(YEAR FROM order_date) AS order_year,
    EXTRACT(MONTH FROM order_date) AS order_month,
    SUM(amount) AS monthly_revenue,
    COUNT(*) AS monthly_order_volume
FROM 
    online_sales
GROUP BY 
    order_year, order_month;
```

### ✅ Output:
| order_year | order_month | monthly_revenue | monthly_order_volume |
|------------|--------------|------------------|------------------------|
| 2023       | 1            | 350.50           | 2                      |
| 2023       | 2            | 255.75           | 2                      |
| 2023       | 3            | 300.00           | 1                      |

---

## 🛠 Tools Used
- **MySQL Workbench**
- **SQL (MySQL 8.0)**

---

## 📸 Screenshot
> The screenshot shows the SQL table creation, data insertion, and a query to extract monthly revenue and order volume.

---

## 📁 Folder Structure
```
📦task7s
 ┣ 📜README.md
 ┗ 📸 screenshot.png
```

---

## 📌 Purpose
This task demonstrates the ability to:
- Design a simple database table
- Insert sample data
- Use SQL aggregation functions
- Group data by month and year

---

## 🧠 Learning Outcome
- Gained hands-on experience with **EXTRACT**, **SUM**, **COUNT**, and **GROUP BY** in MySQL.
