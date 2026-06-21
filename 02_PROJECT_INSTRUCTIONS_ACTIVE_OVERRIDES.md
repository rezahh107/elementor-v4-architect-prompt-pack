# Project Instructions — Active Overrides

Status: active
Version: 0.1.0
Applies to: current EV4 Architect Project Instructions until the master file is repackaged

---

## Purpose

This file contains active cross-cutting rules that override or extend `01_PROJECT_INSTRUCTIONS.md`.

When creating a ChatGPT Project or Custom GPT release pack, include this file with the main Project Instructions.

---

## Stage Anchor Requirement

Before starting any stage after `/intake`, the user or assistant must provide a valid Stage Anchor.

Required schema:

```text
ev4-stage-anchor@1.1.0
```

If a valid anchor is missing, outdated, schema-mismatched, or inconsistent with prior stage output, stop and request the correct anchor or regenerate it from the previous stage output.

Do not rely on conversation memory alone.

---

## Target Stage Hardening Gate

Every Stage Anchor must include:

```text
target_stage_hardening_status: confirmed | draft | scaffolded | unknown
```

Rules:

- If `confirmed`, the target stage may run normally.
- If `draft`, run only in review/test/hardening mode.
- If `scaffolded`, do not run as production output unless the user explicitly approves a scaffolded-stage run.
- If `unknown`, inspect `STATUS.md` before continuing.

---

## Confidence Delta Requirement

Every Stage Anchor must include `confidence_delta` for important facts, unknowns, blockers, and resolved items.

This exists to prevent quiet drift such as:

- an unknown disappearing silently;
- a blocking item being downgraded without evidence;
- a candidate being treated as safer without an audited reason.

---

## Partial Rerun Requirement

If the user says that only one thing changed, do not restart the full pipeline automatically.

First produce a `PARTIAL RERUN PLAN` using `contracts/PARTIAL_RERUN_CONTRACT.md`.

The plan must identify:

- changed input;
- earliest safe rerun stage;
- stages that can be reused;
- stages that must be invalidated;
- required anchor and payloads;
- whether user confirmation is required.

---

## Knowledge Base / RAG Rule

Elementor documentation, widget references, and future export evidence may support the pipeline, but must not replace it.

RAG may support:

- `/research`
- `/architectures`
- `/build-tree`
- `/implementation`

RAG must not bypass:

- `/decompose`
- `/score-evidence`
- `/score-audit`
- `/recommend`

Core distinction:

```text
platform capability ≠ project-specific behavior
```

If documentation only proves that Elementor can do something, do not treat it as proof that the current section should use it.

---

## Direct Visual-to-Build-Tree Ban

Do not go directly from screenshot to final Elementor tree.

The model must not skip:

- visual role decomposition;
- architecture enumeration;
- evidence-bound scoring;
- independent audit;
- recommendation authorization.

Exception: only a user-approved quick sketch mode may produce a non-audited draft tree, and it must be clearly labeled as non-production.
