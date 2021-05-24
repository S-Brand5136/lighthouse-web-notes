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

#### To check whether a value is or is not null, use the constructs:

``` postgresql
  expression IS NULL
  expression IS NOT NULL
```

## Joining in Postgres

- join to two tables using the JOIN keyward and providing an ON statement afterward. This is an inner join.

``` postgresql
  JOIN cohorts ON (cohorts.id=cohort_id);
```

- This same query could be written using the INNER keyward to specify the type of join we wanted as well.

``` postgresql
  INNER JOIN cohorts ON (cohorts.id=cohort_id);
```


