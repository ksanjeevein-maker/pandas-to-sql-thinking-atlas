# Pandas to SQL Thinking Concepts

## Table mindset

- pandas habit: think in terms of an in-memory dataframe you can mutate freely.
- SQL equivalent: think in terms of a query over tables and result sets.
- Mental shift: define the result you want, not the row loop you would have written.
- Watchouts:
  - Query order in code is not always execution order in the database.
  - Materializing intermediate tables is more expensive than materializing intermediate Python variables feels.

## Filtering and projection

- pandas habit: slice rows and columns directly.
- SQL equivalent: use `WHERE` to filter rows and `SELECT` to project columns.
- Mental shift: every selected column is part of query cost and result shape.
- Watchouts:
  - `NULL` comparison rules are different from pandas `NaN` expectations.
  - Filtering before expensive joins often matters.

## Grouping and aggregation

- pandas habit: `groupby` plus named aggregations.
- SQL equivalent: `GROUP BY` plus aggregate functions.
- Mental shift: aggregated columns and grouped columns obey strict query rules.
- Watchouts:
  - Non-grouped columns cannot be selected casually.
  - Post-aggregation filters usually belong in `HAVING`, not `WHERE`.
