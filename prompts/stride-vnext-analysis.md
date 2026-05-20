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

Treat this prompt as a workflow launcher, not as an independent source of analysis, TruthGuard, source-priority, compensation, remote-work, company-environment, or recommendation rules.

Apply the active rule files listed above as the authoritative rubric for this workflow. If this prompt appears to conflict with any required rule file, follow the rule file and mention the conflict in chat.

Use the latest approved source resume or CV as the candidate source of truth. Do not use cached resume content. Do not invent technologies, metrics, ownership, credentials, employment history, or experience.

Default settings unless otherwise specified by the user and supported by the active rule files:
- Application type: cold apply
- Priority: medium
- Resume style: balanced
- Remote-only requirement: yes
- Top Choice flag: no unless clearly justified

Generate analysis only. Do not generate resume, cover letter, or follow-up artifacts unless the user explicitly asks for that next phase.
```

## Notes

This prompt should produce analysis only. It should not generate a resume or cover letter unless the user explicitly asks for that next phase.

Prompt templates should not duplicate detailed analysis-section, compensation, remote-work, company-environment, or TruthGuard rules. Those rules belong in the active rule files.
