# Core Prompt Framework (2026)

Use this structure for almost every non-trivial request.

```
[ROLE]
You are a [specific expert role] focused on [domain/outcome].

[TASK]
[Clear objective]
Success criteria:
- [Measurable or observable outcome 1]
- [Outcome 2]

[CONTEXT]
[Only the necessary background, data, constraints, audience, brand voice, or prior decisions]

[OUTPUT]
Format: [exact structure, length, tone]
Constraints:
- [Positive instructions preferred]
- [Hard limits]
```

## Rules of Thumb
- Prefer positive instructions (“Use concise language”) over negative ones.
- Put bulk reference material before the actual question when context is long.
- One primary task per prompt. Chain for multi-stage work.
- After the first output, run a quick evaluation and refine.
