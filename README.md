# 📚 Online Bookstore SQL Project

## 📌 Project Overview

This project analyzes an online bookstore database using **PostgreSQL**.

The database contains information about:

* Books
* Customers
* Orders

The project demonstrates SQL skills including data filtering, aggregation, joins, grouping, subqueries, and inventory analysis.

---

## 🛠️ Tools & Technologies

* **Database:** PostgreSQL
* **Language:** SQL
* **Data Format:** CSV
* **Version Control:** Git & GitHub

---

## 🗂️ Database Schema

The project contains three main tables:

### 1. BOOKS

| Column         | Description             |
| -------------- | ----------------------- |
| BOOK_ID        | Unique ID of the book   |
| TITLE          | Book title              |
| AUTHOR         | Book author             |
| GENRE          | Book genre              |
| PUBLISHED_YEAR | Publication year        |
| PRICE          | Book price              |
| STOCK          | Available/initial stock |

### 2. CUSTOMERS

| Column      | Description        |
| ----------- | ------------------ |
| CUSTOMER_ID | Unique customer ID |
| NAME        | Customer name      |
| EMAIL       | Customer email     |
| PHONE       | Customer phone     |
| CITY        | Customer city      |
| COUNTRY     | Customer country   |

### 3. ORDERS

| Column       | Description                   |
| ------------ | ----------------------------- |
| ORDER_ID     | Unique order ID               |
| CUSTOMER_ID  | Customer who placed the order |
| BOOK_ID      | Book ordered                  |
| ORDER_DATE   | Date of order                 |
| QUANTITY     | Number of books ordered       |
| TOTAL_AMOUNT | Total order amount            |

---

## 🔗 Relationships

The database uses foreign keys to connect the tables.

```text
CUSTOMERS
    |
    | CUSTOMER_ID
    |
    v
ORDERS
    |
    | BOOK_ID
    |
    v
BOOKS
```

* One customer can place multiple orders.
* A book can appear in multiple orders.
* Each order references one customer and one book.

---

## 🔎 SQL Analysis Performed

### Basic Analysis

The project answers questions such as:

1. Retrieve books from the Fiction genre.
2. Find books published after 1950.
3. Find customers from Canada.
4. Retrieve orders from November 2023.
5. Calculate total available stock.
6. Find the most expensive book.
7. Find orders containing more than one book.
8. Find orders above $20.
9. List available genres.
10. Find the book with the lowest stock.
11. Calculate total revenue.

### Advanced Analysis

The project also analyzes:

1. Total books sold by genre.
2. Average price of Fantasy books.
3. Customers with at least two orders.
4. Most frequently ordered book.
5. Top three most expensive Fantasy books.
6. Books sold by each author.
7. Customers who spent more than $30.
8. Highest-spending customer.
9. Remaining stock after fulfilling orders.

---

## 📁 Project Structure

```text
online-bookstore-sql-project/
│
├── README.md
│
├── sql/
│   ├── 01_create_tables.sql
│   ├── 02_import_data.sql
│   ├── 03_basic_queries.sql
│   └── 04_advanced_queries.sql
│
├── data/
│   ├── Books.csv
│   ├── Customers.csv
│   └── Orders.csv
│
└── screenshots/
    ├── database_tables.png
    ├── basic_queries.png
    └── advanced_queries.png
```

---

## ▶️ How to Run the Project

### Step 1: Create the database

```sql
CREATE DATABASE BOOKSTORE;
```

### Step 2: Connect to the database

```sql
\c BOOKSTORE
```

### Step 3: Create the tables

Run:

```text
sql/01_create_tables.sql
```

### Step 4: Import the CSV data

Run:

```text
sql/02_import_data.sql
```

Update the CSV file paths according to your local PostgreSQL setup.

### Step 5: Run the analysis

Execute:

```text
sql/03_basic_queries.sql
```

and

```text
sql/04_advanced_queries.sql
```

---

## 💡 SQL Concepts Demonstrated

This project demonstrates:

* `SELECT`
* `WHERE`
* `ORDER BY`
* `LIMIT`
* `DISTINCT`
* `BETWEEN`
* `SUM()`
* `AVG()`
* `COUNT()`
* `GROUP BY`
* `HAVING`
* `INNER JOIN`
* `LEFT JOIN`
* `COALESCE()`
* Aggregate functions
* Foreign keys
* Primary keys
* Data import using CSV
* Inventory calculations

---

## 🎯 Project Objective

The objective of this project is to demonstrate how SQL can be used to analyze bookstore data and answer business-related questions involving:

* Sales
* Revenue
* Customers
* Books
* Genres
* Authors
* Orders
* Inventory

---

## 📌 Key Takeaway

This project provides practical experience in querying a relational database and transforming raw bookstore data into useful business insights using PostgreSQL and SQL.
