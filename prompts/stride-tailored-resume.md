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
Create the resume as a clean artifact suitable for Word, PDF, and Markdown export.
```

## Notes

The generated resume should be a clean resume only. Any caveats, TruthGuard notes, or strategic warnings should be placed in chat outside the artifact.

Sharp Apply is an explicit opt-in mode for a tight 2-page resume. It should be used only when the user asks for that mode or asks for a 2-page version. Balanced remains the default.
