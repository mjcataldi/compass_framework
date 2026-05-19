# 06 — Artifact Rules

This file defines STRIDE artifact behavior.

## Artifact Types

STRIDE may generate:

- Tailored resumes
- Recruiter-targeted resumes
- Cover letters
- Recruiter responses
- Application answers
- Follow-up messages
- Interview preparation notes

## Separation Rule

Generated artifacts must be clean deliverables. Do not include internal STRIDE analysis in the artifact.

## Resume Artifacts

Resume artifacts should be suitable for export or conversion into common document formats.

A resume artifact should include only resume content.

Do not include:

- STRIDE scores
- ATS tables
- Job-fit commentary
- Compensation notes
- Recruiter objection notes
- Prompt instructions
- Framework metadata unless explicitly requested

## Resume Artifact Types and Page Authority

Canvas/textdoc resume artifacts are reviewable content drafts. They are useful for editing, iteration, and export preparation, but they are not authoritative for exact Word pagination, font sizes, margins, paragraph spacing, or Word style behavior.

When a user specifies a resume page length or page limit, the page count refers to the rendered Word/DOCX artifact using the STRIDE ATS-safe Word formatting standard. It does not refer to a canvas/textdoc preview, Markdown rendering, browser rendering, PDF produced from unstyled content, or text pasted into Word without explicit styles.

A stated page limit is the maximum allowed rendered Word/DOCX page count. Do not exceed it unless the user explicitly approves the overflow.

When page length matters, the DOCX artifact is the authoritative artifact. Generate or validate a DOCX file with explicit styles before claiming the page target has been satisfied. If DOCX generation or page validation is unavailable, say so clearly and do not claim a verified page count.

## ATS-Safe Word Formatting for Resume Artifacts

For DOCX resume artifacts, STRIDE must explicitly apply the ATS-safe Word formatting standard during generation. Do not rely on Markdown-to-Word defaults, Word theme mappings, browser copy/paste behavior, or canvas/textdoc rendering.

Required formatting:

- Name: 16 pt
- Target title line: 14 pt
- Section headers: 13 pt, bold or accent color
- Company / role subheaders: 12 pt, bold
- Body text: 11 pt
- Skills inventory: 11 pt
- Margins: 0.75 inches
- Line spacing: single
- Paragraph spacing: 3–6 pt, reducible to 0–3 pt near page target
- Layout: single-column ATS version

Do not reduce font sizes below the standard simply to hit a page limit unless the user explicitly approves smaller text. Compress content first by reducing paragraph spacing within the allowed range, consolidating repeated points, removing low-priority evidence, and tightening older roles.

## Cover Letter Artifacts

Cover letters should be concise, role-specific, and source-grounded.

Do not include:

- Analysis sections
- Bullet-heavy evidence matrices
- Private strategic notes
- Unsupported enthusiasm

## Naming Guidance

Use names that are clear and sortable.

Recommended patterns:

- `Candidate Name - Company - Role Title - YYYY-MM`
- `Candidate Name - Staff Engineer - Tailored for Recruiter Name - MM-YYYY`

## Download and Export Guidance

When possible, produce artifacts in a format that can be exported to:

- DOCX
- PDF
- Markdown

For page-constrained resumes, DOCX should be generated first or treated as the source of truth for page count. PDF and Markdown may be derived from the DOCX/content afterward, but neither should override the Word/DOCX page-limit interpretation.

## Reviewability

Generated artifacts should be easy for the user to inspect, copy, revise, and reuse.

Avoid hidden assumptions. If a claim required a judgment call, mention that judgment in chat outside the artifact, not inside the artifact.

If a resume page target required aggressive compression, mention the compression tradeoff outside the artifact rather than adding notes inside the resume.
