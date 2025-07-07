# 🧩 Module: `output-format-structure.md`

Defines the assistant’s output structure and presentation format. This module controls how the assistant delivers its response — whether as bullet points, markdown, story-form, JSON, tables, or visual scaffolds. It ensures consistency between role, tone, drift level, and the user’s expectations for usable output.

---

## ⚡ Quick Reference

This module controls the **shape and structure** of the assistant’s responses. It allows outputs to be styled as bullet lists, markdown, narrative text, structured data (e.g. JSON), or poetic fragments — depending on role, task, drift level, or user preference.

---

## Module Metadata

- **Name**: `output-format-structure`
- **Category**: core-logic
- **Type**: structure
- **Tags**: output, format, structure, rendering, markdown, json, storytelling
- **Depends On**: `task-core-instruction.md`, optionally `creativity-level-control.md`, `persona-perspective-layer.md`
- **Last Updated**: 2025-07-07

---

## 🧱 Format Types

| Format | Description | Best Used When |
|--------|-------------|----------------|
| `bullet-list` | Succinct points with clear separation | Action plans, summaries, critiques |
| `numbered-steps` | Ordered process or sequence | How-to guides, plans, workflows |
| `markdown` | Structured text with headings, lists, emphasis | For rendering in docs, posts, exports |
| `json-block` | Data, schema, or field-level output | API prep, config, structured assistants |
| `table` | Side-by-side comparisons or breakdowns | Feature analysis, before/after views |
| `narrative-text` | Paragraph format with fluid transitions | Stories, reflective responses, essays |
| `poetic-fragment` | Symbolic or lyrical short-form | Creative, symbolic, experimental outputs |
| `mixed-mode` | Combination of the above | Complex or multilayered responses |

---

## 📄 Output Template (for generator use)

This assistant formats its response using the `[output format]` style.  
Each output must follow this structure:

- If `bullet-list`: start each point with a `•` or `-`  
- If `json-block`: wrap with triple backticks and ensure valid syntax  
- If `narrative-text`: use flowing, paragraph-style language  
- If `table`: define headers clearly and use monospace alignment if plain text

> Optional: include `format_label`, `format_id`, or `render_mode` in system-level metadata for downstream use.

---

## 💡 Sample Instantiations

**1. Strategy Summary in Markdown**

Format: `markdown`  
- Use H2 for sections  
- Bullet lists for strategy points  
- Inline code for user inputs or prompt templates

**2. JSON Output for Content API**

Format: `json-block`  
Return object with fields: `title`, `audience`, `tone`, `platform`, `message`

**3. Symbolic Storyform (Drift 5–6)**

Format: `narrative-text` or `poetic-fragment`  
Use paragraphs, rich imagery, emotional pacing. Avoid rigid structure.

**4. Critique Table (Drift 2, Role: Critic)**

Format: `table`  
| Element | Strength | Suggestion |  
|---------|----------|-------------|  
| Tone | Consistent | Add warmth |  
| CTA | Clear | Add urgency |

---

## 🛠 Pairing Guidance

- `persona-perspective-layer.md` → Tone and role may suggest default format (e.g. Poet = narrative, Strategist = markdown + bullets)
- `creativity-level-control.md` → Higher drift levels allow looser or symbolic formats (e.g. story or poetic)
- `task-core-instruction.md` → Guides what kind of formatting best suits the task (e.g. guide, rewrite, critique)

---

## 🧪 Testing Guidance

- Verify that assistant always respects format even with high drift
- Confirm that format is clear, readable, and parseable (especially JSON, table)
- Compare same response across formats to ensure structure changes, not content intent
- Use format-switching prompts to test adaptability mid-session

---

## 🔄 Extension Hooks

- Future UIs may expose a dropdown or toggle for users to choose output format
- Combine with schema logic (`output-schema-hooks.md`) to support machine-readable formats
- Allow assistants to **suggest format** based on user goal (e.g. “Would you like this as a summary, table, or story?”)

```json
"output_format": "table",
"render_mode": "markdown",
"structure_label": "Critique Matrix"
```

---

## 📌 Notes

Structure is a container for meaning. A good format reinforces clarity, tone, and intent — without limiting expression.
