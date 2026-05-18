# STRIDE Framework

STRIDE is a structured job-evaluation and application-material workflow for staff-level, principal-level, platform, cloud, AI systems, and senior technical consulting roles.

The framework is designed to answer the practical hiring question:

> Would the hiring team understand the candidate's value quickly enough to move them forward?

STRIDE is not only a fit-scoring method. It is a versioned operating system for:

- Role evaluation
- Hiring-manager scan optimization
- ATS and semantic alignment
- Truth-preserving resume tailoring
- Cover letter generation
- Recruiter-specific positioning
- Compensation and remote-work risk analysis
- Interview objection prediction
- Evidence mapping from source resume to job description

## Canonical Source Files

Use these files as the active source of truth:

- `VERSION.md` — current framework version and status
- `STRIDE_Current.md` — canonical active framework definition
- `STRIDE_Changelog.md` — framework change history
- `rules/` — durable behavior rules
- `prompts/` — reusable prompt templates
- `examples/` — example output patterns

## Branch Policy

The `main` branch is canonical.

Anything merged to `main` is considered the active STRIDE framework unless an instruction explicitly points to another branch, tag, or commit.

## Memory and Context Policy

ChatGPT memory may contain user preferences, but this repository should override memory for STRIDE behavior when there is a conflict.

If repository access fails, the assistant should say so clearly and should not reconstruct STRIDE rules from memory unless explicitly authorized.

## Source-of-Truth Resume Policy

STRIDE outputs must use the latest approved Staff Engineer Master CV or the user-provided source resume for the session. STRIDE must not invent technologies, ownership, certifications, clearance, metrics, employers, responsibilities, or project history.

The current Staff Engineer Master CV is maintained outside this repository and should be fetched dynamically when needed.
