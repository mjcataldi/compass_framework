# STRIDE Tailored Resume Prompt

Use this prompt after a STRIDE analysis when the user wants a tailored resume.

```text
Generate the STRIDE-tailored resume using the latest approved source resume or CV.

Before running this workflow, read the latest STRIDE framework files from the connected GitHub repo `mjcataldi/stride_framework` on the `main` branch.

Use the repository as the source of truth for STRIDE behavior. Do not rely on cached STRIDE instructions when the repo is available.

Required framework files:
- VERSION.md
- STRIDE_Current.md
- rules/00-operating-principles.md
- rules/02-resume-generation.md
- rules/04-truthguard.md
- rules/06-artifact-rules.md

If GitHub access fails, say so clearly before proceeding. Do not reconstruct STRIDE behavior from memory unless explicitly authorized.

Use the STRIDE findings above.
Resume density mode: Balanced unless otherwise specified.

Balanced is the default resume mode and should generally target 3–4 pages.
Use Sharp Apply only when I explicitly request "Sharp Apply," "2-page resume," or equivalent language indicating a deliberately compressed 2-page application artifact.
Do not automatically switch from Balanced to Sharp Apply just because the role is narrow.

Keep it truthful, ATS-aware, staff-level, and recruiter-readable.
Do not include STRIDE analysis inside the resume artifact.
Do not invent technologies, metrics, ownership, credentials, employment history, or experience.
Use the STRIDE resume skills formatting standard: Core Strength Areas should use synthesized staff-level bullets rather than long one-keyword-per-line inventories, and Technical Skills Inventory should use comma-separated category lines for dense tool and technology coverage.

Generate the resume as a DOCX-first artifact when document-generation tools are available.

For the DOCX artifact, explicitly apply the STRIDE ATS-safe Word formatting standard:
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

Do not rely on Markdown, canvas/textdoc rendering, browser copy/paste, Word theme defaults, Markdown-to-DOCX defaults, or generic export behavior to apply these styles.

If a DOCX artifact cannot be generated or validated, say so clearly in chat and do not claim that Word formatting or page count has been verified.

Markdown and PDF outputs may be provided as secondary exports, but the DOCX artifact is authoritative for formatting and page count.

Create the resume as a clean artifact suitable for Word, PDF, and Markdown export, with DOCX treated as the source of truth when page count or styling matters.
```

## Notes

The generated resume should be a clean resume only. Any caveats, TruthGuard notes, or strategic warnings should be placed in chat outside the artifact.

Sharp Apply is an explicit opt-in mode for a tight 2-page resume. It should be used only when the user asks for that mode or asks for a 2-page version. Balanced remains the default.

When document-generation tools are available, tailored resumes should be generated DOCX-first with explicit STRIDE ATS-safe Word styles applied. Canvas/textdoc and Markdown versions are reviewable content drafts, not authoritative evidence of Word formatting or pagination.
