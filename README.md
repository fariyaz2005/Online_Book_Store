# Online Books Store — SQL Project

<img width="1458" height="635" alt="Online_book_store" src="https://github.com/user-attachments/assets/94f8a5a6-ae8c-4389-aac8-499a70abaad6" />

## Overview
This project is an Online Bookstore Database built using SQL.  
It includes 3 main tables (`Books`, `Customers`, and `Orders`) and 20 SQL questions — 11 Basic and 9 Advanced — each solved with queries.

The project is perfect for practicing SQL concepts like:
- SELECT, WHERE, GROUP BY, ORDER BY  
- JOINs, Aggregation, HAVING, and Subqueries  
- Basic to advanced analytical SQL tasks

---

## Database Schema

### Books Table
| Column | Type | Description |
|--------|------|-------------|
| Book_ID | SERIAL PRIMARY KEY | Unique ID for each book |
| Title | VARCHAR(100) | Book title |
| Author | VARCHAR(100) | Book author |
| Genre | VARCHAR(50) | Book genre/category |
| Published_Year | INT | Year published |
| Price | NUMERIC(10,2) | Book price |
| Stock | INT | Number of copies available |

### Customers Table
| Column | Type | Description |
|--------|------|-------------|
| Customer_ID | SERIAL PRIMARY KEY | Unique customer ID |
| Name | VARCHAR(100) | Customer name |
| Email | VARCHAR(100) | Customer email |
| Phone | VARCHAR(15) | Contact number |
| City | VARCHAR(50) | Customer’s city |
| Country | VARCHAR(150) | Customer’s country |

### Orders Table
| Column | Type | Description |
|--------|------|-------------|
| Order_ID | SERIAL PRIMARY KEY | Unique order ID |
| Customer_ID | INT | References Customers(Customer_ID) |
| Book_ID | INT | References Books(Book_ID) |
| Order_Date | DATE | Date of order |
| Quantity | INT | Quantity ordered |
| Total_Amount | NUMERIC(10,2) | Total cost of the order |

---

## How to Run
1. Open PostgreSQL (or MySQL).  
2. Run the `Online_Bookstore.sql` file to create all tables and insert data:
   ```sql
   \i /path/to/Online_Bookstore.sql
