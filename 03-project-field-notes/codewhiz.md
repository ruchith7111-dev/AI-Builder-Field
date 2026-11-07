# Project field note · CodeWhiz — Coding Habit Monitor

**Evidence label:** Academic project scope recorded in prior planning. Confirm the current source code and persistence behaviour before treating this as a finished implementation.

## Project intent

A menu-driven Python application for recording coding activity and producing simple summaries.

## Scope recorded

The planned feature set included:

- Add, update, and delete activity records.
- Display reports and summaries.
- Use lists and dictionaries for in-memory data.
- Use loops and modular functions to organise menu actions.
- Persist data in TXT or JSON files.

## A clean module boundary

    main menu
       |
       +--> add activity
       +--> update activity
       +--> delete activity
       +--> view report
       +--> show summary
       |
       v
    validation + storage helpers
       |
       v
    JSON / TXT file

A small program still benefits from clear ownership of input validation, business rules, and file operations.

## Tests that make the demo dependable

| Scenario | Behaviour to verify |
|---|---|
| First run, no data file | App starts with an empty state |
| Add valid entry | Entry appears in the next report |
| Add invalid duration/date | Input is rejected with a useful message |
| Update unknown ID | No unrelated entry is modified |
| Delete unknown ID | App remains stable |
| Empty report | Clear empty-state message |
| Malformed JSON | Error is handled; original file is not silently overwritten |
| Restart application | Saved records load correctly |

## Useful next engineering step

If the project is extended, assign stable IDs to records and centralise read/write operations. Write updates safely so a crash during saving does not corrupt the only copy of the data.

## Lesson

Small projects are an excellent place to practise professional habits: predictable interfaces, input validation, data integrity, and tests for failure cases.
