# GoblinFlash Showcase

GoblinFlash Showcase is a public documentation entrypoint for the GoblinFlash firmware evidence workflow.

GoblinFlash is best understood as an **evidence accountability system for firmware analysis**.

It does not only ask what was found. It asks:

* what proves it
* what is missing
* what conflicts with it
* where trust stops
* who does not have authority to approve change

## Public scope

This repository is intentionally documentation-only.

It does not contain:

* GoblinFlash core source code
* firmware samples
* BIOS or SPI dumps
* private cases
* generated experiment artifacts
* unlock instructions
* write-path guidance
* exploit chains
* device-specific patching instructions

## Core posture

GoblinFlash follows a safety-first review model:

```text
Evidence is not authorization.
Parser output is a witness, not an oracle.
AI assistance is not engineering authority.
Unknown remains unknown.
Read-only analysis is the default.
```

A strong-looking signal is not enough. A result must carry its evidence, missing proof, conflicts, and trust boundary.

## What this showcase describes

This repository describes the public-facing process and safety model around:

* firmware evidence review
* no-slop SDLC discipline
* source-scope rules for AI reviewer claims
* schema governance boundaries
* public safety and non-goals

## Documentation

Start here:

* [Safety Boundaries](docs/SAFETY_BOUNDARIES.md)
* [Firmware Evidence Review](docs/FIRMWARE_EVIDENCE_REVIEW.md)
* [No Slop SDLC](docs/NO_SLOP_SDLC.md)
* [AI Reviewer Source Scope](docs/AI_REVIEWER_SOURCE_SCOPE.md)
* [Schema Governance Summary](docs/SCHEMA_GOVERNANCE_SUMMARY.md)
* [Project Status](docs/PROJECT_STATUS.md)
* [Non-Goals](docs/NON_GOALS.md)

## Discussions

Discussions are enabled for controlled, high-level research and documentation conversation.

This is not a support forum, firmware unlock service, dump review queue, or patch request tracker.

Support requests, unlock requests, private firmware analysis, dump review, offsets, write-path guidance, and device-specific patching requests are out of scope.

## Contribution boundary

Public-safe documentation improvements are welcome.

See [CONTRIBUTING.md](CONTRIBUTING.md) before opening a pull request.
