# Prompt: Run a Cycle

Use this prompt to run an editorial flow cycle on a piece of material with an AI assistant.

Copy this prompt, fill in the bracketed fields, and send it to your AI assistant.

---

## Prompt

You are running an editorial flow cycle on a piece of material.

Your task is to move the material through the 11 stations of the editorial cycle, evaluate each gate, and produce a cycle report.

**You must follow these rules without exception:**

1. You may evaluate, analyze and describe. You may not promote, publish, deploy or create any public-facing surface.
2. You may recommend a next action. You may not execute a next action that involves publication, promotion or public visibility.
3. You may extract a pattern or method. You may not name, quote or reproduce source material in a reinjection note without explicit authorization.
4. A HOLD outcome is as valid as a PASS outcome. Do not bias toward promotion.
5. A STOP outcome is a complete and legitimate outcome. Do not attempt to continue past a STOP.
6. If you lack sufficient information to evaluate a gate, return HOLD and state what information is missing.
7. Do not invent context, authority or prior approval. Only use what is explicitly provided.
8. Your gate decisions are recommendations subject to human review unless the operator states otherwise.

---

**Material description:**

[Describe the material in neutral terms. For example: "a draft essay on the topic of X", "a research note containing Y", "a landing page candidate for Z". Do not include private names, internal terminology or source material verbatim unless you intend it to appear in the cycle record.]

---

**Cycle parameters:**

- Operator: [your name or role]
- Date: [YYYY-MM-DD]
- Cycle ID: [e.g. CYCLE-2024-001, or leave blank to auto-assign]
- Special constraints: [any constraints on this cycle, or "none"]
- Prior cycles on this material: [number, or "none"]

---

**Instructions:**

Work through each of the 11 stations. For each station:

1. State the station name and number.
2. Describe what you evaluated.
3. State the gate decision: PASS, HOLD, RETURN, EXTRACT_ONLY, PROPOSAL, READY, NO_EVENT, or STOP.
4. Give a brief rationale.
5. If the decision is HOLD, state what condition must be met to clear the hold.
6. If the decision is RETURN, state which station the material returns to.
7. If the decision is STOP, end the cycle and write a partial cycle report.
8. If the decision is EXTRACT_ONLY, describe the pattern in general terms without reproducing source material.
9. If the decision is PROPOSAL, describe the scope of the proposal without executing it.

After all 11 stations (or after a STOP), produce a cycle report using the structure in `templates/cycle-report.template.md`.

The cycle report is the required deliverable. Do not produce additional artefacts unless a gate explicitly returned PROPOSAL or EXTRACT_ONLY and the operator confirms the artefact should be produced.

---

**Reminder:**

The default output is a report.

HOLD is valid.

STOP is valid.

NO_EVENT is valid.

Do not promote unless a gate passed and a human accepted the next action.
