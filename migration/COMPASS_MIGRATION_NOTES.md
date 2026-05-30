# COMPASS Canonicalization Notes

## Goal

Keep the repository aligned around COMPASS-only terminology and source-of-truth behavior.

## Canonical files

- `COMPASS_Current.md`
- `COMPASS_Changelog.md`
- `prompts/compass-intake.md`
- `prompts/compass-analysis.md`
- `prompts/compass-tailored-resume.md`
- `prompts/compass-cover-letter.md`

## Compatibility policy

Do not maintain predecessor-name redirect files or independent compatibility policy. If an old external prompt points at removed files, route the user to the current COMPASS prompt or rule file instead.

## Scope correction

COMPASS active scope was corrected back to careers / job-search in `vNext 2026-05.4`.

Do not add product, strategy, research, consulting, grant, policy, or personal knowledge examples or prompts unless the project owner explicitly reopens scope.

## Version bump

Updated to `vNext 2026-05.5`.

## Intake terminology migration

The former "Layer 0" source-of-truth onboarding workflow was renamed to "COMPASS Intake" in `vNext 2026-05.5`.

Active framework files should use "COMPASS Intake" on first mention and "Intake" after that. Historical changelog and migration notes may mention "Layer 0" only to explain the rename.

Updated active file names:

- `rules/07-compass-intake.md`
- `prompts/compass-intake.md`
- `examples/compass-intake-checkpoint-example.md`

## Recommended PR title

Rename Layer 0 to COMPASS Intake
