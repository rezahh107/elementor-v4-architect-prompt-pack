# Build Tree Naming and Structure Contract

Status: active
Version: 1.0.0
Applies to: Stage 7 — /build-tree

## Purpose

This contract defines how Stage 7 names Elementor Structure Panel nodes and class candidates.

The goal is to make the build tree readable to humans, traceable to the selected recommendation, and stable enough for Stage 8 implementation.

## Dual Naming Model

Every meaningful node should distinguish between:

```text
structure_label = human-readable Elementor Structure Panel label
class_name = machine-readable class candidate
```

Example:

```text
structure_label: Hero / Copy / Primary
class_name: hero__copy--primary
```

## Class Naming Pattern

Use:

```text
[section-role]__[content-group]--[variant]
```

Examples:

```text
hero__copy--primary
hero__cta--secondary
feature-grid__card--default
pricing__card--featured
smart-home__connector-layer--desktop
```

## Rules

- Class names must use lowercase Latin letters, numbers, and hyphens.
- Use `__` only between section/block and content group.
- Use `--` only for variant, state, or role distinction.
- Do not encode pixel values, coordinates, colors, or temporary implementation details.
- Do not use vague names such as `box-1`, `left`, `right`, `wrapper`, `nice`, `cool`, or `visual` by themselves.
- Do not create global class candidates for one-off coordinates.
- Repeated items should share the same base class.
- Variants must explain a real role/state difference, not visual taste.

## Structure Label Rules

Structure labels should be readable in Elementor Structure Panel.

Pattern:

```text
[Section] / [Group] / [Role or Variant]
```

Examples:

```text
Hero / Copy / Primary
Hero / Visual / Dashboard Mockup
Features / Card Grid
Features / Card / Default
Smart Home / Relative Stage
Smart Home / Connector Layer / Desktop
```

## Wrapper Budget Contract

Every wrapper must have a structural reason.

Allowed wrapper reasons:

```text
normal-flow grouping
responsive order control
overlay containment
decoration isolation
repeated component boundary
design-system reuse
widget-native requirement
accessibility/semantic grouping
```

Forbidden wrapper reasons:

```text
looks cleaner
maybe useful later
because Elementor needs it
styling only with no reusable role
unknown reason
```

## Required Build-Tree Tables

Stage 7 must produce:

1. Elementor Structure Panel Tree
2. Tree Node Table
3. Naming Map
4. Wrapper Justification Table
5. Content Editability Map
6. Overlay / Decoration Map
7. Responsive Structure Contract
8. Design-System Hook Map

## Failure Conditions

Fail Stage 7 if:

- a selected candidate is missing;
- class names do not follow this contract;
- structure labels are too vague for a human builder;
- one-child wrappers are not justified;
- meaningful content is placed into static SVG/HTML without explicit authorization;
- overlays are not contained in a named relative stage;
- unknowns from Stage 6 are dropped;
- Stage 8 anchor is missing.
