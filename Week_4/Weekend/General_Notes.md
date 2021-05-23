## Notes

### Relational Databases

- Terms

  - Entity
    - Represents a person, place or thing that you want to track in a database.
  - Attribute
    - Describes various characteristics about an individual entity. These are the columns in the table.
  - Primary Key
    - An attribute or group of attributes that uniquely identifies an instance of the entity. Makes sure no two rows will have the same value.
  - Relationship
    - Describes how one or more entities interact with each other. Usually described with a verb.
  - Cardinality
    - The count of instances that are allowed or are necessary between entity relationships. It tells us the min/max we need to connect entitys.

- Structured Query Language (SQL) is a programming language used to interact with relational databases.

***

- Create: a database

```SQL
  CREATE TABLE db (id INTEGER PRIMARY KEY, name TEXT, quantity INTEGER);
```
- 
  - db is the name of the Database
  - id is the primary key for this database
  - name is the first column which contains a text value
  - quantity is the second column which contains an Integer value

***

- Insert: data into a database

```SQL
   INSERT INTO db VALUES (1, "Bananas", 4);
```
  -
    - 1: is the unique row ID
    - "Bananas": is a name column
    - 4: is a quantity column

***

- Select: data from a database

```SQL
  SELECT * FROM db WHERE rating > 5 ORDER BY rating;
```

- 
  - *: is the table we want, * stands for all the tables
  - db: is the table we want to qeury
  - WHERE: is the query claus 
  - rating > 5: is the expression we use to define what we want to filter
  - ORDER BY: is the identifier that describes how we want the data sorted
  - rating: is what value we want to sort it by

***

- Aggregating data

  - is useful for getting things like the maximum, minimum or average from values in the database

```SQL
  SELECT aisle, SUM(quantity) FROM groceries GROUP BY aisle;
```
-
  - SUM: is the aggregate function. There is others like (MAX, MIN, etc)
  - (quantity): is the value we want to pass to the aggregate function
  - groceries: is the table we want to query
  - GROUP BY clause: specifing the column name we want to group by 
  - asile: Being the column we want to group the sums by