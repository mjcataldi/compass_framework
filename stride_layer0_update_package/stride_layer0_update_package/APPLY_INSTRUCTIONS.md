# STRIDE Layer 0 Source-of-Truth Update

This package contains a PR-ready patch for `mjcataldi/stride_framework`.

## Apply

From the repository root:

```bash
git checkout main
git pull --ff-only
git checkout -b feature/layer0-source-of-truth-onboarding
git apply stride_layer0_source_of_truth_update.patch
git status
git diff --stat
git add README.md VERSION.md STRIDE_Current.md STRIDE_Changelog.md rules prompts
git commit -m "Add Layer 0 source-of-truth onboarding"
git push -u origin feature/layer0-source-of-truth-onboarding
```

Then open a PR titled:

```text
Add STRIDE Layer 0 source-of-truth onboarding
```

## What changes

- Adds `rules/07-source-of-truth-onboarding.md`.
- Adds `prompts/stride-layer0-source-of-truth.md`.
- Updates `README.md`, `VERSION.md`, `STRIDE_Current.md`, and `STRIDE_Changelog.md`.
- Integrates Layer 0 with operating principles, resume generation, TruthGuard, and artifact rules.

## Commit message

```text
Add Layer 0 source-of-truth onboarding

Adds STRIDE Layer 0 as the verified career source-of-truth onboarding workflow for creating a claim ledger and master CV from source documents and user cross-examination.

Layer 0 treats prior resumes, cover letters, LinkedIn exports, recruiter resumes, brag docs, reviews, certifications, and project notes as evidence leads rather than automatic truth. It requires user confirmation before adding inferred skills or extracted claims to the master CV, classifies claims by depth, tracks do-not-claim items, supports pause/resume checkpoints, and documents honest Google Drive storage behavior.
```
