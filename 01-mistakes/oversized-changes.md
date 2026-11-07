# Mistake pattern · Asking for too much in one change

## The trap

A single prompt asks an AI tool to create the UI, API, database schema, authentication, tests, and deployment configuration. If the result fails, the cause is spread across too many moving parts.

Large generated diffs are harder to review. A small bug can hide inside a large amount of plausible code.

## Safer sequence
1. Agree on requirements and interfaces.
2. Define the data contract.
3. Implement one vertical slice.
4. Run the smallest relevant test.
5. Inspect the diff.
6. Continue only after the slice is understood.

## Example: resume parsing

Instead of "build the full resume platform", split the work into file validation, text extraction, schema definition, model output validation, persistence, UI review, and tests for malformed inputs.

## Working rule

A good AI-assisted change should be small enough that you can explain every changed file and defend the important decisions.
