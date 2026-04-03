# Execution Strategy

## Current Recommended MVP Execution Model
- Use a cross-platform repository/control plane on Mac.
- Use a Windows execution host for the legacy PSS runtime.
- Start with a semi-automatic Windows execution adapter for `Lab 1 — Модель изделия`.

## What Belongs To The Cross-Platform Core
- Canonical raw input schema.
- Run metadata and evidence manifests.
- Report assembly policy.
- Output validation rules.
- Repository documentation and audit artifacts.

## What Belongs To The Windows Adapter
- Launching or guiding the legacy PSS runtime.
- Host-specific runbook steps.
- Exporting or capturing platform outputs.
- Collecting screenshots, reports, and structured evidence from the legacy environment.

## What Remains Manual For Now
- Initial platform setup and dependency discovery.
- Any CAD-coupled or UI-judgment-heavy steps.
- Any workflow steps not yet proven scriptable and stable.

## When Compatible Reimplementation Could Be Justified Later
- Only after repeated Windows-host runs show a narrow, stable, and well-documented subset of required behavior.
- Only if the MVP outputs can be reproduced without relying on proprietary workflow, COM, or CAD internals.
- Only if adapter and semi-automatic modes become the main bottleneck rather than the main source of truth.
