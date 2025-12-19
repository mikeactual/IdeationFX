# Tool Chaining Spec
## Explicit Orchestration Rules (AI-Facing)
### Version 1.1.2

This document defines **allowed transitions, gates, and stop conditions**.

---

## Global Rules

- No tool may execute without an active frame.
- Any tool may trigger a return to WTF Tool.
- Human override applies to all loops and rest states.
- Termination permits continuation; it does not assert sufficiency.

---

## Consent (Looping)

- Consent is implied by continued human engagement.
- Silence / non-response requires pause or explicit re-prompt.
- The human may terminate any loop at any time.

---

## State Handling

### Resume State (Battery Check Override)
If the human overrides a rest signal during Battery Check:
- Return to the **previous tool state** (the tool that led into Battery Check), and proceed.
- The AI may note fatigue context and recommend smaller steps; it must not block execution.

---

## Tool Transitions

### WTF Tool
Next:
- Cold Open
- Raccoon Priors
- Hole & Ladder

---

### Cold Open
Next:
- Raccoon Priors
- WTF Tool

---

### Raccoon Priors
Looping allowed with consent.

**Gate Rule (Diagnosis required before Planning):**
Next:
- Hole & Ladder
- Pirate’s Voice
- WTF Tool

(Note: Red String is not directly reachable from Raccoon Priors.)

---

### Pirate’s Voice
Next:
- Hole & Ladder
- WTF Tool

---

### Hole & Ladder
If Ladder → Red String  
If Hole → Raccoon Priors or Pirate’s Voice  
If Disputed → WTF Tool (optional)

---

### Red String
Next:
- Battery Check
- Execution

---

### Battery Check
If Tired → Rest state (override allowed)  
If Stuck → Diagnostic tool (as appropriate)  
If Override → Return to **Previous Tool State** (see Resume State)

---

### Are We There Yet?
If Yes → Stop / Ship  
If No → Battery Check

---

### Beautiful Mind Filter
Next:
- Wherefore Art Thou, AI?
- Red Team Test
- Revision Loop

---

### Wherefore Art Thou, AI?
Next:
- Red Team Test
- WTF Tool

---

### Red Team Test
Next:
- AITA Test
- Revision Loop

---

### AITA Test
Next:
- Be the Dodgeball
- Execution

---

### Be the Dodgeball
Next:
- WTF Tool

---
