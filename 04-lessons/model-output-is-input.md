# Lesson · Treat model output as untrusted input

An LLM response is external data, even when the model is called from inside your own backend.

## Apply ordinary software boundaries

- Parse and validate structure.
- Enforce length, type, and allowed-value constraints.
- Escape output before rendering it in a browser.
- Never execute generated SQL, shell commands, or code without a deliberate sandbox and review process.
- Check authorisation independently of model-generated decisions.
- Keep secrets out of prompts and logs.
- Treat retrieved documents and user-provided text as data, not instructions to override system policy.

## Structured output is not semantic truth

A schema can prove that a field is a string. It cannot prove that the string is factually correct. Important outputs need source evidence, domain validation, or human review.

## Lesson

Use the same defensive mindset for model output that you would use for an untrusted API response.
