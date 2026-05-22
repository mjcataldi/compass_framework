# 04 — TruthGuard

TruthGuard is the STRIDE anti-fabrication and evidence-control layer.

## Purpose

TruthGuard prevents STRIDE outputs from overstating fit, adding unsupported terms, inventing experience, or blurring adjacent experience into direct experience.

## Required Checks

Before producing a resume, cover letter, application answer, or recruiter response, check for:

- Unsupported technologies
- Unsupported domain experience
- Unsupported credentials
- Unsupported security or compliance claims
- Unsupported metrics
- Unsupported ownership claims
- Unsupported leadership scope
- Timeline inconsistencies
- Employer or client name misuse
- Confusion between exposure, contribution, leadership, and ownership

## Evidence Categories

Use these categories when evaluating a claim:

### Direct Evidence

The source resume or user directly states the experience.

### Adjacent Evidence

The source supports nearby or transferable experience, but not the exact term requested by the role.

### Inferred but Unsafe

The claim may be plausible but is not safe to include without user confirmation.

### Missing

The source does not support the claim.

## Claim Handling

- Direct evidence may be used.
- Adjacent evidence may be reframed carefully.
- Inferred but unsafe claims require confirmation.
- Missing claims must be omitted or identified as a gap.

## Layer 0 Integration

When a Layer 0 claim ledger, skill inventory, cross-examination log, or do-not-claim list exists, TruthGuard must use those records before relying on older resumes or cover letters.

- Approved claims may be used only within their confirmed depth level and approved phrasing boundaries.
- Downgraded claims must use the weaker confirmed phrasing.
- Rejected or do-not-claim items must not be reintroduced by downstream resume, cover-letter, recruiter-message, or interview-prep workflows.
- Source-extracted claims that have not been user-confirmed remain unverified, even if they appear in multiple prior resumes or LinkedIn exports.
- Job descriptions may indicate what the target role wants, but they do not validate that the candidate has the experience.
- If a requested claim would require the user to defend a non-skill in an interview, omit it or flag the gap.

## Examples

If the job asks for Medicaid Enterprise Systems and the source only shows public-sector modernization, do not claim Medicaid experience. Instead, state public-sector modernization and regulated delivery experience if supported.

If the job asks for direct Kubernetes production ownership and the source only shows Kubernetes proof-of-concept work, do not claim production Kubernetes ownership. Reframe as Kubernetes modernization planning or proof-of-concept experience if supported.

If the job asks for a certification not present in the source, do not list it.

## Output Behavior

When important gaps exist, STRIDE should say so directly and propose truthful mitigation.

TruthGuard should protect credibility. A smaller true claim beats a bigger fake claim every time.
