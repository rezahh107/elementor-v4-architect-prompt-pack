# SCORING-CAL-003 — Arithmetic Needs Audit

## Purpose

Teach Stage 4 and Stage 5 that language-model arithmetic is not enough for final scoring.

## Synthetic Input

A candidate has all criteria numeric and no `?`.

Stage 4 calculates weighted rows but does not use Python, calculator, spreadsheet, or another runtime.

## Correct Stage 4 Behavior

```text
arithmetic_confidence: needs_audit
raw_weighted_total: shown with formula
normalized_total: shown only if arithmetic is tool-verified; otherwise marked needs audit
```

## Correct Stage 5 Behavior

Stage 5 must recompute:

```text
raw_weighted_total = sum(score * weight)
normalized_total = raw_weighted_total / applicable_raw_max * 100
```

If a `?` exists:

```text
final_total: incomplete
provisional_known_percent: allowed only as non-final
```

## Wrong Behavior

```text
Do not accept Stage 4's arithmetic because it looks plausible.
Do not allow Stage 4 to self-certify math without a tool.
Do not compare incomplete candidates using provisional_known_percent.
```

## Expected Audit Trigger

```text
stage_5_spot_check_triggers:
- arithmetic_confidence_needs_audit
```
