# Volume 3: Testing & Security — Free Sample

> 3 of 10 real, complete prompts from the **Writing Unit Tests for a New Function** category. Unedited — exactly what's in the paid volume. [Get all 200 prompts →](https://gumroad.com/l/YOUR-VOLUME-3-LINK)

---

## 1. Write Unit Tests for a New Python Function in Payment Processing Service
`UT-NEW-01` &nbsp;·&nbsp; **Difficulty:** Beginner &nbsp;·&nbsp; **Time saved:** 15-25 min per function

**When to use it:** Use right after writing a new function for a payment processing service, before it gets any harder to test in isolation.

**The Prompt:**
```
Act as a Python test engineer writing unit tests for a new function in a payment
processing service, using [TEST_FRAMEWORK].

Function: [CODE_SNIPPET]

Write unit tests covering: the happy path with typical input, each edge case
implied by the function's logic (empty/null/zero/max values), and any error
conditions it should raise. Use clear, descriptive test names that state the
scenario and expected outcome. Mock any external dependencies so the test is fully
isolated and deterministic.
```

**Variables to customize:** `[CODE_SNIPPET]`, `[TEST_FRAMEWORK]`

**Tips for better results:**
- Share the function's full signature and docstring/comments, not just the body — intent matters for picking edge cases.
- Name your test framework explicitly; assertion style and mocking APIs differ a lot between frameworks.
- Ask for descriptive test names ('returns_empty_list_when_input_is_empty') over generic ones ('test1', 'test2').

**Example input:** A Python function in a payment processing service that calculates a discount with 3 tiers and one edge case at the tier boundary
**Example output:** 6 tests covering each tier, the exact boundary value, and a negative-input error case, with descriptive names.

**Recommended AI models:** Claude Sonnet 5 (root-cause reasoning) + GitHub Copilot Chat (inline fix)

**Common mistakes to avoid:**
- Testing only the happy path and skipping the edge cases implied by the function's own logic.
- Writing tests with vague names that don't say what's being verified or why it should pass.

---

## 2. Write Unit Tests for a New JavaScript Function in User Authentication Flow
`UT-NEW-02` &nbsp;·&nbsp; **Difficulty:** Intermediate &nbsp;·&nbsp; **Time saved:** 15-25 min per function

**When to use it:** Use right after writing a new function for a user authentication flow, before it gets any harder to test in isolation.

**The Prompt:**
```
Act as a JavaScript test engineer writing unit tests for a new function in a user
authentication flow, using [TEST_FRAMEWORK].

Function: [CODE_SNIPPET]

Write unit tests covering: the happy path with typical input, each edge case
implied by the function's logic (empty/null/zero/max values), and any error
conditions it should raise. Use clear, descriptive test names that state the
scenario and expected outcome. Mock any external dependencies so the test is fully
isolated and deterministic.
```

**Variables to customize:** `[CODE_SNIPPET]`, `[TEST_FRAMEWORK]`

**Tips for better results:**
- Name your test framework explicitly; assertion style and mocking APIs differ a lot between frameworks.
- Ask for descriptive test names ('returns_empty_list_when_input_is_empty') over generic ones ('test1', 'test2').
- Request fully isolated tests — any hidden dependency on real I/O makes tests slow and flaky over time.

**Example input:** A JavaScript function in a user authentication flow that calculates a discount with 3 tiers and one edge case at the tier boundary
**Example output:** 6 tests covering each tier, the exact boundary value, and a negative-input error case, with descriptive names.

**Recommended AI models:** Claude Opus 4.8 (complex multi-file reasoning) + ChatGPT (quick sanity check)

**Common mistakes to avoid:**
- Writing tests with vague names that don't say what's being verified or why it should pass.
- Leaving a real network or database call inside a 'unit' test, turning it into a slow integration test.

---

## 3. Write Unit Tests for a New TypeScript Function in File Upload Handler
`UT-NEW-03` &nbsp;·&nbsp; **Difficulty:** Intermediate &nbsp;·&nbsp; **Time saved:** 15-25 min per function

**When to use it:** Use right after writing a new function for a file upload handler, before it gets any harder to test in isolation.

**The Prompt:**
```
Act as a TypeScript test engineer writing unit tests for a new function in a file
upload handler, using [TEST_FRAMEWORK].

Function: [CODE_SNIPPET]

Write unit tests covering: the happy path with typical input, each edge case
implied by the function's logic (empty/null/zero/max values), and any error
conditions it should raise. Use clear, descriptive test names that state the
scenario and expected outcome. Mock any external dependencies so the test is fully
isolated and deterministic.
```

**Variables to customize:** `[CODE_SNIPPET]`, `[TEST_FRAMEWORK]`

**Tips for better results:**
- Ask for descriptive test names ('returns_empty_list_when_input_is_empty') over generic ones ('test1', 'test2').
- Request fully isolated tests — any hidden dependency on real I/O makes tests slow and flaky over time.
- Share the function's full signature and docstring/comments, not just the body — intent matters for picking edge cases.

**Example input:** A TypeScript function in a file upload handler that calculates a discount with 3 tiers and one edge case at the tier boundary
**Example output:** 6 tests covering each tier, the exact boundary value, and a negative-input error case, with descriptive names.

**Recommended AI models:** Claude Sonnet 5 + Gemini (cross-checking an alternate diagnosis)

**Common mistakes to avoid:**
- Leaving a real network or database call inside a 'unit' test, turning it into a slow integration test.
- Testing only the happy path and skipping the edge cases implied by the function's own logic.

---
