# Notes

## Database Design

- Database Design is the organization of data according to a model

- Determining what data is to be stored is usually done by someone who understands how databases are designed and someone with knowledege of the data thats being stored

- When determining data relationships the dependency of data must be taken into consideration 


    - `Sometimes when data is changed you can be changing other data that is not visible. For example, in a list of names and addresses, assuming a situation where multiple people can have the same address, but one person cannot have more than one address, the address is dependent upon the name. When provided a name and the list the address can be uniquely determined; however, the inverse does not hold - when given an address and the list, a name cannot be uniquely determined because multiple people can reside at an address. Because an address is determined by a name, an address is considered dependent on a name.` - wiki

- Once the relationships and dependencies amongst the various pieces of information have been determined, it is possible to arrange the data into a logical structure which can then be mapped into the storage objects supported by the database management system. 

- Database designs also indcude ERDs (entity-relationship model) diagrams. 
   - These diagrams help to show the design of a database in an efficent way


## Database Normalization

  - **To enforce data integrity reduce duplication, and make it easier to manage our data.**

  - Database normalization is the process of making the data in a database available in the most organized way possible

  - We normalize our data to **reduce duplicate data**

  - It is normal to create more tables when normalizing a database.

  - Normalization of data makes the data highly space-effcient on disk, but this can be a draw back when querying large datasets

#### Normal Forms

  - To achieve first normal form for a database, you need to make sure that no table contains multiple columns that you could use to get the same information 

  - To achieve second normal form, it would be helpful to split out the pets into an independent table, and match them up using the student names as foreign keys.

  - Third normal form would suggest making sure each non-key element in each table provides information about the key in the row.

  - we need to add a third table of relationships. Now we have a flexible and searchable structure in fourth normal form that can represent all the available information about each of the students, each of the pets, and the relationships among them.

  - `Normalizing our database reduces duplicate or redundant data and improves data integrity. This process usually involves the creation of new tables in our database.`

******
### RESOURCES

  - [wiki article about database design]('https://en.wikipedia.org/wiki/Database_design')

  - [Article about data normalization]('https://blog.udemy.com/normalization-in-database-with-example/')