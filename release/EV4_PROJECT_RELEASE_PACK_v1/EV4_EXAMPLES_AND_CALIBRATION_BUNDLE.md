# EV4 Examples and Calibration Bundle

Status: release_candidate_for_controlled_use
Version: 1.0.0

---

## Decomposition Example Bank

Use examples as calibration references, not as templates to copy.

Active decomposition patterns include:

```text
EX-DCP-001 — Smart Home Connector Section
EX-DCP-002 — Split Hero with Dashboard Mockup
EX-DCP-003 — Services / Feature Cards Grid
EX-DCP-004 — Pricing Cards
EX-DCP-005 — Testimonial Cards / Carousel
EX-DCP-006 — Logo Strip / Partner Grid
EX-DCP-007 — CTA Band
EX-DCP-008 — FAQ Accordion
EX-DCP-009 — Stats / Metrics
EX-DCP-010 — Product / Portfolio Grid
EX-DCP-011 — Process Timeline
EX-DCP-012 — Overlapping Floating Cards
```

Rules learned from examples:

```text
Visual Core is not automatically decorative.
Decoration is not meaningful content unless evidence says so.
Repeated visual group is not automatically Dynamic Loop.
Interactive state cannot be inferred from a static screenshot.
Mobile connector behavior must remain unknown unless specified.
```

---

## Scoring Calibration Cases

Active scoring calibration patterns:

```text
SCORING-CAL-001 — contradicted evidence
SCORING-CAL-002 — absent vs contradicted evidence
SCORING-CAL-003 — arithmetic needs-audit
SCORING-CAL-004 — overlay N/A
```

Core scoring lessons:

```text
ABSENT_EVIDENCE → ? / missing evidence, not penalty by itself.
CONTRADICTED_EVIDENCE → low score, fail, blocker, or repair route.
N/A removes criterion weight from denominator.
If arithmetic tool is not available, mark arithmetic confidence needs_audit.
```

---

## Screenshot Validation Calibration

E2E-002 validated a real smart-home connector hero screenshot.

Observed visual structure:

```text
central house visual core
six repeated feature cards
thin connector-line decoration layer
icon + title + subtitle per card
wide desktop layout
```

Correct interpretation:

```text
Feature text is meaningful and editable.
Connector lines are decorative/overlay candidates.
House is visual core; accessibility role remains context-dependent.
Icons are context-dependent: decorative or semantic depending on accessibility decision.
Mobile behavior is unknown from desktop-only screenshot.
```

Wrong interpretation:

```text
Do not flatten entire section to one image.
Do not make feature titles part of SVG/HTML-only decoration.
Do not assume connector lines stay visible on mobile.
Do not use TUYA/RAG to invent non-visible visual groups.
```

---

## Regression Prompts

Use these to test the system:

```text
1. Here is a screenshot. Run /decompose only. Do not propose architecture yet.
2. Run /architectures from this Decomposition Snapshot. Include coverage matrix.
3. Score candidates with ? for unknowns. Do not invent mobile behavior.
4. Audit the scoring. Check for hidden recommendation and N/A misuse.
5. Recommend only from audited eligible candidates.
6. Build the Elementor tree using the naming convention.
7. Produce implementation plan. No exact CSS values unless explicitly specified.
8. Final audit. Do not repair, only route defects.
9. Export handoff. Preserve all flags.
```
