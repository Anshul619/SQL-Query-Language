# SQL Query Optimizations

|Title|Remarks|
|--|--|
|Use Proper Indexing||
|Avoid SELECT *||
|Avoid Redundant or Unnecessary Data Retrieval||
|Use Joins Efficiently||
|Optimize WHERE Clauses|Filtering out as many rows as possible early in the WHERE clause can help us optimize the query.|
|Optimize Subqueries|Use common table expressions (CTEs) instead.  CTEs separate our code into a few smaller rather than one big query, which is much easier to read.|
|Use EXISTS Instead of IN for Subqueries||
|Limit the use of DISTINCT||
|Avoid Unnecessary Ordering and Grouping||
|Use UNION ALL Instead of UNION||
|Break Down Complex Queries|One of the most frequently used strategies to break down queries is materialized views. These are precomputed and stored query results that can be accessed quickly rather than recalculating the query each time it’s referenced.|

[Read more](https://www.datacamp.com/blog/sql-query-optimization)
