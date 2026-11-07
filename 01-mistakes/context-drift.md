# Mistake pattern · Losing context between sessions

## The trap

A long AI conversation accumulates choices, constraints, and rejected approaches. A fresh session may not know which details are current. Repeating the full history is inefficient; assuming the model remembers it is risky.

## Keep a compact project handoff

Record the goal and current scope, repository entry points, stack and relevant versions, data contracts and API routes, decisions and reasons, known bugs and reproduction steps, tests run and results, and the next smallest task.

## Handoff prompt

    Use only the project notes and files provided in this session.
    Summarise the current state and list uncertainties.
    Do not change code until I confirm the next task.
    Do not reintroduce decisions marked as rejected.

A concise, maintained handoff is more reliable than a huge unfiltered chat transcript.
