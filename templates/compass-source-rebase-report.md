# COMPASS Source Rebase Report Template

Use this template for dry-run and create-missing-only Source Rebase reports.

```yaml
source_rebase_report:
  framework: COMPASS
  workflow: "COMPASS Source Rebase"
  mode: "dry-run"
  target_source_repo_or_path: "[target]"
  framework_scaffold_source: "templates/compass-source-of-truth-scaffold.md"
  direct_write_available: false
  storage_or_write_verification_status: "not verified / dry-run only"
  existing_paths_skipped:
    - path: "[existing path]"
      reason: "Existing user-owned path wins over framework scaffold."
  missing_paths_proposed_or_created:
    - path: "[missing path]"
      action: "proposed"
      mode_required: "create-missing-only"
  blocked_destructive_actions_refused:
    - action: "overwrite existing files"
      status: "refused"
  source_content_changes:
    claims_verified: false
    source_records_modified: false
    intake_performed: false
  next_safe_action: "Review this dry-run report. Approve create-missing-only for the exact target only if the proposed missing paths should be created."
```

## Required Report Sections

Every Source Rebase report should include:

1. Mode: `dry-run` or `create-missing-only`.
2. Target source repository or path.
3. Framework scaffold version or source.
4. Existing paths skipped.
5. Missing paths proposed or created.
6. Blocked destructive actions refused.
7. Storage or write verification status.
8. Next safe action.

Do not report writes as completed unless the paths were actually created and verified.
