# Layer 0 Checkpoint Example

Use this example when a user pauses STRIDE Layer 0 by saying `I need a break`, `pause`, `bookmark this`, or `let's continue later`.

```yaml
checkpoint:
  checkpoint_id: layer0-YYYY-MM-DD-001
  current_stage: "Stage 0E — Cross-Examination"
  current_focus: "Role claim verification"
  source_folder: "Google Drive folder link or project source reference"
  storage_mode: "direct-save | copy-ready"
  completed_items:
    - "Confirmed identity/contact facts"
    - "Inventoried source documents"
    - "Built preliminary career timeline"
  approved_claims_count: 0
  downgraded_claims_count: 0
  rejected_claims_count: 0
  unresolved_claims_count: 0
  current_role_or_source_under_review: "Employer / role / source document name"
  approved_claims:
    - claim_id: "example-claim-001"
      claim_text: "Example user-confirmed claim"
      depth_level: "implemented"
      source_role: "Example role"
      status: "user_confirmed"
  do_not_claim:
    - item: "Example rejected skill or overstated ownership claim"
      reason: "User said they cannot defend this in an interview."
      allowed_phrasing:
        - "Exposure to the environment where this was used."
      prohibited_phrasing:
        - "Owned the technology."
        - "Implemented the technology."
  next_recommended_question_batch:
    - "Confirm whether Skill A was exposure, support, implementation, ownership, or do-not-claim."
    - "Confirm whether Metric B is exact, approximate, unsupported, or should be removed."
    - "Clarify whether leadership claim C was formal ownership, informal influence, or team participation."
  files_updated_or_to_save:
    - "01_source_document_manifest.md"
    - "02_role_timeline.md"
    - "03_claim_ledger.md"
    - "05_do_not_claim.md"
    - "06_cross_examination_log.md"
    - "checkpoints/layer0-YYYY-MM-DD-001.md"
  resume_safe: false
  resume_safe_reason: "Layer 0 has unresolved source-extracted claims that need user confirmation."
```

Resume instruction for the next session:

```text
Resume STRIDE Layer 0 from the last checkpoint. Start with the next recommended question batch and do not generate a master CV or resume until the unresolved claims are confirmed, downgraded, or rejected.
```
