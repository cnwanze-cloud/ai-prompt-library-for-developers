# Volume 1: Debugging & Code Reviews — Free Sample

> 3 of 10 real, complete prompts from the **Exception & Error Message Diagnosis** category. Unedited — exactly what's in the paid volume. [Get all 220 prompts →](https://gumroad.com/l/YOUR-VOLUME-1-LINK)

---

## 1. Diagnose a Python Error in Payment Processing Service
`DBG-ERR-01` &nbsp;·&nbsp; **Difficulty:** Beginner &nbsp;·&nbsp; **Time saved:** 15-25 min per incident

**When to use it:** Use when Python throws a runtime error inside a payment processing service and the message alone doesn't tell you the root cause.

**The Prompt:**
```
Act as a senior Python engineer debugging a payment processing service. I'm
getting this error:

Error message: [ERROR_MESSAGE]

Relevant code: [CODE_SNIPPET]

Environment: [LANGUAGE_VERSION] / [FRAMEWORK_VERSION]

Please: (1) explain in plain language what this error means and why it's happening
here, (2) point to the exact line(s) most likely responsible, (3) give a corrected
version of the code, (4) flag any other spot in this snippet that could throw the
same error under different inputs, (5) suggest one defensive-coding practice to
prevent this class of bug going forward.
```

**Variables to customize:** `[ERROR_MESSAGE]`, `[CODE_SNIPPET]`, `[LANGUAGE_VERSION]`, `[FRAMEWORK_VERSION]`

**Tips for better results:**
- Paste the full error message including the exception type — truncated errors lead to guessed fixes.
- Include 10-15 lines of context above and below the failing line, not just the one line.
- State your framework/library versions; many errors are version-specific.

**Example input:** [ERROR_MESSAGE]: AttributeError: 'NoneType' object has no attribute
[CODE_SNIPPET]: 14-line handler function inside a payment processing service
**Example output:** A 3-part answer: root-cause explanation, the corrected function with the null-check added, and one note about a second call site with the same risk.

**Recommended AI models:** Claude Sonnet 5 (root-cause reasoning) + GitHub Copilot Chat (inline fix)

**Common mistakes to avoid:**
- Pasting only the error message with no surrounding code.
- Leaving out the language/framework version, which invites outdated syntax fixes.

---

## 2. Diagnose a JavaScript Error in User Authentication Flow
`DBG-ERR-02` &nbsp;·&nbsp; **Difficulty:** Intermediate &nbsp;·&nbsp; **Time saved:** 15-25 min per incident

**When to use it:** Use when JavaScript throws a runtime error inside a user authentication flow and the message alone doesn't tell you the root cause.

**The Prompt:**
```
Act as a senior JavaScript engineer debugging a user authentication flow. I'm
getting this error:

Error message: [ERROR_MESSAGE]

Relevant code: [CODE_SNIPPET]

Environment: [LANGUAGE_VERSION] / [FRAMEWORK_VERSION]

Please: (1) explain in plain language what this error means and why it's happening
here, (2) point to the exact line(s) most likely responsible, (3) give a corrected
version of the code, (4) flag any other spot in this snippet that could throw the
same error under different inputs, (5) suggest one defensive-coding practice to
prevent this class of bug going forward.
```

**Variables to customize:** `[ERROR_MESSAGE]`, `[CODE_SNIPPET]`, `[LANGUAGE_VERSION]`, `[FRAMEWORK_VERSION]`

**Tips for better results:**
- Include 10-15 lines of context above and below the failing line, not just the one line.
- State your framework/library versions; many errors are version-specific.
- If the bug is intermittent, say so explicitly — that changes the diagnosis path entirely.

**Example input:** [ERROR_MESSAGE]: TypeError: Cannot read properties of undefined
[CODE_SNIPPET]: 14-line handler function inside a user authentication flow
**Example output:** A 3-part answer: root-cause explanation, the corrected function with the null-check added, and one note about a second call site with the same risk.

**Recommended AI models:** Claude Opus 4.8 (complex multi-file reasoning) + ChatGPT (quick sanity check)

**Common mistakes to avoid:**
- Leaving out the language/framework version, which invites outdated syntax fixes.
- Accepting the first suggested fix without asking why the error occurred in the first place.

---

## 3. Diagnose a TypeScript Error in File Upload Handler
`DBG-ERR-03` &nbsp;·&nbsp; **Difficulty:** Intermediate &nbsp;·&nbsp; **Time saved:** 15-25 min per incident

**When to use it:** Use when TypeScript throws a runtime error inside a file upload handler and the message alone doesn't tell you the root cause.

**The Prompt:**
```
Act as a senior TypeScript engineer debugging a file upload handler. I'm getting
this error:

Error message: [ERROR_MESSAGE]

Relevant code: [CODE_SNIPPET]

Environment: [LANGUAGE_VERSION] / [FRAMEWORK_VERSION]

Please: (1) explain in plain language what this error means and why it's happening
here, (2) point to the exact line(s) most likely responsible, (3) give a corrected
version of the code, (4) flag any other spot in this snippet that could throw the
same error under different inputs, (5) suggest one defensive-coding practice to
prevent this class of bug going forward.
```

**Variables to customize:** `[ERROR_MESSAGE]`, `[CODE_SNIPPET]`, `[LANGUAGE_VERSION]`, `[FRAMEWORK_VERSION]`

**Tips for better results:**
- State your framework/library versions; many errors are version-specific.
- If the bug is intermittent, say so explicitly — that changes the diagnosis path entirely.
- Mention any fix you already tried so the model doesn't suggest it again.

**Example input:** [ERROR_MESSAGE]: runtime type mismatch despite passing the type checker
[CODE_SNIPPET]: 14-line handler function inside a file upload handler
**Example output:** A 3-part answer: root-cause explanation, the corrected function with the null-check added, and one note about a second call site with the same risk.

**Recommended AI models:** Claude Sonnet 5 + Gemini (cross-checking an alternate diagnosis)

**Common mistakes to avoid:**
- Accepting the first suggested fix without asking why the error occurred in the first place.
- Omitting recent changes to the file, which are often the real root cause.

---
