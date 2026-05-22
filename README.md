# STRIDE Framework

STRIDE is a structured job-evaluation and application-material workflow for staff-level, principal-level, platform, cloud, AI systems, and senior technical consulting roles.

The framework is designed to answer the practical hiring question:

> Would the hiring team understand the candidate's value quickly enough to move them forward?

STRIDE is not only a fit-scoring method. It is a versioned operating system for:

- Role evaluation
- Hiring-manager scan optimization
- ATS and semantic alignment
- Verified career source-of-truth onboarding
- Master CV claim-ledger construction
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
- `rules/07-source-of-truth-onboarding.md` — Layer 0 source-of-truth onboarding and claim verification rules
- `prompts/` — reusable prompt templates
- `prompts/stride-layer0-source-of-truth.md` — reusable Layer 0 onboarding launcher prompt
- `examples/` — example output patterns
- `examples/layer0-checkpoint-example.md` — example Layer 0 pause/resume checkpoint

## Layer 0 Source-of-Truth Onboarding

Layer 0 is STRIDE's verified career source-of-truth onboarding workflow.

Use Layer 0 when a new person is onboarding to STRIDE, when a master CV needs to be created from scattered source material, or when an existing master CV needs to be rebuilt into a more defensible claim ledger.

Layer 0 is not primarily a resume-writing workflow. It is an evidence-capture and claim-verification workflow that later compiles into a master CV.

Layer 0 accepts prior resumes, cover letters, LinkedIn exports or copied profile text, brag documents, performance reviews, project notes, certifications, portfolio materials, recruiter-submitted resumes, and other career source documents. These sources are treated as evidence leads, not automatic truth.

Default setup for non-technical users:

1. Create a Google Drive folder named `STRIDE Career Source of Truth`.
2. Add prior resumes, cover letters, LinkedIn exports, brag docs, reviews, certifications, project notes, and other source documents.
3. Copy the folder link.
4. Add the folder link to the ChatGPT Project sources.
5. Start Layer 0 using `prompts/stride-layer0-source-of-truth.md`.

GitHub remains optional for end users. Technical users may fork this repository or maintain their own optimized STRIDE framework source. When multiple STRIDE framework sources are available, the assistant should ask which source takes precedence before starting Layer 0.

Layer 0 must support pause/resume behavior. Users may say `I need a break`, `pause`, `bookmark this`, or `let's continue later`; STRIDE should stop asking new questions and emit a checkpoint that can be resumed later.

Layer 0 storage behavior must be honest:

- If direct Google Drive write/update access is available, save or update the Layer 0 source-of-truth files in the user's selected folder.
- If direct write/update access is not available, produce copy-ready files and clearly tell the user what to save where.
- Never claim that files were saved when they were only generated in chat.

## Branch Policy

The `main` branch is canonical.

Anything merged to `main` is considered the active STRIDE framework unless an instruction explicitly points to another branch, tag, or commit.

## Memory and Context Policy

ChatGPT memory may contain user preferences, but this repository should override memory for STRIDE behavior when there is a conflict.

If repository access fails, the assistant should say so clearly and should not reconstruct STRIDE rules from memory unless explicitly authorized.

## Source-of-Truth Resume Policy

STRIDE outputs must use the latest approved Staff Engineer Master CV, verified Layer 0 claim ledger when available, do-not-claim list when available, or user-provided source resume for the session. STRIDE must not invent technologies, ownership, certifications, clearance, metrics, employers, responsibilities, or project history.

The current Staff Engineer Master CV is maintained outside this repository and should be fetched dynamically when needed.
