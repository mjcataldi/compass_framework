# Recruiter-Targeted Resume Prompt

Use this prompt when tailoring for a recruiter rather than a single job description.

```text
Generate a recruiter-targeted staff-level resume using the latest approved source resume or CV.

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

Position broadly for Staff Engineer / Platform Architect / Senior Technical Consultant opportunities unless otherwise specified.
Preserve the breadth of relevant platform engineering, cloud, distributed systems, modernization, leadership, architecture, compliance, AI systems, and enterprise integration experience.
Do not over-tailor to a single role unless a specific role is provided.
Do not invent technologies, metrics, ownership, credentials, employment history, or experience.
Do not include STRIDE analysis inside the resume artifact.
Use the STRIDE resume skills formatting standard: Core Strength Areas should use synthesized staff-level bullets rather than long one-keyword-per-line inventories, and Technical Skills Inventory should use comma-separated category lines for dense tool and technology coverage.
Create the resume as a clean artifact suitable for Word, PDF, and Markdown export.

Recruiter name:
[RECRUITER NAME]

Recruiter context, domain, or target role family:
[OPTIONAL CONTEXT]
```

## Notes

Recruiter-targeted resumes should stay broader than cold-apply resumes because recruiters may have access to multiple opportunities.
