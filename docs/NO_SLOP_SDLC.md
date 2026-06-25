# No Slop SDLC

GoblinFlash uses a no-shortcuts development process for safety-critical boundaries.

## Core Rule

A green test result is not enough if the test only blesses the same bad assumption as the implementation. Evidence must challenge the implementation, not rubber-stamp it.

## Review Discipline

The project separates roles:

- implementer writes the patch
- reviewer tries to break the patch
- operator controls merge, commit, tag, and public release decisions

A finding is not a fix. A plan is not permission. Understanding a bug does not authorize broadening scope.

## Evidence Before Claims

Claims about safety, compatibility, or correctness require fresh validation. The expected pattern is:

1. define the contract
2. write deterministic regression coverage
3. patch the narrow boundary
4. run targeted tests
5. run wider tests when practical
6. report what passed, what failed, and what remains out of scope

## Trust Boundaries

The same bug class must be closed centrally when possible. Repeated local string filters, path rewriting, or truthy checks are not accepted as durable safety controls.

Examples of rejected shortcut classes include:

- basename laundering
- silent path normalization
- broad exception fallback to success
- truthy authorization
- raw payload promotion into trusted evidence
- metadata laundering
- hidden export or write enablement
- unbounded archive extraction
- unbounded binary parsing

## Public Documentation Boundary

Public material must describe process and architecture. It must not include device-specific instructions, private identifiers, firmware write instructions, or operational recipes.
