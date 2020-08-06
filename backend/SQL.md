# SQL

1.  What is an Index?
An index creates an entry for each value and hence it will be faster to retrieve data.

2. Explain different types of index?
    - __Unique Index__: This index does not allow the field to have duplicate values if the column is unique indexed. If a primary key is defined, a unique index can be applied automatically.

    - __Clustered Index__: This index reorders the physical order of the table and searches based on the basis of key values. Each table can only have one clustered index.

    - __Non-Clustered Index__: Non-Clustered Index does not alter the physical order of the table and maintains a logical order of the data. Each table can have many nonclustered indexes.


3. Explain different types of Normalization?

    - There are many successive levels of normalization. These are called normal forms. Each consecutive normal form depends on the previous one.

    - __First Normal Form (1NF)__: No repeating column
    - __Second Normal Form (2NF)__: Every non-key column value is dependent on the whole primary key.
    - __Third Normal Form (3NF)__: Dependent solely on the primary key and no other non-key column value. No transitive dependence.

4. “Trigger” in SQL?
Trigger in SQL is are a special type of stored procedures that are defined to execute automatically in place or after data modifications. It allows you to execute a batch of code when an insert, update or any other query is executed against a specific table.

5. What are the different types of a subquery?
    - Correlated subquery: These are queries which select the data from a table referenced in the outer query. It is not considered as an independent query as it refers to another table and refers the column in a table.

    - Non-Correlated subquery: This query is an independent query where the output of subquery is substituted in the main query.

6. What is a Relationship and what are they?
    - One to One Relationship.
    - One to Many Relationship.
    - Many to One Relationship.
    - Self-Referencing Relationship.

7. What is the main difference between ‘BETWEEN’ and ‘IN’ condition operators?
    - __BETWEEN operator__ is used __to display__ rows based on a range of values in a row

    - The __IN condition__ operator is used __to check__ for values contained in a specific set of values.

8. What does UNION do? What is the difference between UNION and UNION ALL?
UNION merges the contents of two structurally-compatible tables into a single combined table. The difference between UNION and UNION ALL is that UNION will omit duplicate records whereas UNION ALL will include duplicate records.

9. Name the operator which is used in the query for pattern matching?
    - % – It matches zero or more characters.
    - _ (Underscore) – it matches exactly one character.

