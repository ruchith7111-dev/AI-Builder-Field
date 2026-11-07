# Project field note · AI Resume Parser Platform

**Evidence label:** Design context recorded during project planning. Verify the current repository before treating this as an implementation report.

## Product intent

A user uploads a resume PDF, the system extracts text, an LLM converts the text into structured fields, and the user can inspect the result before it is stored.

## Architecture discussed

    PDF upload
       |
       v
    API route: /api/parse-resume
       |
       v
    PDF text extraction (pdf-parse)
       |
       v
    LLM structured extraction
       |
       v
    schema validation
       |
       v
    user review / correction
       |
       v
    Supabase persistence

The discussed stack included Next.js 14, TypeScript, Tailwind CSS, API routes, Supabase, and Gemini. A low generation temperature was considered for extraction; temperature alone does not guarantee valid or accurate structured data.

## Data model discussed

Potential tables included:

- **resumes** — file metadata, owner, processing status, and timestamps.
- **work_experience** — role, organisation, dates, and description.
- **education** — institution, qualification, dates, and relevant details.
- **certifications** — name, issuer, issue date, and credential reference.

This is a planning snapshot. Check the migrations and current schema before assuming these exact tables exist.

## Engineering decisions to make explicit

### 1. File boundary
Define accepted MIME types, extension checks, maximum size, page limits, and whether encrypted or scanned PDFs are supported. A filename extension is not a sufficient file-type check.

### 2. Extraction quality
Store extraction status and surface low-quality or empty text. Test multiple layouts; do not silently treat missing text as a valid empty resume.

### 3. Structured output
Use a typed schema and validate every field. Distinguish a missing value from a confidently extracted value. Preserve source snippets or page references where practical so a user can review important fields.

### 4. Persistence
Validate ownership and data shape before writing. Decide what happens when one of several database writes fails. Avoid leaving half-created records without a recoverable status.

### 5. Privacy
Resumes contain personal information. Define retention, deletion, access control, logging redaction, and which external model provider receives document text.

## High-value tests

| Test input | Expected behaviour to define |
|---|---|
| Valid one-column resume | Expected fields extracted with reviewable values |
| Two-column resume | Reading order checked; uncertainty shown when extraction is ambiguous |
| Scanned PDF | OCR requirement identified or a clear unsupported result returned |
| Corrupt or encrypted file | Controlled error; no false success |
| Oversized file | Rejected before expensive processing |
| Missing dates or sections | Optional fields remain absent/unknown, not invented |
| Model returns invalid structure | Validation failure handled without unsafe persistence |
| User A requests User B's record | Access denied |

## Portfolio evidence to collect

- Architecture diagram that matches the running code.
- Schema or migration files.
- Tests for the cases above.
- A redacted demo document.
- Screenshots or a short walkthrough showing the review-and-correction flow.
- A clear statement of what is implemented versus planned.

## Lesson

For document AI, extraction is not the same as understanding. A useful product needs traceable fields, visible uncertainty, validation, and a human correction path.
