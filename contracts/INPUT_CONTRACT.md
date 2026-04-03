# Input Contract

## Purpose
Freeze the boundary between canonical lab intent and host-local execution details before automation work starts.

## Already Known
- Inputs must identify the target lab and execution context explicitly.
- Variant/assignment-defining data must remain canonical repo truth.
- Windows-host runtime details must not be mixed into the same layer as canonical lab intent by default.

## Intentionally Unbound In RN1
- Exact machine-readable schema format.
- Whether future inputs live in YAML, JSON, or another normalized form.
- How Windows credentials, DB endpoints, or session selectors are referenced.
- Whether one contract will cover all labs or Lab 1 will freeze first.
