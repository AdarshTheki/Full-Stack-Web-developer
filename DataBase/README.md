### File Based Storage System (FBSS) :

- Advantages of FBSS:\
   Easy to used and get started, manual sharing, easy to manage.

- Challenges of FBSS:\
  Duplicate Data / copy, Read, write,update anomaly is a Redundances, Security file and system

### DataBase:

Database is a organized collection of structured information, or data.

### Schema:

It is a list of logical structure of data. Three Schema Architecture

1. [Internal Schema]() (physical storage structure)
2. [Conceptual Schema]() (row, column tables)
3. [External Schema]() (users views and changes )

## DataBase Management System (DBMS):

DBMS are software system used to store, retrieves, and run queries on data.
There are two types of DBMS

1. [Relational](#relational-database-rdbms) (SQL likes MySql , Oracle, etc.)
2. [Non-Relational]() (NoSql likes MongoDB)
   > **Create, Read, Update, Delete**

### Relational DataBase (RDBMS):

A relational database is an collection of data items with pre-define relationship between them, stored in the forms of `table`, `rows` and `column`.

> **MySql** is a Relational Database management system (RDBMS) developed on **Oracle** that is based on "**Structure Query Language**".

75 Most Popular MySQL Commands: **[visit here](https://www.shiksha.com/online-courses/articles/most-popular-mysql-commands/)**

### Primary Key:

- Primary key always contains unique data. It cannot be null.
- There must be a single primary data.

### Foreign key:

- Foreign key is used to link two tables.
- A foreign key is one table (child table) is used to point `PRIMARY KEY` is another table (parent table)\
  Example: `employee(id)` in given old table:

```sql
CREATE TABLE student (
    id INT NOT NULL UNIQUE,
    name VARCHAR(100) NOT NULL,
    email VARCHAR(150) NOT NULL UNIQUE,
    old_Id INT NULL,
    PRIMARY KEY (id),
    FOREIGN KEY (old_Id) REFERENCES employee (id)
);

insert into student (id, name, email, old_Id)
values (1, "ayush", "ayush@gmail.com", 101),
```

### Some of The Most Important SQL Commands

- `CREATE DATABASE` - creates a new database
- `ALTER DATABASE` - modifies a database
- `CREATE TABLE` - creates a new table
- `INSERT INTO` - inserts new data into a database
- `ALTER TABLE` - modifies a table
- `DROP TABLE` - deletes a table
- `SELECT` - extracts data from a database
- `UPDATE` - updates data in a database
- `DELETE` - deletes data from a database
- `CREATE INDEX` - creates an index (search key)
- `DROP INDEX` - deletes an index

```sql
-- CREATE QUERY

-- INSERT INTO
INSERT INTO table_name (col1, col2, col3) VALUES (value_1, ‘value_2’, value_3);

-- READ QUERY 
syntax: SELECT column_name FROM table_name;

SELECT * FROM table_name WHERE age < 0 ;                        -- OPERATORS
SELECT * FROM table_name WHERE age < 0 AND city = "Nagpur" ;    -- OPERATOR & CONDITION
SELECT * FROM table_name WHERE age IN(10, 12, 15, 28, 35) ;     -- SPECIFIC RANGE
SELECT * FROM table_name WHERE age LIKE "%d_%" ;   -- WILDCARD(%)ZERO TO MULTIPLE (_) SINGLE
SELECT * FROM table_name WHERE age BETWEEN 20 AND 45 ;          -- RANGE
SELECT * FROM table_name ORDER BY age DESC ;                    -- ORDER
SELECT DISTINCT(age) FROM table_name ORDER BY age DESC ;        -- UNIQUE VALUE
SELECT * FROM table_name WHERE age IS NOT NULL ;                -- NULL
SELECT * FROM table_name WHERE age LIMIT 10 OFFSET 5 ;          -- RANGE LIMIT
SELECT COUNT(AGE) FROM table_name WHERE age < 18 ;              -- AGGREGATION

-- UPDATE QUERY
UPDATE table_name SET some_column = some_value WHERE id = 0;    -- UPDATE

-- DELETE QUERY
DELETE FROM table_name WHERE id = 0;                        -- DELETE
```
