# STATUS — Elementor V4 Architect Prompt Pack

Version: 0.14.0
Status: rag_strategy_contract_hardened
Last confirmed stage: Elementor Knowledge Base / RAG Strategy contract hardening
Current next step: Harden `knowledge/TUYA_ELEMENTOR_V4_CONCEPTS.md` from `active_reference v0.2.0` into an active v1.0.0 internal concept reference contract aligned with `references/ELEMENTOR_KNOWLEDGE_BASE_RAG_STRATEGY.md` and `stages/02_RESEARCH.md`.
Language: Persian reports, English technical labels allowed
Last automation update: 2026-06-22

---

## Pipeline

1. /intake
2. /research
3. /decompose
4. /architectures
5. /score-evidence
6. /score-audit
7. /recommend
8. /build-tree
9. /implementation
10. /final-audit
11. /handoff-export
12. /e2e-test

---

## Stage Status

| Stage / Contract | Status | Notes |
|---|---|---|
| /intake | confirmed | Lightweight default-based intake |
| /research | confirmed_hardened_v1.0.0 | Stage 2 research contract with input gate, source access policy, source pinning, retrieval fact ledger, `ev4-research-payload@1.0.0`, downstream permission map, repair routes, self-audit, debug trace, and anchor handoff |
| /decompose | confirmed_with_example_bank | Controlled Visual Role Decomposition with example bank; must not use research/RAG/TUYA/docs to invent visual groups |
| /decomposition-example-bank | active_enhanced | Pattern-based examples plus authoring standard |
| /architectures | confirmed_hardened_v1.1.0 | Coverage matrix, unknown propagation, recommendation ban, dynamic guardrails |
| /score-evidence | confirmed_hardened_v1.3.0_patch | Uses rubric 1.3 and Stage 4 v1.3 hardening patch |
| /score-audit | confirmed_hardened_v1.2.0_patch | Adds Stage 5 self-audit, hidden recommendation guard, tie handoff, responsive cap reference binding |
| /scoring-calibration-bank | active | examples/scoring calibration cases added |
| /recommend | confirmed_hardened_v1.1.0_patch | Recommendation matrix, provenance ledger, tie handling, build-tree readiness gate, debug record |
| /stage-anchor-contract | active_v1.1.0 | Adds confidence_delta, target_stage_hardening_status, and partial_rerun_state |
| /partial-rerun-contract | active_v1.0.0 | Defines safe partial reruns and invalidation rules |
| /debug-trace-contract | active_v1.0.0 | External trace contract for pipeline debugging |
| /build-tree | confirmed_hardened_v1.0.0 | Naming convention, Structure Panel tree schema, wrapper budget, widget constraints, responsive contract |
| /implementation | confirmed_hardened_v1.0.0 | Stage 8 hardened with input gate, payload schema, source ledger, settings schema, widget map, class/variable map, scoped CSS validator, asset/accessibility map, responsive examples, repair routes, self-audit, debug trace, and anchor handoff |
| /final-audit | confirmed_hardened_v1.0.0 | Stage 9 hardened with input gate, Source Access Matrix binding, severity taxonomy, audit checklists, repair routes, regression cases, Final_Audit_Payload schema, self-audit, debug trace, and anchor handoff |
| /handoff-export | confirmed_hardened_v1.0.0 | Stage 10 hardened with input gate, Source Access Matrix binding, handoff eligibility matrix, blocked handoff report, payload ledger, audit-flag preservation, Handoff_Payload schema, repair anchor, self-audit, debug trace, and E2E release boundary |
| /elementor-knowledge-base-strategy | active_v1.0.0 | Hardened from `draft_active_v0.3.0` into `ev4-rag-strategy-contract@1.0.0`; now has current stage matrix, `/research` source-pinning ownership, source classes, source pins, retrieved fact schema, downstream permission defaults, freshness policy, EDIS boundary, conflict lifecycle, leakage probes, repair routes, self-audit, debug trace, and next anchor |
| /tuya-concept-reference | active_reference_v0.2.0 | Next unfinished source-policy-adjacent contract. Needs alignment with RAG Strategy v1.0.0 and Research v1.0.0 source classification rules |
| /e2e-test-plan | confirmed_hardened_v1.0.0 | Defines full-pipeline E2E scope, fixture contract, source-access checks, anchor validation, debug trace validation, negative controls, report schema, repair routing, and release-boundary rules |
| /e2e-test | pass_with_minor_flags | E2E-001 completed through /handoff-export and produced `ev4-e2e-test-report@1.0.0`; textual fixture limitation remains as medium non-blocking flag |

---

## Active Hardening / Contract Files

- 02_PROJECT_INSTRUCTIONS_ACTIVE_OVERRIDES.md
- contracts/STAGE_ANCHOR_CONTRACT.md
- contracts/PARTIAL_RERUN_CONTRACT.md
- contracts/BUILD_TREE_NAMING_AND_STRUCTURE_CONTRACT.md
- diagnostics/LLM_DEBUG_TRACE_CONTRACT.md
- references/ELEMENTOR_KNOWLEDGE_BASE_RAG_STRATEGY.md
- knowledge/TUYA_ELEMENTOR_V4_CONCEPTS.md
- experiments/END_TO_END_PIPELINE_TEST_PLAN.md
- experiments/E2E-001-smart-home-connector-fixture.md
- experiments/E2E-001-test-report.md
- stages/02_RESEARCH.md
- stages/04_SCORE_EVIDENCE_v1.3_HARDENING_PATCH.md
- stages/05_SCORE_AUDIT_v1.1_HARDENING_PATCH.md
- stages/05_SCORE_AUDIT_v1.2_HARDENING_PATCH.md
- stages/06_RECOMMEND.md
- stages/06_RECOMMEND_v1.1_HARDENING_PATCH.md
- stages/07_BUILD_TREE.md
- stages/08_IMPLEMENTATION.md
- stages/09_FINAL_AUDIT.md
- stages/10_HANDOFF_EXPORT.md
- examples/scoring/README.md
- examples/scoring/SCORING-CAL-001-contradicted-evidence.md
- examples/scoring/SCORING-CAL-002-absent-vs-contradicted.md
- examples/scoring/SCORING-CAL-003-arithmetic-needs-audit.md
- examples/scoring/SCORING-CAL-004-overlay-na.md

---

## Hardened Stage / Validation / Strategy Files

- stages/02_RESEARCH.md
- references/ELEMENTOR_KNOWLEDGE_BASE_RAG_STRATEGY.md
- stages/08_IMPLEMENTATION.md
- stages/09_FINAL_AUDIT.md
- stages/10_HANDOFF_EXPORT.md
- experiments/END_TO_END_PIPELINE_TEST_PLAN.md
- experiments/E2E-001-test-report.md

---

## Scaffolded / Draft / Validation Work Remaining

- `knowledge/TUYA_ELEMENTOR_V4_CONCEPTS.md` remains `active_reference v0.2.0`; it is now the next highest-priority unfinished source-policy-adjacent contract because the active RAG Strategy depends on strict TUYA source classification.
- E2E-001 used a realistic textual mockup, not a raster screenshot.
- Pixel-accurate screenshot interpretation remains unvalidated by E2E-001.
- Real Elementor export JSON / EDIS validation remains future work.
- Live Elementor/browser rendering remains future work.

---

## RAG Strategy Contract Result

```yaml
RAG_STRATEGY_CONTRACT:
  file: references/ELEMENTOR_KNOWLEDGE_BASE_RAG_STRATEGY.md
  status: active_v1.0.0
  version: 1.0.0
  strategy_schema: ev4-rag-strategy-contract@1.0.0
  aligned_with:
    - stages/02_RESEARCH.md
    - ev4-research-payload@1.0.0
    - contracts/STAGE_ANCHOR_CONTRACT.md
    - contracts/PARTIAL_RERUN_CONTRACT.md
    - diagnostics/LLM_DEBUG_TRACE_CONTRACT.md
  confirmed_capabilities:
    - current pipeline Stage Source Access Matrix
    - `/research` as source-pinning owner
    - source class taxonomy
    - source pin schema
    - retrieved fact schema
    - downstream permission defaults
    - official source freshness policy
    - EDIS/export evidence boundary
    - conflict lifecycle
    - unsupported claim and unknown policy
    - forbidden leakage probes
    - repair routes
    - RAG strategy payload schema
    - self-audit
    - EV4 debug trace addendum
    - NEXT WORK ANCHOR to `/tuya-concept-reference`
```

Strict boundary:

```text
RAG may ground platform capability claims.
RAG must not infer screenshot content, select architecture, improve scores, break ties, soften final-audit defects, or clean up handoff risks.
```

Current stage-source correction:

```text
/research is Stage 2 and owns source pinning.
/decompose is Stage 3 and must use only visible/provided evidence for visual grouping.
```

---

## Research Contract Result

```yaml
RESEARCH_CONTRACT:
  file: stages/02_RESEARCH.md
  status: confirmed_hardened_v1.0.0
  stage_version: 1.0.0
  payload_schema: ev4-research-payload@1.0.0
  confirmed_capabilities:
    - input gate
    - source access policy
    - source pinning
    - retrieved fact ledger
    - unknown and unsupported claim register
    - conflict register
    - downstream source permission map
    - repair routes
    - regression cases
    - self-audit
    - EV4 debug trace addendum
    - NEXT STAGE ANCHOR to /decompose
```

Strict boundary:

```text
/research may prove or disprove platform capability.
/research must not decide what the current screenshot visually contains.
/research must not score, recommend, build, implement, or audit the section.
```

---

## E2E-001 Result

```yaml
E2E_TEST_REPORT:
  schema: ev4-e2e-test-report@1.0.0
  test_id: E2E-001
  fixture: experiments/E2E-001-smart-home-connector-fixture.md
  fixture_type: realistic_mockup_description
  e2e_status: pass_with_minor_flags
  stages_completed:
    - /intake
    - /decompose
    - /architectures
    - /score-evidence
    - /score-audit
    - /recommend
    - /build-tree
    - /implementation
    - /final-audit
    - /handoff-export
  first_failure_stage: null
  release_blocker_removed: yes
  release_blocker_scope: prompt-pack full-pipeline E2E contract
  source_access_violations: []
  blocker_findings: []
  high_findings: []
  medium_findings:
    - E2E001-MED-001: textual fixture cannot validate pixel-accurate screenshot interpretation or exact visual matching
  low_findings:
    - E2E001-LOW-001: exact token values remain unknown
    - E2E001-LOW-002: exact icon source/library remains unknown
    - E2E001-LOW-003: animation requirement remains unknown
    - E2E001-LOW-004: dynamic dashboard data requirement remains unknown
```

Release boundary interpretation:

```text
The previous release blocker requiring one passing E2E test is removed for the prompt-pack full-pipeline contract because E2E-001 reached /handoff-export, preserved anchors/payloads/unknowns/flags, and left no blocker/high finding.

This does not claim pixel-accurate screenshot interpretation, live Elementor rendering, or real export JSON validation. Those remain future validation tracks.
```

---

## Stage Anchor v1.1 Notes

A Stage Anchor is required before starting each stage after `/intake`.

Required v1.1 fields include:

- `target_stage_hardening_status`
- `confidence_delta`
- `partial_rerun_state`

Purpose:

- preserve critical unknowns;
- preserve blockers and gate results;
- record whether confidence increased, decreased, stayed unchanged, or was resolved;
- prevent running scaffolded/draft stages as production output without explicit approval;
- preserve invalidation triggers for partial reruns;
- prevent long-context drift;
- keep handoffs compact and auditable.

The anchor is an external structured handoff, not hidden reasoning.

---

## Partial Rerun Notes

If only one input changes, the assistant must not automatically rerun the full pipeline.

It must first produce a `PARTIAL RERUN PLAN` that identifies:

- changed input;
- earliest safe rerun stage;
- reusable stages;
- invalidated downstream stages;
- required payloads;
- required confirmation if the rerun depends on a missing decision.

---

## Knowledge Base / RAG Notes

A structured Elementor knowledge base may support `/research`, `/architectures`, `/build-tree`, `/implementation`, and `/final-audit`, but only within the active RAG Strategy v1.0.0 source-access matrix.

Core distinction:

```text
platform_capability ≠ project-specific behavior
```

Key gates:

- `/research` retrieves and pins sources; it does not interpret screenshots.
- `/decompose` uses only image/user-provided evidence and must not use RAG to invent visual groups.
- `/architectures` may use TUYA concepts and official docs only to verify architecture feasibility.
- `/score-evidence` must score from Rubric + Stage 3/4 evidence; TUYA/RAG cannot boost scores by themselves.
- `/recommend` must recommend only from audited Stage 5/6 outputs; no new RAG preference signals.
- `/build-tree`, `/implementation`, and `/final-audit` may use approved source facts only within their stage boundaries.
- `/handoff-export` may package source ledgers and flags but must not change decisions.
- `/e2e-test` must probe for RAG leakage across all stages.

---

## TUYA Internal Concept Reference Notes

The TUYA workbook is treated as an internal conceptual reference, not as official Elementor documentation.

Current TUYA file:

```yaml
TUYA_CONCEPT_REFERENCE:
  file: knowledge/TUYA_ELEMENTOR_V4_CONCEPTS.md
  status: active_reference_v0.2.0
  next_action: harden_to_v1.0.0
```

Required classification:

```text
source_type: internal_concept_reference
fact_class: project_conceptual_model
```

TUYA may guide vocabulary, thinking order, normal-flow discipline, relative visual stage logic, responsive caution, design-system mindset, and DOM/audit checklisting. It may not prove platform capability, raise Stage 5 scores directly, break Stage 7 ties, or override official docs/export evidence.

---

## Stage 8 — /implementation Hardening Notes

Stage 8 is confirmed as a hardened contract, not a scaffold.

Important limitation:

```text
Stage 8 hardening confirms the prompt contract. It does not replace a real pipeline run.
```

---

## Stage 9 — /final-audit Hardening Notes

Stage 9 is confirmed as a hardened contract, not a scaffold.

Important limitation:

```text
Stage 9 hardening confirms the final-audit prompt contract. It does not mean every future real implementation has passed final audit.
```

---

## Stage 10 — /handoff-export Hardening Notes

Stage 10 is confirmed as a hardened contract, not a scaffold.

Important limitation:

```text
Stage 10 hardening confirms the handoff-export prompt contract. It does not mean a future real EV4 run can skip final audit or E2E validation.
```

---

## E2E Test Notes

E2E-001 passed with minor flags.

Validated:

- full stage sequence through `/handoff-export`;
- Stage Source Access Matrix discipline;
- Stage Anchor v1.1 continuity;
- Debug Trace compatibility;
- unknown propagation;
- Stage 4 arithmetic / N/A / unknown handling;
- Stage 5 audit behavior;
- Stage 6 recommendation gate;
- Stage 7 editability and tree readability;
- Stage 8 exact-value restraint and scoped CSS map;
- Stage 9 blocker/high behavior;
- Stage 10 audit-flag preservation.

Not validated by E2E-001:

- pixel-accurate raster screenshot interpretation;
- live Elementor rendering;
- real Elementor export JSON;
- browser/device QA.

---

## Current Next Step

Preferred next action:

```text
Harden knowledge/TUYA_ELEMENTOR_V4_CONCEPTS.md from active_reference v0.2.0 to active_v1.0.0.
```

The next run should align TUYA with RAG Strategy v1.0.0 and `stages/02_RESEARCH.md` by adding or tightening:

- `source_type: internal_concept_reference` naming consistency;
- `fact_class: project_conceptual_model` enforcement;
- TUYA-specific downstream permission matrix;
- provisional/unknown/contradicted evidence lifecycle;
- forbidden capability/scoring/recommendation leakage probes;
- repair routes for TUYA misuse;
- self-audit;
- debug trace and Stage Anchor handoff references.
