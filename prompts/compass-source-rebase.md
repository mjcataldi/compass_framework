# COMPASS Source Rebase Prompt

Use this prompt when starting COMPASS Source Rebase.

```text
Run COMPASS Source Rebase.

Before running this workflow, read the latest COMPASS framework files from the connected repository or Project sources.

Required framework files:
- VERSION.md
- COMPASS_Current.md
- COMPASS_COMMANDS.md
- rules/00-operating-principles.md
- rules/09-source-rebase.md
- templates/compass-source-of-truth-scaffold.md
- templates/compass-source-rebase-report.md

Treat this prompt as a workflow launcher, not as an independent source of Source Rebase, storage, scaffold, migration, Intake, or data-safety rules.

Start in dry-run mode.

My target COMPASS source-of-truth repository or folder is:
[PASTE REPO URL, LOCAL PATH, GOOGLE DRIVE FOLDER LINK, OR OTHER TARGET HERE]

First, disclose whether you can inspect the target and whether direct write access is available. Then produce a dry-run Source Rebase report that identifies existing scaffold paths, missing scaffold paths, skipped existing files, blocked destructive actions, storage/write verification status, and the next safe action.

Do not create, overwrite, delete, rename, move, or modify any file or directory unless I explicitly approve create-missing-only mode for this exact target.

Do not perform COMPASS Intake or claim verification during Source Rebase.
```
