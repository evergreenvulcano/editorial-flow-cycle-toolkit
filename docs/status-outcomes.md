# Status Outcomes

Each station in the cycle returns one of the following outcomes. Outcomes are recorded in the cycle report.

---

## `PASS`

**Meaning:** The gate condition at this station was met. The material may continue to the next station.

**Does it promote the material?** No. A PASS at a station means the station's gate is cleared. It does not mean the material is approved for publication, distribution or any downstream system.

**When to use:** When the material meets the criteria for the current station and no reason to hold or return exists.

---

## `HOLD`

**Meaning:** The gate at this station was not passed. The material remains at its current station. No forward movement occurs.

**Does it block the material permanently?** No. A HOLD is not a rejection. It is a pause pending further action, information or review.

**When to use:** When the material cannot proceed because a specific condition is unmet and the condition may be addressed. Record what condition was unmet and what would be needed to clear the hold.

---

## `RETURN`

**Meaning:** The material is sent back to a previous station. The current station identified a deficiency that requires work at an earlier stage.

**Does it mean the material failed?** No. A RETURN is a navigation decision. It means the current station is not the right place to resolve the identified issue.

**When to use:** When review, readiness check or context reading reveals that the material needs rework before the current station can be meaningfully evaluated.

---

## `EXTRACT_ONLY`

**Meaning:** The material contains a method, pattern or insight worth extracting. The extraction proceeds. The source material is not promoted.

**Does it copy or publish the source material?** No. Extraction means a reinjection note is written. The note records the pattern or method in general terms. The source is referenced only with explicit authorization.

**When to use:** When the material is not ready or appropriate for promotion but contains reusable learning.

---

## `PROPOSAL`

**Meaning:** A proposal has been written. The proposal describes a possible next step — a public-bound dossier, a repo surface, a publication candidate — but does not execute that step.

**Does it create a surface, page or artefact?** No. A PROPOSAL is a draft recommendation. It requires explicit human acceptance before any surface or artefact is created.

**When to use:** When the material passes the threshold for a specific proposal type, and a recommendation document should be prepared for human review and decision.

---

## `READY`

**Meaning:** The material has been evaluated and confirmed ready for the next gate.

**Does it mean the next gate will pass?** No. READY means the material is in a state where the next gate can be meaningfully evaluated. The next gate may still return HOLD.

**When to use:** When all conditions for the current station are met and the material is explicitly confirmed ready for forward evaluation.

---

## `NO_EVENT`

**Meaning:** The cycle completed this station with no change in status and no artefact produced.

**Is this a failure?** No. NO_EVENT is a valid and complete outcome. It means the station was evaluated and nothing required action or change.

**When to use:** When a station's evaluation finds nothing to act on — no pattern to extract, no proposal needed, no editorial body required.

---

## `STOP`

**Meaning:** The cycle ends at this point. No further stations are processed. The cycle report is written as a final record.

**Is this a negative outcome?** No. STOP is a decisive and legitimate outcome. It means the cycle has reached a point where continuing is not appropriate, possible or useful.

**When to use:** When a fundamental condition cannot be met (e.g., no fragment can be identified), when continuing would violate a constraint, or when a deliberate decision is made to end the cycle.

---

## Outcome reference table

| Outcome | Forward movement? | Artefact created? | Source promoted? | Cycle continues? |
|---|---|---|---|---|
| `PASS` | Yes | No | No | Yes |
| `HOLD` | No | No | No | No |
| `RETURN` | No (backward) | No | No | No |
| `EXTRACT_ONLY` | No | Reinjection note | No | Optional |
| `PROPOSAL` | No | Proposal document | No | Optional |
| `READY` | Prepared | No | No | Yes |
| `NO_EVENT` | No | No | No | Yes |
| `STOP` | No | Partial report | No | No |

---

## Important: outcomes are records, not commands

An outcome describes what happened at a station. It does not instruct a downstream system to take action. All actions following a cycle require human decision.
