# Cycle Model

A cycle is a single structured pass through a piece of material. It moves through eleven stations. Each station may produce a gate decision. The cycle ends with a cycle report.

## Station overview

| # | Station | Description |
|---|---|---|
| 1 | Read status | Determine the material's current state before anything else happens. |
| 2 | Read local context | Understand the circumstances that shape this specific cycle. |
| 3 | Check production readiness | Evaluate whether the material is ready for structured handling. |
| 4 | Identify or create a fragment body | Locate or define the specific fragment of material being cycled. |
| 5 | Run review | Subject the material to structured review at the current station. |
| 6 | Test for blueprint or reusable pattern | Check whether the material contains a method or pattern worth extracting. |
| 7 | Decide whether an editorial body is needed | Evaluate whether a formal editorial assessment should be written. |
| 8 | Decide whether a public-bound dossier is appropriate | Determine whether a dossier for potential public-facing work should be prepared. |
| 9 | Decide whether a repo/public surface is appropriate | Evaluate whether the material is a candidate for a repository or public surface proposal. |
| 10 | Extract reusable learning | Record any method, pattern or insight in a reinjection note. |
| 11 | Write a cycle report | Produce the cycle report as the default deliverable. |

---

## Station details

### Station 1 — Read status

**Purpose:** Establish the material's baseline state before the cycle begins.

**Inputs:** The material itself, any prior cycle reports.

**Gate:** Is the material's status legible? If status cannot be determined, the cycle returns `HOLD` and no further stations are processed.

**Possible outcomes:** `PASS`, `HOLD`

---

### Station 2 — Read local context

**Purpose:** Understand the conditions specific to this cycle run. Who is running it. What the operational context is. Whether there are any constraints or prior decisions that affect handling.

**Inputs:** Cycle parameters, any contextual notes provided by the operator.

**Gate:** Is the local context sufficient to proceed? If context is missing and cannot be inferred, the cycle returns `HOLD`.

**Possible outcomes:** `PASS`, `HOLD`

---

### Station 3 — Check production readiness

**Purpose:** Determine whether the material is ready for structured cycle handling, or whether it needs preparation work first.

**Inputs:** Status from Station 1, context from Station 2.

**Gate:** Does the material meet a minimum threshold for structured review? If not, return `RETURN` to drafting or `HOLD` for further preparation.

**Possible outcomes:** `PASS`, `RETURN`, `HOLD`

---

### Station 4 — Identify or create a fragment body

**Purpose:** Locate the specific fragment of material that this cycle will process. If no fragment body exists, create a minimal working fragment.

**Inputs:** The source material.

**Gate:** Has a fragment been successfully identified or created? If neither is possible, the cycle returns `STOP`.

**Note:** Creating a fragment does not promote or duplicate the source material. The fragment is a working unit for this cycle only.

**Possible outcomes:** `PASS`, `STOP`

---

### Station 5 — Run review

**Purpose:** Subject the fragment to structured review. Evaluate quality, coherence, completeness and fitness for the stated purpose.

**Inputs:** Fragment body from Station 4.

**Gate:** Does the material pass review at the current level? Partial passes are recorded and attached to the report.

**Possible outcomes:** `PASS`, `HOLD`, `RETURN`

---

### Station 6 — Test for blueprint or reusable pattern

**Purpose:** Evaluate whether the material contains a method, structure or pattern that could be reused in other contexts — independently of whether the material itself proceeds further.

**Inputs:** Fragment body, review notes from Station 5.

**Gate:** Is there a reusable pattern? If yes, flag for extraction at Station 10. Extraction does not promote the source.

**Possible outcomes:** `PASS`, `EXTRACT_ONLY`, `NO_EVENT`

---

### Station 7 — Decide whether an editorial body is needed

**Purpose:** Evaluate whether the material requires a formal editorial assessment — a structured document that represents an editorial position on the material.

**Inputs:** Cycle status so far.

**Gate:** Is an editorial body appropriate at this stage? An editorial body is not a publication. It is an internal assessment document.

**Possible outcomes:** `PASS`, `HOLD`, `NO_EVENT`

---

### Station 8 — Decide whether a public-bound dossier is appropriate

**Purpose:** Evaluate whether the material is a candidate for a dossier intended to support potential public-facing work.

**Inputs:** Review notes, editorial body decision.

**Gate:** Does the material meet the threshold for public-bound dossier preparation? A dossier is a candidate document, not a publication.

**Possible outcomes:** `PROPOSAL`, `HOLD`, `NO_EVENT`

---

### Station 9 — Decide whether a repo/public surface is appropriate

**Purpose:** Evaluate whether the material is a candidate for representation on a public-facing repository or surface.

**Inputs:** Dossier decision from Station 8.

**Gate:** Is a repo/public surface proposal appropriate? A proposal is not a publication or deployment. A proposal requires explicit human acceptance before any surface is created.

**Possible outcomes:** `PROPOSAL`, `READY`, `HOLD`, `NO_EVENT`

---

### Station 10 — Extract reusable learning

**Purpose:** Record any method, pattern or insight in a reinjection note. This station runs regardless of whether the material is promoted.

**Inputs:** All prior stations.

**Output:** A reinjection note (if learning was identified). The reinjection note does not reference source material by name unless explicitly authorized.

**Possible outcomes:** `PASS`, `NO_EVENT`

---

### Station 11 — Write a cycle report

**Purpose:** Produce the cycle report. This is the default and required deliverable of every completed cycle.

**Inputs:** All station records and gate decisions from this cycle.

**Output:** A completed cycle report in the format defined by [`templates/cycle-report.template.md`](../templates/cycle-report.template.md).

**Possible outcomes:** `PASS` (report completed), `STOP` (cycle terminated before completion — partial report written)

---

## Flow summary

```
Station 1: Read status
    ↓ PASS → Station 2
    ↓ HOLD → end (report HOLD)

Station 2: Read local context
    ↓ PASS → Station 3
    ↓ HOLD → end (report HOLD)

Station 3: Check production readiness
    ↓ PASS → Station 4
    ↓ RETURN → back to drafting (report RETURN)
    ↓ HOLD → end (report HOLD)

Station 4: Identify or create fragment body
    ↓ PASS → Station 5
    ↓ STOP → end (report STOP)

Station 5: Run review
    ↓ PASS → Station 6
    ↓ HOLD → end (report HOLD)
    ↓ RETURN → back to prior station (report RETURN)

Station 6: Test for blueprint or reusable pattern
    ↓ PASS or EXTRACT_ONLY or NO_EVENT → Station 7

Station 7: Decide whether editorial body is needed
    ↓ PASS or NO_EVENT → Station 8
    ↓ HOLD → end (report HOLD)

Station 8: Decide whether public-bound dossier is appropriate
    ↓ PROPOSAL or NO_EVENT → Station 9
    ↓ HOLD → end (report HOLD)

Station 9: Decide whether repo/public surface is appropriate
    ↓ PROPOSAL or READY or NO_EVENT → Station 10
    ↓ HOLD → end (report HOLD)

Station 10: Extract reusable learning
    ↓ PASS or NO_EVENT → Station 11

Station 11: Write cycle report
    → cycle complete
```

The cycle always ends with a cycle report. The report records the outcome of every station and every gate that was evaluated.
