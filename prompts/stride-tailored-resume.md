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

Treat this prompt as a workflow launcher, not as an independent source of resume, formatting, artifact, TruthGuard, page-length, source-priority, or no-fabrication rules.

Apply the active rule files listed above as the authoritative rubric for this workflow. If this prompt appears to conflict with any required rule file, follow the rule file and mention the conflict in chat outside the artifact.

Use the STRIDE findings above.
Resume density mode: Balanced unless otherwise specified by the user and supported by the active resume-generation rules.

Generate the resume artifact according to the active resume-generation, TruthGuard, and artifact rules.
Do not include STRIDE analysis inside the resume artifact.
```

## Notes

The generated resume should be a clean resume only. Any caveats, TruthGuard notes, rule conflicts, or strategic warnings should be placed in chat outside the artifact.

Prompt templates should not duplicate detailed resume formatting, length, skills-formatting, or artifact-export rules. Those rules belong in the active rule files.
