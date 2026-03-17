---
name: pandas-sql-thinking-atlas
description: A reference pack for analysts and engineers moving from dataframe-first thinking into SQL. It focuses on joins, grouping, windows, null semantics, CTEs, and when to push work into the database instead of Python. Use when an agent needs a concise reference, migration guide, or side-by-side pattern library for this topic.
---

# Pandas to SQL Thinking Atlas

Use this skill to answer the practical question, "what is the target-platform way to do the thing I already know?"

## Quick Start

- Read `references/concepts.md` for conceptual mapping and mindset shifts.
- Read `references/patterns.md` for concrete rewrite or debugging patterns.
- Read `references/official-links.md` when official docs or source repos are needed.

## Workflow

1. Identify the source-side habit or failure mode.
2. Translate the mental model before changing code.
3. Prefer native target-platform patterns.
4. Show a small example or checklist instead of a giant transliteration.
5. Call out the main watchouts clearly.

## Output

- Start with the target-side equivalent in one sentence.
- Explain the mental shift in plain language.
- Show a concise mapping, snippet, or checklist.
- Mention 1-3 watchouts.
- Add official links only when useful.

## Guardrails

- Prefer set-based operations over row-by-row Python thinking.
- Keep null semantics explicit.
- Use CTEs to make multi-step query logic readable, not to imitate dataframe sprawl.
- Move work into SQL when the database can do it cheaper and closer to the data.
