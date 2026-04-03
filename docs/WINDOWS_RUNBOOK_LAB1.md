# Windows Runbook — Lab 1

## Host Used
- Control-plane host actually used in this scope:
  - macOS `26.2`
  - `arm64`
  - host: `MacBook-Pro-Vlad.local`
- Real Windows execution host:
  - not available in the current execution environment
  - not observed directly in this scope

## Launch / Install Path Actually Attempted
- Inspected `Лаб PSS/pss_4_353.exe`.
- Verified locally that it is a `PE32 executable (GUI) Intel 80386, for MS Windows, Nullsoft Installer self-extracting archive`.
- Checked for available local Windows execution bridges:
  - `wine`, `wine64`, `pwsh`, `prlctl`, `VBoxManage`, `qemu-system-x86_64`, `virsh`
  - installed GUI access paths such as `Microsoft Remote Desktop`, `Windows App`, `Parallels Desktop`, `VMware Fusion`, `UTM`
- No usable Windows host or local Windows bridge was found.

## Smallest Truthful Manual Runbook For Lab 1

### Actually observed in this scope
1. Locate the installer `Лаб PSS/pss_4_353.exe`.
2. Confirm that it is a Windows NSIS installer rather than a native macOS executable.
3. Confirm that no real Windows execution path is available from the current host.

### Documented in Lab 1 materials but NOT yet verified on Windows
- The methodical guide states that the PDM module is launched through:
  - `Пуск -> Программы -> PDM STEP Suite -> Настройка -> Модуль PDM`
- The documented Lab 1 flow then proceeds through:
  1. user identification and working database selection
  2. units and characteristics setup
  3. document types setup
  4. dictionaries setup
  5. product and version creation
  6. product structure formation
  7. characteristic attachment to versions
  8. linked document creation
  9. document viewing
  10. DB search and table export
  11. full-composition report export
  12. specification generation/printing
  13. mass and cost calculation
  14. report assembly

## Where The Process Currently Stops
- The process stops before installer launch on Windows.
- Reason: no accessible Windows host, VM, remote desktop path, or local Windows compatibility layer was available in the current environment.

## What Remains Unknown
- Actual installer screens and whether installation completes.
- Whether admin rights are required.
- Whether the system can run with a self-contained demo DB or requires broader Oracle/database setup.
- Actual login flow and working database selection dialogs.
- Whether Lab 1 can be completed from one client workflow without extra server-side preparation.
- Actual export dialogs and file formats emitted by the live runtime.
