# 🍕 Pizza Sales Analysis using SQL Workbench

### 📌 Project by: [Utkarsh Singh Rawat](https://www.linkedin.com/in/utkarsh-singh-rawat)

---

## 📖 Overview

This project aims to analyze a pizza sales dataset using **SQL Workbench** to extract meaningful business insights. Through structured SQL queries, I explored order trends, sales performance, and revenue distribution.

---

## 🧰 Tools & Technologies

- **SQL Workbench** – Querying and data analysis
- **CSV Files** – Data source
- **Excel** – Data inspection and preview
- **GitHub** – Project documentation

---

## 🗃️ Datasets Used

The analysis was based on four interconnected CSV files:

| Table Name         | Description                                                      |
|--------------------|------------------------------------------------------------------|
| `orders`           | Order metadata with timestamps                                   |
| `order_details`    | Itemized list of pizzas per order with quantities                |
| `pizzas`           | Pizza price and size details linked by pizza ID                 |
| `pizza_types`      | Pizza names, categories, and ingredients                         |

---

## 🧩 Database Schema

```plaintext
orders (order_id, order_date, order_time)
    ⬇ (one-to-many)
order_details (order_detail_id, order_id, pizza_id, quantity)
    ⬇ (many-to-one)
pizzas (pizza_id, pizza_type_id, size, price)
    ⬇ (many-to-one)
pizza_types (pizza_type_id, name, category, ingredients)
