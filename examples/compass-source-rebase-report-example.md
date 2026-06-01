# COMPASS Source Rebase Report Example

This generic example shows a safe dry-run report. It does not describe an actual user source-of-truth repository.

```yaml
source_rebase_report:
  framework: COMPASS
  workflow: "COMPASS Source Rebase"
  mode: "dry-run"
  target_source_repo_or_path: "Example COMPASS source-of-truth repository"
  framework_scaffold_source: "templates/compass-source-of-truth-scaffold.md"
  direct_write_available: false
  storage_or_write_verification_status: "not verified / dry-run only"
  existing_paths_skipped:
    - path: "/sources/"
      reason: "Existing user-owned path wins over framework scaffold."
    - path: "/ledgers/Approved_Claim_Ledger.md"
      reason: "Existing user-owned source-of-truth file must not be overwritten."
  missing_paths_proposed_or_created:
    - path: "/checkpoints/"
      action: "proposed"
      mode_required: "create-missing-only"
    - path: "/exports/"
      action: "proposed"
      mode_required: "create-missing-only"
  blocked_destructive_actions_refused:
    - action: "overwrite /ledgers/Approved_Claim_Ledger.md"
      status: "refused"
    - action: "rename existing source folders"
      status: "refused"
  source_content_changes:
    claims_verified: false
    source_records_modified: false
    intake_performed: false
  next_safe_action: "Review this dry-run report. If the missing paths are correct, explicitly approve create-missing-only for this exact target."
```

Source Rebase is scaffold alignment only. It is not COMPASS Intake and does not verify, extract, reconcile, approve, reject, or modify user claims.
