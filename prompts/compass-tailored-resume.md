# COMPASS Career Profile: Tailored Resume Prompt

```text
Generate the COMPASS-tailored resume for the role most recently analyzed by COMPASS in this conversation, using the latest approved source resume, master CV, canonical career record, and Intake claim ledger when available.

Required framework files:
- VERSION.md
- COMPASS_Current.md
- rules/00-operating-principles.md
- rules/02-resume-generation.md
- rules/04-truthguard.md
- rules/06-artifact-rules.md

Treat this prompt as a workflow launcher, not as an independent source of resume, formatting, artifact, TruthGuard, page-length, source-priority, or no-fabrication rules.

Use the previously analyzed target role, job description, recruiter requirement set, COMPASS findings, and approved role-fit evidence only as tailoring inputs. Do not invent facts, claims, metrics, ownership, credentials, technologies, responsibilities, or experience.

If the previously analyzed role is not available in the current context or approved source records, stop and ask me to provide the target role, job description, or recruiter requirement set instead of generating a generic resume.

If multiple previously analyzed roles are available, stop and ask me which role should control tailoring before generating the resume.

Do not include COMPASS analysis, scoring, risk notes, ATS matrix commentary, compensation strategy, recruiter objection notes, or framework commentary inside the resume artifact.
```
