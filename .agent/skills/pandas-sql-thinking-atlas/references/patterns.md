# Pandas to SQL Thinking Patterns

## Filter and select

Pandas:

```python
result = df.loc[df["country"] == "IN", ["user_id", "revenue"]]
```

SQL:

```sql
SELECT user_id, revenue
FROM users
WHERE country = 'IN';
```

## Group and aggregate

Pandas:

```python
summary = df.groupby("team", as_index=False).agg(total_sales=("sales", "sum"))
```

SQL:

```sql
SELECT team, SUM(sales) AS total_sales
FROM sales
GROUP BY team;
```

## Merge to join

Pandas:

```python
merged = orders.merge(customers, on="customer_id", how="left")
```

SQL:

```sql
SELECT o.*, c.*
FROM orders o
LEFT JOIN customers c
  ON o.customer_id = c.customer_id;
```
