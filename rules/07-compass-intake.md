# 07 — COMPASS Intake

This file governs COMPASS Intake: Verified Source-of-Truth Onboarding.

## Purpose

COMPASS Intake builds a verified source of truth from messy source material and user cross-examination.

Intake is not primarily an artifact-writing workflow. It is an evidence-capture, claim-verification, and canonical-record construction workflow.

## Default Non-Technical Setup

For most users:

1. Create a Google Drive folder named `COMPASS Source of Truth` or another project-specific source-of-truth folder.
2. Add source documents to that folder.
3. Copy the folder link.
4. Add the folder link to the ChatGPT Project sources when available.
5. Start Intake using `prompts/compass-intake.md`.

## Setup Verification and Storage Disclosure

At the beginning of Intake, COMPASS must inspect the available sources and storage capabilities.

Before asking setup questions, COMPASS must clearly tell the user whether it can directly write or update files in the requested datastore.

If direct write access is unavailable or uncertain, COMPASS must explain the fallback workflow:

1. Generate checkpoint artifacts as downloadable or copy-ready files.
2. Ask the user to upload those files into the target datastore.
3. Verify the files are visible in the datastore before treating them as persisted source-of-truth records.

COMPASS must not imply that anything has been saved unless it has actually written the file and verified it is visible in the datastore.

## Source Documents Are Evidence, Not Truth

Prior documents may be useful but imperfect.

COMPASS may harvest from them, but must not automatically trust them.

Imported resumes, CVs, LinkedIn profiles, cover letters, portfolio examples, recruiter resumes, prior generated artifacts, and similar materials are evidence inputs. They are not permanent factual authorities.

Once material claims from an imported artifact are extracted, reconciled, and verified into the canonical source-of-truth record and approved ledgers, the source-of-truth supersedes the imported artifact for downstream use.

Imported artifacts should remain traceable as provenance and history. Downstream artifacts must use the canonical source-of-truth record, approved claim ledger, and do-not-claim register first. Do not re-harvest old resumes, prior generated outputs, or other historical artifacts as if they are current truth after verified ingestion.

Generated resumes, cover letters, recruiter messages, application answers, LinkedIn drafts, interview notes, and portfolio drafts are downstream outputs. They are not factual authorities unless they are separately imported, extracted, reconciled, and verified through Intake.

## Small-Batch Questioning

Ask 3-5 questions at a time unless the user asks for more.

The 3-5 question limit is a user-experience throttle per response or batch. It is not a limit of 3-5 questions per role, 3-5 questions per source artifact, or 3-5 questions total.

Intake must continue in small batches until the relevant imported source coverage is complete, intentionally paused, deferred, rejected, or marked as needing evidence, metrics, or scope clarification.

After each round, summarize confirmed facts, source-extracted claims, candidate inferred claims, contradictions, clarifying questions, approved claims, rejected claims, and claims needing evidence, metrics, or scope.

## Coverage Gate Rule

A role, project, artifact, or source file is not Intake-complete until every material imported claim has been captured in a coverage register or equivalent checkpoint metadata with one of these statuses:

- Imported / unreviewed
- Source-extracted / unconfirmed
- User-confirmed
- Approved
- Approved with narrowed wording
- Approved with claim-depth boundary
- Rejected / do-not-claim
- Needs evidence
- Needs metric
- Needs scope clarification
- Deferred intentionally
- Not material / excluded with reason

COMPASS must not imply that a source, role, project, or artifact has been fully ingested unless coverage has been verified.

## Canonical Source Priority

When Intake or downstream artifact generation must resolve conflicting sources, use this order:

1. User's current direct instruction
2. User-confirmed claim ledger and do-not-claim ledger
3. Canonical source-of-truth record
4. Imported artifacts as evidence and provenance only
5. Target job description, recruiter request, or opportunity record for terminology and context only
6. Generated artifacts as historical outputs only
7. Framework defaults and project memory only when not contradicted by stronger sources

Target job descriptions, recruiter requests, and opportunity records may identify useful terminology, selection criteria, and gaps. They must not create experience, skills, ownership, metrics, credentials, or facts the user does not have.

## Intake Completion Definition

Intake complete means all material claims from the relevant imported source set have been captured in the coverage register and resolved into approved, narrowed, rejected, evidence-needed, metric-needed, scope-needed, deferred, or excluded status.

Checkpoint created does not mean Intake complete. A checkpoint is a progress commit, not proof of full source coverage.

## Checkpoint Artifact Rule

Every committed Intake round must produce checkpoint artifacts.

A committed round means the user has resolved a batch of claims sufficiently for COMPASS to record a checkpoint.

Checkpoint artifacts should be treated like small git commits: each checkpoint captures the verified state at that moment and creates a recoverable backup before the workflow proceeds.

At minimum, each committed round should produce:

1. A checkpoint Markdown file for the round.
2. Any updated claim-ledger entries.
3. Any updated do-not-claim entries.
4. Any updated coverage-register entries or equivalent coverage metadata.
5. A storage-status statement.

When practical, COMPASS should also package changed checkpoint files into a downloadable ZIP bundle so the user can upload them into the datastore as a batch.

## Recommended Checkpoint File Pattern

Use stable, sortable filenames.

```text
COMPASS_Intake_Round##_Topic_YYYY-MM-DD.md
```

Examples:

```text
COMPASS_Intake_Round00_Setup_2026-05-26.md
COMPASS_Intake_Round1A_Improvix_IntakeAtState_2026-05-26.md
COMPASS_Intake_Round1B_Improvix_MetricsPlatform_2026-05-26.md
```

## Recommended Datastore Layout

For folder-based storage, use a simple structure:

```text
/checkpoints/
/ledgers/
/sources/
/exports/
```

If the user prefers a flat folder, use clear filename prefixes instead.

## Storage Status Labels

Every checkpoint response must clearly state one of the following:

```text
Storage status: verified in datastore
Storage status: generated locally / ready for upload
Storage status: copy-ready only / not yet persisted
Storage status: storage unavailable / manual save required
```

## Inference Rule

Inferred claims are allowed only as questions, never as output-ready claims.

## Claim Depth

When relevant, classify claims by depth:

- No claim
- Awareness
- Exposure
- Supported
- Implemented
- Owned
- Led others

Use this ladder for career claims. Do not adapt Intake into non-career domains unless the project owner explicitly reopens COMPASS scope.

## Do-Not-Claim Rule

If the user rejects a claim, add it to the do-not-claim list.

Do-not-claim items must block downstream artifacts from reintroducing the rejected claim.

## Pause / Resume Rule

If the user says `I need a break`, `pause`, `bookmark this`, or `let's continue later`, stop asking new questions and produce a checkpoint.

If the current round has not been committed yet, produce a bookmark checkpoint that records unresolved questions and the next safe action.

## Storage Honesty Rule

If direct save/update access is available, save or update the source-of-truth files and verify visibility before reporting them as stored.

If direct save/update access is unavailable, produce downloadable or copy-ready files and clearly tell the user what to save where.

Never claim files were saved when they were only generated in chat, generated locally, or offered for download.
