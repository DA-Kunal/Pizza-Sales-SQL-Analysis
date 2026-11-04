# 🍕 Pizza Sales SQL Data Analytics Project

A comprehensive data analytics project examining a pizza restaurant's sales operations. This project leverages **Advanced SQL** (joins, subqueries, and window functions) in **MySQL** to extract critical business insights, analyze product performance, track revenue trends, and evaluate category-wise distribution.
---

## 🚀 1. Project Overview
Understanding customer purchasing habits and operational capacity is vital for restaurant optimization. This project analyzes a transactional dataset comprising orders, product pricing, and category types to answer high-level business questions, optimize inventory stocking, and pinpoint menu revenue drivers.

> **Project Preview Banner:**  
> ![Pizza Sales Data Title Slide](Title%20Page.png) 

---

## 🗄️ 2. Entity-Relationship (ER) Diagram & Schema
The relational database structure consists of four core tables:
* **`pizza_types`**: Stores descriptive item details including name, category, and ingredient lists.
* **`pizzas`**: Maps individual size variations (Small, Medium, Large, XL, XXL) and prices to each pizza type.
* **`orders`**: Captures transaction timestamps (`order_date`, `order_time`).
* **`order_details`**: Acts as a junction table linking specific orders to exact pizza variants and quantities ordered.

> **Database Schema Architecture:**  
> ![ER Diagram](ER$diagram.png) *(Replace with your database schema slide image)*

---

## 🎯 3. Business Requirements & Objectives
Management outlined specific key performance indicators (KPIs) and analytical requirements:
1. **Operational Metrics:** Calculate total order volumes and daily average production demands.
2. **Product Performance:** Identify top-selling items by quantity ordered and total revenue contribution.
3. **Category Analysis:** Evaluate which product categories (Chicken, Classic, Supreme, Veggie) drive the highest volume and variety.
4. **Advanced Financial Tracking:** Monitor cumulative revenue growth over time and segment top performers dynamically within categories using window functions.

---

## 🛠️ 4. SQL Solutions & Technical Implementation

Here is a breakdown of how key business requirements were solved using SQL queries:

### Query 1: Total Order Volume & High-End Pricing
* **Business Goal:** Understand total transaction scale and find the premium ceiling of the menu.
* **SQL Implementation:**
  ```sql
  -- Retrieve total orders placed
  SELECT COUNT(*) AS total_order_placed 
  FROM orders;
