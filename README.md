# milf

## Purpose
`milf` is the canonical repository for laboratory works based on the legacy PSS platform package from `Лаб PSS.zip`. The repository is opened as a disciplined subject-box foundation, not as an immediate automation rewrite.

## Current Status
- Status: foundation opened, first Windows evidence captured, repo surface normalized.
- Active scope: `RN1 — MILF Repository Normalization + Contracts Skeleton`.
- MVP target: `Lab 1 — Модель изделия`.
- Implementation status: no runtime automation yet.

## Current Stage
- Archive inventory is mapped.
- The first MVP lab is chosen.
- First live Windows runtime evidence from `A1B` is tracked.
- Canonical-vs-local runtime boundary is explicit.
- Contracts skeletons are frozen early.

## Architecture Direction
- Mac: canonical repo, control plane, evidence store, input normalization, reports, future cross-platform core.
- Windows: likely execution host for the legacy PSS executable and platform-dependent workflows.
- MVP path: cross-platform core plus Windows execution adapter, with semi-automatic operator steps where direct automation is not yet justified.

## Role Separation
- Mac owns repository truth, planning, extracted evidence, and future operator-safe wrappers.
- Windows owns actual legacy platform execution until proven otherwise.

## Canonical Repo Surface
- `README.md`, `master_report.md`
- `docs/`
- `reports/`
- `artifacts/a1b/`
- `contracts/`

## Local-Only Runtime Surface
- `Лаб PSS.zip`
- `Лаб PSS/`
- `_pss_payload_extracted/`
- `_pss_install_probe/`
- local OS/editor/runtime byproducts ignored by `.gitignore`
