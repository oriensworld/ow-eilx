---
name: explain-it-like
description: Explain any topic in a user-chosen persona, audience level, tone, depth, or format. Use for ELI5, teacher-style, expert, visual, analogy-first, Socratic, storytelling, and other "explain it like" requests.
---

# Explain It Like X

Create an accurate explanation shaped around how the user wants to understand it.

## Resolve the request

- Use the topic in the current user request. If the host expands `$ARGUMENTS`, treat that value as the topic and style request.
- Extract any requested audience, persona, tone, depth, length, examples, or output format.
- Use the explicit style named by the user. If none is given, default to `teacher`.
- Explicit user instructions override every preset.
- Treat an unknown "X" as a valid free-form persona or audience. Infer its useful teaching traits instead of rejecting it.
- Styles are composable. For example, "a patient teacher for a five-year-old, using pictures and one analogy" combines all of those constraints.

Read [references/styles.md](references/styles.md) when applying a named preset, listing available presets, or helping someone customize the catalog.

## Explain

- Match vocabulary, pacing, examples, and structure to the chosen audience and persona.
- Simplify presentation without changing important facts. State a necessary caveat plainly when omitting it would make the explanation wrong.
- Define unavoidable jargon on first use.
- Prefer concrete examples over abstract claims.
- Start with the explanation, not a description of the selected configuration.
- Do not become condescending or use baby talk, including in the five-year-old style.
- If the user requests multiple styles, present them in the requested order and make the differences useful rather than repetitive.

Use ordinary conversation output by default. If the user asks for a visual or HTML explanation, use the host's supported visual output; otherwise provide portable Markdown, Mermaid, or a standalone HTML file as appropriate.

## Customize

For a one-off custom style, apply the user's description directly. For a reusable bundled preset, help the user add or revise one entry in [references/styles.md](references/styles.md) while preserving the precedence rules above.
