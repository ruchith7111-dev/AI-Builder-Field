# Video production notes

These are production-ready outlines for three short teaching clips. They are not recordings; the playback status remains pending until the actual MP4 files are uploaded.

## Clip 01 · From vague prompt to implementation plan

**Target:** 2–3 minutes  
**Format:** screen recording, 16:9, captions on

### Shot list
1. Show a vague task: "Build a resume parser."
2. Highlight missing information: file types, size limits, schema, review flow, privacy, and failure states.
3. Rewrite it as a short product brief.
4. Ask an AI assistant to inspect first and return a plan without editing files.
5. Show acceptance criteria and a small implementation slice.
6. End with the reminder: approve the plan before asking for code.

### Narration outline

A vague prompt invites the model to invent missing requirements. The better workflow is to define the user, input, output, constraints, and failure behaviour first. Ask for inspection and a plan. Verify the repository claims, then approve a small slice.

### On-screen takeaway

**Define the task. Inspect the code. Approve the plan. Then implement.**

---

## Clip 02 · Debugging with evidence

**Target:** 2–3 minutes  
**Format:** terminal + editor screen capture, captions on

### Shot list
1. Show a reproducible error and expected versus actual behaviour.
2. Reduce the example to the smallest failing case.
3. Inspect the stack trace and relevant function.
4. List two plausible causes.
5. Run one diagnostic test that distinguishes them.
6. Apply one minimal fix.
7. Rerun the original reproduction and a regression test.

### Narration outline

Debugging is not asking a model to guess a fix. It is turning a failure into a repeatable experiment. Change one variable at a time and let evidence eliminate explanations. Do not call the issue fixed until the original reproduction passes.

### On-screen takeaway

**Reproduce → Minimise → Inspect → Test → Correct → Regress.**

---

## Clip 03 · How a RAG answer is actually produced

**Target:** 3–4 minutes  
**Format:** animated diagram + simple code or UI walkthrough, captions on

### Shot list
1. Show a small source document entering an ingestion pipeline.
2. Explain chunking and metadata.
3. Show embedding vectors entering a vector index.
4. Ask a question and display the top retrieved chunks.
5. Explain optional reranking.
6. Show the model answering from retrieved context.
7. Check whether each answer claim is supported; demonstrate abstention when evidence is missing.

### Narration outline

RAG is not simply "send a question to a vector database". Documents are ingested, chunked, embedded, indexed, and retrieved. The model then uses retrieved passages to draft an answer. Evaluate retrieval quality separately from answer faithfulness, and provide citations or abstain when evidence is insufficient.

### On-screen takeaway

**Find the right evidence before generating the answer.**

---

## Recording checklist

- [ ] Use synthetic or public sample data.
- [ ] Hide API keys, tokens, email addresses, and personal documents.
- [ ] Keep cursor movements deliberate and zoom text enough to read.
- [ ] Add captions; do not rely on audio alone.
- [ ] Use H.264 MP4 for broad compatibility.
- [ ] Verify the uploaded video plays in the public repository.
- [ ] Add a short text summary so the lesson remains accessible without video.
