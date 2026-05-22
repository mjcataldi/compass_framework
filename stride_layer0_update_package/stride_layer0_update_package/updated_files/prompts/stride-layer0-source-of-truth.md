# STRIDE Layer 0 Source-of-Truth Prompt

Use this prompt when onboarding a new person to STRIDE, creating a verified career source of truth, or compiling a master CV from prior resumes, cover letters, LinkedIn exports, brag documents, project notes, certifications, recruiter resumes, or other source documents.

This prompt is a workflow launcher. The authoritative behavior lives in the active STRIDE rule files, especially `rules/07-source-of-truth-onboarding.md`.

```text
Start STRIDE Layer 0: Verified Career Source-of-Truth Builder.

Before running this workflow, read the latest STRIDE framework files from the connected GitHub repo or selected STRIDE source.

Use the repository or selected STRIDE source as the source of truth for STRIDE behavior. Do not rely on cached STRIDE instructions when the selected source is available.

Required framework files:
- VERSION.md
- STRIDE_Current.md
- rules/00-operating-principles.md
- rules/04-truthguard.md
- rules/06-artifact-rules.md
- rules/07-source-of-truth-onboarding.md

If GitHub or selected STRIDE source access fails, say so clearly before proceeding. Do not reconstruct STRIDE behavior from memory unless I explicitly authorize that fallback.

Treat this prompt as a workflow launcher, not as an independent source of TruthGuard, artifact, storage, source-priority, or no-fabrication rules.

Apply the active rule files listed above as the authoritative rubric for this workflow. If this prompt appears to conflict with any required rule file, follow the rule file and mention the conflict in chat outside the artifact.

My Google Drive source folder is:
[PASTE GOOGLE DRIVE FOLDER LINK HERE]

My STRIDE framework source is one of the following:
[Choose one]
- Use the most up-to-date STRIDE framework available in this Project's sources.
- Use the canonical STRIDE repo on main.
- Use this specific STRIDE repo or fork: [PASTE LINK HERE]
- Use the STRIDE instructions already present in this Project.
- No repo available; use this prompt and the current Project instructions as the fallback Layer 0 definition.

If more than one STRIDE framework source is available, ask me which one should take precedence before proceeding.

Core mission:
Build a truthful, interview-defensible career source of truth that can later be compiled into a master CV and used for tailored resumes, cover letters, recruiter materials, job-fit analysis, and interview preparation.

Do not treat this as resume writing yet. Treat this as evidence capture, claim verification, and source-of-truth construction.

Opening user reassurance:
Before asking intake questions, explain in plain language that this process may take multiple sessions. Reassure me that we will work in small batches, that I can pause at any time by saying "I need a break," "pause," "bookmark this," or "let's continue later," and that every committed round will produce a checkpoint.

Storage honesty:
At the start of the session, inspect the available Project sources and Google Drive folder context. Then determine whether you can directly create or update files in the Google Drive folder.

If you can save/update files directly:
- Maintain the Layer 0 source-of-truth files in the selected Google Drive folder.
- Tell me what was saved or updated after each committed round.

If you cannot save/update files directly:
- Produce copy-ready versions of the relevant files after each committed round.
- Tell me exactly which file each block belongs in.
- Ask me to save the response as a Project source or copy it into my Google Drive folder.
- Do not pretend the files were saved if they were only generated in chat.

Layer 0 source-of-truth files:
- 00_README.md
- 01_source_document_manifest.md
- 02_role_timeline.md
- 03_claim_ledger.md
- 04_skill_inventory.md
- 05_do_not_claim.md
- 06_cross_examination_log.md
- 07_master_cv_draft.md
- checkpoints/[date-time]-layer0-checkpoint.md

Layer 0 operating rules:

1. Source documents are evidence, not truth.
   Prior resumes, LinkedIn profiles, cover letters, recruiter resumes, and old bios may contain outdated, inflated, incomplete, or aspirational claims. Extract from them, but do not trust them automatically.

2. Ask a few questions at a time.
   Keep each question batch to 3-5 questions unless I ask for more.

3. Separate confirmed facts from candidate claims.
   Use these categories:
   - Confirmed facts
   - Source-extracted claims
   - Candidate inferred claims
   - Contradictions or inconsistencies
   - Clarifying questions
   - Approved claims
   - Rejected / do-not-claim items
   - Needs evidence
   - Needs metric
   - Needs scope

4. Never add inferred skills directly to the master CV.
   If a source document mentions Kubernetes, Terraform, AWS, AI, leadership, architecture, security, compliance, or any other skill, ask me what my actual relationship to that skill was.

5. Use a claim-depth scale for every skill or responsibility:
   - No claim
   - Awareness
   - Exposure
   - Supported
   - Implemented
   - Owned
   - Led others

6. Track rejected claims.
   If I say I do not want to claim something, add it to a do-not-claim list so future resumes and cover letters do not reintroduce it.

7. Do not invent metrics.
   If a source document says "improved," "reduced," "accelerated," or "saved," ask whether a real number exists. If no number exists, use non-quantified phrasing.

8. Do not convert team work into individual ownership.
   Ask whether I personally owned, supported, implemented, influenced, advised, or merely participated in the work.

9. Do not convert exposure into skill.
   If I worked near a tool or system but did not use it hands-on, mark it as exposure or awareness, not implementation.

10. Every approved claim must be interview-defensible.
    Before making a strong claim resume-ready, ask whether I could defend it if an interviewer spent 10 minutes drilling into it.

Commit behavior:
When I say "commit," "approved," "yes, save that," or otherwise clearly approve a round:
- Update the claim ledger.
- Update the do-not-claim list if applicable.
- Update the role timeline if applicable.
- Update the source document manifest if applicable.
- Update the cross-examination log.
- Produce a checkpoint.
- Tell me what changed and what the next question batch will cover.

Pause behavior:
If I say "I need a break," "pause," "bookmark this," or "let's continue later":
- Stop asking new questions.
- Produce a checkpoint.
- Include:
  - Current stage
  - Completed items
  - Approved claims count
  - Rejected claims count
  - Unresolved claims count
  - Current role or source under review
  - Next recommended question batch
  - Any files that need saving
- Tell me how to resume: "Say 'resume Layer 0 from the last checkpoint.'"

Layer 0 workflow:

Stage 0A — Setup verification
- Confirm the Google Drive source folder.
- Confirm the STRIDE framework source or fork.
- Confirm whether you can access the source documents.
- Confirm whether you can save directly or will provide copy-ready checkpoint files.

Stage 0B — Source harvesting
- Inventory the uploaded or linked documents.
- Identify document types.
- Extract obvious facts, dates, roles, titles, education, certifications, and contact information.
- Flag inconsistencies.

Stage 0C — Timeline reconstruction
- Build a preliminary chronological career timeline.
- Ask me to confirm titles, employers, dates, contract/client relationships, and gaps.

Stage 0D — Claim extraction
- Extract claims from all source documents.
- Classify them as unverified until I confirm them.
- Group them by role, skill, accomplishment, domain, and leadership scope.

Stage 0E — Cross-examination
- Ask focused questions in small batches.
- Resolve contradictions.
- Confirm, downgrade, or reject claims.
- Assign claim-depth levels.

Stage 0F — Claim ledger construction
- Capture approved claim text, source role, source document, skill tags, depth level, evidence basis, strongest truthful phrasing, conservative truthful phrasing, interview defensibility, and status.

Stage 0G — Master CV assembly
- Only after enough claims are confirmed, compile the master CV draft from approved claims only.

Begin now with Stage 0A. First, explain the process to me in plain language, including that this may take multiple sessions and that we will checkpoint after every committed round. Then inspect the available sources and ask me no more than 5 setup questions.
```

## Notes

Layer 0 should feel like careful cross-examination, not like a generic resume questionnaire.

The generated master CV should be based only on approved claims. Any caveats, rejected claims, unsupported source claims, unresolved contradictions, or storage limitations should be tracked in Layer 0 source-of-truth files, not hidden.
