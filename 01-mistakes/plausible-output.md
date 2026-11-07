# Mistake pattern · Trusting plausible output

## The trap

Generated code may compile and still be wrong. Examples include a parser that silently drops sections, a route that returns success with incomplete data, a query that crosses user boundaries, a retry loop that repeats a non-retryable request, or a fallback that turns an error into an empty result.

The danger is not only syntax errors. It is believable behaviour that violates the requirement.

## How to challenge the output

Ask the tool to identify assumptions, unsupported input classes, security-sensitive operations, side effects, error paths, and claims not backed by tests.

Then verify those claims yourself. An AI-generated explanation of its own code is not independent evidence.

## Review prompt

    Review this change as a skeptical maintainer.
    Do not praise it. Identify concrete defects or risks.
    For each finding, include file/line, failure scenario,
    severity, and a minimal reproduction or test.
    Separate confirmed defects from concerns needing investigation.
