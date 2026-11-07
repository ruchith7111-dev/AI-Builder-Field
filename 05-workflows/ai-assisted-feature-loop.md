# Workflow · AI-assisted feature loop

## 1. Frame the change

Write the user problem, expected behaviour, non-goals, constraints, and acceptance criteria. Ask the AI tool to restate the task and expose missing information.

## 2. Inspect before planning

Read the current implementation, types, dependencies, and tests. Ask the tool to point to the files that establish existing behaviour. Check those files yourself.

## 3. Plan a narrow slice

Agree on interfaces and a small implementation sequence. Each step should leave the project in a state that can be checked.

## 4. Implement with a diff boundary

Ask for one focused change. Review the diff before asking for another. Reject unrelated refactors unless they are necessary and explicitly agreed.

## 5. Verify

Run formatting, lint, type checks, unit tests, and relevant integration tests. Add negative and boundary cases. Inspect logs and the user-visible behaviour.

## 6. Review risks

Check authorisation, data handling, input validation, dependency failures, performance, accessibility, and observability as appropriate to the feature.

## 7. Record the result

Write what changed, what tests ran, what did not run, known limitations, and rollback considerations.

**Done means:** acceptance criteria have evidence, not that the model has finished generating text.
