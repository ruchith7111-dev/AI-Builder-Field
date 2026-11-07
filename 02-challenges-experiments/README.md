# 02 · Challenges, Experiments & Lessons

This section records how to investigate difficult engineering work without turning every attempt into a success story.

A challenge may be solved, partially solved, deferred, or still unexplained. The record should make that status visible.

## The experiment format
1. **Context** — what were we building and what was blocked?
2. **Observation** — what happened, with a reproducible example?
3. **Hypothesis** — what might explain it?
4. **Experiment** — what single test can distinguish possibilities?
5. **Evidence** — what did the test, log, or output show?
6. **Result** — confirmed, rejected, inconclusive, or not run?
7. **Lesson** — what should another builder remember?

Use the [challenge log template](../templates/challenge-log.md).

## Starter investigations
- [Unreliable structured output](structured-output-investigation.md)
- [PDF extraction uncertainty](pdf-extraction-investigation.md)
- [RAG retrieval quality](rag-retrieval-investigation.md)

## Status vocabulary

| Status | Use it when |
|---|---|
| **Hypothesis** | A possible cause has been proposed |
| **Experiment designed** | A test is specified but not run |
| **Tested** | The stated test was run and its result recorded |
| **Partially confirmed** | Evidence supports part, but not all, of the explanation |
| **Inconclusive** | The test did not distinguish the possibilities |
| **Resolved** | The cause and correction are verified against the reproduction |
| **Deferred** | Work is intentionally postponed |

Do not mark a note resolved just because a code change was suggested.
