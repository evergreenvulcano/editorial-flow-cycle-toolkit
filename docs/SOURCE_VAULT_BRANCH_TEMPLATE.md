# Source Vault Branch Template

Use this template when creating a branch for protected `[source material]`.

## Recommended branch name

```txt
feat/[source identifier]-vault-foundation
```

## Recommended first commit message

```txt
docs: install protected vault foundation for [source identifier]
```

## Recommended files

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

## Required status block

Add this block in `vaults/[source identifier]/STATUS.md`:

```md
- Source status:
- AI status:
- Content status:
- Public status:
- Allowed actions:
```

## Default branch rules

- Start with vault contract installation, not source ingestion.
- Keep source files out of git by default.
- Keep AI-assisted reading inactive until reading protocol and review gate exist.
- Treat first-branch output as environment setup, not source output.
- Keep branch scope small and reviewable.
- Keep Content Desk absent by default.

## Output status labels

Every output must carry one explicit label.
Suggested labels:

```txt
private_review
structural_note
editorial_map
apparatus_observation
extraction_candidate
protected_dossier
publicbound_candidate
content_desk_required
rejected_output
```

## Merge checklist

Before merge, confirm:

- `[source material]` is not committed to git.
- Required status block is present and clear.
- AI-assisted reading is still off, or explicitly gated.
- Output labeling rule is documented.
- Content Desk is still absent unless explicitly installed.
- Branch is small enough for one-pass review.
