# STRIDE Version

Current STRIDE Version: vNext 2026-05

Canonical Branch: main

Status: Active

Initialized: 2026-05-18

## Version Rule

The version declared here governs the active framework behavior when used from the `main` branch.

When STRIDE changes materially, update this file and `STRIDE_Changelog.md` in the same change set.

## Active Behavior Notes

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
- Prompt templates remain workflow launchers and must defer to active rule files for workflow behavior
