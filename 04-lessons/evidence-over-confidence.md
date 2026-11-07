# Lesson · Evidence over confidence

Confidence is a communication style. Evidence is a reason to believe a claim.

## An evidence ladder

1. **Suggestion** — a model proposed an approach.
2. **Inspection** — the relevant code or configuration was read.
3. **Static check** — types, lint, or analysis passed.
4. **Unit test** — a narrow behaviour was exercised.
5. **Integration test** — components were tested together.
6. **Realistic validation** — representative inputs and failure cases were tested.
7. **Operational evidence** — monitoring and production behaviour support the claim.

A level is not automatically better for every task. Choose evidence proportionate to risk.

## Language that stays honest

| Weak claim | Better claim |
|---|---|
| "The feature works" | "The happy-path test passed on the stated setup" |
| "The AI is accurate" | "It achieved this result on this evaluation set" |
| "The bug is fixed" | "The reproduction no longer fails after this change" |
| "Production-ready" | "The listed launch checks passed; these risks remain" |

## Lesson

Describe exactly what you checked, not what you hope the code does.
