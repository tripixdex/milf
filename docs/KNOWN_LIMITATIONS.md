# KNOWN_LIMITATIONS

## A1B limitations actually encountered

- The original installer artifact `pss_4_353.exe` was not present in the current `milf` workspace snapshot.
- A recursive search one level above the workspace did not recover that installer.
- Because of that, installer launch/install completion/UAC behavior could not be observed truthfully in A1B.

- The requested prior A0/A1 markdown set was not present in the current workspace snapshot:
  - `README.md`
  - `master_report.md`
  - `docs/...`
  - `reports/report_A0_milf_inventory.md`
  - `reports/report_A1_windows_validation.md`

- `PSM.exe` reached only a disconnected shell:
  - `Модуль PDM - [Соединение не установлено]`
  - no live DB/session connection was established during A1B

- A positive save/export dialog was not observed.
  - `ReportConstructor.exe` launched
  - `Ctrl+S` did not surface a save dialog during the capture interval
