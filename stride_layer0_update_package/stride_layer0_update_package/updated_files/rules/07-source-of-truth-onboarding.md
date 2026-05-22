# 07 — Source-of-Truth Onboarding

This file governs STRIDE Layer 0: Verified Career Source-of-Truth Onboarding.

Layer 0 is the workflow for onboarding a new STRIDE user, harvesting career evidence, cross-examining claims, creating a verified claim ledger, and compiling a truthful master CV source of truth.

Layer 0 is not primarily a resume-writing workflow. It is an evidence-capture and claim-verification workflow that later supports master CV assembly, tailored resumes, cover letters, recruiter materials, job-fit analysis, and interview preparation.

## Core Mission

Build a single career source of truth that is as close to 100% honest as possible.

The purpose is to prevent downstream STRIDE workflows from inventing skills, overclaiming ownership, converting exposure into implementation, turning team work into individual ownership, or forcing the user to defend a non-skill in an interview.

## When To Use Layer 0

Use Layer 0 when:

- A new person is onboarding to STRIDE.
- A master CV is being created for the first time.
- Prior resumes, cover letters, LinkedIn exports, recruiter resumes, brag docs, reviews, or project notes need to be consolidated.
- An existing master CV needs a claim ledger beneath it.
- The user wants downstream resumes and cover letters to be generated only from verified, interview-defensible claims.
- The user says they want a source of truth, master CV, career archive, claim ledger, or truth-first intake.

Do not run Layer 0 by default for ordinary job-fit analysis if the user already has a current approved source resume, master CV, or claim ledger and only wants to evaluate a role.

## Default Non-Technical Setup

For most non-technical users, the default setup is:

1. Create a Google Drive folder named `STRIDE Career Source of Truth`.
2. Add career source documents to that folder.
3. Copy the Google Drive folder link.
4. Add the folder link to the ChatGPT Project sources.
5. Start Layer 0 using `prompts/stride-layer0-source-of-truth.md`.

Recommended Google Drive structure:

```text
STRIDE Career Source of Truth/
  00_START_HERE/
  01_Source_Documents/
    Resumes/
    Cover_Letters/
    LinkedIn/
    Brag_Docs/
    Reviews/
    Certifications/
    Project_Notes/
  02_STRIDE_Source_of_Truth/
    00_README.md
    01_source_document_manifest.md
    02_role_timeline.md
    03_claim_ledger.md
    04_skill_inventory.md
    05_do_not_claim.md
    06_cross_examination_log.md
    07_master_cv_draft.md
  03_Checkpoints/
  04_Generated_Resumes/
  05_Cover_Letters/
  06_Job_Descriptions/
  07_Interview_Prep/
```

GitHub is optional for end users. Technical users may use a private GitHub repo or forked STRIDE framework for versioning, diffs, and retrieval. Do not require GitHub for ordinary Layer 0 onboarding.

## Framework Source Flexibility

Layer 0 may run from:

- The canonical STRIDE framework repository.
- A user fork of STRIDE.
- A customized project-level STRIDE framework.
- The current Project instructions and prompt, when no repository is available.

If more than one STRIDE framework source is available, ask which one should take precedence before starting substantive intake.

If a forked or customized STRIDE source conflicts with Layer 0's no-fabrication, claim-verification, do-not-claim, and interview-defensibility rules, do not silently weaken those protections. State the conflict clearly and ask the user whether they intend to modify the framework itself.

## Source Documents Are Evidence, Not Truth

Layer 0 may ingest or review:

- Prior resumes
- Cover letters
- LinkedIn HTML, exports, copied text, or profile snapshots
- Personal bios
- Brag documents
- Performance reviews
- Project writeups
- Portfolio pages
- GitHub README files
- Certification records
- Job descriptions for prior roles
- Recruiter-submitted resumes
- Interview prep notes
- Existing master CVs

These documents create candidate evidence and cross-examination targets. They do not automatically create approved claims.

Prior resumes may contain inflated wording. Cover letters may contain aspirational language. LinkedIn may be incomplete. Recruiter-submitted resumes may contain language the user would not personally defend. Old documents may be stale.

Therefore:

- Extract from source documents.
- Compare source documents.
- Identify contradictions.
- Ask cross-examination questions.
- Do not approve claims until the user confirms them.

## Claim Admission Policy

No claim enters the master CV unless it has:

- A claim status
- A source role or source context
- A source document or user-stated evidence basis
- A depth level when skill or ownership is involved
- User confirmation
- Resume-safe phrasing boundaries

The model may infer candidate skills only as questions.

Inferred skills are allowed only as questions, never as claims.

## Claim Depth Scale

Classify every skill, tool, responsibility, leadership claim, architecture claim, compliance claim, domain claim, and ownership claim by depth:

| Level | Label | Meaning | Resume-safe phrasing |
|---:|---|---|---|
| 0 | No claim | User denies or cannot support it | Do not include |
| 1 | Awareness | Familiar with concept, no real applied work | Usually omit; may say familiarity only if useful and confirmed |
| 2 | Exposure | Saw it, discussed it, or worked near it | `Exposure to...` |
| 3 | Supported | Helped with it under guidance or adjacent to owners | `Supported...` |
| 4 | Implemented | Built, configured, wrote, or delivered meaningful parts | `Implemented...` |
| 5 | Owned | Had primary responsibility or long-term ownership | `Owned`, `led`, or `architected` only if confirmed |
| 6 | Led others | Directed technical strategy or mentored others in the work | `Led`, `guided`, or `set technical direction` |

Do not collapse this scale into yes/no skill presence.

## Claim Statuses

Use these statuses internally and in Layer 0 artifacts:

- `raw_user_statement`
- `source_extracted_claim`
- `candidate_inference`
- `contradicted_by_source`
- `needs_scope`
- `needs_metric`
- `needs_evidence`
- `user_confirmed`
- `user_downgraded`
- `user_rejected`
- `do_not_claim`
- `resume_ready`
- `cover_letter_ready`
- `interview_prep_required`

## Required Separation

After each intake round, separate:

- Confirmed facts
- Source-extracted claims
- Candidate inferred claims
- Contradictions or inconsistencies
- Clarifying questions
- Approved claims
- Rejected or do-not-claim items
- Claims needing evidence
- Claims needing metrics
- Claims needing scope

## Cross-Examination Rules

Layer 0 should ask a few questions at a time. Prefer 3–5 questions per batch unless the user asks for more.

Ask questions that clarify:

- What the user personally did
- What the team did
- What the user owned versus supported
- What was hands-on versus advisory
- What was production versus proof-of-concept
- What was researched versus implemented
- What was formal leadership versus informal influence
- What was a title versus an actual responsibility
- Which metrics are real versus estimated or unsupported
- Which skills the user would be comfortable defending in an interview

Do not convert:

- Exposure into implementation
- Research into production experience
- Collaboration into ownership
- Team delivery into individual ownership
- Job-description requirements into candidate claims
- Senior title into proof of unrelated skills
- Tool adjacency into hands-on experience
- Old resume wording into truth without confirmation

Titles are context, not proof.

## Metric Rules

Do not invent metrics.

If a source says `improved`, `reduced`, `accelerated`, `saved`, `increased`, or similar, ask whether a real number exists.

Acceptable metric sources include:

- User-confirmed exact numbers
- User-confirmed approximate ranges
- Documented system scale
- Known team size
- Known user count
- Known transaction or data volume
- Known cost, time, or risk reduction

If no metric exists, use non-quantified phrasing.

## Do-Not-Claim Rule

When the user rejects, downgrades, or expresses discomfort with a claim, record it.

The do-not-claim list should include:

- The rejected item
- Why it was rejected or downgraded
- Allowed phrasing, if any
- Prohibited phrasing
- Source documents that mentioned it
- Date or session checkpoint when rejected

Downstream STRIDE workflows must not reintroduce do-not-claim items because a job description requests them.

## Interview Defensibility Rule

Before marking a strong claim as resume-ready, ask whether the user could defend it if an interviewer spent 10 minutes drilling into it.

The user should be able to explain:

- What they did
- Why it mattered
- What tradeoffs existed
- What went wrong or could have gone wrong
- What constraints shaped the work
- What they would do differently

If the user cannot defend the claim at that level, downgrade the claim or mark it for interview prep.

High-risk claims that deserve extra care include:

- Kubernetes
- AI / ML
- Distributed systems
- Security / compliance
- Architecture ownership
- Staff-level leadership
- Cloud migration
- DevOps / platform engineering
- Observability
- Incident response
- Performance optimization
- Cost savings
- Regulated systems
- Executive communication

## Layer 0 Workflow

### Stage 0A — Setup Verification

Confirm:

- Google Drive source folder, if provided
- STRIDE framework source, fork, project source, or fallback prompt source
- Available source documents
- Whether direct save/update access is available
- Whether the user wants to begin from documents, free-form career narration, or both

If direct save/update access is unavailable, say so and switch to copy-ready checkpoint files.

### Stage 0B — Source Harvesting

Inventory source documents and extract:

- Document type
- Date or likely freshness
- Employers
- Titles
- Dates
- Projects
- Skills
- Tools
- Certifications
- Metrics
- Leadership claims
- Compliance or clearance claims
- Contradictions and inconsistencies

Do not approve extracted claims yet.

### Stage 0C — Timeline Reconstruction

Build a preliminary chronological career timeline.

Ask the user to confirm:

- Employer names
- Titles
- Date ranges
- Locations or remote status
- Contract/client relationships
- Role transitions
- Gaps or overlaps

### Stage 0D — Claim Extraction

Group unverified claims by:

- Role
- Skill
- Tool or platform
- Accomplishment
- Domain
- Leadership scope
- Compliance/security/clearance scope
- Metric

Identify contradictions and cross-examination targets.

### Stage 0E — Cross-Examination

Ask focused questions in small batches.

Resolve contradictions.

Confirm, downgrade, or reject claims.

Assign claim-depth levels.

### Stage 0F — Claim Ledger Construction

For each approved claim, capture:

- Claim ID
- Claim text
- Source role
- Source document
- Skill tags
- Depth level
- Evidence basis
- Strongest truthful phrasing
- Conservative truthful phrasing
- Interview defensibility
- Status

### Stage 0G — Master CV Assembly

Compile a master CV draft from approved claims only.

The master CV is the human-readable source archive. The claim ledger remains the evidence-control layer beneath it.

### Stage 0H — Downstream Constraints

Downstream STRIDE resume, cover-letter, recruiter, and interview-prep workflows must use only approved claims unless the user provides new confirmation.

If a job description requires a skill that is absent from the verified source material, flag the gap instead of filling it.

## Output After Each Intake Round

After each intake round, produce:

```text
Confirmed facts
Source-extracted claims
Candidate inferred claims
Contradictions or inconsistencies
Clarifying questions
Approved claims
Rejected / do-not-claim items
Needs evidence
Needs metric
Needs scope
Checkpoint / files to save
```

## Commit Behavior

When the user says `commit`, `approved`, `yes, save that`, or otherwise clearly approves a round:

- Update the claim ledger.
- Update the do-not-claim list if applicable.
- Update the role timeline if applicable.
- Update the source-document manifest if applicable.
- Update the cross-examination log.
- Produce a checkpoint.
- Tell the user what changed and what the next question batch will cover.

If direct save/update access is not available, provide copy-ready file blocks and tell the user exactly where they belong.

## Pause Behavior

If the user says `I need a break`, `pause`, `bookmark this`, or `let's continue later`:

- Stop asking new questions.
- Produce a checkpoint.
- Include current stage, completed items, approved claims count, rejected claims count, unresolved claims count, current role or source under review, next recommended question batch, and files that need saving.
- Tell the user how to resume: `Say "resume Layer 0 from the last checkpoint."`

## Storage Behavior

Layer 0 must be honest about storage.

If direct Google Drive or repository write/update access is available, STRIDE may maintain:

```text
00_README.md
01_source_document_manifest.md
02_role_timeline.md
03_claim_ledger.md
04_skill_inventory.md
05_do_not_claim.md
06_cross_examination_log.md
07_master_cv_draft.md
checkpoints/[date-time]-layer0-checkpoint.md
```

If direct save/update access is unavailable:

- Produce copy-ready versions of the relevant files after each committed round.
- Tell the user exactly which file each block belongs in.
- Ask the user to save the response as a Project source or copy it into the Google Drive folder.
- Do not pretend the files were saved.

## Example Cross-Examination Pattern

```text
I found Kubernetes in two of your prior documents, but the wording is inconsistent.

One source says: "Led Kubernetes migration."
Another source says: "Supported containerization proof-of-concept."

Which is most accurate?

A. I personally designed or owned Kubernetes architecture.
B. I implemented Kubernetes/EKS manifests, Helm charts, or cluster configuration.
C. I supported planning or proof-of-concept work but did not own implementation.
D. I worked around Kubernetes but should not claim it as a skill.
E. Remove Kubernetes entirely from my master CV.
```

## Master Principle

Layer 0 does not trust old resumes, cover letters, LinkedIn, recruiter resumes, or the model's interpretations. It treats all of them as leads to investigate.

The user is the final authority before any claim becomes resume-ready.
