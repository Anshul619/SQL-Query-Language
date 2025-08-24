# Materialized View
- One of the most frequently used strategies to break down queries is [materialized views]().
- These are precomputed and stored query results that can be accessed quickly rather than recalculating the query each time it’s referenced.

# Example

````
CREATE MATERIALIZED VIEW sales_summary AS
SELECT product_id, 
       SUM(quantity) AS total_quantity, 
       SUM(price * quantity) AS total_revenue
FROM sales
GROUP BY product_id;   
````

# Refreshing Materialized View
- Materialized views can be refreshed in different ways depending on the database system. 
- PostgreSQL requires manual refresh using REFRESH MATERIALIZED VIEW, while Oracle supports automatic refresh on a schedule or on demand.
- Microsoft SQL Server implements materialized views as "Indexed Views," which are automatically updated when the underlying data changes, provided the view meets specific deterministic requirements.
= In Google BigQuery, materialized views can be incrementally updated, reading only the changes since the last refresh to improve efficiency.

# View vs Materialized View
- Materialized views are disk based and are updated periodically based upon the query definition.
- Views are virtual only and run the query definition each time they are accessed.
- [Read more](https://stackoverflow.com/questions/93539/what-is-the-difference-between-views-and-materialized-views-in-oracle)
