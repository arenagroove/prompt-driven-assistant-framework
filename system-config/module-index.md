# 📚 Module Index – Prompt-Driven Assistant Framework

This is a complete catalog of all modular prompt files available in the system. Use this file to browse available components, understand dependencies, and locate relevant modules by category or tag.

---

## ✅ Status Key
- `done`: Finalized and validated
- `drafted`: Written, pending review
- `pending`: Not started yet

---

## 🧠 1. Core Instruction Logic

| Module Filename | Description | Category | Depends On | Tags | Status |
|------------------|-------------|-----------|------------|------|--------|
| `task-core-instruction.md` | Defines the assistant’s core task and user goal | core | – | instruction, task, role | done |
| `persona-perspective-layer.md` | Sets tone, voice, lens, and role identity | core | task-core-instruction | persona, lens, tone, strategist | done |
| `creativity-level-control.md` | Controls interpretive drift (0–6 scale) | core | persona-perspective-layer | creativity, drift, generative | done |
| `output-format-structure.md` | Defines response structure (list, story, etc.) | core | task-core-instruction | format, structure, output | done |

---

## 🛠 2. Prompt Design Utilities

| Module Filename | Description | Category | Depends On | Tags | Status |
|------------------|-------------|-----------|------------|------|--------|
| `placeholder-syntax-support.md` | Enables `{variable}` slots in prompt templates | utility | – | template, placeholder, reuse | pending |
| `sample-instantiated-prompt.md` | Provides filled-in example prompts | utility | task-core-instruction | example, test, clarity | pending |
| `prompt-testing-logic.md` | Adds test logic for validating outputs | utility | core logic modules | testing, validation, reliability | pending |
| `examples-counterexamples.md` | Shows good vs. bad prompt usage | utility | task-core-instruction | boundaries, clarity, examples | pending |
| `feedback-refinement-cycle.md` | Enables critique and output refinement loops | utility | output-format-structure | feedback, iteration, critique | pending |

---

## 🧩 3. Behavior Layers & Output Logic

| Module Filename | Description | Category | Depends On | Tags | Status |
|------------------|-------------|-----------|------------|------|--------|
| `context-history-management.md` | Simulates memory and manages context threading | behavior | – | memory, context, thread | pending |
| `adaptive-tone-lens-switching.md` | Enables mid-session persona/lens shifts | behavior | persona-perspective-layer | adaptive, dynamic, switch | pending |
| `agent-collaboration-logic.md` | Enables prompt handoffs between assistants | behavior | context-history-management | agent, collaboration, flow | pending |

---

## 🖼 4. Prompt-as-Interface Modules

| Module Filename | Description | Category | Depends On | Tags | Status |
|------------------|-------------|-----------|------------|------|--------|
| `mode-presets-catalog.md` | Predefined assistant behavior presets | interface | persona-perspective-layer | presets, modes, roles | pending |
| `output-schema-hooks.md` | Adds SEO, GEO, or structured schema blocks | interface | output-format-structure | schema, structured, geo | pending |
| `multimodal-content-guide.md` | Handles images, audio, and code inputs/outputs | interface | task-core-instruction | multimodal, hybrid, media | pending |
| `prompt-metadata-tags.md` | Adds tags and categories for indexing/search | interface | – | metadata, tags, ui | pending |

---

## ⚙️ 5. System Configuration

| Module Filename | Description | Category | Depends On | Tags | Status |
|------------------|-------------|-----------|------------|------|--------|
| `active-modules.json` | JSON file declaring active modules for generation | config | – | config, toggle, enabled | drafted |
| `module-index.md` | This file – searchable index of all modules | config | all modules | index, catalog, lookup | done |
| `prompt-export-template.md` | Combines active modules into final prompt | config | active-modules.json | export, generator, builder | pending |

---

## 🧭 6. Meta-Prompting & Microtask Modules

| Module Filename | Description | Category | Depends On | Tags | Status |
|------------------|-------------|-----------|------------|------|--------|
| `microtask-prompt-generator.md` | Breaks abstract goals into concrete subtasks | meta | task-core-instruction | subtasks, microstep, logic | pending |
| `cross-assistant-prompt-adapter.md` | Converts prompts between assistant schemas | meta | output-format-structure | adapter, interop, schema | pending |
| `facing-prompt-generator.md` | Builds follow-up or reflection prompts | meta | task-core-instruction | reflection, dialogue, followup | pending |
| `prompt-to-prompt-module.md` | Converts prompt ideas into reusable modules | meta | placeholder-syntax-support | symbolic, template, module | pending |

---

## 📌 Notes

- This index reflects the current state of `prompt-module-progress.md`
- For development progress, see: `system-config/prompt-module-progress.md`
- All modules follow consistent metadata, dependency, and behavioral patterns

```json
{
  "total_modules": 23,
  "completed": 4,
  "drafted": 1,
  "pending": 18
}
```
