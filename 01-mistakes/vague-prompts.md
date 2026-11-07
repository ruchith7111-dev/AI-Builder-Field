# Mistake pattern · Starting with a vague request

## The trap

A request such as "build a complete dashboard" leaves critical decisions unstated: users, permissions, data shape, empty states, error behaviour, constraints, and acceptance criteria.

The model fills those gaps with assumptions. The result can look polished while solving the wrong problem.

## Better approach

Before asking for implementation, write a short problem brief:

| Question | Example |
|---|---|
| Who is the user? | A signed-in student reviewing parsed resume data |
| What is the job to be done? | Inspect and correct extracted fields |
| What comes in? | A PDF within a defined size limit |
| What comes out? | Validated structured data plus clear errors |
| What must not happen? | Persisting malformed or unreviewed data |
| How will it be checked? | Valid, malformed, oversized, and scanned-PDF cases |

## Prompt pattern

    Do not write code yet.
    Restate the problem in your own words.
    List missing requirements and assumptions.
    Identify the data flow and failure cases.
    Propose testable acceptance criteria.
    Ask only the questions that block a safe implementation.

## Review question

Could a second developer implement the same behaviour from this brief without guessing? If not, the request still needs work.
