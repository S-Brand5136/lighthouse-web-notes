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

### Update

- The SQL UPDATE Query is used to modify the existing records in a table. You can use the WHERE clause with the UPDATE query to update the selected rows, otherwise all the rows would be affected.

Basic Syntax
``` postgresql
  UPDATE table_name
  SET column1 = value1, column2 = value2 etc..
  WHERE [condition];
```

- If you want to modify all the values in a column in a table you do not need dto use the WHERE clause as the UPDATE query would be enough

``` postgresql
    UPDATE table_name
    SET column1 = value1, column2 = value2 etc..
```

