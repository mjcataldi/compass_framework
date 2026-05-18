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

## Reviewability

Generated artifacts should be easy for the user to inspect, copy, revise, and reuse.

Avoid hidden assumptions. If a claim required a judgment call, mention that judgment in chat outside the artifact, not inside the artifact.
