# COMPASS Layer 0 Checkpoint Example

```yaml
checkpoint:
  framework: COMPASS
  layer: "Layer 0 — Verified Source-of-Truth Onboarding"
  checkpoint_id: "compass-layer0-YYYY-MM-DD-001"
  round_id: "Round1A"
  current_stage: "Source harvesting / cross-examination"
  storage_status: "generated locally / ready for upload"
  direct_write_available: false
  target_datastore: "Google Drive folder supplied by user"
  generated_artifacts:
    - "checkpoints/COMPASS_Layer0_Round1A_Example_YYYY-MM-DD.md"
    - "ledgers/Approved_Claim_Ledger.md"
    - "ledgers/Do_Not_Claim_Register.md"
    - "exports/COMPASS_Layer0_Round1A_Example_YYYY-MM-DD.zip"
  completed_sections:
    - source_document_inventory
    - preliminary_timeline
  partially_completed_sections:
    - claim_verification
    - capability_depth_classification
  approved_claims_count: 12
  rejected_claims_count: 3
  unresolved_claims_count: 18
  next_questions:
    - "Confirm the actual depth of involvement for the next extracted claim."
    - "Resolve the contradiction between two source documents."
    - "Confirm whether a real metric exists or if non-quantified phrasing is required."
  next_safe_action: "Upload generated checkpoint artifacts to the datastore, verify visibility, then resume Layer 0 from unresolved claims."
```

## Artifact Expectations

Every committed Layer 0 checkpoint should produce at least one checkpoint Markdown artifact.

When applicable, it should also produce updated ledger artifacts:

- Approved claim ledger
- Do-not-claim register
- Source register updates
- Claim-depth rubric updates

If direct datastore write access is unavailable, the assistant should generate downloadable or copy-ready files and clearly state that the files still need to be uploaded by the user.
