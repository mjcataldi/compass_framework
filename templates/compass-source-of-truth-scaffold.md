# COMPASS Source-of-Truth Scaffold Template

This file defines the framework-owned default scaffold for a COMPASS source-of-truth repository.

Existing user-owned files always win over this scaffold. These paths are defaults for missing structure only.

## Baseline Layout

```text
/checkpoints/
/ledgers/
/sources/
/exports/
```

## Directory Purposes

- `/checkpoints/` - COMPASS Intake checkpoint records and Source Rebase reports.
- `/ledgers/` - Approved claim ledgers, do-not-claim registers, coverage registers, and related evidence-control files.
- `/sources/` - User-provided source documents, source inventories, and provenance records.
- `/exports/` - Generated bundles, downloadable checkpoint packages, and user-approved export artifacts.

## Optional Placeholder Files

These files may be proposed or created only when absent and explicitly approved through `create-missing-only` mode:

```text
/README.md
/checkpoints/.gitkeep
/ledgers/.gitkeep
/sources/.gitkeep
/exports/.gitkeep
```

## Safety Rule

If any path already exists, skip it and report it. Do not overwrite, delete, rename, move, or modify existing source-of-truth records.
