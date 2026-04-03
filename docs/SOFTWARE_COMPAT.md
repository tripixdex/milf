# Software Compatibility

## Windows-Specific Indicators
- `pss_4_353.exe` is a Windows executable.
- Archive materials and methodical text point to a larger PSS platform with client/server deployment, database setup, workflow surface, reports, and integrations.
- CAD-related assets include `*.dwg` and `*.dwl`, which further increase Windows-host likelihood.

## Native macOS Outlook
- Native macOS execution is currently unverified.
- Based on archive evidence, native macOS execution is currently unlikely enough that it must not be assumed.

## What Must Be Verified Later on Windows
- Whether `pss_4_353.exe` is an installer, launcher, or already packaged client.
- Required runtime dependencies.
- Whether the MVP lab can be executed from one client workflow or needs server/database setup.
- What export surfaces exist for reports, structures, document lists, and screenshots.
- Whether CAD-linked steps are mandatory for the MVP lab.

## Recommended Primary Execution Host
- Windows should be treated as the primary execution host for the legacy software.

## Role Separation
- Mac:
  - canonical repository,
  - planning,
  - input normalization,
  - evidence collation,
  - future cross-platform orchestration.
- Windows:
  - legacy software execution,
  - platform-dependent data entry,
  - workflow/report export capture.
