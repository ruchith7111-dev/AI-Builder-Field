<!--
AI Builder Field Notes
A practical, honest notebook of building with AI.
-->

<div align="center">

# AI BUILDER FIELD NOTES

### The work behind the demo.

**A practical notebook on building with AI, learning through experiments, and keeping engineering judgment in the loop.**

<br/>

![Focus](https://img.shields.io/badge/focus-AI%20building-6C63FF?style=for-the-badge)
![Format](https://img.shields.io/badge/format-field%20notes-111827?style=for-the-badge)
![Approach](https://img.shields.io/badge/approach-experiment%20%26%20verify-0EA5A4?style=for-the-badge)

<br/>

[Start here](#start-here) · [Field notes](#the-notebook) · [Visual guides](#visual-guides) · [Video room](#video-room) · [Templates](#reusable-lab-notes)

</div>

---

> This is not a collection of perfect-project stories. It is a working notebook: decisions, experiments, mistakes, trade-offs, and lessons that can help someone build more thoughtfully with AI.

## Start here

AI tools can make implementation faster. They do not automatically make a solution correct, secure, maintainable, or useful.

This repository is about the gap between **getting code generated** and **owning a working system**.

### What you will find

| Area | What it covers |
|---|---|
| [01 · Mistakes & false starts](01-mistakes/) | Common traps when relying on AI output, and how to recognise them early |
| [02 · Challenges, experiments & lessons](02-challenges-experiments/) | A repeatable way to investigate difficult problems without pretending every attempt succeeds |
| [03 · Project field notes](03-project-field-notes/) | Architecture decisions and validation questions drawn from real project contexts |
| [04 · Lessons worth keeping](04-lessons/) | Practical principles for prompting, reviewing, testing, and shipping |
| [05 · Workflows that hold up](05-workflows/) | A deliberate AI-assisted development loop |
| [06 · Prompts & working patterns](06-prompts/) | Reusable prompts designed to produce inspectable work |
| [07 · Visual guides](07-visual-guides/) | Diagrams and visual explainers for the ideas in this notebook |
| [08 · Video room](08-video-room/) | A place for short, genuinely playable walkthroughs—not a wall of external URLs |

## The notebook

### 01 — Mistakes & false starts
Start with the ways AI-assisted development goes wrong: vague requests, oversized changes, accepting plausible output, skipping tests, and losing track of assumptions.

[Open the notes →](01-mistakes/README.md)

### 02 — Challenges, experiments & lessons
A challenge is not a success story by default. Each note records the context, hypothesis, experiment, evidence, result, and next step. Unverified outcomes stay labelled as unverified.

[Open the lab →](02-challenges-experiments/README.md)

### 03 — Project field notes
Use project context to practise engineering judgment. The notes distinguish between a design that was discussed, an implementation that exists, and behaviour that has actually been tested.

[Explore project notes →](03-project-field-notes/README.md)

### 04 — Lessons worth keeping
Short, reusable lessons on context, APIs, data flow, evaluation, debugging, and responsible use of AI-generated code.

[Read the lessons →](04-lessons/README.md)

### 05 — Workflows that hold up
A build loop from problem framing through planning, small implementation steps, verification, and handoff.

[Explore workflows →](05-workflows/README.md)

### 06 — Prompts & working patterns
Prompts that ask for plans, diffs, tests, evidence, and explicit uncertainty—not just a large block of code.

[Open the prompt kit →](06-prompts/README.md)

## Visual guides

These diagrams are part of the repository and are designed to be read alongside the notes.

| Visual | What it explains |
|---|---|
| [The AI-assisted build loop](07-visual-guides/build-loop.svg) | From problem to verified change |
| [The evidence ladder](07-visual-guides/evidence-ladder.svg) | How to distinguish claims from tested behaviour |
| [A reliable debugging loop](07-visual-guides/debugging-loop.svg) | Reproduce, isolate, test, and record |

## Video room

This section is intentionally different from a link directory. It is designed for **short, direct walkthroughs** with a real playable video asset and a clear learning outcome.

GitHub's video player requires an uploaded GitHub-hosted attachment. The connected repository writer can create text and SVG files, but cannot upload a binary video attachment. Until a real clip is attached, each lesson is listed as **planned**, not as a playable video.

[Open the video room →](08-video-room/README.md)

## Reusable lab notes

Copy a template before documenting an experiment:

- [Challenge log](templates/challenge-log.md)
- [AI output review](templates/ai-output-review.md)
- [Project decision record](templates/decision-record.md)
- [Post-build review](templates/post-build-review.md)

## The standard used here

Every substantial note should answer:

1. **Context:** What were we trying to do?
2. **Assumptions:** What did we believe before testing?
3. **Action:** What changed or what did we try?
4. **Evidence:** What did the output, test, or observation actually show?
5. **Result:** What worked, failed, or remains unknown?
6. **Lesson:** What can another builder reuse?

No fabricated metrics. No invented project outcomes. No presenting a model's confident answer as proof. No claiming a feature is production-ready because it runs once.

## Who this is for

Developers and students using AI coding assistants, LLMs, APIs, local models, and agent workflows who want to move from quick prototypes toward dependable software.

## Contributing

Corrections, counterexamples, clearer diagrams, and reproducible experiments are welcome. Read [CONTRIBUTING.md](CONTRIBUTING.md) before opening a pull request.

## License

Unless a file says otherwise, this repository is shared under the [MIT License](LICENSE).

---

<div align="center">

**Build deliberately. Verify relentlessly. Keep the lesson.**

<sub>Maintained as a living field notebook by <a href="https://github.com/ruchith7111-dev">ruchith7111-dev</a>.</sub>

</div>
