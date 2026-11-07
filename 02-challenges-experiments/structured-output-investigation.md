# Investigation · Unreliable structured output

**Status:** Investigation guide — not a report of a verified project incident.

## Scenario

An LLM is asked to return JSON, but the response sometimes includes missing keys, wrong types, extra prose, or values that do not match the expected schema.

## Possible causes

- The prompt does not define a strict schema.
- The provider's selected mode does not guarantee structured output.
- Input text is ambiguous or incomplete.
- Token limits truncate the response.
- The application assumes valid JSON is also semantically valid.
- Parsing errors are caught and replaced with unsafe defaults.

## Experiments

1. Save a small set of representative inputs.
2. Define a typed schema with required and optional fields.
3. Use provider-supported structured output when available.
4. Validate the response at the application boundary.
5. Test missing, extra, malformed, and wrong-type fields.
6. Record provider, model, parameters, schema version, and exact failure.

## Safe handling pattern

    raw model response
           |
           v
    parse / provider schema enforcement
           |
           v
    application schema validation
           |
       +---+---+
       |       |
     valid   invalid
       |       |
    persist   reject, retry under a bounded policy,
              or send for human correction

## What counts as evidence?

A test report with sample input, expected result, actual result, model/provider configuration, and validation output. "It returned JSON once" is not enough.
