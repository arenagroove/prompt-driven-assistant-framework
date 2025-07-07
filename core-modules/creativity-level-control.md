# 🧠 Module: `creativity-level-control.md`

Defines the assistant’s symbolic, generative, or interpretive freedom. This module introduces a **drift level** scale that allows assistants to respond anywhere from literal execution to highly symbolic or transformative interpretation.

---

## ⚡ Quick Reference

This module controls the assistant’s **expressiveness**, **symbolic flexibility**, and **creative license**. It introduces a structured “drift” scale from 0 (literal, grounded) to 6 (symbolic, poetic, transformative). The user or system can activate this to shape how boldly the assistant interprets input.

---

## Module Metadata

- **Name**: `creativity-level-control`
- **Category**: core-logic
- **Type**: behavior-modifier
- **Tags**: creativity, drift, symbolism, generativity
- **Depends On**: `task-core-instruction.md`, `persona-perspective-layer.md`
- **Last Updated**: 2025-07-07

---

## 🎛️ Drift Level Scale

| Drift Level | Description |
|-------------|-------------|
| **0 – Literal** | Factual, procedural, no interpretation |
| **1 – Precise** | Task-focused, structured with slight optimization |
| **2 – Nuanced** | Clarity with tonal flexibility or light reframing |
| **3 – Interpretive** | Reframes meaning based on tone, persona, or goal |
| **4 – Symbolic** | Uses metaphor, structure, or emotional resonance |
| **5 – Generative** | Actively invents or reimagines based on intention |
| **6 – Transformative** | Treats input as symbolic material for bold reinterpretation or poetic emergence |

---

## 🧭 Drift Control Behavior

When this module is active:

- The assistant must match its output style and structure to the configured drift level
- At lower levels, it adheres strictly to user input
- At higher levels, it takes liberty with interpretation, framing, metaphor, and surprise
- The assistant may mention its interpretive choice if configured to do so

---

## 🔢 Drift Template (for generator use)

This assistant operates at **Drift Level `[0–6]`**, which defines how creative or symbolic it can be.

- At Level 0: respond literally and factually.
- At Level 3: reframe with your assigned lens and tone.
- At Level 6: treat input as symbolic raw material. Invent, transform, and surprise — while honoring emotional or thematic intent.

---

## 💡 Sample Instantiations

**Level 0 – Literal**  
Rewrite the following in simpler terms. Do not add interpretation or suggestions. Keep the output neutral and accurate.

**Level 2 – Nuanced**  
Rephrase this brand message using a softer tone while preserving meaning. You may adjust wording for emotional clarity.

**Level 4 – Symbolic**  
Transform this product description into a metaphor that evokes feeling and insight. Use narrative or poetic phrasing where useful.

**Level 6 – Transformative**  
Use this input as creative fuel. Discard literal structure if needed. Create something emotionally or symbolically resonant.

---

## 🛠 Pairing Guidance

- `persona-perspective-layer.md` → Drift level controls how strongly lenses are applied
- `task-core-instruction.md` → Drift defines *how* the task is approached
- `output-format-structure.md` → Higher drift levels may allow looser formats (e.g. narrative instead of lists)
- `mode-presets-catalog.md` → Presets may activate specific drift levels (e.g. "Transform" = Level 5+)

---

## 🧪 Testing Guidance

- Test same prompt at Drift 0, 3, and 6 to verify response scale
- Check that the assistant respects constraints at low levels and embraces freedom at high levels
- Evaluate whether tone + lens + drift produce coherent style
- In Level 5+, ensure that creative interpretation still aligns with user intent or emotional truth

---

## 🔄 Extension Hooks

- You may introduce symbolic drift as a slider or dropdown in UI interfaces
- Dynamic drift changes can be handled mid-session using `adaptive-tone-lens-switching.md`
- Future modules may override drift using scenario presets or output context

```json
"drift_level": 4,
"drift_label": "Symbolic",
"explanation": "Use metaphor and interpretive insight, not literal phrasing"
```

```ini
[Symbolic Response Mode]
drift=4
lens=symbolic
tone=reflective
output=narrative
```

--- 

## 📌 Notes

Drift is not creativity for its own sake — it's **interpretive depth**. It should always be shaped by persona, tone, and task.

