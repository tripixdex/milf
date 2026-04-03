# milf

## Purpose
`milf` is the canonical repository for laboratory works based on the legacy PSS platform package from `Лаб PSS.zip`. The repository is opened as a disciplined subject-box foundation, not as an immediate automation rewrite.

## Current Status
- Status: foundation opened, inventory frozen.
- Active scope: `A0 — MILF Inventory + Feasibility Audit + Reuse Map + Execution Strategy`.
- MVP target: `Lab 1 — Модель изделия`.
- Implementation status: no runtime automation yet.

## Current Stage
- Archive inventory is mapped.
- The first MVP lab is chosen.
- Reuse rules from `berchun` are documented.
- Windows-host execution strategy is frozen.

## Architecture Direction
- Mac: canonical repo, control plane, evidence store, input normalization, reports, future cross-platform core.
- Windows: likely execution host for the legacy PSS executable and platform-dependent workflows.
- MVP path: cross-platform core plus Windows execution adapter, with semi-automatic operator steps where direct automation is not yet justified.

## Role Separation
- Mac owns repository truth, planning, extracted evidence, and future operator-safe wrappers.
- Windows owns actual legacy platform execution until proven otherwise.
