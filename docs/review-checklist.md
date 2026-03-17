# Pandas to SQL Thinking Atlas Review Checklist

Use this checklist during code review, design review, or migration planning.

- Is the query written in a set-based style instead of procedural dataframe steps?
- Are group-by and having semantics correct?
- Do joins clearly express intended cardinality?
- Are window functions used where row-level outputs must be preserved?
- Would this query be easier to run in the database than in Python memory?
