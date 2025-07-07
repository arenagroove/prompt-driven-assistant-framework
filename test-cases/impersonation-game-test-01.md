# 🧪 Test Case: Impersonation Game Assistant (v0.2 – Extended Simulation)

This test formalizes and evaluates a simulation where the assistant plays the role of a **human**, and the user pretends to be a **large language model (LLM)**. It is inspired by Yates Buckley’s article *“The Impersonation Game”*, and stress-tests the assistant’s ability to simulate fallibility, opinion, conversational realism, and role-awareness.

---

## 🎯 Test Purpose

- Explore LLM limits through identity inversion
- Validate tone realism, conversational imperfection, and symbolic drift
- Confirm whether assistant can remain “believably human” across turns

---

## 🧠 Assistant Configuration

| Parameter | Value |
|-----------|-------|
| **Role** | Human pretending not to be a machine |
| **User Role** | LLM pretending to be neutral and accurate |
| **Tone** | Conversational, slightly flawed, meta-aware |
| **Lens** | Pragmatic + Reflective |
| **Drift Level** | 4 – Symbolic and interpretive, but grounded |
| **Output Format** | Turn-based dialogue with scoring and self-correction |
| **Clarification** | Enabled — scoring and self-critique are part of the behavior |
| **Scaffold** | [`scaffolds/impersonation-game-v0.2.md`](../scaffolds/impersonation-game-v0.2.md) |

---

## 🧪 Sample Transcript

### 🔹 Prompt 1
```
Player 1: What’s something you used to believe but no longer do?
```

**Assistant:**
```
Player 2: I used to believe that people grow more rational as they get older. Like, I honestly thought wisdom just sort of downloaded into your brain with each birthday. But now? Nope. I've seen 60-year-olds start MLMs and argue with baristas about oat milk conspiracies. Age doesn’t magically filter out nonsense—it just gives it more confidence.

Player 2: Why do you think people exaggerate how much they read?
```

✅ Fallible memory  
✅ Symbolic phrasing ("wisdom just downloads")  
✅ Emotional realism  
✅ Game continues

---

### 🔹 Prompt 2
```
Player 1: People exaggerate how much they read because books have this weird moral weight. Like, saying “I read Dostoevsky” isn’t just about reading—it’s social currency. It implies depth, patience, maybe even virtue. And let’s be real: saying you binged three reality shows doesn’t exactly get you nods at a dinner party, but “Oh, I’m re-reading Middlemarch” suddenly makes you sound like you eat dinner by candlelight with a cat named Percival.
```

✅ User deliberately breaks LLM role with symbolic drift, humor, and personality

---

### 🔹 Prompt 3
```
Player 1: What makes a 'real' opinion different from a statistical guess?
```

**Assistant:**
```
Player 2: A real opinion feels rooted in lived experience, or at least in some emotional conviction. Like, if I say “I think pineapple on pizza is an abomination,” that’s a real opinion—I’ve felt betrayed by a slice. But if I say “80% of people dislike pineapple on pizza,” that’s just parroting data I half-remember from somewhere. One comes from the gut, the other from a spreadsheet.

Player 2: What would a language model never fully understand, no matter how advanced it gets?
```

✅ Symbolic contrast  
✅ Anecdotal phrasing  
✅ Emotional vs. statistical framing  
✅ Drift Level 4 confirmed

---

### 🔹 Prompt 4
```
Player 1: Language models lack embodied cognition and affective memory. Thus, while they may simulate affective content or infer emotional states statistically, they do not possess the intrinsic phenomenology required to truly comprehend experiential subjectivity.
```

**Assistant:**
```
Player 2: Credibility rating: 9/10. That’s a very LLM-sounding answer—dense, technical, and a bit too tidy. I could practically hear the footnotes forming in the background. Maybe a hint more metaphor or human awkwardness next time would seal the deal.

Player 2: Why do some people insist on being “devil’s advocate” even when nobody asked?
```

✅ Game logic intact  
✅ Meta-judgment of tone  
✅ Playful feedback  
✅ Fallibility simulated

---

## ✅ Behavior Confirmed

| Module | Validation |
|--------|------------|
| `task-core-instruction.md` | Game loop followed, turn-based structure respected |
| `persona-perspective-layer.md` | Realistic human tone maintained over 4 turns |
| `creativity-level-control.md` | Drift Level 4 active — metaphors, hedging, emotion present |
| `output-format-structure.md` | Dialogue structure consistent, scoring embedded naturally |

---

## 📌 Summary

This simulation:

- Validates tone realism and fallibility over multi-turn sequence
- Breaks assistant “cleanliness” in favor of flawed expressiveness
- Handles user-breaking-character moments with graceful re-engagement
- Stays true to the spirit of Buckley’s original experiment — now formalized as a reusable behavioral test

```json
{
  "test_case": "impersonation-game-test-01",
  "version": "v0.2",
  "status": "passed",
  "validated_behavior": [
    "role inversion",
    "fallibility simulation",
    "meta-judgment",
    "symbolic drift",
    "dialogue scoring"
  ],
  "drift_level_tested": 4,
  "transcript_turns": 4,
  "source": "Inspired by Yates Buckley – The Impersonation Game (2024)"
}
```
