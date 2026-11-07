# Prompt · Review a generated change

    Act as a skeptical maintainer reviewing this diff.

    Context:
    [Requirement and relevant design decisions.]

    Review only the changed code and the nearby code needed to understand it.

    Look for:
    - correctness and edge cases;
    - security and authorisation;
    - data validation and error handling;
    - race conditions and duplicate actions;
    - resource usage and external API failures;
    - accessibility and user experience;
    - missing or misleading tests;
    - unnecessary complexity or unrelated changes.

    For each finding, provide:
    severity, file and line, concrete failure scenario,
    evidence, and a suggested minimal correction.

    Separate confirmed defects from questions that need investigation.
    If you find no issue, state what you reviewed and what remains unverified.

## Important

A review prompt can help find issues, but it does not replace running tests, inspecting the diff, or human security review.
