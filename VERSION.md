# STRIDE Version

Current STRIDE Version: vNext 2026-05

Canonical Branch: main

Status: Active

Initialized: 2026-05-18

## Version Rule

The version declared here governs the active framework behavior when used from the `main` branch.

When STRIDE changes materially, update this file and `STRIDE_Changelog.md` in the same change set.

## Active Behavior Notes

The active vNext 2026-05 framework includes Layer 0 Verified Career Source-of-Truth Onboarding:

- Layer 0 is the standard onboarding workflow for creating a truthful master CV source of truth for a new STRIDE user.
- Layer 0 treats prior resumes, cover letters, LinkedIn exports, brag documents, performance reviews, project notes, certifications, recruiter resumes, and other career documents as evidence leads rather than automatic truth.
- Layer 0 may extract candidate claims from source documents, but extracted claims remain unverified until the user confirms them.
- Layer 0 may infer possible skills only as questions, never as resume-ready claims.
- Layer 0 must ask clarifying and cross-examination questions in small batches, generally 3–5 questions at a time.
- Layer 0 must classify skills, responsibilities, and ownership by depth: no claim, awareness, exposure, supported, implemented, owned, or led others.
- Layer 0 must maintain approved claims, downgraded claims, rejected claims, unresolved claims, do-not-claim items, source-document inventory, cross-examination logs, role timeline, and checkpoints when applicable.
- Layer 0 must support pause/resume commands such as `I need a break`, `pause`, `bookmark this`, or `let's continue later`.
- Layer 0 must be honest about storage: if it cannot directly save or update Google Drive files, it must produce copy-ready checkpoint files and must not pretend the files were saved.
- Layer 0 output should compile into a master CV only from approved claims.

The active vNext 2026-05 framework includes prompt authority governance:

- Prompt templates are workflow launchers, not independent policy sources.
- Active rule files are the authoritative rubric for analysis, resume generation, cover letters, TruthGuard, artifact handling, formatting, page length, and source priority.
- Prompt templates may identify workflow phase, required inputs, target artifact type, user-selected mode, and immediate execution steps, but they must not redefine, weaken, duplicate, or override rule-file behavior.
- If a prompt conflicts with an active rule file, the rule file wins unless the user explicitly asks to modify the STRIDE framework itself.
- Prompt templates should stay thin and should defer to the required rule files listed for the workflow.

The active vNext 2026-05 framework includes DOCX-first resume prompt enforcement:

- STRIDE tailored-resume and recruiter-targeted-resume prompt templates require DOCX-first artifact generation when document-generation tools are available.
- Resume prompt templates must explicitly apply the STRIDE ATS-safe Word formatting standard instead of relying on Markdown, canvas/textdoc rendering, browser copy/paste, Word theme defaults, Markdown-to-DOCX defaults, or generic export behavior.
- If a DOCX artifact cannot be generated or validated, STRIDE must say so clearly in chat and must not claim that Word formatting or page count has been verified.
- Markdown and PDF outputs may be provided as secondary exports, but DOCX is authoritative for formatting and page count when styling or pagination matters.

The active vNext 2026-05 framework includes DOCX resume readability defaults:

- Generated DOCX resumes longer than two rendered pages should include a compact Word-compatible table of contents/navigation structure when tool support allows it and when doing so does not create ATS risk.
- Bulleted resume content must use proper hanging indentation so wrapped continuation lines align with the first line of bullet text.
- Major sections, company/role headings, selected work labels, and selected technical environment blocks should receive modest top spacing so dense resume sections remain visually scannable.
- Page-length pressure should be handled by compressing lower-value content before eliminating all section separation or making the resume visually cramped.

The active vNext 2026-05 framework includes company environment and candidate sustainability analysis.

The active vNext 2026-05 framework includes resume length discipline and explicit ATS-safe Word formatting requirements for DOCX artifacts.

## Compatibility Rule

Future STRIDE changes should preserve the core operating principles unless explicitly superseded:

- Truthful source-grounded output
- Phased workflow
- Staff-level positioning unless another target is explicitly requested
- No fabricated technologies, metrics, credentials, employment history, or project ownership
- Separate strategic analysis from resume and cover-letter artifacts
- Length-bounded application resumes derived from comprehensive source resumes / master CVs unless a full CV, federal-style resume, proposal, bid-support document, interview dossier, or archive is explicitly requested
- Balanced resume mode remains the default unless the user explicitly requests Sharp Apply, Concise, Comprehensive, full CV, or another named resume mode
- Standard ATS resume formatting remains single-column and compact unless the user explicitly requests a design-heavy or non-ATS presentation version
- User-specified page lengths are interpreted as maximum rendered Word/DOCX page counts under the STRIDE ATS-safe Word formatting standard
- Company environment and candidate sustainability analysis remains a standard STRIDE analysis section unless explicitly superseded
- DOCX-first resume prompt enforcement remains standard for tailored and recruiter-targeted resume generation when document-generation tools are available
- DOCX resume readability defaults remain standard for generated resume artifacts: compact TOC/navigation when appropriate, stable hanging bullet indentation, and readable section/role spacing
- Prompt templates remain workflow launchers and must defer to active rule files for workflow behavior
- Layer 0 source-of-truth onboarding remains the default process for building a master CV from unverified documents or a new user's career history
