# SQL Query Optimizations

| Title|Remarks|
|--|--|
| Use Proper Indexing||
| Avoid SELECT *||
| Avoid Redundant or Unnecessary Data Retrieval||
| Use Joins Efficiently||
| Optimize WHERE Clauses|Filtering out as many rows as possible early in the WHERE clause can help us optimize the query.|
| Optimize Subqueries|Use common table expressions (CTEs) instead.  CTEs separate our code into a few smaller rather than one big query, which is much easier to read.|
| Use EXISTS Instead of IN for Subqueries||
| Limit the use of DISTINCT||
| Avoid Unnecessary Ordering and Grouping||
| Use UNION ALL Instead of UNION||
| Break Down Complex Queries|One of the most frequently used strategies to break down queries is materialized views. These are precomputed and stored query results that can be accessed quickly rather than recalculating the query each time it’s referenced.|
| Prevent having JSON columns                       | Avoid JSON/JSONB columns for frequently filtered data. They are slower to query and harder to index efficiently. [Read more](https://stackoverflow.com/questions/71086258/query-on-json-jsonb-column-super-slow-can-i-use-an-index).                                                                                                                     |
| Materialized Views, De-normalization              | Precompute heavy queries or flatten data where real-time joins are too costly.                                                                                                                                                                                                                                                                           |
| Regular Vacuum (garbage-collect and optionally analyze a database)                                    | [Vacuum](https://www.postgresql.org/docs/current/sql-vacuum.html) regularly in PostgreSQL to prevent bloat and maintain healthy performance in high-churn tables.                                                                                                                                                                                        |

[Read more](https://www.datacamp.com/blog/sql-query-optimization)
