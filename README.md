dataexp
=======

Dataexps are like regexp for data access, allowing all CRUD operations without knowing the monstrous SQL syntax. They allow people who don't know SQL to query relational databases and author complex queries. The syntax of dataexps is similar to those of closures or list generators in programming languages and is very compact.

# CRUD

CRUD stands for Create, Read, Update and Delete and describes four basic operations one can perform on data. In real-world scenarios, however, Read is the most common operation accounting for over 99.99% of all database operations. Thus we begin with that type of operation.

## Data Selection

| Action       | dataexp       | SQL           |
| -------------| ------------- | ------------- |
| Select all rows in a table, output all columns | sales(*)  | SELECT * FROM sales  |
| Select all rows, output only certain columns | sales(id, name)  | SELECT id, name FROM sales  |
| Filter row by a criterion, output only certain columns | sales\[amount > 1000\](id, name, amount)  | SELECT id, name, amount FROM sales WHERE amount > 1000  |
| Select rows with aggregation | sales\[amount > 1000\](name, avg(amount))  | SELECT name, amount FROM sales WHERE amount > 1000 GROUP BY name  |







