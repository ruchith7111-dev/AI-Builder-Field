# Mistake pattern · Skipping verification

## The trap

"It runs on my machine" is treated as proof that a feature is correct. A single happy-path click does not establish behaviour under invalid input, slow dependencies, duplicate requests, or permission boundaries.

## Minimum verification grid

| Case | Example check |
|---|---|
| Happy path | A valid request returns the expected shape |
| Invalid input | Missing or malformed fields are rejected |
| Boundary | Empty, very large, or maximum-length values |
| Dependency failure | Database or model API unavailable |
| Repeated action | Duplicate submission does not duplicate state |
| Access control | A user cannot read another user's data |
| Regression | Existing behaviour still passes |

Include the exact command, environment, and outcome. If a test was not run, say so. A test that exists in the repository is not evidence that it passed.
