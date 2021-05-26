# Notes

### Data Manipulation Language

- The SQL commands that let us interact with our data are sometimes referred to as Data Manipulation Language (DML) These include:

  - SELECT: get data from tables.
  - INSERT: add rows to a table.
  - UPDATE: update rows within a table.
  - DELETE: delete rows from a table.

### Insert

- The SQL INSERT INTO Statement is used to add new rows of data to a table in the database.

Basic syntax
``` postgresql
  INSERT INTO table_name (column1, column2 ....)
  VALUES (value1, value2);
```
- You can populate the data into a table through the select statement over another table; provided the other table has a set of fields, which are required to populate the first table.

``` postgresql
  INSERT INTO first_table_name [(column1, column2, ... columnN)] 
   SELECT column1, column2, ...columnN 
   FROM second_table_name
   [WHERE condition];
```

### Delete

- The SQL DELETE Query is used to delete the existing records from a table.

Basic syntax
``` postgresql
  DELETE FROm table_name
  WHERE [condition];
```

- You can combine N number of conditions using AND or OR operators

- If you want to DELETE all the records from the CUSTOMERS table, you do not need to use the WHERE clause and the DELETE query would be as follows −

``` postgresql
  SQL > DELETE FROM CUSTOMERS;
```

- Always include a WHERE clause when deleting.
