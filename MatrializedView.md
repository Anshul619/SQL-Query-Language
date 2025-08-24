# Materialized View
- One of the most frequently used strategies to break down queries is [materialized views]().
- These are precomputed and stored query results that can be accessed quickly rather than recalculating the query each time it’s referenced.

# View vs Materialized View
- Materialized views are disk based and are updated periodically based upon the query definition.
- Views are virtual only and run the query definition each time they are accessed.
- [Read more](https://stackoverflow.com/questions/93539/what-is-the-difference-between-views-and-materialized-views-in-oracle)
