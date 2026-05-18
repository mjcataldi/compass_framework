# STRIDE vNext Analysis Prompt

Use this prompt to run a STRIDE analysis for a target role.

```text
Run a STRIDE vNext analysis for this role.

Before running this workflow, read the latest STRIDE framework files from the connected GitHub repo `mjcataldi/stride_framework` on the `main` branch.

Use the repository as the source of truth for STRIDE behavior. Do not rely on cached STRIDE instructions when the repo is available.

Required framework files:
- VERSION.md
- STRIDE_Current.md
- rules/00-operating-principles.md
- rules/01-analysis-workflow.md
- rules/04-truthguard.md
- rules/05-remote-compensation-rules.md

If GitHub access fails, say so clearly before proceeding. Do not reconstruct STRIDE behavior from memory unless explicitly authorized.

Use the latest approved source resume or CV as the source of truth. Do not use cached resume content. Do not invent technologies, metrics, ownership, credentials, employment history, or experience.

Default settings:
- Application type: cold apply unless otherwise specified
- Priority: medium unless otherwise specified
- Resume style: balanced unless otherwise specified
- Remote-only requirement: yes unless otherwise specified
- Top Choice flag: no unless clearly justified

Include:
1. Role fit summary
2. 10-second hiring manager scan
3. ATS + semantic alignment matrix
4. Narrative cohesion assessment
5. JD-to-resume evidence mapping
6. Missing high-priority terms
7. Recruiter/hiring manager objection prediction
8. Compensation and remote-work risk
9. TruthGuard notes
10. Recommendation: pass, apply, apply cautiously, recruiter-only, or top choice

If facts are missing that cannot be reasonably inferred, ask up to three clarifying questions before generating resume content.
```

## Notes

This prompt should produce analysis only. It should not generate a resume or cover letter unless the user explicitly asks for that next phase.
