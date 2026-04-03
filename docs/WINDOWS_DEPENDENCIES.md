# Windows Dependencies

## Installer Behavior

### Actually observed
- `pss_4_353.exe` is a Windows `PE32` GUI executable.
- The binary contains `Nullsoft Install System v2.45` manifest text.
- It should be treated as an installer package, not as a proven standalone portable client.

### Not yet verified on a real Windows host
- Actual installer UI flow.
- Install target directories.
- Whether the installer bundles all required runtime components.
- Whether it launches the client immediately after installation.

## Required Host Dependencies

### Actually observed
- A Windows execution environment is required.
- No native macOS execution path was found.

### Documented in methodical materials, but not yet host-verified
- The Lab 1 guide describes a three-level architecture:
  - `Oracle Server 9.2+`
  - `Oracle Client 9.2+` together with `PSSOracleServer`
  - client module `PSS`
- The same guide describes initial setup actions such as:
  - DB creation
  - organization structure setup
  - user/group setup
  - dictionaries, units, characteristics, document types

## Admin Rights
- Not actually verified.
- Because installation was not executed on Windows, any claim about administrator privileges would be speculative.

## Database / Server Prerequisites
- They seem likely from the methodical guide.
- They are not yet verified on the real host.
- At this stage Lab 1 must not be assumed to be runnable as a purely isolated desktop client.

## CAD / Office Dependencies For Lab 1

### Actually observed
- Lab 1 source assets include `DOC`, `JPG`, and `TIF`.
- Labs 3–4 include `DWG`/`DWL`, but those belong to a later workflow block.

### Current evidence-based stance
- CAD dependencies are not yet proven mandatory for the smallest Lab 1 path.
- Office or document-viewer capability may be practically useful because Lab 1 includes linked textual and raster documents.
- No live Windows-side dependency was verified in this scope.
