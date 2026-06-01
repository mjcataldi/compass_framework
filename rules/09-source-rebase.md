# 09 - COMPASS Source Rebase

This file governs COMPASS Source Rebase: safe source-of-truth scaffold alignment.

## Purpose

COMPASS Source Rebase aligns an existing COMPASS source-of-truth repository with the current framework-owned scaffold.

It is a scaffold alignment workflow. It is not COMPASS Intake, claim verification, evidence extraction, source reconciliation, git history rebasing, or source record migration.

## Core Safety Rule

Existing user-owned source-of-truth files always win over framework scaffold templates.

Framework templates are defaults. Source repository files are records.

COMPASS Source Rebase must never overwrite, delete, rename, move, edit, or otherwise modify existing user-owned source records.

## Default Mode

The default mode is `dry-run`.

In `dry-run`, COMPASS Source Rebase may inspect the target source repository structure and produce a report. It must not create, edit, delete, move, rename, or overwrite files or directories.

The dry-run report should identify:

1. Existing scaffold paths found.
2. Missing scaffold paths.
3. Existing paths that would be skipped.
4. Proposed create-missing-only actions.
5. Any destructive or unsupported actions refused.
6. Storage and write-access status.
7. Next safe action.

## Writable Mode

The first permitted writable mode is `create-missing-only`.

COMPASS may use `create-missing-only` only after explicit user approval for that mode and target repository or path.

In `create-missing-only`, COMPASS may create only absent scaffold directories or absent framework template placeholder files. If a path already exists, COMPASS must skip it and report it.

COMPASS must verify created paths before reporting them as created.

## Prohibited Behavior

COMPASS Source Rebase must not:

- Overwrite existing files
- Delete existing files or directories
- Rename existing files or directories
- Move existing files or directories
- Modify existing user-owned records
- Normalize, rewrite, or reformat source records
- Infer, verify, extract, reconcile, approve, or reject career claims
- Treat scaffold alignment as Intake completion
- Treat missing scaffold paths as evidence gaps
- Claim writes were performed unless they were actually performed and verified
- Use destructive migration behavior to satisfy a framework upgrade

## Scaffold Source

Use `templates/compass-source-of-truth-scaffold.md` as the framework-owned scaffold source.

The baseline Intake-compatible layout is:

```text
/checkpoints/
/ledgers/
/sources/
/exports/
```

Optional README or placeholder files may be proposed or created only when absent and explicitly approved through `create-missing-only`.

## Report Template

Use `templates/compass-source-rebase-report.md` for Source Rebase reports.

Every report should include:

1. Mode: `dry-run` or `create-missing-only`.
2. Target source repository or path.
3. Framework scaffold version or source.
4. Existing paths skipped.
5. Missing paths proposed or created.
6. Blocked destructive actions refused.
7. Storage or write verification status.
8. Next safe action.

## Relationship to COMPASS Intake

COMPASS Intake builds or updates verified career source-of-truth content through evidence capture and claim verification.

COMPASS Source Rebase aligns only the source repository scaffold. It must not change claim ledgers, do-not-claim registers, source documents, checkpoints, or generated user artifacts except to create missing placeholder files after explicit approval.

If the user needs claim verification, route them to COMPASS Intake after Source Rebase completes or after the dry-run report identifies that the scaffold is ready.

## Storage Honesty

Before performing any write-capable action, disclose whether direct write access to the target source repository or path is available and verified.

If write access is unavailable or uncertain, stay in `dry-run` and provide copy-ready instructions.

Never claim that directories or files were created unless they were actually created and verified.
