# GoblinFlash — Public Project Status

**Status:** Active development  
**Distribution model:** Proprietary  
**Repository role:** Public showcase and documentation  
**Source code:** Not published in this repository

## Overview

GoblinFlash is an actively developed firmware-analysis project centered on UEFI/BIOS inspection, deterministic validation, evidence preservation, and safe review workflows.

The current public-facing goal is to show the engineering direction of the project without publishing the complete production implementation.

## Current development focus

Active work is concentrated on the following areas:

- firmware parser hardening;
- handling of irregular and real-world firmware structures;
- deterministic validation and regression testing;
- schema governance and bounded data contracts;
- evidence provenance and traceability;
- firmware-state comparison;
- Firmware Workspace improvements;
- review-oriented patch planning;
- recovery and diagnostic workflows;
- preservation of negative and failed test results where scientifically useful.

Recent work has also included parser cleanup and correction of assumptions that were too permissive or too closely tied to synthetic fixtures.

## Engineering model

GoblinFlash is developed using an evidence-first workflow.

A change is not treated as complete merely because it appears to work once. Where practical, development records:

1. the exact input or fixture;
2. the parser or component revision;
3. the observed result;
4. the validation or regression result;
5. the evidence location;
6. the remaining uncertainty.

This is intended to reduce silent parser drift and make later review possible.

## Firmware Workspace

The Firmware Workspace is the main user-facing review surface currently being presented publicly.

It is intended to bring together firmware findings, evidence, validation state, and proposed actions in one place so that the operator can inspect what the system believes before any consequential action is considered.

The public showcase uses one representative screenshot:

`docs/assets/firmware-workspace.webp`

## Safety boundary

GoblinFlash is intended for owner-authorized firmware analysis.

The project does not equate:

- visibility with writability;
- configuration discovery with safe modification;
- the existence of a firmware setting with permission to bypass the mechanism protecting it.

The project is therefore not presented as a universal BIOS-unlocking tool.

Potential firmware writes, platform-protection changes, vendor-specific security mechanisms, and other consequential operations require separate validation and explicit authorization.

## Public vs. private material

The public repository may contain:

- project descriptions;
- screenshots;
- selected architecture summaries;
- public status notes;
- non-sensitive workflow documentation.

The public repository does not contain the complete proprietary GoblinFlash implementation.

Internal source code, research material, firmware-derived evidence, sensitive implementation details, and unpublished engineering artifacts may remain outside the public repository.

## Release state

GoblinFlash is not being represented here as a finished consumer release.

The project remains in active development, with continued work on parser correctness, firmware coverage, validation, evidence quality, workflow design, and release preparation.

Public material should therefore be read as a snapshot of an evolving system rather than as a frozen product specification.

## Licensing

Unless explicitly stated otherwise, **GoblinFlash and its associated materials are proprietary. All rights reserved.**

GoblinFlash is **not open source** and **not freeware**.

No public-source license is granted for the unpublished implementation.