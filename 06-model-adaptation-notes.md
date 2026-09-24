# Model Adaptation Notes (2026)

Quick adjustments when switching between major model families.

## General
- State the goal and success criteria clearly. Modern models need less step-by-step control.
- Prefer positive instructions.
- Use structured output (markdown headings, XML-style tags, or JSON) when format matters.

## OpenAI (GPT-5.x / reasoning models)
- Put high-level role and constraints in the system / instructions field.
- For reasoning models: focus on objective + constraints; avoid rigid procedure lists.
- Use native JSON mode / schema when available.
- Pin model snapshots in production.

## Anthropic (Claude 4.x)
- XML tags work especially well for separating Role / Task / Context / Output.
- Prefilling the start of the response is effective for strict formats.
- Extended / adaptive thinking is preferred over manual “think step-by-step” for complex work.

## Google (Gemini)
- Data-first ordering (bulk context first, question last) often improves long-context performance.
- Few-shot examples remain highly effective.
- Keep temperature near default for most generative tasks unless you need more determinism.

## Cross-model tip
When a prompt works well on one model, run the Evaluation Template and note which parts transfer. Keep a short “model notes” log per high-value prompt.
