# OW EILX — Explain It Like X

OW EILX is a shared Claude and Codex plugin for creating render-first visual explainers in the style that best fits the learner.

## Examples

```text
Explain Kubernetes like a patient teacher.
Explain black holes like I'm five years old.
Explain OAuth like a senior security engineer with a sequence diagram.
Give me the five-year-old version first, then the expert version.
```

The plugin includes teacher, five-year-old, beginner, expert, storyteller, Socratic coach, analogy-first, visual, executive, and step-by-step presets. Styles can be combined freely.

By default, EILX creates a rendered visual explainer and lets the model balance pictures, diagrams, and words for the requested style, audience, topic complexity, and depth. When the host exposes an inline HTML artifact or widget renderer, the model must invoke it and may not silently substitute ASCII art or text-only output. Standalone HTML, Mermaid, and visual Markdown are fallbacks only when inline rendering is unavailable. An explicit format request such as `text only` or `no artifact` always takes priority.

## Invoke the skill

- Claude Code: `/explain-it-like <topic and style>`
- Codex: `$ow-eilx:explain-it-like <topic and style>`
- Both hosts may also select the skill automatically from a natural-language request.

## Customize styles

Edit [`skills/explain-it-like/references/styles.md`](skills/explain-it-like/references/styles.md). Add a `## Preset name` section describing only the traits that should change the explanation. Explicit instructions in an individual request always override the preset.

## Structure

```text
.claude-plugin/plugin.json
.codex-plugin/plugin.json
skills/explain-it-like/SKILL.md
skills/explain-it-like/agents/openai.yaml
skills/explain-it-like/references/styles.md
```

## License

MIT
