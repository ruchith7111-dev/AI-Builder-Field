# Lesson · Context before code

A model can only reason over the context it receives and the tools it can actually use. Missing context is often replaced by assumptions.

## Give the model a working map

For a code task, supply the relevant entry points, file paths, types, existing patterns, constraints, expected behaviour, and commands used to test the feature.

Do not dump the entire repository by default. Provide the smallest useful slice and ask the model to identify what else it needs.

## Verify repository claims

When an AI tool says "the project already uses X", inspect the dependency file or source. When it says "this function is called here", search the code. A confident summary is not a substitute for reading the repository.

## Practical check

Before implementation, ask the model to list:
- files it expects to change;
- files it needs to inspect first;
- assumptions it is making;
- acceptance criteria;
- risks that need human decisions.

Then compare that plan with the actual repository.
