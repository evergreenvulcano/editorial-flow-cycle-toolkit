# Editorial Flow Cycle Toolkit

A lightweight framework for running gated editorial cycles without turning every material into content.

This toolkit is for teams who need structured movement across drafting, review, testing, publication-readiness and reinjection, but do not want an automatic publishing pipeline.

It helps you run a cycle on a piece of material and return a clear report:

- what was read
- what status the material has
- which gates were passed
- which gates held
- what can happen next
- what must not happen
- what learning can be reused elsewhere

## Why this exists

Most content pipelines assume that forward movement is good.

This toolkit assumes something different:

Forward movement is only good when the next gate is actually passed.

A cycle may end in publication-readiness. It may also end in a hold, a return to draft, a method extraction, a review note, a surface proposal, or no event.

All of those are valid outcomes.

## Core rule

The cycle may automate traversal, review structure and reporting.

It must not automate promotion, publication, canonization or ownership.

## The cycle

1. Read status.
2. Read local context.
3. Check production readiness.
4. Identify or create a fragment body.
5. Run review.
6. Test for blueprint or reusable pattern.
7. Decide whether an editorial body is needed.
8. Decide whether a public-bound dossier is appropriate.
9. Decide whether a repo/public surface is appropriate.
10. Extract reusable learning.
11. Write a cycle report.

See [`docs/cycle-model.md`](docs/cycle-model.md) for a full description of each station.

## Valid outcomes

| Outcome | Meaning |
|---|---|
| `PASS` | Gate passed; material may continue to the next station. |
| `HOLD` | Gate held; material stays at current station pending further action. |
| `RETURN` | Material sent back to a previous station. |
| `EXTRACT_ONLY` | A method or pattern is extracted; the source material is not promoted. |
| `PROPOSAL` | A surface or publication proposal is written; the material is not published. |
| `READY` | Material is confirmed ready for the next gate to evaluate. |
| `NO_EVENT` | Cycle completes with no change in status and no artefact produced. |
| `STOP` | Cycle ends definitively; no further action recommended. |

See [`docs/status-outcomes.md`](docs/status-outcomes.md) for definitions.

## Default output

The default output is a cycle report.

The cycle only creates additional artefacts when a gate explicitly allows it.

## What this is not

- not a CMS
- not a content calendar
- not a publishing automation
- not a productivity framework
- not a replacement for editorial judgment
- not a decision engine

## First use

1. Copy [`templates/cycle-report.template.md`](templates/cycle-report.template.md).
2. Run the prompt in [`prompts/run-cycle.md`](prompts/run-cycle.md).
3. Fill one report.
4. Do not create new workflow infrastructure until at least three reports show repeated need.

## Repository structure

```
/
├── README.md
├── LICENSE
├── CONTRIBUTING.md
├── docs/
│   ├── concept.md
│   ├── cycle-model.md
│   ├── status-outcomes.md
│   └── gates.md
├── templates/
│   ├── cycle-report.template.md
│   ├── gate-card.template.md
│   ├── review-note.template.md
│   ├── reinjection-note.template.md
│   └── repo-surface-proposal.template.md
├── schemas/
│   ├── cycle-report.schema.json
│   ├── gate-decision.schema.json
│   └── status-outcome.schema.json
├── prompts/
│   ├── run-cycle.md
│   ├── review-cycle.md
│   ├── extract-method.md
│   └── propose-surface.md
└── examples/
    ├── example-cycle-report.md
    ├── example-hold-decision.md
    └── example-reinjection-note.md
```

## Who should use this

- editors
- writers
- creative technologists
- research teams
- product strategists
- AI-assisted editorial workflows
- small teams handling sensitive or experimental material
