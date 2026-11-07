# Prompt · Plan before code

Use this when the task has more than one moving part or touches an unfamiliar area.

    You are helping me work in an existing codebase.

    Goal:
    [Describe the user-visible outcome.]

    Constraints:
    [List stack, compatibility, security, performance, and scope limits.]

    First inspect the relevant files. Do not modify anything yet.

    Return:
    1. Your understanding of the problem.
    2. Existing implementation and relevant file paths.
    3. Missing requirements and explicit assumptions.
    4. Proposed smallest implementation steps.
    5. Data/API changes, if any.
    6. Failure cases and security concerns.
    7. Tests that would demonstrate acceptance.

    Do not invent repository details. Quote paths or symbols you actually inspected.
    Stop and ask about any decision that changes product behaviour.

## Human review

Check whether the named files and symbols exist. Approve or edit the plan before implementation.
