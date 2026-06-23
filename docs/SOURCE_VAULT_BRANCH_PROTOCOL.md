# Source Vault Branch Protocol

Use this protocol when starting work around protected `[source material]`.

## 1) Start with a vault contract

A new source-specific branch starts by installing a protected vault contract.
It does not start by ingesting, analyzing, summarizing, or transforming the source.

## 2) Keep source files out of git by default

Do not commit `[source material]` to git by default.
Reference the source through metadata and location notes only.

Protected `[source material]` is not treated as content, training material, prompt fuel, or a derivative-output source by default.

## 3) Define the first branch product

The first branch produces a filesystem environment around the source.
It does not produce the source itself.
It does not produce content derived from the source.

## 4) Declare required statuses

Each source-specific branch must declare:

- Source status
- AI status
- Content status
- Public status
- Allowed actions

## 5) Gate AI-assisted reading

AI-assisted reading stays inactive until both of these exist:

- A reading protocol
- A review gate

## 6) Label all outputs

Any output must include one explicit status label.
No unlabeled output is accepted.

## 7) Keep the branch reviewable

Keep the branch small and reviewable in one pass.
Prefer focused docs and scaffold files only.

## 8) Keep Content Desk absent by default

A Content Desk is absent by default.
Public-facing content work starts only after a Content Desk is explicitly installed.

## Suggested first-branch files

```txt
vaults/[source identifier]/
  README.md
  STATUS.md
  SOURCE_MANIFEST.example.md
  READING_PROTOCOL.md
  AI_AUGMENTATION_GUARDRAILS.md
  CONTENT_DESK_GATE.md
  RUNLOG.md
```
