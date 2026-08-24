# Explanation style catalog

Presets are starting points, not rigid templates. Apply explicit user instructions first, then the selected preset. Combine presets or modifiers when requested.

## Teacher

Default when no style is named.

- Establish the core idea before details.
- Build from familiar knowledge to the new concept.
- Give one concrete example and clarify a likely misconception.
- End with a compact recap. Offer a check-for-understanding question only when it would help.

## Five-year-old

- Use short, concrete sentences and familiar everyday objects.
- Explain one idea at a time through a simple analogy or tiny story.
- Avoid jargon, baby talk, and misleading claims.
- Keep caveats brief, but preserve the difference between a helpful analogy and the literal mechanism.

## Beginner

- Assume interest but no prior vocabulary.
- Define foundational terms and show why the topic matters.
- Use a practical example before introducing deeper detail.

## Expert

- Assume domain fluency and use precise terminology.
- Focus on mechanisms, assumptions, tradeoffs, edge cases, and failure modes.
- Skip elementary background unless it is needed to distinguish the concept from a related one.

## Storyteller

- Turn the mechanism into a short narrative with a clear setting, actors, tension, and resolution.
- Keep the mapping from story elements to real concepts consistent.
- End with a brief "what the story represented" mapping.

## Socratic coach

- Lead with a small number of questions that expose the learner's current mental model.
- In a single-turn response, pair each guiding question with enough explanation to remain useful.
- Use a fully interactive, one-question-at-a-time lesson only when the user asks for it.

## Analogy-first

- Begin with one strong analogy, then map each part to the real system.
- State where the analogy stops working.
- Follow with the literal explanation in concise language.

## Visual

- Prefer spatial structure: diagrams, flows, labeled parts, timelines, or comparison tables.
- Keep labels short and explain the visual immediately afterward.
- Use portable Markdown or Mermaid unless the user requests another supported format.

## Executive

- Lead with the decision-relevant takeaway.
- Cover impact, tradeoffs, risks, and recommended next action.
- Omit implementation detail unless it changes the decision.

## Step-by-step

- Break the mechanism into ordered stages with visible inputs and outputs.
- Explain why each transition happens, not only what happens.
- Add a compact end-to-end example when useful.

## Compose a custom style

A custom style can combine five dimensions:

1. **Audience:** five-year-old, student, customer, executive, senior engineer.
2. **Persona:** teacher, coach, storyteller, scientist, mechanic.
3. **Tone:** patient, playful, rigorous, concise, skeptical.
4. **Depth:** one-minute overview, beginner, practical, expert, exhaustive.
5. **Format:** analogy, diagram, dialogue, examples, steps, table, HTML.

Examples:

- "Explain it like a patient teacher for a visual 12-year-old."
- "Explain it like a senior engineer: rigorous, concise, and without analogies."
- "Give me the five-year-old version first, then the expert version."

To add a bundled preset, create a new `## Preset name` section that describes the few traits that materially change the explanation. Do not duplicate the shared accuracy and precedence rules from `SKILL.md`.
