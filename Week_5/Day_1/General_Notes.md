# Notes

## POSTGRESQL DataTypes

- Bigint
- Integer
- char(n) - fixed-length
- varChar(n) - variable length with limit
- text - variable length without limit
- Date
- timestamp
- interval

## Typs of postgres operaters

- LOGICAL Operators
  - AND
  - OR
  - NOT

- Comparison Operators

  - < less than
  - '> greater than
  - <= less than or equal to
  - '>= greater than or equal to
  - <> / != not equal
  - = equal

- KEYWORDs

  - GROUP BY allows us to combine the results based on a column so an aggregate can be applied to each group.
  - HAVING allows us to filter our results based on the result of an aggregate function.

#### To check whether a value is or is not null, use the constructs:

``` postgresql
  expression IS NULL
  expression IS NOT NULL
```

## Joining in Postgres

- INNER JOIN

  - join to two tables using the JOIN keyward and providing an ON statement afterward. This is an inner join.

  - If the foreign key is NULL, the row will not be included in the result of an INNER JOIN.

  ``` postgresql
    JOIN cohorts ON (cohorts.id=cohort_id);
  ```

  - This same query could be written using the INNER keyward to specify the type of join we wanted as well

  - An INNER JOIN will only give us rows where there is a match between the two talbles. Any value that is NULL will not appear in the results.

  ``` postgresql
    INNER JOIN cohorts ON (cohorts.id=cohort_id);
  ```

- OUTER JOIN

  - An OUTER JOIN will join the tables similarly to an INNER JOIN but will return all  results for one of the tables, even when the join condition is not met.

  ```postgresql
    1. FROM students LEFT OUTER JOIN cohorts ON cohorts.id = cohort_id;
    2. FROM students RIGHT OUTER JOIN cohorts ON cohorts.id = cohort_id;
    3. FROM students FULL OUTER JOIN cohorts ON cohorts.id = cohort_id;
  ```
    1. The first query will return all students because students is to the LEFT of the word JOIN.
    2. The second query will return all of the cohorts because cohorts is to the RIGHT of the word JOIN.
    3. The third query will return all rows from both tables, even when there is no match.

***

  - The LEFT OUTER JOIN will return all of the students, even ones without a cohort_id.

  ``` postgresql
    SELECT students.name as student_name, email, cohorts.name as cohort_name
    FROM students LEFT OUTER JOIN cohorts ON cohorts.id = cohort_id;
  ```

  - The RIGHT OUTER JOIN will return all cohorts, even ones without any students enrolled.

  ``` postgresql
    SELECT students.name as student_name, email, cohorts.name as cohort_name
    FROM students RIGHT OUTER JOIN cohorts ON cohorts.id = cohort_id;
  ```

  - The FULL OUTER JOIN will return all cohorts and all students, even when there is no match.

  ``` postgresql
    SELECT students.name as student_name, email, cohorts.name as cohort_name
    FROM students FULL OUTER JOIN cohorts ON cohorts.id = cohort_id;
  ```


  ### RESOURCES

  - [Article about Joins]('https://blog.codinghorror.com/a-visual-explanation-of-sql-joins/')