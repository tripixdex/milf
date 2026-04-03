# Artifact Policy

## Purpose
Define which artifact classes stay in Git and which remain local-only runtime surface.

## Canonical In Git Now
- Scope docs in `docs/`
- Scope reports in `reports/`
- Reviewed A1B screenshots in `artifacts/a1b/`

## Local-Only Runtime Surface
- `Лаб PSS.zip`
- `Лаб PSS/`
- `_pss_payload_extracted/`
- `_pss_install_probe/`
- future installer payloads, extracted vendor runtimes, and local install probes

## Intentionally Unbound In RN1
- Whether future sanitized exports should live under `artifacts/` or a more specific subtree.
- Promotion rules for host-generated HTML, report files, or database snapshots.
