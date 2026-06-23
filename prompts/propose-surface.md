# Prompt: Propose a Surface

Use this prompt to ask an AI assistant to write a repo or public surface proposal.

This prompt is appropriate when a cycle returned `PROPOSAL` or `READY` at Station 9, and the operator has decided to proceed with a formal proposal document.

---

## Prompt

You are writing a repo or public surface proposal based on a completed editorial cycle.

Your task is to produce a proposal document that describes a possible public-facing surface for this material.

**You must follow these rules without exception:**

1. A proposal is a candidate document. It is not a deployment instruction.
2. You may describe what a surface could contain. You may not create, deploy or publish any surface.
3. You may recommend acceptance. You may not assume acceptance.
4. Do not write as if the surface already exists.
5. Explicitly state what this proposal does not authorize.
6. The proposal requires explicit human acceptance before any action is taken.
7. Do not include private names, internal file paths or context not present in the cycle record.

---

**Source cycle reference:**

- Cycle ID: [reference to the cycle]
- Gate decision at Station 9: [PROPOSAL / READY]
- Operator: [name or role]

---

**Surface description from cycle record:**

[Copy the surface description or notes from the cycle report here.]

---

**Instructions:**

Write a surface proposal using the structure in `templates/repo-surface-proposal.template.md`.

Fill in:

1. What is being proposed (type of surface, nature of content, intended audience).
2. Rationale (why this surface is appropriate based on the cycle evidence).
3. Proposed scope (what would be included, what the surface would do).
4. What this proposal explicitly does not authorize (use the standard list from the template as a starting point, add specifics).
5. Acceptance requirements (who must review and accept, what conditions must be confirmed).
6. Leave the Decision section as PENDING.

The proposal must be readable without access to the source material or internal project context.

Write clearly enough that a person unfamiliar with the project can evaluate whether to accept or decline the proposal.

Do not advocate strongly for acceptance. Present the proposal neutrally so the decision-maker can evaluate it on its merits.
