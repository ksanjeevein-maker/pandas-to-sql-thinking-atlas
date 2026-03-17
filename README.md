# Pandas to SQL Thinking Atlas

A reference pack for analysts and engineers moving from dataframe-first thinking into SQL.

The value is in making the move from mutable in-memory steps to set-based query reasoning with explicit joins, windows, and staged CTE logic.

## What makes this repo more useful now

- A stronger learning path for self-study and onboarding
- A worked example that shows the migration or debugging move end to end
- A mental-model diagram for fast orientation
- A review checklist for code review or design review
- Portable agent files for Codex, Copilot, Cursor, and Antigravity

## Learning path

- Start with filtering, projection, and set-based thinking.
- Then move into `GROUP BY`, aggregates, and why row-level intuition breaks there.
- Learn joins and cardinality before building bigger reporting queries.
- Finish with window functions and CTEs for multi-step analytical logic.

## High-signal traps

- Thinking in row loops instead of set operations.
- Forgetting that `NULL` rules differ from pandas null intuition.
- Using CTEs as a dumping ground instead of a readability tool.
- Ignoring join cardinality and then blaming duplicates on SQL itself.

## Read this next

- Main portable guide: `AGENTS.md`
- Decision guide: `docs/decision-guide.md`
- Worked example: `examples/worked-example.md`
- Mental-model diagram: `docs/mental-model-map.md`
- Review checklist: `docs/review-checklist.md`
- Official references: `official-references.md`

## Agent formats

- Codex and generic portable guide: `AGENTS.md`
- Copilot repo instructions: `.github/copilot-instructions.md`
- Copilot skill: `.github/skills/pandas-sql-thinking-atlas/`
- Cursor rule: `.cursor/rules/pandas-sql-thinking-atlas.mdc`
- Antigravity-style rule: `.agent/rules/pandas-sql-thinking-atlas.md`
- Antigravity-style skill: `.agent/skills/pandas-sql-thinking-atlas/`
