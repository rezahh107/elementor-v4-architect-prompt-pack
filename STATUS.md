# STATUS — Elementor V4 Architect Prompt Pack

Version: 0.1.0  
Status: in_progress  
Last confirmed stage: Stage 1 — `/intake`  
Language: Persian reports, English technical labels allowed  

---

## Confirmed Decisions

### System Architecture

- This project uses GPT Projects.
- The system is a prompt pipeline, not a single giant prompt.
- The GPT Project will contain:
  - Project Instructions / Master Prompt
  - Elementor V4 documentation files
  - Workbook methodology notes
  - Architecture scoring rubric
  - Few-shot examples
  - Calibration cases

### Pipeline

Current planned stages:

1. `/intake`
2. `/research`
3. `/decompose`
4. `/architectures`
5. `/score-evidence`
6. `/score-audit`
7. `/recommend`
8. `/build-tree`
9. `/implementation`
10. `/final-audit`

---

## Stage Status

| Stage | Status | Notes |
|---|---|---|
| `/intake` | confirmed | Lightweight default-based intake |
| `/research` | draft | Needs documentation source policy |
| `/decompose` | not_started | Needs output schema |
| `/architectures` | not_started | Needs architecture enumeration rules |
| `/score-evidence` | not_started | Needs Rubric v2 and evidence schema |
| `/score-audit` | not_started | Needs audit rules |
| `/recommend` | not_started | Depends on score audit |
| `/build-tree` | not_started | Needs naming convention |
| `/implementation` | not_started | Needs Elementor settings schema |
| `/final-audit` | not_started | Needs checklist |

---

## Confirmed Project Defaults

- Elementor V4
- Elementor Pro available
- Container/Flexbox-first workflow
- Structure Panel clarity matters
- Scoped Custom CSS allowed
- SVG Widget allowed
- HTML Widget allowed when practical
- No third-party plugin/add-on unless approved by the user
- Meaningful content should remain editable when practical
- Do not convert meaningful content into a single static image
- Primary content should remain in normal flow
- Absolute positioning only inside a clearly named relative Stage
- Decorative connector lines may use SVG and may be hidden or simplified on mobile
- Prefer one DOM across desktop, tablet, and mobile
- Avoid duplicate mobile-only sections unless strongly justified
- Use reusable classes for repeated visual patterns
- Use variables for repeated colors, spacing, radius, typography, and shadows when useful
- Do not create global classes for one-off coordinates
- Meaningful text must remain real text
- Images must be classified as meaningful or decorative
- DOM reading order should remain logical
- Avoid heavy full-image sections
- Avoid excessive wrappers
- Optimize large visual assets
- Reports and reasoning must be in Persian
- Elementor labels, class names, and technical terms may remain English

---

## Current Next Step

Define Stage 2 — `/decompose`.

Goal:
Create a fixed visual decomposition schema for Elementor V4 section analysis.
