# Pandas to SQL Thinking Atlas

A reference pack for analysts and engineers moving from dataframe-first thinking into SQL. It focuses on joins, grouping, windows, null semantics, CTEs, and when to push work into the database instead of Python.

The real migration is not from one syntax to another. It is from row objects in memory to declarative set-based reasoning with explicit database costs.

## Best use

- training analysts who know pandas but need stronger SQL instincts
- rewriting dataframe-heavy reporting logic into database queries
- reviewing pipelines where Python is doing work the warehouse should own
- teaching joins, group-bys, and window functions through familiar pandas examples

## Core topics

- set-based thinking instead of in-memory row iteration
- groupby to `GROUP BY` and aggregate functions
- merge to `JOIN` patterns
- window functions for ranking and cumulative logic
- CTEs, null semantics, and pushing work to the database

## Questions this pack should answer well

- What is the SQL equivalent of a pandas `groupby().agg()` chain?
- How should I translate `merge` and post-merge filtering?
- What does a pandas rolling or ranking operation look like in SQL?
- When should I use a CTE instead of another intermediate dataframe?

## When not to use this pack

- database tuning at the index and query-plan level
- vendor-specific SQL dialect edge cases beyond common patterns
- streaming SQL systems and real-time materialization strategies

## Agent formats

- Codex and generic portable guide: `AGENTS.md`
- Copilot repo instructions: `.github/copilot-instructions.md`
- Copilot skill: `.github/skills/pandas-sql-thinking-atlas/`
- Cursor rule: `.cursor/rules/pandas-sql-thinking-atlas.mdc`
- Antigravity-style rule: `.agent/rules/pandas-sql-thinking-atlas.md`
- Antigravity-style skill: `.agent/skills/pandas-sql-thinking-atlas/`

## Source policy

- Prefer official framework and library docs first.
- Prefer official GitHub org repos second.
- Re-check official docs when framework behavior may have changed.
