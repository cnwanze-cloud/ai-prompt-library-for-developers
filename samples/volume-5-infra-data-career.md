# Volume 5: Infra, Data & Career — Free Sample

> 3 of 10 real, complete prompts from the **Write Complex SQL Queries** category. Unedited — exactly what's in the paid volume. [Get all 240 prompts →](https://gumroad.com/l/YOUR-VOLUME-5-LINK)

---

## 1. Write a Complex SQL Query for Python Backend (Payment Processing Service)
`SQL-QRY-01` &nbsp;·&nbsp; **Difficulty:** Beginner &nbsp;·&nbsp; **Time saved:** 15-30 min per query

**When to use it:** Use when you need to pull data for a payment processing service that requires joins, aggregation, or window functions beyond a simple SELECT.

**The Prompt:**
```
Act as a database engineer writing a SQL query for a Python backend serving a
payment processing service.

Requirement: [QUERY_REQUIREMENT] Schema (relevant tables): [SCHEMA_DEFINITION]
Database: [DATABASE_ENGINE]

Write the query, using window functions, CTEs, or aggregation as appropriate
rather than pulling raw rows into application code for processing. Explain any
non-obvious clause, and note which columns would benefit from an index given this
query's filter and join conditions.
```

**Variables to customize:** `[QUERY_REQUIREMENT]`, `[SCHEMA_DEFINITION]`, `[DATABASE_ENGINE]`

**Tips for better results:**
- Specify your actual database engine — window function syntax and query planner behavior differ meaningfully across engines.
- Push aggregation and filtering into SQL rather than pulling raw rows into application code when the database can do it more efficiently.
- Share the real schema, including types and existing indexes, not just table/column names.

**Example input:** A requirement to rank top customers by monthly spend for a payment processing service, using PostgreSQL
**Example output:** A CTE-based query using a window function for ranking, with an index recommendation on (customer_id, created_at).

**Recommended AI models:** Claude Sonnet 5 (root-cause reasoning) + GitHub Copilot Chat (inline fix)

**Common mistakes to avoid:**
- Pulling far more rows than needed into application code and filtering/aggregating there instead of in SQL.
- Writing a query that works but ignoring the index implications until it's slow in production.

---

## 2. Write a Complex SQL Query for JavaScript Backend (User Authentication Flow)
`SQL-QRY-02` &nbsp;·&nbsp; **Difficulty:** Intermediate &nbsp;·&nbsp; **Time saved:** 15-30 min per query

**When to use it:** Use when you need to pull data for a user authentication flow that requires joins, aggregation, or window functions beyond a simple SELECT.

**The Prompt:**
```
Act as a database engineer writing a SQL query for a JavaScript backend serving a
user authentication flow.

Requirement: [QUERY_REQUIREMENT] Schema (relevant tables): [SCHEMA_DEFINITION]
Database: [DATABASE_ENGINE]

Write the query, using window functions, CTEs, or aggregation as appropriate
rather than pulling raw rows into application code for processing. Explain any
non-obvious clause, and note which columns would benefit from an index given this
query's filter and join conditions.
```

**Variables to customize:** `[QUERY_REQUIREMENT]`, `[SCHEMA_DEFINITION]`, `[DATABASE_ENGINE]`

**Tips for better results:**
- Push aggregation and filtering into SQL rather than pulling raw rows into application code when the database can do it more efficiently.
- Share the real schema, including types and existing indexes, not just table/column names.
- Ask for the index recommendation in the same pass — it's easy to forget until the query is already slow in production.

**Example input:** A requirement to rank top customers by monthly spend for a user authentication flow, using PostgreSQL
**Example output:** A CTE-based query using a window function for ranking, with an index recommendation on (customer_id, created_at).

**Recommended AI models:** Claude Opus 4.8 (complex multi-file reasoning) + ChatGPT (quick sanity check)

**Common mistakes to avoid:**
- Writing a query that works but ignoring the index implications until it's slow in production.
- Not specifying the database engine, resulting in syntax that doesn't actually run on yours.

---

## 3. Write a Complex SQL Query for TypeScript Backend (File Upload Handler)
`SQL-QRY-03` &nbsp;·&nbsp; **Difficulty:** Intermediate &nbsp;·&nbsp; **Time saved:** 15-30 min per query

**When to use it:** Use when you need to pull data for a file upload handler that requires joins, aggregation, or window functions beyond a simple SELECT.

**The Prompt:**
```
Act as a database engineer writing a SQL query for a TypeScript backend serving a
file upload handler.

Requirement: [QUERY_REQUIREMENT] Schema (relevant tables): [SCHEMA_DEFINITION]
Database: [DATABASE_ENGINE]

Write the query, using window functions, CTEs, or aggregation as appropriate
rather than pulling raw rows into application code for processing. Explain any
non-obvious clause, and note which columns would benefit from an index given this
query's filter and join conditions.
```

**Variables to customize:** `[QUERY_REQUIREMENT]`, `[SCHEMA_DEFINITION]`, `[DATABASE_ENGINE]`

**Tips for better results:**
- Share the real schema, including types and existing indexes, not just table/column names.
- Ask for the index recommendation in the same pass — it's easy to forget until the query is already slow in production.
- Specify your actual database engine — window function syntax and query planner behavior differ meaningfully across engines.

**Example input:** A requirement to rank top customers by monthly spend for a file upload handler, using PostgreSQL
**Example output:** A CTE-based query using a window function for ranking, with an index recommendation on (customer_id, created_at).

**Recommended AI models:** Claude Sonnet 5 + Gemini (cross-checking an alternate diagnosis)

**Common mistakes to avoid:**
- Not specifying the database engine, resulting in syntax that doesn't actually run on yours.
- Pulling far more rows than needed into application code and filtering/aggregating there instead of in SQL.

---
