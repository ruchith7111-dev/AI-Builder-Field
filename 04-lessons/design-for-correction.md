# Lesson · Design for correction

AI features will sometimes be incomplete or wrong. A good product makes correction possible instead of hiding uncertainty.

## Useful product patterns

- Show the source or evidence behind important extracted fields.
- Let the user edit a generated answer before saving or sharing it.
- Distinguish unknown, missing, and inferred values.
- Provide an explicit retry or report-problem path.
- Preserve a record of material user corrections where appropriate.
- Do not make the user fight an automatic decision they cannot inspect.

## Example: extracted resume field

Instead of displaying only "Python — 4 years", show the source passage or page, mark confidence as system-generated only if confidence is calibrated, and allow the user to correct the value.

## Lesson

Human review should be a designed part of the workflow, not an emergency patch added after the first failure.
