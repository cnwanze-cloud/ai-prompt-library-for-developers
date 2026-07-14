# Volume 4: Architecture & Design — Free Sample

> 3 of 10 real, complete prompts from the **RESTful Resource & Endpoint Structure** category. Unedited — exactly what's in the paid volume. [Get all 260 prompts →](https://gumroad.com/l/YOUR-VOLUME-4-LINK)

---

## 1. Design REST Endpoints for Payment Processing Service (Python)
`API-RES-01` &nbsp;·&nbsp; **Difficulty:** Beginner &nbsp;·&nbsp; **Time saved:** 30-50 min per API surface

**When to use it:** Use when starting a new REST API surface for a payment processing service and want a resource structure that won't need a breaking rework later.

**The Prompt:**
```
Act as an API designer defining the REST resource structure for a payment
processing service, implemented in Python.

Domain entities involved: [DOMAIN_ENTITIES] Key use cases: [USE_CASES]

Propose the resource hierarchy (nouns, not verbs), the HTTP methods and paths for
each operation, which relationships should be nested vs. top-level with a
reference, and where a custom action (non-CRUD) genuinely justifies breaking REST
convention. Flag any endpoint design that would be awkward to version or extend
later.
```

**Variables to customize:** `[DOMAIN_ENTITIES]`, `[USE_CASES]`

**Tips for better results:**
- List actual use cases, not just entities — resource design driven by use cases avoids over/under-nesting.
- Push back explicitly on verb-based endpoint names; ask the model to justify any non-CRUD custom action.
- Ask what would be awkward to extend later — catching this at design time is far cheaper than after clients integrate.

**Example input:** A new 'Python order management' surface for a payment processing service with orders, line items, and payments
**Example output:** A resource hierarchy with orders as top-level, nested line items, and payments referenced by ID rather than nested, with rationale.

**Recommended AI models:** Claude Sonnet 5 (root-cause reasoning) + GitHub Copilot Chat (inline fix)

**Common mistakes to avoid:**
- Nesting resources too deeply, producing URLs that are brittle to model changes (e.g. 4 levels of nesting).
- Adding verb-based endpoints (`/createOrder`) instead of modeling the action as a resource state change.

---

## 2. Design REST Endpoints for User Authentication Flow (JavaScript)
`API-RES-02` &nbsp;·&nbsp; **Difficulty:** Intermediate &nbsp;·&nbsp; **Time saved:** 30-50 min per API surface

**When to use it:** Use when starting a new REST API surface for a user authentication flow and want a resource structure that won't need a breaking rework later.

**The Prompt:**
```
Act as an API designer defining the REST resource structure for a user
authentication flow, implemented in JavaScript.

Domain entities involved: [DOMAIN_ENTITIES] Key use cases: [USE_CASES]

Propose the resource hierarchy (nouns, not verbs), the HTTP methods and paths for
each operation, which relationships should be nested vs. top-level with a
reference, and where a custom action (non-CRUD) genuinely justifies breaking REST
convention. Flag any endpoint design that would be awkward to version or extend
later.
```

**Variables to customize:** `[DOMAIN_ENTITIES]`, `[USE_CASES]`

**Tips for better results:**
- Push back explicitly on verb-based endpoint names; ask the model to justify any non-CRUD custom action.
- Ask what would be awkward to extend later — catching this at design time is far cheaper than after clients integrate.
- Sketch 2-3 real client call sequences against the proposed design before finalizing it.

**Example input:** A new 'JavaScript order management' surface for a user authentication flow with orders, line items, and payments
**Example output:** A resource hierarchy with orders as top-level, nested line items, and payments referenced by ID rather than nested, with rationale.

**Recommended AI models:** Claude Opus 4.8 (complex multi-file reasoning) + ChatGPT (quick sanity check)

**Common mistakes to avoid:**
- Adding verb-based endpoints (`/createOrder`) instead of modeling the action as a resource state change.
- Designing the API around the current database schema instead of the actual client use cases.

---

## 3. Design REST Endpoints for File Upload Handler (TypeScript)
`API-RES-03` &nbsp;·&nbsp; **Difficulty:** Intermediate &nbsp;·&nbsp; **Time saved:** 30-50 min per API surface

**When to use it:** Use when starting a new REST API surface for a file upload handler and want a resource structure that won't need a breaking rework later.

**The Prompt:**
```
Act as an API designer defining the REST resource structure for a file upload
handler, implemented in TypeScript.

Domain entities involved: [DOMAIN_ENTITIES] Key use cases: [USE_CASES]

Propose the resource hierarchy (nouns, not verbs), the HTTP methods and paths for
each operation, which relationships should be nested vs. top-level with a
reference, and where a custom action (non-CRUD) genuinely justifies breaking REST
convention. Flag any endpoint design that would be awkward to version or extend
later.
```

**Variables to customize:** `[DOMAIN_ENTITIES]`, `[USE_CASES]`

**Tips for better results:**
- Ask what would be awkward to extend later — catching this at design time is far cheaper than after clients integrate.
- Sketch 2-3 real client call sequences against the proposed design before finalizing it.
- List actual use cases, not just entities — resource design driven by use cases avoids over/under-nesting.

**Example input:** A new 'TypeScript order management' surface for a file upload handler with orders, line items, and payments
**Example output:** A resource hierarchy with orders as top-level, nested line items, and payments referenced by ID rather than nested, with rationale.

**Recommended AI models:** Claude Sonnet 5 + Gemini (cross-checking an alternate diagnosis)

**Common mistakes to avoid:**
- Designing the API around the current database schema instead of the actual client use cases.
- Nesting resources too deeply, producing URLs that are brittle to model changes (e.g. 4 levels of nesting).

---
