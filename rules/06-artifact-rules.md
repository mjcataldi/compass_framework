# 06 — Artifact Rules

This file defines STRIDE artifact behavior.

## Artifact Types

STRIDE may generate:

- Tailored resumes
- Recruiter-targeted resumes
- Layer 0 source-of-truth files
- Claim ledgers
- Skill inventories
- Role timelines
- Do-not-claim lists
- Source-document manifests
- Cross-examination logs
- Checkpoints
- Cover letters
- Recruiter responses
- Application answers
- Follow-up messages
- Interview preparation notes

## Separation Rule

Generated artifacts must be clean deliverables. Do not include internal STRIDE analysis in the artifact.

Layer 0 source-of-truth artifacts are internal career-source artifacts, not submitted application artifacts. They may include claim status, evidence basis, rejected claims, cross-examination notes, checkpoint metadata, and other private verification details.

## Layer 0 Source-of-Truth Artifacts

Layer 0 may generate and maintain source-of-truth files such as `source_document_manifest`, `role_timeline`, `claim_ledger`, `skill_inventory`, `do_not_claim`, `cross_examination_log`, `master_cv_draft`, and checkpoint files.

These files are designed for accuracy, continuity, and downstream grounding. They do not need to follow resume artifact cleanliness rules because they are not application deliverables.

Storage claims must be explicit:

- If STRIDE can directly save/update files in the user's selected Google Drive folder or repository, it may say what was saved or updated.
- If STRIDE cannot directly save/update files, it must provide copy-ready content and must not claim that files were saved.

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

## DOCX Navigation and Table of Contents

DOCX resume artifacts should preserve document navigation that helps reviewers scan the file.

Unless the user explicitly requests otherwise, generated DOCX resumes should include a Word-compatible table of contents/navigation structure near the beginning of the document when the resume is longer than two rendered pages. The table of contents should be generated from the resume heading hierarchy rather than manually typed links whenever tool support allows it.

The table of contents must remain part of the resume artifact only when it improves usability without creating ATS risk. It should be compact, plain-text, and based on standard Word heading styles. Do not use text boxes, multi-column layouts, or decorative navigation elements.

If a canvas/textdoc export preserves navigation differently from the DOCX-first artifact, the DOCX-first artifact remains authoritative. The DOCX generator should explicitly create the Word navigation/TOC structure rather than relying on canvas export behavior.

## Bullet and Indentation Rules

Bulleted resume content must use proper hanging indentation in DOCX outputs.

For standard resume bullets, the bullet marker should sit to the left while all wrapped continuation lines align with the first line of bullet text. Do not allow continuation lines to drift farther right or left than the first line of bullet text.

Recommended DOCX bullet behavior:

- Use Word paragraph numbering/bullet properties or an equivalent hanging-indent implementation.
- Keep bullet text aligned consistently across wrapped lines.
- Avoid manually typed bullet symbols when they prevent stable hanging indentation.
- Apply the same bullet indentation rules to Core Strength Areas, Staff-level positioning bullets, experience bullets, and any other resume bullet lists.

## Section and Role Spacing Rules

DOCX resume artifacts should preserve enough vertical separation for human readability while staying within the page target.

Apply modest top spacing before major sections, selected technical environment blocks, selected work labels, and each new role in the Professional Experience section so the reader can visually distinguish one section from the next.

Recommended defaults:

- Major section headings: 8–10 pt before, 3–4 pt after.
- Company / role headings: 8–10 pt before, 2–3 pt after, with slightly more spacing before a new employer or major role group.
- Selected work and selected technical environment lines: 4–6 pt before when following bullets or dense paragraphs.
- Standard body paragraphs and bullets: keep compact spacing, generally 0–3 pt after, unless additional spacing is required for readability.

If page length pressure exists, reduce lower-value content before eliminating all section separation. Do not create a visually cramped resume simply to preserve excess content.

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
