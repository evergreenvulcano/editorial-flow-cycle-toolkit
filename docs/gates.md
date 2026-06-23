# Gates

## What a gate is

A gate is a named checkpoint in the editorial cycle at which a judgment is made about whether a specific condition has been met.

Gates are **local judgment points**. They are not automatic approvals. They are not pass/fail evaluations run by the system. They are structured moments at which a person — or an AI assistant operating under explicit, bounded instructions — evaluates whether the material meets a defined criterion.

A gate produces a decision. A decision is recorded. The decision determines what happens next in the cycle.

## What a gate is not

A gate is **not**:

- an automatic approval trigger
- a quality score threshold
- a publishing condition
- a step that the system can clear on its own
- a formality that defaults to pass

## Gate decisions

Every gate produces one of the following decisions:

| Decision | Meaning |
|---|---|
| `PASS` | The gate condition was met. The material may continue. |
| `HOLD` | The gate condition was not met. The material stays at this station. |
| `RETURN` | The material must go back to a prior station. |
| `STOP` | The cycle ends here. |
| `PROPOSAL` | A proposal should be written. The gate does not execute the proposal. |
| `READY` | The material is ready for the next gate to evaluate. |
| `EXTRACT_ONLY` | Only an extraction should occur. The material is not promoted. |
| `NO_EVENT` | Nothing requires action at this gate. |

## Gate format

Each gate is described by a gate card. See [`templates/gate-card.template.md`](../templates/gate-card.template.md).

A gate card records:

- the station this gate belongs to
- the condition being evaluated
- the decision made
- the rationale
- the next action (if any)

## Gate authority

Gates are evaluated by:

- the person running the cycle, or
- an AI assistant operating with explicit instructions, bounded scope and recorded reasoning

An AI assistant evaluating a gate must:

- state the basis for its evaluation
- not invent authority or context not present in the material
- record its decision as a recommendation subject to human review
- not execute the action implied by the decision (e.g., not publish, not create a surface, not promote)

## Key principle

**Automation may support traversal. Automation may not execute promotion.**

The cycle can be traversed with AI assistance. Review notes can be generated. Patterns can be identified. Reports can be drafted.

But no gate decision that results in public visibility, publication, ownership or promotion may be executed automatically. That decision belongs to a person.

## Gate examples by station

| Station | Gate condition | Possible decisions |
|---|---|---|
| Read status | Is the material's status legible? | `PASS`, `HOLD` |
| Check production readiness | Does the material meet the threshold for structured review? | `PASS`, `RETURN`, `HOLD` |
| Identify fragment | Has a fragment been identified or created? | `PASS`, `STOP` |
| Run review | Does the material pass review at the current level? | `PASS`, `HOLD`, `RETURN` |
| Test for reusable pattern | Does the material contain a reusable method or pattern? | `PASS`, `EXTRACT_ONLY`, `NO_EVENT` |
| Editorial body needed? | Is a formal editorial assessment appropriate? | `PASS`, `HOLD`, `NO_EVENT` |
| Public-bound dossier? | Does the material meet the threshold for dossier preparation? | `PROPOSAL`, `HOLD`, `NO_EVENT` |
| Repo/public surface? | Is a surface proposal appropriate? | `PROPOSAL`, `READY`, `HOLD`, `NO_EVENT` |

## Handling disagreement

If the person running the cycle and an AI assistant's evaluation disagree, the person's judgment overrides. The AI's reasoning is recorded in the gate card for reference. The person's decision is recorded as the final gate decision.

The cycle report notes when a gate decision was overridden and by whom.
