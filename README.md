# Grocery_Store_Management

A SQL-based project that simulates a real-world **Grocery Store Management System**
using **MySQL Workbench**.

This project focuses on designing a **relational database schema** and performing
SQL-based analysis on grocery store operations including customers, products,
suppliers, employees, and orders.

The system enables structured data storage, relationship management, and analytical
querying for business insights.

## Project Objective

The objective of this project is to design and implement a relational
database system for managing grocery store operations. The project
demonstrates database design principles, table relationships,
data integrity constraints, and SQL-based analytical queries to
extract business insights.

## Sample SQL Queries

Example queries used in this project:

-- Total orders placed by each customer
SELECT customer_id, COUNT(order_id) AS total_orders
FROM orders
GROUP BY customer_id;

-- Total sales per product
SELECT p.product_name, SUM(od.quantity * od.price) AS total_sales
FROM order_details od
JOIN products p ON od.product_id = p.product_id
GROUP BY p.product_name;

##  Key Features

- Normalized relational database schema with **7 interconnected tables**
- Proper use of **primary keys and foreign keys**
- Cascading updates and deletes to maintain data integrity
- Realistic sample data for practical analysis:
  - 200 customers across Indian cities
  - 50 grocery products (grains, spices, dairy, household items)
  - 300 orders and 600 order detail records
- SQL queries for business-oriented insights and reporting


##  Database Tables

- `categories`
- `supplier`
- `products`
- `customers`
- `employees`
- `orders`
- `order_details`

All tables are linked through foreign key relationships to ensure
**referential integrity**.


##  ER Diagram

The ER Diagram represents the complete database structure and relationships
between entities such as products, orders, customers, and suppliers.

The ER diagram was generated using **MySQL Workbench reverse engineering**
based on the implemented schema.

Included files:
- `ERD.mwb`
- 
## Core Analyses Performed

| Analysis Category      | Key Insights Generated |
|------------------------|------------------------|
| Customer Insights      | Unique customers, repeat orders, order frequency |
| Product Performance    | Category-wise products, average price, sales volume |
| Sales Trends           | Total orders, order dates, basic revenue trends |
| Supplier Contribution  | Products supplied and sales contribution |
| Order Deep Dive        | Quantity vs price analysis, order-level details |


##  Technologies & Setup

- **Database**: MySQL 8.0  
- **Tool**: MySQL Workbench  
- **Language**: SQL (DDL, DML, Joins, Aggregations)  
- **Data Source**: CSV files  

### Setup Process:
1. Created database schema using SQL DDL statements
2. Defined relationships using foreign key constraints
3. Imported CSV data using **Table Data Import Wizard**
4. Verified data using SELECT queries
5. Performed analytical queries using JOIN, GROUP BY, COUNT, SUM, AVG


## Author

**Nagavaram Sri Varshini**

Email: varshinirao1815@gmail.com  
LinkedIn: https://www.linkedin.com/in/varshini-nagavaram-134779254/


