# 01 — Analysis Workflow

This file defines the standard STRIDE analysis phase.

## Required Inputs

A STRIDE analysis should use:

- The current job description, recruiter message, or target role description
- The latest approved source resume or CV
- Any user-provided application constraints
- Active STRIDE rules from this repository

## Default Analysis Sections

A complete analysis should include the following sections:

1. Role fit summary
2. 10-second hiring manager scan
3. ATS and semantic alignment matrix
4. Narrative cohesion assessment
5. Job-description-to-resume evidence mapping
6. Missing high-priority terms
7. Recruiter and hiring-manager objection prediction
8. Compensation and remote-work risk
9. Company environment and candidate sustainability
10. TruthGuard notes
11. Recommendation

## 10-Second Hiring Manager Scan

Assess whether the resume or candidate story would immediately communicate:

- Role level
- Domain relevance
- Technical depth
- Leadership scope
- Evidence of impact
- Risk or mismatch

## ATS and Semantic Alignment Matrix

Compare job requirements against source evidence.

Recommended columns:

- Requirement or keyword
- Evidence from source resume
- Strength: Strong / Moderate / Weak / Missing
- Notes or truthful mitigation

## Narrative Cohesion Assessment

Evaluate whether the candidate's story fits the role's needs. Identify whether the resume should emphasize platform engineering, architecture, AI systems, cloud modernization, leadership, compliance, product engineering, full-stack engineering, or another theme.

## Evidence Mapping

Map job-description expectations to source-resume evidence. Do not treat an unsupported keyword as evidence.

## Objection Prediction

Identify likely concerns, such as:

- Missing direct domain experience
- Missing specific technology
- Too much breadth / not enough specialization
- Scope mismatch
- Compensation mismatch
- Remote-work mismatch
- Industry mismatch
- Leadership scope ambiguity

## Company Environment and Candidate Sustainability

Evaluate whether the company environment appears sustainable for the candidate, not merely whether the role is technically aligned.

Assess available signals such as:

- Work-life balance patterns
- Psychological safety and leadership trust signals
- Employee-review patterns from platforms such as Glassdoor, Indeed, Comparably, Blind, Levels.fyi discussions, or cautiously interpreted Reddit / public forum commentary
- Company-authored signals from careers pages, benefits pages, values pages, engineering blogs, remote-work policies, interview-process descriptions, or public employee handbooks
- Professional-network signals such as LinkedIn company activity, employee tenure patterns, leadership posts, recruiter behavior, hiring volume, or role churn
- Public business and news signals, including layoffs, reorgs, acquisitions, funding, earnings, leadership changes, product shutdowns, lawsuits, regulatory issues, or customer concentration concerns
- Engineering and product culture signals where available
- Remote-work credibility and whether the company's actual language appears consistent with the posted remote status
- Candidate-specific sustainability fit, including remote-only requirements, compensation goals, staff-level scope expectations, healthy operating-environment needs, ambiguity tolerance, and likely respect for senior technical judgment

Treat these sources as signals with different confidence levels. Do not present anonymous reviews, single comments, or weak patterns as verified fact. Look for repeated patterns and distinguish:

- Verified facts
- Company-authored claims
- Repeated employee-review patterns
- Anonymous or anecdotal commentary
- Inference from hiring, financial, leadership, or organizational signals
- Unknowns where evidence is too thin

Recommended sub-output:

- Work-life balance signals
- Psychological safety / leadership trust signals
- Employee-review pattern summary
- Remote-work credibility
- Engineering / product culture signals
- Stability risks: layoffs, reorgs, funding, leadership churn, or business uncertainty
- Candidate-specific sustainability verdict
- Confidence level: High / Medium / Low

If company-environment research is unavailable, blocked, not requested, or too thin to support a reliable view, say so clearly and use a lower confidence level instead of over-interpreting sparse evidence.

## Recommendation

Use one of:

- Pass
- Apply
- Apply cautiously
- Recruiter-only
- Top choice

Explain the recommendation directly and practically.
