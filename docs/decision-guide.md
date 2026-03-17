# Pandas to SQL Thinking Atlas Decision Guide

Use this when you need to choose the next move instead of reading every reference front to back.

## When to use this guide

- Use it when the user is blocked by one of these traps: Thinking in row loops instead of set operations., Forgetting that `NULL` rules differ from pandas null intuition..
- Use it when you need to decide the order of migration work, not just the target syntax.
- Use it when you need a short review path before shipping or approving code.

## Recommended sequence

### Step 1: Orient

- Focus: Start with filtering, projection, and set-based thinking.
- Exit check: Is the query written in a set-based style instead of procedural dataframe steps?

### Step 2: Translate

- Focus: Then move into `GROUP BY`, aggregates, and why row-level intuition breaks there.
- Exit check: Are group-by and having semantics correct?

### Step 3: Implement

- Focus: Learn joins and cardinality before building bigger reporting queries.
- Exit check: Do joins clearly express intended cardinality?

### Step 4: Harden

- Focus: Finish with window functions and CTEs for multi-step analytical logic.
- Exit check: Are window functions used where row-level outputs must be preserved?

## If the user is stuck, choose this next move

- If they are porting line by line, redirect to the mental model in `docs/mental-model-map.md` and call out: Ignoring join cardinality and then blaming duplicates on SQL itself.
- If they need proof, show `examples/worked-example.md` and explain what changed structurally.
- If they are ready to merge or publish, run the checklist in `docs/review-checklist.md`.

## Escalate when

- The implementation still violates this review check: Would this query be easier to run in the database than in Python memory?
- The chosen approach depends on preserving a source-side habit that keeps causing trouble: Thinking in row loops instead of set operations.
