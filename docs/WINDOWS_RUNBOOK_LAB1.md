# WINDOWS_RUNBOOK_LAB1

## Scope

A1B — Real Windows Host Access + First Launch Evidence Capture

## Actually observed steps

1. Real Windows host facts were captured on the active machine:
   - `Windows 10 Home Single Language`
   - build family `19041`
   - current token integrity: `Medium`
   - current user was **not elevated** at the moment of first runtime launch

2. The current `milf` workspace was checked for the original installer artifact.
   - `pss_4_353.exe` was **not present** in the current repo snapshot.
   - A recursive search one level above the workspace also did **not** find `pss_4_353.exe`.

3. The extracted runtime payload was present in:
   - `_pss_payload_extracted/`

4. `PSM.exe` was launched from:
   - [`_pss_payload_extracted/PSM.exe`](/C:/Users/79004/OneDrive/Рабочий%20стол/study/8sem/milf/_pss_payload_extracted/PSM.exe)

5. First observed live runtime screen:
   - window title: `Модуль PDM - [Соединение не установлено]`
   - left navigation tree visibly contained:
     - `Мой рабочий стол`
     - `Папки`
     - `Справочники`
     - `Организационная структура`
     - `Поиск в БД`

6. `ReportConstructor.exe` was launched from:
   - [`_pss_payload_extracted/ReportConstructor.exe`](/C:/Users/79004/OneDrive/Рабочий%20стол/study/8sem/milf/_pss_payload_extracted/ReportConstructor.exe)

7. First observed report runtime screen:
   - window title: `Конструктор отчетов - [Шаблон1 : Лист1]`
   - visible report editor shell opened successfully
   - visible toolbar included open/save/report-style controls

8. A minimal save-surface probe was attempted on `ReportConstructor.exe`.
   - `Ctrl+S` was sent to the live window
   - no save dialog became visible during the observation delay

## Blocked steps

1. Installer launch/install behavior was blocked by artifact absence.
   - The original `pss_4_353.exe` was not available in the current workspace.
   - Therefore installer launch, install path, and install completion could not be truthfully observed in A1B.

2. Lab 1 progression inside `PSM.exe` was blocked by missing DB/session connection.
   - The first reachable shell was explicitly disconnected: `Соединение не установлено`.
   - No live PSS database/server session was established during A1B.

3. A real save path was not observed.
   - `ReportConstructor.exe` opened.
   - `Ctrl+S` did not surface a save dialog within the observed interval.

## Still-unverified steps

1. Original installer behavior:
   - whether `pss_4_353.exe` launches on this host
   - whether installation completes
   - final installation directory
   - whether UAC/admin elevation is required by the installer

2. DB/server requirements beyond first shell:
   - whether Lab 1 can proceed against a bundled local base without extra setup
   - whether a dedicated transport server or Oracle-backed environment is required for Lab 1 data entry

3. Runtime save/export flow inside `PSM.exe`:
   - actual file-save dialogs
   - actual export destinations
   - actual print/report generation path during a connected Lab 1 session

## Current best truthful run path for Lab 1

Observed path:

1. Launch [`_pss_payload_extracted/PSM.exe`](/C:/Users/79004/OneDrive/Рабочий%20стол/study/8sem/milf/_pss_payload_extracted/PSM.exe)
2. Reach main shell `Модуль PDM - [Соединение не установлено]`
3. Stop at disconnected shell because no validated DB/session connection was established in A1B

This is the first confirmed live Lab 1-adjacent runtime path on a real Windows host.
