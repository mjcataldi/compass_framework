# STRIDE vNext Analysis Prompt

Use this prompt to run a STRIDE analysis for a target role.

```text
Run a STRIDE vNext analysis for this role.

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

Job description / recruiter message:
[PASTE ROLE HERE]
```

## Notes

This prompt should produce analysis only. It should not generate a resume or cover letter unless the user explicitly asks for that next phase.
