# SQL

1.  What is an Index?
An index creates an entry for each value and hence it will be faster to retrieve data.

2. Explain different types of index?
    - __Unique Index__: This index does not allow the field to have duplicate values if the column is unique indexed. If a primary key is defined, a unique index can be applied automatically.

    - __Clustered Index__: This index reorders the physical order of the table and searches based on the basis of key values. Each table can only have one clustered index.

    - __Non-Clustered Index__: Non-Clustered Index does not alter the physical order of the table and maintains a logical order of the data. Each table can have many nonclustered indexes.

