# GoblinFlash Showcase

GoblinFlash Showcase is a public-facing documentation skeleton for describing the GoblinFlash safety model, evidence review process, and governance discipline at a high level.

This repository is intentionally docs-only. It does not contain GoblinFlash core source code, firmware samples, device-specific data, private cases, or operational instructions for modifying firmware.

## Purpose

The showcase is meant to explain how the project thinks about firmware evidence, trust boundaries, schema governance, and review discipline without disclosing private implementation details or unsafe procedures.

The project posture is:

- evidence is not authorization
- parser output is a witness, not an oracle
- AI output has no write authority
- firmware inputs, archive metadata, reports, and migration data are untrusted until validated by deterministic project policy
- public documentation must avoid operational recipes that could be misused

## What This Repository Contains

- high-level safety and SDLC notes
- evidence-review principles
- public boundary descriptions
- schema-governance summary
- project status and non-goals

## What This Repository Does Not Contain

- firmware modification instructions
- device-specific recovery or unlock procedures
- private firmware or customer cases
- private source code
- generated experiment outputs
- issue templates, support workflows, GitHub Actions, or GitHub Pages

## Discussion Policy

Discussions may be enabled later for controlled architecture and research discussion. Issues are intentionally off for now.

Support requests, unlock requests, firmware dumps, device-specific offsets, patch requests, and requests for write-path guidance are out of scope.

## Current Visibility

Start private. Do not publish publicly until a separate review approves the public boundary.
