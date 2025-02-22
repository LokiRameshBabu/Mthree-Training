# SQL Guide

## Introduction
SQL (Structured Query Language) is a powerful tool used for managing and manipulating relational databases. It enables users to store, retrieve, and manipulate data efficiently in an organized manner.

## Types of SQL
SQL is categorized into five main types:
1. **DDL (Data Definition Language)** – Defines and modifies database structure.
2. **DML (Data Manipulation Language)** – Manages data within schema objects.
3. **DCL (Data Control Language)** – Handles permissions and access control.
4. **TCL (Transaction Control Language)** – Manages transactions within a database.
5. **DQL (Data Query Language)** – Performs queries to retrieve data.

---

## DDL (Data Definition Language)
DDL is used to define, modify, and manage database schema objects such as tables, views, and indexes.

### DDL Commands:
- **CREATE** – Creates a new database object (table, index, function, view, etc.)
  ```sql
  CREATE TABLE table_name (
      column1 data_type,
      column2 data_type,
      ...
  );
  ```
- **DROP** – Deletes an existing object from the database
  ```sql
  DROP TABLE table_name;
  ```
- **ALTER** – Modifies the structure of a table
  ```sql
  ALTER TABLE table_name ADD COLUMN column_name data_type;
  ```
- **TRUNCATE** – Removes all records from a table while retaining its structure
  ```sql
  TRUNCATE TABLE table_name;
  ```
- **RENAME** – Changes the name of an existing table
  ```sql
  RENAME TABLE old_table_name TO new_table_name;
  ```

---

## DQL (Data Query Language)
DQL is used to retrieve data from a database using queries.

### DQL Command:
- **SELECT** – Extracts data from one or more tables
  ```sql
  SELECT column1, column2 FROM table_name WHERE condition;
  ```

---

## Cloning in SQL
Cloning is used to create duplicate tables for testing or backup purposes.
1. **Simple Cloning:** Copies both structure and data but does not preserve constraints like primary keys and indexes.
   ```sql
   CREATE TABLE STUDENT_COPY AS SELECT * FROM STUDENT;
   ```
2. **Shallow Cloning:** Copies only the table structure without copying data.
   ```sql
   CREATE TABLE clone_table LIKE original_table;
   ```

---

## Temporary Tables
Temporary tables store data temporarily and are automatically deleted when the session ends.
```sql
CREATE TEMPORARY TABLE table_name (
    column_name datatype,
    column_name datatype
);
```

---

## Aggregation Functions
SQL provides several aggregate functions to perform calculations on data:
- **MIN()** – Returns the smallest value in a column
- **MAX()** – Returns the largest value in a column
- **COUNT()** – Returns the number of rows in a set
- **SUM()** – Computes the sum of numeric values in a column
- **AVG()** – Computes the average of numeric values in a column

Example:
```sql
SELECT MIN(salary), MAX(salary), COUNT(*), SUM(salary), AVG(salary) FROM employees;
```

---

## Exercises
Practice the following SQL commands to enhance your understanding:
1. Create a new table and insert sample data.
2. Use SELECT queries with WHERE conditions.
3. Implement table cloning techniques.
4. Practice aggregate functions on different datasets.

---

## Author
[Lokeswari](https://github.com/LokiRameshBabu/c406firstproject)
