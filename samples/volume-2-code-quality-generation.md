# Volume 2: Code Quality & Generation — Free Sample

> 3 of 10 real, complete prompts from the **Extract Method / Function** category. Unedited — exactly what's in the paid volume. [Get all 220 prompts →](https://gumroad.com/l/YOUR-VOLUME-2-LINK)

---

## 1. Extract Methods from a Long Python Function (Payment Processing Service)
`REF-EXT-01` &nbsp;·&nbsp; **Difficulty:** Beginner &nbsp;·&nbsp; **Time saved:** 15-30 min per function

**When to use it:** Use when a function in a payment processing service has grown past ~40 lines or does more than one clear job.

**The Prompt:**
```
Act as a senior Python engineer refactoring a long function from a payment
processing service.

Function to refactor: [CODE_SNIPPET]

Identify the distinct responsibilities inside this function and extract each into
its own well-named method or function. Keep the original function as a thin
orchestrator that calls the new pieces in order. Preserve existing behavior
exactly — do not change logic, only structure. Show the full refactored code, and
list the extracted functions with a one-line description of what each now does.
```

**Variables to customize:** `[CODE_SNIPPET]`

**Tips for better results:**
- Paste the whole function, not a truncated version — partial context leads to incomplete extraction.
- Explicitly say 'preserve behavior exactly' so the model doesn't quietly 'improve' logic while restructuring.
- Ask for a one-line description per extracted function — it doubles as a naming sanity check.

**Example input:** A 90-line Python function in a payment processing service that validates input, calls an API, and formats the response inline
**Example output:** Three extracted functions (validate, callApi, formatResponse) plus a 6-line orchestrator function.

**Recommended AI models:** Claude Sonnet 5 (root-cause reasoning) + GitHub Copilot Chat (inline fix)

**Common mistakes to avoid:**
- Accepting a refactor that subtly changes behavior along with structure.
- Extracting functions with vague names like `helper1`, `doStuff` instead of intention-revealing names.

---

## 2. Extract Methods from a Long JavaScript Function (User Authentication Flow)
`REF-EXT-02` &nbsp;·&nbsp; **Difficulty:** Intermediate &nbsp;·&nbsp; **Time saved:** 15-30 min per function

**When to use it:** Use when a function in a user authentication flow has grown past ~40 lines or does more than one clear job.

**The Prompt:**
```
Act as a senior JavaScript engineer refactoring a long function from a user
authentication flow.

Function to refactor: [CODE_SNIPPET]

Identify the distinct responsibilities inside this function and extract each into
its own well-named method or function. Keep the original function as a thin
orchestrator that calls the new pieces in order. Preserve existing behavior
exactly — do not change logic, only structure. Show the full refactored code, and
list the extracted functions with a one-line description of what each now does.
```

**Variables to customize:** `[CODE_SNIPPET]`

**Tips for better results:**
- Explicitly say 'preserve behavior exactly' so the model doesn't quietly 'improve' logic while restructuring.
- Ask for a one-line description per extracted function — it doubles as a naming sanity check.
- Run your existing tests immediately after applying the refactor, before making any further changes.

**Example input:** A 90-line JavaScript function in a user authentication flow that validates input, calls an API, and formats the response inline
**Example output:** Three extracted functions (validate, callApi, formatResponse) plus a 6-line orchestrator function.

**Recommended AI models:** Claude Opus 4.8 (complex multi-file reasoning) + ChatGPT (quick sanity check)

**Common mistakes to avoid:**
- Extracting functions with vague names like `helper1`, `doStuff` instead of intention-revealing names.
- Not re-running tests right after the refactor, making it hard to isolate a regression later.

---

## 3. Extract Methods from a Long TypeScript Function (File Upload Handler)
`REF-EXT-03` &nbsp;·&nbsp; **Difficulty:** Intermediate &nbsp;·&nbsp; **Time saved:** 15-30 min per function

**When to use it:** Use when a function in a file upload handler has grown past ~40 lines or does more than one clear job.

**The Prompt:**
```
Act as a senior TypeScript engineer refactoring a long function from a file upload
handler.

Function to refactor: [CODE_SNIPPET]

Identify the distinct responsibilities inside this function and extract each into
its own well-named method or function. Keep the original function as a thin
orchestrator that calls the new pieces in order. Preserve existing behavior
exactly — do not change logic, only structure. Show the full refactored code, and
list the extracted functions with a one-line description of what each now does.
```

**Variables to customize:** `[CODE_SNIPPET]`

**Tips for better results:**
- Ask for a one-line description per extracted function — it doubles as a naming sanity check.
- Run your existing tests immediately after applying the refactor, before making any further changes.
- Paste the whole function, not a truncated version — partial context leads to incomplete extraction.

**Example input:** A 90-line TypeScript function in a file upload handler that validates input, calls an API, and formats the response inline
**Example output:** Three extracted functions (validate, callApi, formatResponse) plus a 6-line orchestrator function.

**Recommended AI models:** Claude Sonnet 5 + Gemini (cross-checking an alternate diagnosis)

**Common mistakes to avoid:**
- Not re-running tests right after the refactor, making it hard to isolate a regression later.
- Accepting a refactor that subtly changes behavior along with structure.

---
