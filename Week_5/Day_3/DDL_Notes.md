### Data Definition Language

- The statements use to alter database schema are refered to as Data Definition language (DDL).

  - These can be use to create, mnodify, remove tables indexes and users

### Data types

- There are a handful of data types to choose from, some include
  - SMALLINT
  - INTEGER
  - BIGINT
  - DECIMAL
  - DATE
  - NUMERIC
  - REAL
  - DOUBLE
  - SMALLSERIAL
  - SERIAL
  - BIGSERIAL
  - TIMESTAMP

### Table altering

- The basic syntax for table altering is such

``` postgresql
    ALTER TABLE table_name action;
```

- Thers many different actions you can do against tables such sa 
  - add a column
  - drop a column
  - change the data type of a column
  - renamne a column
  - set a default value
  - add a constraint to a column
  - rename a table

To add multiple columns to a table at once

``` postgresql
    ALTER TABLE table_name ADD COLUMN col1 TYPE, ADD COLUMN col2 TYPE
```

``` postgresql
  ALTER TABLE products ALTER COLUMN price SET DEFAULT 
```

### Removing a Table

- To drop a table we can do a DROP TABLE command

``` postgresql
  DROP TABLE IF EXISTS users CASCADE;
```

- If we have multiple tables in our database, CASCADE will make sure that all records from other tables that depend on this table will also be deleted

### NULL

- If we add a row and don't include a value, by default it will be set to null.

### Auto incrementing / serial

- The value for the id column always needs to be one more than the previous entry. Rather then doing this ourselves we can set the Primary key to be auto incrementing

- In postgresql this is done by setting the primary keys data type to serial

``` postgresql
  id SERIAL PRIMARY KEY, 
```

### Foreign Keys

- The foriegn key in this case is the owner_id

``` postgresql
CREATE TABLE pets (
  id SERIAL PRIMARY KEY,
  name VARCHAR(255) NOT NULL,
  owner_id INTEGER NOT NULL REFERENCES users(id)
);
```