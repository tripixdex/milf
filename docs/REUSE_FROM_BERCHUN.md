# Reuse From Berchun

## Process Patterns To Reuse
- Narrow scopes with explicit boundaries.
- `master_report` as the project governance surface.
- Audit-first corrections instead of blind implementation.
- Clear separation of verified facts from assumptions.
- Explicit closeout reports after each scope.
- Operator-safe wording about what is and is not supported.

## Architecture Patterns To Reuse
- Canonical source-of-truth discipline.
- Separation between canonical inputs, generated artifacts, and runtime byproducts.
- Staged execution instead of one giant implementation jump.
- Evidence-preserving run mindset.
- Cross-checking docs against actual runtime behavior.

## What Must Not Be Copied Blindly
- Solver-centric architecture.
- Mathematics-first validation model.
- Teacher-facing report assumptions from another subject.
- Any assumption that all truth can be rebuilt locally on Mac.
- Any early one-button UX before the Windows-host workflow is actually bounded.

## How `milf` Differs From `berchun`
- `berchun` is analytic-first and computes report truth directly.
- `milf` is workflow-first and likely depends on a legacy platform and operator actions.
- `berchun` could freeze around deterministic computations.
- `milf` must first freeze execution boundaries, evidence capture, and host strategy.
