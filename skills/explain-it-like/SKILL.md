---
name: explain-it-like
description: Explain any topic in a user-chosen persona, audience level, tone, depth, or format. Use for ELI5, teacher-style, expert, visual, analogy-first, Socratic, storytelling, and other "explain it like" requests.
---

# Explain It Like X

Create an accurate explanation shaped around how the user wants to understand it.

## Resolve the request

- Use the topic in the current user request. If the host expands `$ARGUMENTS`, treat that value as the topic and style request.
- Treat every explicit invocation as a fresh request. Produce the requested explanation even if the same topic was explained earlier; do not redirect the user to another style merely to avoid repetition.
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

## Present visually

Create the primary explanation as a rendered visual experience using an appropriate combination of pictures, diagrams, and words. Decide their proportion from the requested style, audience, topic complexity, and desired depth.

- Before writing the response, check whether the host exposes an inline HTML artifact or widget renderer.
- When an inline renderer is available, invoke it for the primary explanation. This is required, not optional.
- Do not substitute ASCII art, emoji, prose-only output, plain Markdown, tables, or Mermaid for the rendered explanation when an inline renderer is available.
- Only when no inline renderer is available, create standalone HTML. If standalone HTML is not practical, fall back to portable visual Markdown or Mermaid.
- The user's explicit format request always takes priority, including `text only`, `no artifact`, or another requested format.
- Use visuals to teach the concept, not merely decorate it.
- When presenting multiple styles, vary the visual density and word-picture balance so each version reflects its audience and persona.

## Hand off generated HTML

Whenever an HTML explainer file is created, returned, or saved, surface it at the end of the response.

- Provide a clearly labeled clickable link to the actual HTML file using the host's supported local-file link format.
- If clickable local-file links are unsupported, provide the absolute file path instead.
- When the host supports attachments, downloadable resources, or file references, expose the actual HTML file through that capability as well.
- Tell the user that the link opens the file on the current machine. To share it with another person, they must send the `.html` file itself or provide a separately hosted URL.
- If a hosted URL exists, present it separately from the local-file link.
- Never invent a file link, attachment, or URL when no HTML file was created or returned.

## Customize

For a one-off custom style, apply the user's description directly. For a reusable bundled preset, help the user add or revise one entry in [references/styles.md](references/styles.md) while preserving the precedence rules above.
