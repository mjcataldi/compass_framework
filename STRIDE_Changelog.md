# STRIDE Changelog

All notable framework changes should be documented here.

## vNext 2026-05 — Initial Repository Baseline

Initialized the STRIDE framework repository with:

- Canonical active framework definition
- Version marker
- Operating principles
- Analysis workflow rules
- Resume generation rules
- Cover letter generation rules
- TruthGuard rules
- Remote and compensation risk rules
- Artifact separation rules
- Prompt templates
- Example output patterns

## Change Management Rules

When changing STRIDE:

1. Update the relevant framework or rules file.
2. Update `VERSION.md` if the change materially affects framework behavior.
3. Add a changelog entry explaining what changed and why.
4. Preserve backward compatibility unless the change intentionally supersedes prior behavior.
5. Avoid burying major behavior changes only inside prompt templates.

## Versioning Guidance

Use date-based framework versions until semantic versioning becomes useful.

Recommended format:

`vNext YYYY-MM`

Example:

`vNext 2026-05`
