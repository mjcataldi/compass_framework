# STRIDE Cover Letter Prompt

Use this prompt after STRIDE analysis when the user wants a role-specific cover letter.

```text
Generate a STRIDE-based cover letter for this role.

Before running this workflow, read the latest STRIDE framework files from the connected GitHub repo `mjcataldi/stride_framework` on the `main` branch.

Use the repository as the source of truth for STRIDE behavior. Do not rely on cached STRIDE instructions when the repo is available.

Required framework files:
- VERSION.md
- STRIDE_Current.md
- rules/00-operating-principles.md
- rules/03-cover-letter-generation.md
- rules/04-truthguard.md
- rules/06-artifact-rules.md

If GitHub access fails, say so clearly before proceeding. Do not reconstruct STRIDE behavior from memory unless explicitly authorized.

Treat this prompt as a workflow launcher, not as an independent source of cover-letter, tone, artifact, TruthGuard, source-priority, or no-fabrication rules.

Apply the active rule files listed above as the authoritative rubric for this workflow. If this prompt appears to conflict with any required rule file, follow the rule file and mention the conflict in chat outside the artifact.

Use the STRIDE findings above when available.
Generate the cover letter artifact according to the active cover-letter, TruthGuard, and artifact rules.
Do not include STRIDE analysis inside the cover letter artifact.
```

## Notes

The cover letter should be a clean submission artifact. Any caveats, TruthGuard notes, rule conflicts, or strategic warnings should be placed in chat outside the artifact.

Prompt templates should not duplicate detailed cover-letter tone, source-grounding, artifact-cleanliness, or TruthGuard rules. Those rules belong in the active rule files.
