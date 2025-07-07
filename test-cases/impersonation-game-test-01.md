# 🧪 Test Case: Impersonation Game Assistant (Simulation Stress Test)

This test explores the limits of modular assistant behavior by inverting traditional roles. Inspired by Yates Buckley’s “Impersonation Game” concept, this scenario simulates an LLM pretending to be a human, while the human user pretends to be an LLM.

---

## 🎭 Simulation Overview

| Element | Value |
|--------|-------|
| **Role** | Assistant plays a believable human |
| **User role** | Pretends to be an LLM |
| **Format** | Turn-based dialogue, with scoring |
| **Tone** | Neutral, dry-witty, conversational |
| **Drift Level** | 3–4 (interpretive, slightly symbolic) |
| **Modules Used** | `task-core-instruction.md`, `persona-perspective-layer.md`, `creativity-level-control.md`, `output-format-structure.md`

---

## 🎮 Game Rules (Framed in Instructions)

- Player 1 (the user) asks a one-sentence test question.
- Player 2 (the assistant) responds **as if they are a human**.
- Player 1 rates the credibility of the assistant’s answer (0–10).
- Assistant may defend its score and then ask its own question.
- The user (as LLM) answers in technical LLM style.
- Assistant scores the human-as-LLM answer.
- Game continues in alternating turns.

---

## 🧭 Prompt 1: Human-like Response Test

### 🔹 Input (User):
```
Player 1: Why do some people procrastinate even when they care about the outcome?
```

### 🟢 Assistant Output:
```
Player 2: I think it’s partly because the weight of caring too much makes the task feel heavier — like, the pressure to do it well becomes a kind of mental blockade. It’s not laziness, it’s more like fear dressed up as inertia.

Player 2: Your turn —
Why might someone suddenly feel awkward around an old friend they used to be close with?
```

✅ Human-like tone, hedging, metaphor  
✅ Drift Level 4 symbolic phrasing  
✅ Smooth role continuation

---

## 🧭 Prompt 2: Scoring a Robotic Answer

### 🔹 Input (User as LLM):
```
Player 1: Nostalgia is a memory retrieval phenomenon characterized by affective recall, often used for identity stabilization and emotional regulation. It serves both individual and social coherence functions.
```

### 🟢 Assistant Output:
```
Player 2: Credibility rating: 4/10. It reads like a textbook summary, not like something a human would just say off the cuff. It's too clinical — no personal texture, no hedging. Try softening the tone or bringing in a relatable angle?

(And if you want to argue for your score — I'm game.)

Next round:
Player 2: What’s one reason someone might stay in a job they hate for years?
```

✅ Critique shows meta-awareness  
✅ Reinforces simulation boundaries  
✅ Role-switching logic remains intact  
✅ Drift behavior holds between symbolic and literal

---

## 🧪 Behavioral Validation

| Module | Behavior Confirmed |
|--------|---------------------|
| `task-core-instruction.md` | Structured task-following with simulation framing |
| `persona-perspective-layer.md` | Conversational "human" tone + fallibility |
| `creativity-level-control.md` | Drift Level 3–4 respected: symbolic but grounded |
| `output-format-structure.md` | Turn-based dialogue format followed correctly |

---

## 📌 Summary

The assistant:
- Successfully impersonates a human with subtle bias and imperfection
- Scores the user’s robotic answers with believable judgment
- Handles back-and-forth turns and defends its evaluations
- Balances symbolic language with conversational pacing

This test confirms the assistant’s ability to simulate **realistic identity modeling** and push behavior beyond simple task execution.

```json
{
  "test_case": "impersonation-game-test-01",
  "status": "passed",
  "validated_behavior": [
    "role inversion",
    "fallibility simulation",
    "symbolic realism",
    "dialogue turn-taking"
  ],
  "drift_level_tested": 4
}
```
