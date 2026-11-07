# Investigation · RAG retrieval quality

**Status:** Investigation guide — not a report of a verified project incident.

## Scenario

A retrieval-augmented generation answer is fluent but misses the relevant source, combines unrelated chunks, or cites evidence that does not support the claim.

## Separate the pipeline

1. **Ingestion:** Were the right documents loaded?
2. **Chunking:** Was useful context split or merged badly?
3. **Embedding:** Were compatible models and dimensions used?
4. **Retrieval:** Did relevant chunks appear in the top results?
5. **Reranking:** Did ordering improve?
6. **Generation:** Did the model stay within retrieved evidence?
7. **Citation:** Does each claim map to the correct source span?

## Build a tiny evaluation set

For each question, record the expected source document and passage, retrieved top-k passages, whether the relevant passage appears, whether the answer is supported, and whether the system should abstain.

## Debugging rule

Do not tune the final prompt to compensate for a retrieval failure until you know whether retrieval supplied the right evidence. Evaluate retrieval and generation separately.
