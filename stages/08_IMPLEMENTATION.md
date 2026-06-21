# Stage 8 - /implementation

Status: draft_scaffolded
Version: 0.1.0
Payload schema: ev4-implementation-payload@0.1.0

Purpose: convert the approved /build-tree output into an implementation-ready Elementor configuration plan.

Required anchor: source_stage=/build-tree, target_stage=/implementation, selected tree, carried unknowns, confirmations, blockers, allowed tools.

Core rule: implement the approved tree without changing the architecture.

Allowed:
- Map containers and widgets to Elementor controls.
- Specify settings categories without overclaiming exact values.
- Define scoped CSS needs at a high level.
- Identify assets, alt requirements, and responsive settings to verify.
- Carry forward any unresolved confirmations.
- Emit NEXT STAGE ANCHOR for /final-audit.

Forbidden:
- No new architecture candidate.
- No recommendation override.
- No third-party plugin unless pre-approved.
- No invented asset or copy.
- No silent conversion of meaningful content into images.
- No hidden global CSS.

Output sections:
1. Input authorization
2. Elementor Settings Plan
3. Widget Mapping
4. Class and Variable Application Map
5. Scoped CSS Need Map
6. Asset and Accessibility Map
7. Responsive Settings Plan
8. Implementation Risks
9. Handoff to /final-audit
10. NEXT STAGE ANCHOR

Pass criteria: valid anchor, approved tree preserved, settings mapped, unknowns preserved, implementation risks listed, next anchor emitted.

Requires hardening: exact settings schema, asset schema, CSS scoping validator, responsive breakpoint examples.
