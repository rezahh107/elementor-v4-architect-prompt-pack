# STATUS — Elementor V4 Architect Prompt Pack

Version: 0.7.0
Status: in_progress
Last confirmed stage: Stage 6 — /recommend
Current next stage: Stage 7 — /build-tree hardening
Language: Persian reports, English technical labels allowed

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

## Stage Status

| Stage | Status | Notes |
|---|---|---|
| /intake | confirmed | Lightweight default-based intake |
| /research | draft_required | Needs source policy and version-pinned source rules |
| /decompose | confirmed_with_example_bank | Controlled Visual Role Decomposition with 12 examples |
| /decomposition-example-bank | active_enhanced | Pattern-based examples plus authoring standard |
| /architectures | confirmed_hardened_v1.1.0 | Coverage matrix, unknown propagation, recommendation ban, dynamic guardrails |
| /score-evidence | confirmed_hardened_v1.3.0_patch | Uses rubric 1.3 and Stage 4 v1.3 hardening patch |
| /score-audit | confirmed_hardened_v1.2.0_patch | Adds Stage 5 self-audit, hidden recommendation guard, tie handoff, responsive cap reference binding |
| /scoring-calibration-bank | active | examples/scoring calibration cases added |
| /recommend | confirmed_hardened_v1.1.0_patch | Adds recommendation basis matrix, provenance ledger, strict tie handling, build-tree readiness gate, and debug record |
| /stage-anchor-contract | active | contracts/STAGE_ANCHOR_CONTRACT.md added; all future stages must start from an anchor |
| /debug-trace-contract | active | Model-readable external trace contract; no hidden chain-of-thought dependency |
| /build-tree | draft_scaffolded | Stage 7 scaffold created; needs hardening |
| /implementation | draft_scaffolded | Stage 8 scaffold created; needs hardening |
| /final-audit | draft_scaffolded | Stage 9 scaffold created; needs hardening |
| /handoff-export | draft_scaffolded | Stage 10 scaffold created; needs hardening |

## Active Hardening / Contract Files

- contracts/STAGE_ANCHOR_CONTRACT.md
- diagnostics/LLM_DEBUG_TRACE_CONTRACT.md
- stages/04_SCORE_EVIDENCE_v1.3_HARDENING_PATCH.md
- stages/05_SCORE_AUDIT_v1.1_HARDENING_PATCH.md
- stages/05_SCORE_AUDIT_v1.2_HARDENING_PATCH.md
- stages/06_RECOMMEND.md
- stages/06_RECOMMEND_v1.1_HARDENING_PATCH.md
- examples/scoring/README.md
- examples/scoring/SCORING-CAL-001-contradicted-evidence.md
- examples/scoring/SCORING-CAL-002-absent-vs-contradicted.md
- examples/scoring/SCORING-CAL-003-arithmetic-needs-audit.md
- examples/scoring/SCORING-CAL-004-overlay-na.md

## Scaffolded Stage Files

- stages/07_BUILD_TREE.md
- stages/08_IMPLEMENTATION.md
- stages/09_FINAL_AUDIT.md
- stages/10_HANDOFF_EXPORT.md

## Stage Anchor Notes

A Stage Anchor is now required before starting each stage after `/intake`.

Purpose:

- preserve critical unknowns;
- preserve blockers and gate results;
- prevent long-context drift;
- keep handoffs compact and auditable;
- avoid reliance on conversational memory alone.

The anchor is not hidden chain-of-thought. It is an external structured handoff.

## Stage 5 v1.2 Notes

Stage 5 now has these additional constraints before Stage 6:

- It must audit its own audit report for hidden recommendation leakage.
- It must keep candidate reporting neutral and avoid implied preference.
- It must emit a tie handoff payload instead of breaking ties.
- It must bind responsive inheritance audits to the authoritative Stage 4/rubric rule.
- It must emit `ev4-score-audit-payload@1.2.0` when the v1.2 patch is active.

## Stage 6 v1.1 Notes

Stage 6 is the first stage allowed to recommend an architecture, but v1.1 makes the recommendation process stricter.

It may run only after Stage 5 returns `pass` or `pass_with_minor_flags`.

It must:

- select only from audit-eligible candidates;
- never override failed gates or Stage 5 findings;
- emit a neutral Recommendation Basis Matrix before selection;
- use a Recommendation Provenance Ledger for every recommendation reason;
- run strict tie handling when Stage 5 emits `selection_ambiguity_flag` or candidates are close;
- avoid subjective or hidden-ranking language outside allowed recommendation sections;
- carry forward unresolved flags and required confirmations;
- block `/build-tree` when confirmations, blockers, or unresolved decision requirements remain;
- emit `ev4-recommend-payload@1.1.0`;
- emit `ev4-recommend-debug-record@1.0.0`.

## Debug Trace Contract Notes

The debug trace layer is active as `diagnostics/LLM_DEBUG_TRACE_CONTRACT.md`.

It does not reveal hidden chain-of-thought. It requires each stage, when debug mode is requested, to externalize a compact trace of:

- inputs received and missing;
- decisions made;
- evidence used;
- unknowns propagated;
- rules applied;
- failure symptoms;
- repair route;
- handoff payload schema.

This allows a model-language debugger to find the first broken stage and propose a minimal repair patch.

## Current Next Step

Harden Stage 7 — /build-tree, including final naming convention, wrapper budget, widget constraints, and Elementor Structure Panel tree contract.
