# RN1 — MILF Repository Normalization + Contracts Skeleton

## Scope ID and name
- `RN1 — MILF Repository Normalization + Contracts Skeleton`

## Objective
- Normalize the `milf` repository surface so canonical evidence remains tracked, runtime-heavy payload stays local-only, and early contracts are frozen before opening the next execution pass.

## Trusted inputs used
- `README.md`
- `master_report.md`
- `reports/report_A0_milf_inventory.md`
- `reports/report_A1_windows_validation.md`
- `reports/report_A1B_first_launch.md`
- `docs/MILF_BRANCH_PLAN.md`
- `docs/LAB_MAP.md`
- `docs/SOFTWARE_COMPAT.md`
- `docs/REUSE_FROM_BERCHUN.md`
- `docs/EXECUTION_STRATEGY.md`
- `docs/WINDOWS_RUNBOOK_LAB1.md`
- `docs/WINDOWS_DEPENDENCIES.md`
- `docs/OBSERVED_EXPORT_SURFACES.md`
- `docs/WINDOWS_SCREEN_EVIDENCE.md`
- `docs/KNOWN_LIMITATIONS.md`
- current repo layout and tracked surface

## Files created
- `contracts/INPUT_CONTRACT.md`
- `contracts/EVIDENCE_CONTRACT.md`
- `contracts/REPORT_CONTRACT.md`
- `contracts/ARTIFACT_POLICY.md`
- `reports/report_RN1_repo_normalization.md`

## Files updated
- `.gitignore`
- `README.md`
- `master_report.md`

## What was normalized
- Expanded `.gitignore` from archive-only ignores to explicit OS/editor plus local runtime payload boundaries.
- Added `contracts/` as a minimal, non-empty governance surface for input, evidence, report, and artifact policy.
- Made canonical repo surface explicit in `README.md`.
- Updated `master_report.md` so the repo no longer looks frozen at pre-A1B status.
- Kept the existing `artifacts/a1b/` structure as the canonical tracked evidence location instead of introducing a new evidence tree.
- No file moves or renames were required in this pass.

## What was intentionally left local-only
- `Лаб PSS.zip`
- `Лаб PSS/`
- `_pss_payload_extracted/`
- `_pss_install_probe/`
- future installer payloads and install probes
- local OS/editor/runtime byproducts
- `_pss_payload_extracted/` and `_pss_install_probe/` are not present in the current Mac clone, but they are now pre-classified as local-only names so later Windows-side sync does not accidentally promote them into canonical repo truth.

## Current canonical repo surface
- `.gitignore`
- `README.md`
- `master_report.md`
- `docs/*.md`
- `reports/*.md`
- `artifacts/a1b/*.png`
- `contracts/*.md`

## Current local-only runtime surface
- ignored vendor/runtime payload and extracted lab package
- future local install probes and unpacked executables
- local byproducts not reviewed as scope evidence
- inspected but absent in the current repo surface:
  - `report.md`
  - `GENERIC_CODEX_SYSTEM_PROMPT.md`

## What contracts were frozen now
- `INPUT_CONTRACT.md`
- `EVIDENCE_CONTRACT.md`
- `REPORT_CONTRACT.md`
- `ARTIFACT_POLICY.md`
- These are skeletons only: they define purpose, what is already known, and what remains intentionally unbound.

## What was validated
- The repo tree remains coherent after adding `contracts/`.
- `.gitignore` now classifies:
  - `.DS_Store`
  - `Лаб PSS.zip`
  - `Лаб PSS/`
  - `_pss_payload_extracted/`
  - `_pss_install_probe/`
- Canonical A1B evidence still exists under `artifacts/a1b/`.
- The working tree changes introduced by RN1 are documentation-only and contract-only; no code or automation files were added.

## Ready for A1C? YES/NO
- `YES`

## Exact next recommendation
- Open `A1C — Connected Lab 1 Session + First Structured Capture` and keep it narrow:
  - use the normalized repo as control plane,
  - keep vendor/runtime payload local-only,
  - capture the first connected Lab 1 object/session evidence without opening automation or broader wrapper work.
