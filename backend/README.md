# Q&A for Backend




# DB
1. Differences between Postgres (MySQL) and MongoDB?
    | Postgres | MongoDB  |
    |:-:|:-:|
    | __SQL__. Relational Database Management System| __NoSQL__. Non-Relational Database Management System |
    | Object Oriented. __Fix__ schema for all records | Document Oriented. __Flexible__ schame for all records |
    | Full supports for __transactions__ | In the past, no transaction. Lately, transactions is supported but __not relible__ |

2. What is index?
    - Indexes support the efficient execution of queries. Without indexes, DBMS must perform a scan for the whole table or collection. If an appropriate index exists for a query, DBMS can use the index to limit the number of documents it must inspect.

