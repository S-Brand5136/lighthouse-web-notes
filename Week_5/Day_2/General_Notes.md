# Notes

## Database Design

- Database Design is the organization of data according to a model

- Determining what data is to be stored is usually done by someone who understands how databases are designed and someone with knowledege of the data thats being stored

- When determining data relationships the dependency of data must be taken into consideration 


    - `Sometimes when data is changed you can be changing other data that is not visible. For example, in a list of names and addresses, assuming a situation where multiple people can have the same address, but one person cannot have more than one address, the address is dependent upon the name. When provided a name and the list the address can be uniquely determined; however, the inverse does not hold - when given an address and the list, a name cannot be uniquely determined because multiple people can reside at an address. Because an address is determined by a name, an address is considered dependent on a name.` - wiki

- Once the relationships and dependencies amongst the various pieces of information have been determined, it is possible to arrange the data into a logical structure which can then be mapped into the storage objects supported by the database management system. 

- Database designs also indcude ERDs (entity-relationship model) diagrams. 
   - These diagrams help to show the design of a database in an efficent way

### RESOURCES

  - [wiki article about database design]('https://en.wikipedia.org/wiki/Database_design')