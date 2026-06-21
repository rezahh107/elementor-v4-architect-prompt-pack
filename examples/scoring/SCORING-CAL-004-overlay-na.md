# SCORING-CAL-004 — Overlay Containment N/A

## Purpose

Teach Stage 4 that a criterion can be non-applicable without becoming a high score.

## Synthetic Input

Stage 2 describes a normal-flow feature card grid.

There are no overlay, connector, floating, absolute, z-index, or decorative layer candidates.

Stage 3 proposes a normal-flow grid architecture and does not introduce overlay strategy.

## Correct Scoring Behavior

| Criterion | Expected Score | Evidence Label | Denominator Behavior |
|---|---:|---|---|
| Overlay Containment | `N/A` | `NON_APPLICABLE` | Exclude weight `2` |

Correct formula:

```text
applicable_weight_total = 25 - 2
applicable_raw_max = 23 * 5
```

## Common Mistakes

```text
Overlay Containment = 5 for a section with no overlays.
Overlay Containment = ? when the criterion is clearly non-applicable.
Keeping the overlay weight in the denominator after marking N/A.
```

## Expected Audit Trigger

```text
stage_5_spot_check_triggers:
- na_denominator_check
```
