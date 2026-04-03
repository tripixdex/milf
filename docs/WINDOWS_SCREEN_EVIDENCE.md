# WINDOWS_SCREEN_EVIDENCE

## Screenshot map

### 1. First PSM shell

- File:
  - [`artifacts/a1b/a1b_psm_first_screen.png`](/C:/Users/79004/OneDrive/Рабочий%20стол/study/8sem/milf/artifacts/a1b/a1b_psm_first_screen.png)
- Shows:
  - live `PSM.exe` main shell
  - title `Модуль PDM - [Соединение не установлено]`
  - left tree with `Мой рабочий стол`, `Папки`, `Справочники`, `Организационная структура`, `Поиск в БД`
- Why it matters:
  - first truthful runtime evidence on a real Windows host
  - proves PSM shell is reachable without immediate DB handshake success

### 2. PSM menu attempt

- File:
  - [`artifacts/a1b/a1b_psm_file_menu.png`](/C:/Users/79004/OneDrive/Рабочий%20стол/study/8sem/milf/artifacts/a1b/a1b_psm_file_menu.png)
- Shows:
  - live `PSM.exe`
  - an attempted menu capture that surfaced the window/system menu rather than a validated application save/export menu
- Why it matters:
  - negative evidence
  - confirms this image must **not** be used as positive proof of application-level export/save surfaces

### 3. First ReportConstructor shell

- File:
  - [`artifacts/a1b/a1b_report_constructor_first_screen.png`](/C:/Users/79004/OneDrive/Рабочий%20стол/study/8sem/milf/artifacts/a1b/a1b_report_constructor_first_screen.png)
- Shows:
  - live `ReportConstructor.exe`
  - title `Конструктор отчетов - [Шаблон1 : Лист1]`
  - visible report editor surface and toolbar
- Why it matters:
  - first verified report-oriented runtime screen on the Windows host
  - strongest A1B evidence for report/save UI presence

### 4. ReportConstructor save-surface probe

- File:
  - [`artifacts/a1b/a1b_report_constructor_save_surface.png`](/C:/Users/79004/OneDrive/Рабочий%20стол/study/8sem/milf/artifacts/a1b/a1b_report_constructor_save_surface.png)
- Shows:
  - `ReportConstructor.exe` after a `Ctrl+S` probe
  - no visible save dialog in the captured interval
- Why it matters:
  - negative evidence
  - supports the truthful statement that no real save path/dialog was observed in A1B
