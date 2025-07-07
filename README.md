# 🧠 Prompt-Driven Assistant Framework

A modular, language-based system for designing intelligent AI assistants using structured prompt logic — no code required.

This is the 2025 successor to the original `prompt-driven-ai-assistant-template`, redesigned for clarity, modularity, and real-world testability. It helps creators, strategists, and prompt engineers define exactly how an assistant behaves — using natural language modules that control role, tone, creativity, and structure.

---

## 🌟 What It Is

A set of clean, swappable **prompt modules** that let you define:

- 🧠 What your assistant does (task logic)
- 🎭 How it speaks and sees the world (persona + tone + lens)
- 🎨 How imaginative or literal it is (drift level)
- 🧾 How it structures output (list, story, JSON, etc.)

---

## 🔧 Key Features

- ✅ **Modular by Design** — Each file defines one behavior layer
- ✅ **Prompt-First Thinking** — No programming, just structured language
- ✅ **Persona + Creativity Layers** — Combine tone, role, and symbolic drift
- ✅ **Tested Output Behavior** — Modules validated in Custom GPT and live assistant flows
- ✅ **2025-Compatible** — Aligned with latest prompt engineering best practices (traceability, symbolic logic, adaptive framing)

---

## 📦 Folder Structure

```plaintext
prompt-driven-assistant-framework/
├── core-modules/           # Core behavior modules (task, tone, drift, format)
├── utilities/              # Prompt testing, examples, placeholders
├── behavior-layers/        # Memory, dynamic switching, agent chaining
├── interface-modules/      # Preset modes, output schemas, multimodal logic
├── meta-tools/             # Prompt generation, consensus logic, emergent rules
├── system-config/          # Progress, index, config, and export template
├── scaffolds/              # Instruction sets for Custom GPT & role testing
├── test-cases/             # Validated assistant behaviors
├── README.md
└── LICENSE
```

---

## ✅ Current Modules (v1.0)

| Module | Purpose |
|--------|---------|
| `task-core-instruction.md` | What the assistant is for |
| `persona-perspective-layer.md` | How the assistant thinks, speaks, and sees |
| `creativity-level-control.md` | How symbolically it interprets inputs (Drift 0–6) |
| `output-format-structure.md` | How it formats its response (bullets, story, JSON, etc.) |

---

## 🧪 Validated Assistants

### ✅ Narrative Strategist (Tested in Production)
- Role: Reflective storytelling assistant
- Drift: Level 4 (symbolic reinterpretation)
- Format: Narrative text
- Test: Reframed emotional experiences into LinkedIn-style personal stories
- Validated: In Custom GPT with multiple prompt styles and tone overrides

### ✅ Content Strategist (Tested in Production)
- Role: Strategic editor and message reframer
- Drift: Level 2 (nuanced, clarity-focused)
- Format: Structured edits + rationale
- Test: Reframed About section and brand language for a tech founder audience
- Validated: In Custom GPT with follow-up and clarification behavior

### ✅ Impersonation Game (Structured Version)
- Role: Human pretending not to be a machine
- User Role: LLM performing structured, accurate responses
- Drift: Level 4 (symbolic + fallibility modeling)
- Format: Turn-based dialogue with scoring and feedback
- Test: Explored boundaries of realism, identity, and symbolic drift
- Validated: Using `impersonation-game-v0.2.md` scaffold

### ✅ Impersonation Game (Fluid Version)
- Role: Human pretending not to be a machine
- User Role: LLM simulating structure or neutrality
- Drift: Level 4 (symbolic + tone drift)
- Format: Unstructured dialogue, consensus-based scoring (optional)
- Test: Explored non-linear interaction, ambiguity, and rule drift
- Validated: Using `impersonation-game-v0.3-fluid.md`, leading to emergent module design

---

## 🔭 Future Enhancements

- Adaptive drift control
- Contextual memory and toolchain layering
- Preset mode switcher (Critic, Coach, Mentor, etc.)
- Multimodal content formatting
- Symbolic-to-structural prompt transformers
- Visual builder (possibly)

### 🧠 Emergent Interaction Support (Now in Progress)
- `emergent-rules-logic.md` — Allows the assistant to suggest, mutate, or discard rules mid-play (*validated in v0.3 scaffold*)
- `consensus-negotiation-layer.md` — Models scoring reflection, soft disagreement, and flexible outcome logic (*validated in v0.3 scaffold*)

---

## 📜 License

MIT — open, remixable, and collaboration-friendly.

---

## 🙌 Contributing

Pull requests, feature ideas, and assistant test cases are welcome.  
Once v1.1.0 launches, we’ll open up issue tracking and release planning.

```json
"version": "1.0.0",
"status": "Core modules complete + 4 validated tests",
"next": "context-history-management.md"
```
