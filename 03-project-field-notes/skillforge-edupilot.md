# Project field note · SkillForge / EduPilot

**Evidence label:** Design and stack context recorded during project planning. Verify the current repository before describing every component as implemented.

## Product intent

A learning-to-career platform concept intended to help a learner understand skill gaps, discover relevant learning actions, and connect learning progress with career preparation.

## Architecture discussed

The planning context included:

- A Next.js / TypeScript / Tailwind front end.
- A FastAPI service for application and model-related endpoints.
- Qwen running through Ollama as a local-model option.
- Supabase / PostgreSQL for application data.
- Retrieval-augmented generation (RAG) for grounded knowledge access.
- Classical ML candidates including Logistic Regression, Random Forest, Gradient Boosting, and Decision Tree models.

These technologies have different jobs. A list of libraries is not an architecture until the boundaries and data flow are defined.

## System questions worth answering

### Product and data
- What learner data is collected, and why?
- Which fields are entered by the learner versus inferred?
- How can a learner correct a wrong profile or skill estimate?
- What is the source and freshness of career or learning content?

### RAG boundary
- Which documents are authoritative?
- How are documents chunked, versioned, and updated?
- Are answers required to cite retrieved evidence?
- What should happen when retrieval finds no relevant source?
- How are retrieval quality and answer faithfulness evaluated separately?

### Classical ML boundary
Do not add a classifier merely because a project includes AI. For each model, define the target, training data, baseline, metric, leakage risks, and how the output changes a user decision.

A model's score should not be described as a validated skill level unless the dataset and evaluation support that interpretation.

### Service boundary
Document the API contract between the Next.js client and FastAPI. Define authentication, request validation, timeouts, error shapes, and which service owns each piece of business logic.

## Suggested evaluation set

1. A learner profile with complete information.
2. A profile with missing or contradictory fields.
3. A question answerable from the knowledge base.
4. A question absent from the knowledge base.
5. A query that should trigger abstention.
6. A model prediction near the decision threshold.
7. A request from an unauthorised user.

## Portfolio evidence to collect

- A diagram of the real deployed data flow.
- A small versioned RAG evaluation set.
- Baseline metrics for every ML model that remains in scope.
- API schemas and error examples.
- A redacted example showing how the user can challenge or correct an output.

## Lesson

The product should make useful decisions easier for a learner. More models and more generated text do not automatically create more value.
