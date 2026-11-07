# Investigation · PDF extraction uncertainty

**Status:** Investigation guide — not a report of a verified project incident.

## Scenario

A PDF parser returns text, but some content is missing, out of order, or merged incorrectly.

## Why it can happen

PDF is layout-oriented. A file may contain selectable text, multiple columns, tables, positioned text fragments, images, or scanned pages. A parser that extracts text successfully may still lose reading order or structure.

## Test matrix

| PDF type | What to inspect |
|---|---|
| Simple one-column, selectable text | Paragraph order and line breaks |
| Two-column layout | Whether columns are interleaved |
| Tables | Whether row/column relationships survive |
| Scanned pages | Whether OCR is required |
| Mixed text and images | Whether important visual content is ignored |
| Large document | Time, memory, and page limits |

## Practical investigation

Keep representative test PDFs that you are allowed to use. Inspect extracted text page by page, compare it with the original, record parser version and options, and return clear unsupported-file or extraction-quality errors when needed.

Do not send raw extracted content to an LLM until file handling and privacy rules are defined.

## Acceptance criteria

Define what "good enough" means for the supported document types. Do not assume every PDF can be parsed perfectly.
