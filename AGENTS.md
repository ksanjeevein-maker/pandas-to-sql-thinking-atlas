# Pandas to SQL Thinking Atlas Codex and Agent Guide

Use this repository when a task involves:

- training analysts who know pandas but need stronger SQL instincts
- rewriting dataframe-heavy reporting logic into database queries
- reviewing pipelines where Python is doing work the warehouse should own
- teaching joins, group-bys, and window functions through familiar pandas examples

## Preferred workflow

1. Identify the source habit, framework concept, or failure mode first.
2. Translate the mental model before jumping to code.
3. Use the local skill references instead of inventing mappings from memory.
4. Prefer native target-platform patterns over transliteration.
5. Add official links when the user wants citations or deeper study.

## Primary local references

- Skill entrypoint: `.github/skills/pandas-sql-thinking-atlas/SKILL.md`
- Antigravity-style skill entrypoint: `.agent/skills/pandas-sql-thinking-atlas/SKILL.md`
- Concept mappings: `.github/skills/pandas-sql-thinking-atlas/references/concepts.md`
- Rewrite patterns: `.github/skills/pandas-sql-thinking-atlas/references/patterns.md`
- Official links: `.github/skills/pandas-sql-thinking-atlas/references/official-links.md`
- Human reference pack: `official-references.md`

## Output shape

- Start with the target-side equivalent in one sentence.
- Explain the mental shift in plain language.
- Show a concise mapping, pattern, or checklist.
- Call out 1-3 practical watchouts.
- Add official links only when useful.

## Guardrails

- Prefer set-based operations over row-by-row Python thinking.
- Keep null semantics explicit.
- Use CTEs to make multi-step query logic readable, not to imitate dataframe sprawl.
- Move work into SQL when the database can do it cheaper and closer to the data.

## Source preference

1. Official docs
2. Official organization repos
3. Local reference files in this repository
