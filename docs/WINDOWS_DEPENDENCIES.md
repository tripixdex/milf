# WINDOWS_DEPENDENCIES

## Host-verified dependencies

- A real interactive Windows desktop session is required.
  Observed host:
  - `Windows 10 Home Single Language`
  - build family `19041`

- A non-elevated user token is sufficient for first launch of extracted runtime binaries.
  Observed:
  - current token integrity was `Medium`
  - `PSM.exe` launched without observed elevation
  - `ReportConstructor.exe` launched without observed elevation

- The extracted application directory must remain intact when launching binaries directly from payload.
  Observed working launch base:
  - [`_pss_payload_extracted`](/C:/Users/79004/OneDrive/Рабочий%20стол/study/8sem/milf/_pss_payload_extracted)

- Bundled runtime libraries inside the extracted payload were sufficient for first launch of:
  - [`PSM.exe`](/C:/Users/79004/OneDrive/Рабочий%20стол/study/8sem/milf/_pss_payload_extracted/PSM.exe)
  - [`ReportConstructor.exe`](/C:/Users/79004/OneDrive/Рабочий%20стол/study/8sem/milf/_pss_payload_extracted/ReportConstructor.exe)

- A live DB/session connection was **not** required to reach the first `PSM.exe` shell.
  Observed:
  - shell title was `Модуль PDM - [Соединение не установлено]`

## Methodical-only inferred dependencies

- Original installer artifact:
  - `Лаб PSS/pss_4_353.exe`
  - not available in the current repo snapshot during A1B

- A real PSS database and/or transport-backed session for actual Lab 1 object work inside `PSM.exe`
  - not host-verified in A1B

- Possible server-side transport/or Oracle-backed environment for some PSS modes
  - inferred from binary inventory and prior static analysis
  - not host-verified in A1B

- Original Lab 1 methodical guide and sample report
  - requested by scope
  - not present in the current workspace snapshot during A1B

## Optional / useful tools

- Screenshot capture capability for runtime evidence
  Observed output location:
  - [`artifacts/a1b`](/C:/Users/79004/OneDrive/Рабочий%20стол/study/8sem/milf/artifacts/a1b)

- Existing extracted payload inventory for fallback runtime work when installer artifact is missing
  - [`_pss_payload_extracted`](/C:/Users/79004/OneDrive/Рабочий%20стол/study/8sem/milf/_pss_payload_extracted)

- Existing deep static reverse-engineering report for component identification
  - [`report.md`](/C:/Users/79004/OneDrive/Рабочий%20стол/study/8sem/milf/report.md)
