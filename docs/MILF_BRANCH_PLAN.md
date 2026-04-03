# MILF Branch Plan

## Project Purpose
Build a disciplined repository around PSS-based laboratory works without pretending the legacy platform can be replaced immediately. The repository must become safe for staged execution, evidence capture, and later bounded automation.

## MVP Target Lab
- `Lab 1 — Модель изделия`
- Why first:
  - It has a clear assignment source document.
  - It has a dedicated methodical guide.
  - It already has a sample report.
  - Its workflow is narrower than change-management labs.
  - It establishes the product/document model that later labs appear to build upon.

## Roadmap
- `A0` — inventory, feasibility audit, reuse map, execution strategy.
- `A1` — Windows host validation and manual runbook capture for Lab 1.
- `A2` — canonical raw input and evidence schema for Lab 1.
- `A3` — semi-automatic artifact capture boundary for Lab 1.
- `A4` — normalized report/data assembly for Lab 1 outputs.
- `A5` — operator-safe execution wrapper around the Windows-host path.
- `A6` — multi-variant hardening for Lab 1.
- `A7` — feasibility gate for Labs 3–4 change-management workflows.
- `A8` — decision review on long-term adapter vs compatible reimplementation.

## Architecture Direction
- Use a cross-platform core for repository truth, inputs, evidence, normalization, and reporting.
- Use a Windows execution adapter for the legacy PSS runtime.
- Keep manual operator steps explicit until they are bounded by real evidence.

## Decision Gate
- Prefer `Windows execution adapter` when the legacy path is stable, host-dependent, and outputs can be captured reliably.
- Prefer `semi-automatic operator mode` when the workflow needs UI judgment, CAD review, or platform steps that are too brittle to wrap immediately.
- Consider `compatible reimplementation` only when:
  - the required lab subset is narrow,
  - repeated runs expose a stable and documented behavior set,
  - proprietary platform subsystems can be avoided,
  - required outputs can be reproduced without COM/CAD/workflow engine dependencies.
