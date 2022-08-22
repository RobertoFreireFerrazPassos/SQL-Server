# SQL-Server

## Set up project

- docker-compose up in /docker folder
- run scripts in /scripts folder
- Use SSMS. ServerName : localhost. User : sa. Password : AS#G6f34G1162

## Project


### Indexes

#### Clustered Indexes

When you create a table with a primary key, SQL Server automatically creates a corresponding clustered index. Each table has only one clustered index because data rows can be only sorted in one order.

#### Non-clustered indexes

A nonclustered index is a data structure that improves the speed of data retrieval from tables. Unlike a clustered index, a nonclustered index sorts and stores data separately from the data rows in the table. It is a copy of selected columns of data from a table with the links to the associated table.

A table may have one or more nonclustered indexes and each non-clustered index may include one or more columns of the table.

A nonclustered index, when used properly, can greatly improve the performance of queries. However, the benefits of nonclustered indexes come at costs: 
- First, it takes additional storage to store the copy of data of the index key columns.
- Second, when you insert, update, or delete rows from the table, SQL Server needs to update the associated non-clustered index.

##### Filtered index

A filtered index is a nonclustered index with a predicate that allows you to specify which rows should be added to the index.

Some usages: not deleted rows or not null value.

# References:

https://www.sqlservertutorial.net/sql-server-indexes/

