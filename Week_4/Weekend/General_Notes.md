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

- Insert: data into a database

```SQL
   INSERT INTO db VALUES (1, "Bananas", 4);
```
  -
    - 1: is the unique row ID
    - "Bananas": is a name column
    - 4: is a quantity column

- Select: data from a database

```SQL
  SELECT * FROM db;
```
