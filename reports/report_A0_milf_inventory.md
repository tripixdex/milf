# A0 — MILF Inventory + Feasibility Audit + Reuse Map + Execution Strategy

## Scope ID and name
- `A0 — MILF Inventory + Feasibility Audit + Reuse Map + Execution Strategy`

## Objective
- Open the `milf` repository as a disciplined subject-box foundation, map the uploaded archive, choose the first MVP lab, freeze the initial execution strategy, and define what should and should not be reused from `berchun`.

## Trusted inputs used
- `Лаб PSS.zip`
- `Лаб PSS/Otchet.docx`
- `Лаб PSS/1.Модель изделия/Исходные данные задания.doc`
- `Лаб PSS/1.Модель изделия/МУ_Модель изделия.doc`
- `Лаб PSS/3-4.Управление изменениями/МУ_Управление изменениями.doc`
- `Лаб PSS/Автоматизация ЖЦП-2009-12/Работа со справочниками.rtf`
- `berchun/README.md`
- `berchun/reports/master_report.md`

## Files created
- `README.md`
- `master_report.md`
- `docs/MILF_BRANCH_PLAN.md`
- `docs/LAB_MAP.md`
- `docs/SOFTWARE_COMPAT.md`
- `docs/REUSE_FROM_BERCHUN.md`
- `docs/EXECUTION_STRATEGY.md`
- `reports/report_A0_milf_inventory.md`

## Files updated
- none

## Archive inventory summary
- The archive contains a legacy PSS platform package plus lab materials, not a narrow standalone lab utility.
- Three main thematic blocks are visible:
  - `1.Модель изделия`
  - `3-4.Управление изменениями`
  - `Автоматизация ЖЦП-2009-12`
- `Otchet.docx` is a sample report and explicitly corresponds to `Лабораторная работа №1`.
- The archive also contains Windows executable surface, CAD files, document templates, and example assets.
- A preexisting root `milf/report.md` was not used as a trusted source because it makes claims beyond the currently verified archive surface.

## Proposed MVP target lab and why
- `Lab 1 — Модель изделия`
- Why:
  - bounded compared with workflow-change labs,
  - has assignment source and methodical guide,
  - already has a sample report,
  - likely establishes the product/document model required by later labs.

## Reuse map from `berchun`
- Reuse:
  - narrow scope discipline,
  - `master_report` governance,
  - audit-first corrections,
  - canonical truth separation,
  - explicit supported-behavior documentation.
- Redesign:
  - no solver-first assumptions,
  - no blind Mac-native execution assumptions,
  - no early one-button UX before Windows-host evidence exists.

## Initial execution strategy
- Mac is the canonical repo and control plane.
- Windows is the likely execution host for the legacy PSS runtime.
- MVP should start as cross-platform core plus Windows execution adapter, with semi-automatic operator mode where direct automation is not yet justified.
- Compatible reimplementation is explicitly deferred behind later evidence.

## Main technical risks
- Windows-only runtime dependencies may be broader than a single executable.
- The MVP lab may still depend on server/database setup not visible from archive-only inspection.
- CAD and document integrations may block naive automation.
- The archive shows a platform-sized surface, so premature rewrite assumptions would be unsafe.
- Some repo-local preexisting notes already describe a wider lab set than what was actually verified in the uploaded archive. Those notes must not be treated as source-of-truth without renewed evidence.

## Ready for A1? YES/NO
- `YES`

## Exact next recommendation
- Open `A1 — Windows Host Validation + Manual Runbook Capture for Lab 1` and keep it strictly execution-evidence-first: verify how `pss_4_353.exe` is actually launched and used, what host dependencies exist, and which exact Lab 1 steps and exports can be reproduced on a Windows machine.
