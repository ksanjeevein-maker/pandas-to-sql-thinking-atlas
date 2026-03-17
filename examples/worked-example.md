# Worked example: revenue ranking by region

This example translates a grouped analytics flow into a SQL query that keeps ranking logic in the database.

## Pandas

```python
summary = (
    df.groupby(["region", "account"], as_index=False)
    .agg(total_revenue=("revenue", "sum"))
)
summary["rank_in_region"] = summary.groupby("region")["total_revenue"].rank(method="dense", ascending=False)
```

## SQL

```sql
WITH revenue_by_account AS (
  SELECT region, account, SUM(revenue) AS total_revenue
  FROM orders
  GROUP BY region, account
)
SELECT
  region,
  account,
  total_revenue,
  DENSE_RANK() OVER (PARTITION BY region ORDER BY total_revenue DESC) AS rank_in_region
FROM revenue_by_account;
```

## What to notice

- The group step and the ranking step are separate but readable.
- The database preserves row-level outputs while still ranking inside a partition.
- This removes expensive dataframe reshaping from Python.
