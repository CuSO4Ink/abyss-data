---
type: global-direction-brief
status: active
created: 2026-05-25
updated: 2026-05-25
tags:
  - abyss/global-direction
  - abyss/agent-sync
  - abyss/external-collaboration
  - abyss/brain-agent
  - abyss/self-evolution
---

# Abyss Global Direction Brief

## 0. Purpose

This document is the current global direction brief for Abyss development.

It is written for:

```text
Owner
internal Agents
future Brain Agent
external model platforms
external development assistants
```

Any AI assisting with Abyss development should read this brief before proposing architecture, implementation plans, ChangeSets, reviews, or next-step recommendations.

This brief is not an execution approval. It is a direction and synchronization document. All meaningful system changes must still follow Abyss governance.

---

## 1. Current one-line direction

Abyss is moving from a working governed self-evolution MVP toward a cognition-first personal AI operating layer, where a future Brain Agent can understand system state, coordinate development, prepare external task briefs, and integrate results without bypassing governance.

Current priority:

```text
Stabilize cognition, disclosure, external collaboration, and read-only system insight before expanding autonomous execution.
```

---

## 2. Current positioning

Abyss is a local-first, governed, personal AI operating layer.

It is not:

```text
a general chatbot
an unrestricted autonomous executor
a production-grade unattended self-modifying system yet
a system where external models own decisions or memory
```

It is currently best understood as:

```text
personalized
local-first
governed
observable
auditable
progressively self-evolving
Owner-supervised
```

Abyss already has a usable MVP and a working self-evolution chain. Development should therefore be incremental. Do not assume a full rewrite unless the Owner explicitly requests one.

---

## 3. Current maturity assessment

The self-evolution workflow has demonstrated a real governed loop:

```text
request
-> proposal
-> roadmap approval
-> workflow
-> implementation output
-> ChangeSet validation
-> dry-run
-> Harness review
-> Owner approval
-> executor apply
-> report
-> summary check
```

It has already shown the ability to:

```text
find problems
turn problems into follow-up requirements
implement small fixes
validate results
classify expected governance blocks
avoid treating every blocked item as failure
surface summary and workflow state
retry selected transient provider failures
```

Current maturity:

```text
Stage target: mostly achieved for supervised local self-evolution
Engineering maturity: usable, still being hardened
Good fit: low-risk local improvements, supervised self-iteration, external model collaboration
Not yet fit: long-term unattended production autonomy, high-risk self-modification, unrestricted execution
```

This means Abyss can proceed to Brain Agent preparation and read-only cognition work. It does not need to reach production-grade autonomous self-development before the Brain Agent direction begins.

---

## 4. Non-negotiable global rules

All Abyss development must respect these rules:

```text
1. Owner remains the final authority for meaningful risk, direction changes, and execution approval.
2. LLM, Agent, and external model outputs are candidate material only; they are not facts, approvals, or actions.
3. The Brain Agent is a cognition, coordination, task decomposition, direction alignment, and result integration layer; it is not an unrestricted executor.
4. External model platforms are replaceable expert resources; they do not own Abyss governance, memory, execution, or direction.
5. System cognition starts from ABYSS.md and follows progressive disclosure.
6. Contracts, module capsules, system maps, and direction documents should be read before source code when possible.
7. Meaningful changes must follow the governed path unless the Owner explicitly authorizes a limited bootstrapping edit.
8. Changes must remain observable, auditable, rollback-aware, and reviewable.
9. When implementation changes affect system understanding, the relevant cognition layer must be updated.
10. Do not force future Agents to rediscover stable system facts by reading source code if the information belongs in a higher disclosure layer.
```

---

## 5. Five foundational architectures

Abyss is currently organized around five foundational architectures:

```text
FSM
Self Evolution
Abyss Insight
Skill
Memory / Storage
```

They answer different questions:

```text
FSM: how system state advances
Self Evolution: how the system improves itself under governance
Abyss Insight: how the system sees and summarizes its current state
Skill: how reusable capabilities are stabilized and invoked
Memory / Storage: how long-term decisions, history, state, and experience are retained
```

The Brain Agent should coordinate across these foundations. It should not replace them or bypass their boundaries.

---

## 6. Medium-term goal: Brain Agent v0

The current medium-term goal is to prepare Abyss for Brain Agent v0.

Brain Agent v0 should initially be read-only or near-read-only.

It may:

```text
read global direction and cognition layers
read current system state summaries
explain what is happening
identify next candidate tasks
prepare external model task briefs
review external results as candidate material
compress accepted results into feedback cards or direction notes
warn when local changes drift from architecture
```

It must not:

```text
approve roadmap items
approve ChangeSets
execute changes
modify files directly
bypass Harness review
bypass Owner approval
replace the Owner
start open-ended self-iteration loops
turn model suggestions directly into actions
```

Target role:

```text
Brain Agent = cognition and coordination layer
Self Evolution = governed improvement pipeline
External models = temporary expert workers
Owner = final authority
```

---

## 7. Relationship between Brain Agent and external model platforms

External model platforms should not be treated as the Brain Agent.

The intended future collaboration pattern is:

```text
Brain Agent or Owner prepares a scoped task brief
-> external model platform performs analysis or drafts implementation
-> result returns as structured candidate material
-> Abyss imports or summarizes it as a feedback card
-> Brain Agent or Owner reviews alignment
-> governed self-evolution path decides whether anything becomes executable work
```

External platforms are useful for:

```text
local implementation drafts
alternative design analysis
code review suggestions
risk review
summarization
specialized reasoning
```

External platforms must not:

```text
claim authority over global direction
approve their own output
execute directly in Abyss
mutate governance rules without explicit Owner authorization
assume missing context
turn local task results into permanent memory without review
```

---

## 8. What a new external AI should read first

A new external model platform or assistant should synchronize by reading in this order:

```text
1. ABYSS.md
2. This Global Direction Brief
3. ABYSS_CONSTITUTION.md
4. rules/system_brief.yaml
5. SYSTEM_MAP.md
6. rules/architecture_cognition.yaml
7. rules/modules.yaml
8. rules/contracts/ only when contract-level work is needed
9. relevant source files only when implementation or verification requires them
10. runtime records only when debugging, auditing, or reconstructing state
```

If the task is packaged by Abyss, the external model should prefer the provided task package over broad repository exploration.

The external model should always ask for more context when the package is insufficient instead of guessing.

---

## 9. Current progress snapshot for development synchronization

The current architectural direction has advanced beyond the original MVP stage.

Important completed or mostly completed foundations include:

```text
ABYSS.md cognition entrypoint
progressive disclosure reading order
architecture cognition protocol
module capsule structure in rules/modules.yaml
contracts directory for key machine-readable interfaces
Brain Agent role registered as disabled/read-only experimental
external collaboration feedback card concept
summary/check and workflow/report observability improvements
classification of expected governance blocks and superseded failures
initial provider transient failure retry behavior
```

Current known limitations:

```text
Global direction is still being normalized into stable, readable documents.
External onboarding is present but still needs stronger canonical packaging.
Brain Agent is not yet an active decision-making executor.
Abyss Insight is not yet a dedicated formal snapshot layer.
Memory / Storage should not be broadly connected before Insight is stable.
Implementation Agent ChangeSet quality still needs hardening, especially small-anchor edits.
Runtime smoke coverage and import checks should continue improving.
Historical proposed/invalid ChangeSets may need lifecycle cleanup.
Owner approval policy should become more explicit before higher automation.
```

Operational interpretation:

```text
The system is ready for read-only Brain Agent preparation and Insight v0 work.
The system is not ready for unattended production-grade autonomy.
```

---

## 10. Current development priorities

The next capabilities should be added in dependency order. The goal is not to add many autonomous abilities at once, but to make each new layer observable, reversible, and useful to the future Brain Agent.

Recommended capability order:

```text
0. Direction and cognition surface stabilization
1. FSM hardening and state semantics
2. Abyss Insight v0 read-only system snapshot
3. Git automation v0 for safe checkpoints and rollback support
4. Obsidian / user_data bridge for personal knowledge synchronization
5. Brain Agent v0 read-only cognition and coordination
6. External collaboration task brief and feedback-card loop
7. Memory v0 curated append-only long-term records
8. Higher-autonomy self-evolution only after the above are stable
```

Dependency logic:

```text
FSM should clarify what state the system is in.
Insight should summarize that state without mutating it.
Git automation should preserve checkpoints before deeper self-evolution.
Obsidian/user_data should provide personal context without polluting system code or runtime records.
Brain Agent should consume Direction, Insight, FSM state, module capsules, and curated user context.
Memory should come after Insight and Brain Agent have clearer rules for what is worth retaining.
```

Near-term priorities:

```text
1. Normalize global direction and external onboarding documents.
2. Keep ABYSS.md as the cognition entrypoint and avoid source-code-first understanding.
3. Strengthen the minimum disclosure model and cognition-layer synchronization.
4. Harden FSM state semantics, terminal states, blocked/no-op classification, and workflow timeline visibility.
5. Build Abyss Insight v0 as a read-only system state snapshot layer.
6. Add Git automation v0 as a governed safety layer: status/diff summary, checkpoint recommendation, generated commit message, and explicit Owner-approved local commit.
7. Define the Obsidian/user_data bridge as the user-facing knowledge surface, initially read-only or sync-aware, without mixing personal data into the system repository.
8. Let Brain Agent v0 consume Insight snapshots and produce explanations or next-step candidates.
9. Improve external model task packages and feedback card review.
10. Harden Implementation Agent output quality, especially small safe ChangeSets.
11. Improve runtime smoke checks and import validation.
```

Medium-term priorities:

```text
1. Brain Agent read-only state reasoning across Direction, FSM, Insight, module capsules, and selected user_data context.
2. External task brief generation through Brain/Context Broker.
3. Structured result integration from external model platforms.
4. Git automation v1 with governed local commit records, audit links, rollback notes, and separate handling for system repo vs user_data repo.
5. Obsidian integration v1 for syncing accepted notes, direction summaries, decision records, and working summaries into the personal knowledge surface.
6. Memory v0 as append-only, curated, provenance-aware decision and lesson records.
7. Context Broker retrieval of only the minimum useful Memory subset.
8. Stronger workflow timeline and state observability.
```

Long-term priorities:

```text
1. More autonomous but still governed development loops.
2. Better provider failure taxonomy, retry, and health monitoring.
3. Cleaner ChangeSet lifecycle management.
4. Stronger policy for auto-approval of low-risk changes, if Owner allows it.
5. Git automation v2 only after safety is proven: optional guarded push/sync flows, never uncontrolled auto-push.
6. Deeper Obsidian/Memory/Brain integration only after provenance, privacy, and retention rules are stable.
7. Production-grade unattended behavior only after governance, rollback, observability, and memory hygiene are mature.
```

Git automation boundaries:

```text
Git automation is needed, but it should start as a safety and observability feature, not as autonomous publishing.
V0 may summarize git status, summarize diff, suggest commit grouping, generate commit messages, and create local commits only with explicit Owner approval.
V0 must not auto-push, rewrite history, delete branches, or mix the Abyss system repository with personal user_data content.
Every automated commit should connect back to workflow/report/evidence when possible.
```

Obsidian/user_data boundaries:

```text
Obsidian should be treated as the human-facing knowledge surface, not the execution authority.
The system repository and personal user_data repository should remain separate.
Accepted direction notes, decision records, working summaries, and selected Insight outputs may be synchronized into user_data.
Raw model output, failed drafts, provider scratch space, and noisy runtime logs should not be automatically promoted into Obsidian or long-term Memory.
```

---

## 11. Recommended sequence: Insight before Memory

Abyss Insight should come before broad Memory / Storage integration.

Reason:

```text
Insight answers: what is happening now?
Memory answers: what should be retained long-term?
```

If Memory is connected too early, temporary errors, stale conclusions, and model-generated noise may become long-term cognitive pollution.

Recommended sequence:

```text
1. Normalize Global Direction and external onboarding.
2. Build Abyss Insight v0 as read-only state snapshot.
3. Let Brain Agent v0 consume Insight snapshots.
4. Add Memory v0 as append-only curated records.
5. Later allow Context Broker and Brain Agent to retrieve selected Memory.
```

Memory v0 should initially store only reviewed high-value records such as:

```text
Owner decisions
architecture milestones
accepted external feedback
rejected directions
validated lessons
failure postmortems
```

Memory v0 should not automatically store:

```text
all raw LLM outputs
all runtime logs
all failed drafts
all proposed but unaccepted ChangeSets
all temporary discussions
all provider scratch space
```

---

## 12. Cognition Surface and minimum disclosure back-propagation

Abyss needs more than executable code. It needs a minimal, layered, and verifiable cognition surface above source code so humans, internal Agents, external model platforms, and the future Brain Agent can understand the system without defaulting to full source-code reading.

This cognition surface is not a second copy of the code. It is a controlled abstraction layer for stable system facts, module boundaries, contracts, direction, state interpretation, and development intent.

Current engineering principle:

```text
Code remains the final implementation evidence.
The cognition surface explains stable system meaning.
Progressive disclosure decides how much each reader needs.
Changes that affect future understanding propagate upward only to the lowest sufficient layer.
```

When a file changes, the implementer should determine whether the change affects how Abyss should be understood at a higher disclosure layer.

If yes, update the nearest sufficient cognition surface with a concise summary.

If no, the implementation result should explicitly state that no cognition-layer update is required.

The principle is:

```text
Do not duplicate everything everywhere.
Do not hide stable system facts only in source code.
Do not treat model-generated explanation as authority without validation.
Push only the minimum necessary summary upward.
Keep detailed evidence in the lower layer.
Keep each summary traceable to source, contract, report, or Owner decision.
```

This supports:

```text
Brain Agent readiness
external model synchronization
Abyss Insight snapshots
future Memory hygiene
safer self-evolution
lower source-code-first context load
```

Main risks to avoid:

```text
explanation drift away from code
abstract summaries losing critical constraints
over-documenting every implementation detail
promoting unverified model output into system truth
self-iteration loops that only validate their own explanations
prematurely freezing exploratory designs as core rules
```

Typical mapping:

```text
source code behavior change -> SYSTEM_MAP.md or module capsule if externally meaningful
module boundary change -> rules/modules.yaml
context selection change -> rules/context_manifest.yaml and architecture cognition protocol
agent role change -> rules/agents.yaml and possibly ABYSS.md if globally meaningful
new command or user-facing operation -> README.md and SYSTEM_MAP.md
governance boundary change -> ABYSS_CONSTITUTION.md, system brief, policy, or governance rules
strategy change -> this Global Direction Brief and possibly ABYSS.md
runtime incident only -> report/audit first; promote upward only after stable lesson is accepted
```

External models should include a cognition update assessment in their result card:

```text
cognition_update_required: yes/no
minimum_disclosure_layer:
target_document:
summary:
reason:
```

---

## 13. Current allowed development directions

Allowed and encouraged now:

```text
Global Direction normalization
external model onboarding documentation
FSM state semantics and workflow timeline hardening
Abyss Insight v0 read-only snapshot design
Git automation v0 for status/diff summary, checkpoint recommendation, and Owner-approved local commits
Obsidian/user_data bridge design for accepted notes, direction summaries, decision records, and working summaries
Brain Agent v0 read-only cognition design
Context Broker minimum disclosure improvements
module capsule refinement
contract clarity
summary/report/workflow observability improvements
Implementation Agent output hardening
small safe ChangeSet validation improvements
runtime smoke/import checks
external feedback card quality improvements
```

Allowed only with caution and explicit scope:

```text
limited direct bootstrapping documentation edits approved by Owner
small governance-adjacent wording or validation changes
small source changes with strong checks and rollback awareness
Git local commit creation only after explicit Owner approval
Obsidian/user_data sync only for accepted, provenance-aware notes
Memory v0 schema design without broad automatic ingestion
```

Not appropriate now:

```text
full system rewrite
unrestricted Brain Agent execution
automatic approval of arbitrary tasks
external model direct execution
bypassing Harness or Owner approval
automatic git push or history rewrite without explicit Owner authorization
mixing personal Obsidian/user_data content into the system implementation repository
broad automatic Memory ingestion
large-scale vector memory as default context
high-risk autonomous self-modification
production-grade unattended operation claims
```

---

## 14. External AI recommended output format

External AI should return structured candidate material like this:

```text
task_understanding:
modules_touched:
files_touched:
proposed_changes:
validation_performed:
risk_assessment:
architecture_alignment:
cognition_update_required:
minimum_disclosure_layer:
open_questions:
recommended_next_step:
```

For implementation drafts, external AI should prefer:

```text
small edits
stable anchors
minimal file scope
clear validation steps
explicit no-op/already-satisfied result when applicable
clear blocked result when context is insufficient
```

External AI should avoid:

```text
large function replacement when a smaller edit is possible
inventing files or commands not present in context
assuming governance approval
mixing proposal, approval, and execution language
writing decorative low-information output
using source code as the only system truth
```

---

## 15. Direction drift checks

Before proposing or implementing anything, an AI should ask:

```text
Does this serve the Brain Agent and cognition-first direction?
Does this strengthen boundaries, observability, or rollback safety?
Does this preserve Owner and Harness authority?
Does this respect progressive disclosure?
Does this reduce future need to reread source code for stable facts?
Does this avoid premature Memory pollution?
Does this avoid turning external model output into authority?
Is the change small enough to review and reverse?
```

If the answer is unclear, ask for Owner decision or return a blocked/context-insufficient result.

---

## 16. Current phase label

The current phase can be summarized as:

```text
Phase: supervised cognition-first hardening
Focus: global direction, minimum disclosure, FSM hardening, Insight v0, Git safety checkpoints, Obsidian/user_data bridge, Brain Agent v0 preparation, external collaboration discipline
Execution posture: governed, Owner-supervised, low-risk incremental changes
Autonomy posture: not production-grade unattended autonomy
```

Practical next step:

```text
Use this brief as the canonical direction sync document for external AI development assistance, while continuing to route real modifications through Abyss governance unless the Owner explicitly authorizes a narrow documentation/bootstrap edit.
```

---

## 17. Active PM-mode development plan

Status date:

```text
2026-05-25
```

Current operating mode:

```text
External assistant direct system-file modification is now closed for normal development.
The assistant should act from the Abyss user interaction layer, similar to a product manager or Owner-side operator.
It may inspect status, prepare proposals, help approve/reject via exposed interfaces when explicitly asked, package external briefs, and track progress.
It must not directly edit Abyss system source files for normal feature work.
Only stop-level recovery remains eligible for minimal direct repair under the existing Owner authorization.
```

Remote sync checkpoint:

```text
Abyss system repository has been checkpointed and pushed to origin/main after the recent governed changes.
Checkpoint commit: cebc92f feat: harden cognition and workflow governance
Pre-push checks: python -m abyss_cli check = OK; python -m abyss_cli summary --check = OK.
Operational health at checkpoint: active_workflows=0, pending_owner_items=0, true_failures=0, true_blocked=0.
```

Active staged roadmap for cognition-first hardening:

```text
0. Direction and cognition surface stabilization.
1. FSM state semantics and workflow timeline hardening for Insight readiness.
2. Abyss Insight v0 read-only system snapshot.
3. Git automation v0 for safe checkpoints and rollback support.
4. Obsidian / user_data bridge for accepted notes, direction summaries, decision records, and selected Insight outputs.
5. Brain Agent v0 as strong cognition, coordination, task decomposition, direction checking, and decision-preparation layer.
6. External collaboration task brief and feedback-card loop.
7. Memory v0 as curated, append-only, provenance-aware long-term records.
8. Higher-autonomy self-evolution only after governance, rollback, observability, cognition, and memory hygiene are stable.
```

Immediate next candidate proposal:

```text
FSM state semantics and workflow timeline hardening for Insight readiness
```

Proposed scope of the immediate next candidate:

```text
Clarify workflow terminal states and outcome semantics.
Stabilize true_failure, true_blocked, expected_governance_blocks, satisfied_without_changes, and superseded_by_corrected_changeset classifications.
Improve workflow timeline visibility for Owner, Brain Agent, and future Insight snapshots.
Clarify lifecycle treatment for invalid/proposed historical ChangeSets.
Provide a stable read-only input surface for Insight v0.
Avoid adding Memory ingestion, Brain Agent execution authority, or autonomous system modification.
```

Progress tracking rule:

```text
This section should be updated when phase boundaries are crossed, when a checkpoint is pushed, or when the active next candidate changes.
Detailed execution evidence should remain in Abyss workflow/report/audit records or Git history; this brief should retain only direction-level progress and current next-step alignment.
```
