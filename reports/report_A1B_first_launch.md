# A1B — Real Windows Host Access + First Launch Evidence Capture

## Scope ID and name

- `A1B`
- `Real Windows Host Access + First Launch Evidence Capture`

## Objective

Capture the first truthful Windows-side execution evidence for Lab 1:

- installer launch/install behavior
- first reachable runtime screens
- admin-rights and dependency evidence
- first actual export/save/report surfaces

## Trusted inputs used

Actually present and used:

- [`report.md`](/C:/Users/79004/OneDrive/Рабочий%20стол/study/8sem/milf/report.md)
- extracted runtime inventory under [`_pss_payload_extracted`](/C:/Users/79004/OneDrive/Рабочий%20стол/study/8sem/milf/_pss_payload_extracted)
- live Windows host observations from A1B commands and screenshots

Requested by scope but **not present** in the current workspace snapshot:

- `README.md`
- `master_report.md`
- `docs/MILF_BRANCH_PLAN.md`
- `docs/LAB_MAP.md`
- `docs/SOFTWARE_COMPAT.md`
- `docs/REUSE_FROM_BERCHUN.md`
- `docs/EXECUTION_STRATEGY.md`
- `docs/WINDOWS_RUNBOOK_LAB1.md`
- `docs/WINDOWS_DEPENDENCIES.md`
- `docs/OBSERVED_EXPORT_SURFACES.md`
- `reports/report_A0_milf_inventory.md`
- `reports/report_A1_windows_validation.md`
- original `Лаб PSS/pss_4_353.exe`
- Lab 1 methodical guide
- Lab 1 sample report

## Files created

- [`docs/WINDOWS_RUNBOOK_LAB1.md`](/C:/Users/79004/OneDrive/Рабочий%20стол/study/8sem/milf/docs/WINDOWS_RUNBOOK_LAB1.md)
- [`docs/WINDOWS_DEPENDENCIES.md`](/C:/Users/79004/OneDrive/Рабочий%20стол/study/8sem/milf/docs/WINDOWS_DEPENDENCIES.md)
- [`docs/OBSERVED_EXPORT_SURFACES.md`](/C:/Users/79004/OneDrive/Рабочий%20стол/study/8sem/milf/docs/OBSERVED_EXPORT_SURFACES.md)
- [`docs/WINDOWS_SCREEN_EVIDENCE.md`](/C:/Users/79004/OneDrive/Рабочий%20стол/study/8sem/milf/docs/WINDOWS_SCREEN_EVIDENCE.md)
- [`docs/KNOWN_LIMITATIONS.md`](/C:/Users/79004/OneDrive/Рабочий%20стол/study/8sem/milf/docs/KNOWN_LIMITATIONS.md)
- [`reports/report_A1B_first_launch.md`](/C:/Users/79004/OneDrive/Рабочий%20стол/study/8sem/milf/reports/report_A1B_first_launch.md)
- [`master_report.md`](/C:/Users/79004/OneDrive/Рабочий%20стол/study/8sem/milf/master_report.md)

## Files updated

- None

## Real Windows host summary

- Host OS: `Windows 10 Home Single Language`
- Build family: `19041`
- Current user token integrity: `Medium`
- Current user was not elevated during first runtime launch
- Admin-group membership was present only as deny-only in the observed token state

## What was actually launched

Successfully launched on the real Windows host:

- [`_pss_payload_extracted/PSM.exe`](/C:/Users/79004/OneDrive/Рабочий%20стол/study/8sem/milf/_pss_payload_extracted/PSM.exe)
- [`_pss_payload_extracted/ReportConstructor.exe`](/C:/Users/79004/OneDrive/Рабочий%20стол/study/8sem/milf/_pss_payload_extracted/ReportConstructor.exe)

Not launched:

- original installer `pss_4_353.exe`
  - reason: artifact not present in current workspace snapshot and not found in the parent tree search

## Whether installation completed

- `NO OBSERVATION`

Reason:

- installation could not be tested truthfully because the original installer artifact was absent

## Whether admin rights were required

- For first launches of `PSM.exe` and `ReportConstructor.exe`: `NO`, not observed as required
- For the original installer: `UNVERIFIED`

## Whether DB/server prerequisites blocked progress

- For reaching the first `PSM.exe` shell: `NO`
  - the shell opened in disconnected state

- For progressing meaningfully into Lab 1 object work: `YES / EFFECTIVELY BLOCKED IN A1B`
  - observed title: `Модуль PDM - [Соединение не установлено]`
  - no live DB/session connection was established

## First reachable Lab 1 runtime path

Observed path:

1. Launch [`_pss_payload_extracted/PSM.exe`](/C:/Users/79004/OneDrive/Рабочий%20стол/study/8sem/milf/_pss_payload_extracted/PSM.exe)
2. Reach window `Модуль PDM - [Соединение не установлено]`
3. See left-side shell tree:
   - `Мой рабочий стол`
   - `Папки`
   - `Справочники`
   - `Организационная структура`
   - `Поиск в БД`
4. Stop there because no validated DB/session connection was available

## First real exports/saves/screens captured

Screens captured:

- [`artifacts/a1b/a1b_psm_first_screen.png`](/C:/Users/79004/OneDrive/Рабочий%20стол/study/8sem/milf/artifacts/a1b/a1b_psm_first_screen.png)
- [`artifacts/a1b/a1b_psm_file_menu.png`](/C:/Users/79004/OneDrive/Рабочий%20стол/study/8sem/milf/artifacts/a1b/a1b_psm_file_menu.png)
- [`artifacts/a1b/a1b_report_constructor_first_screen.png`](/C:/Users/79004/OneDrive/Рабочий%20стол/study/8sem/milf/artifacts/a1b/a1b_report_constructor_first_screen.png)
- [`artifacts/a1b/a1b_report_constructor_save_surface.png`](/C:/Users/79004/OneDrive/Рабочий%20стол/study/8sem/milf/artifacts/a1b/a1b_report_constructor_save_surface.png)

Observed save/report surfaces:

- `ReportConstructor.exe` opened to a live report editor shell
- visible toolbar and menu bar confirm a live report/save UI surface exists
- no positive save dialog or file path was observed

## Main blockers / constraints

- original installer artifact missing from current repo snapshot
- requested prior A0/A1 documentation set missing from current repo snapshot
- no validated PSS DB/server connection available in A1B
- no real save dialog surfaced during the narrow save probe

## Is A2 justified now?

- `NO`

## Exact next recommendation

Restore the original `pss_4_353.exe` artifact into the `milf` workspace and rerun the installer-focused part of A1B on the same Windows host; after that, provide a valid Lab 1 DB/session target so the disconnected `PSM.exe` shell can be advanced to the first connected Lab 1 action.
