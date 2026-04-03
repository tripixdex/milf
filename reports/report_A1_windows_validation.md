# A1 — Windows Host Validation + Manual Runbook Capture for Lab 1

## Scope ID and name
- `A1 — Windows Host Validation + Manual Runbook Capture for Lab 1`

## Objective
- Validate the real host/runtime boundary for Lab 1 on Windows and capture the smallest truthful manual runbook without opening automation or wrapper work prematurely.

## Trusted inputs used
- `README.md`
- `master_report.md`
- `docs/MILF_BRANCH_PLAN.md`
- `docs/LAB_MAP.md`
- `docs/SOFTWARE_COMPAT.md`
- `docs/REUSE_FROM_BERCHUN.md`
- `docs/EXECUTION_STRATEGY.md`
- `reports/report_A0_milf_inventory.md`
- `Лаб PSS/pss_4_353.exe`
- `Лаб PSS/1.Модель изделия/МУ_Модель изделия.doc`
- `Лаб PSS/Otchet.docx`

## Files created
- `docs/WINDOWS_RUNBOOK_LAB1.md`
- `docs/WINDOWS_DEPENDENCIES.md`
- `docs/OBSERVED_EXPORT_SURFACES.md`
- `reports/report_A1_windows_validation.md`

## Files updated
- `master_report.md`

## Windows host and environment summary
- Actual host used in this scope:
  - macOS `26.2`
  - `arm64`
  - no Windows VM tooling
  - no Wine
  - no remote-desktop path to a Windows machine
- Real Windows host execution was therefore not reached in this scope.

## What was actually verified
- `pss_4_353.exe` is a Windows `PE32` NSIS installer.
- No local Windows execution bridge or Windows host path was available.
- The Lab 1 methodical guide documents a three-level PSS architecture involving Oracle server/client components plus a PSS client module.
- The Lab 1 methodical guide documents the user-facing workflow sequence for product creation, structure formation, characteristic attachment, linked documents, search, HTML export, full-composition report, specification, and calculation.
- `Otchet.docx` confirms that Lab 1 outputs are expected to include:
  - structure
  - characteristics
  - document bindings
  - full composition
  - specification
  - mass and cost results

## What was attempted but not verified
- Real installer launch on Windows.
- Actual installation completion.
- Login / working database selection on a live host.
- Whether a self-contained local demo DB exists.
- Whether Oracle/server prerequisites are mandatory in the actual deployment used for the labs.
- Live export dialogs and output file generation from the PSS runtime.

## Manual runbook summary for Lab 1
- Truthfully captured now:
  - preflight stops at the host boundary
  - the current environment can only confirm installer type and absence of a Windows path
- Documented but not yet host-verified runtime path:
  - launch `Модуль PDM` from `Пуск -> Программы -> PDM STEP Suite -> Настройка -> Модуль PDM`
  - identify user and select working DB
  - configure dictionaries / units / characteristics / document types
  - create products and versions
  - build product structure
  - attach characteristics and linked documents
  - search DB and save results
  - generate full composition and specification
  - calculate mass/cost

## Main blockers / constraints
- No accessible Windows execution host existed in the current environment.
- No local virtualization or compatibility layer was available.
- The methodical guide suggests broader Oracle/database setup, so Lab 1 must not yet be treated as a guaranteed single-client-only path.
- CAD/workflow breadth exists in the platform surface even if the MVP target remains Lab 1.

## Is A2 justified? YES/NO
- `NO`

## Exact next recommendation
- Open `A1B — Real Windows Host Access + First Launch Evidence Capture`.
- Keep it narrow:
  - run `pss_4_353.exe` on an actual Windows machine,
  - capture installer screens and installation result,
  - record whether admin rights are required,
  - record whether a database/server is already available or must be provisioned,
  - capture the first reachable live Lab 1 screens and the first real export/save surfaces.
