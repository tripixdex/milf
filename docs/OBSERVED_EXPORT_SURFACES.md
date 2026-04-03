# OBSERVED_EXPORT_SURFACES

## Actually observed runtime exports

- None were positively executed during A1B.

Notes:
- `ReportConstructor.exe` was launched successfully.
- A save-surface probe (`Ctrl+S`) was attempted.
- No save/export dialog became visible during the observation interval.

## Actually observed save paths

- None were positively observed during A1B.

Notes:
- No visible `Save As` / file chooser path was captured.
- Therefore no destination folder, extension, or default save location can be truthfully claimed.

## Actually observed printable/report surfaces

- `ReportConstructor.exe` opened to a live report editor shell:
  - window title: `Конструктор отчетов - [Шаблон1 : Лист1]`
  - visible report/template workspace
  - visible toolbar with report-editor controls
  - visible menu bar including `Файл`

- `PSM.exe` opened to a live PDM shell:
  - window title: `Модуль PDM - [Соединение не установлено]`
  - not a report surface by itself
  - useful as the first verified runtime screen

## Still inferred only surfaces

- `PSM.exe` save/export/report actions extracted from static resources and prior binary analysis
  - still not host-verified in A1B

- `ReportConstructor.exe` actual file-save dialog behavior
  - still not host-verified in A1B

- Any print preview / print path
  - still not host-verified in A1B

- Any export path tied to a connected Lab 1 session
  - still not host-verified in A1B
