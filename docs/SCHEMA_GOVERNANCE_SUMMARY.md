# Schema Governance Summary

GoblinFlash uses schema governance to keep report and evidence shapes explicit, deterministic, and reviewable.

## Current Public Framing

This showcase only describes the governance idea. It does not promote experimental migration code, generated artifacts, or a separate source of truth.

Schema governance is used to reason about:

- schema identity
- versioned shape
- field compatibility
- blocked or unknown transitions
- deterministic compatibility reporting
- separation between evidence shape and decision authority

## What Is Deferred

Migration decision logic is not public authority here. Any future promotion of migration behavior requires separate review of:

- verdict semantics
- reference-oracle independence
- forbidden-field handling
- sanitizer and privacy interactions
- downgrade and unknown-route behavior
- generated metadata boundaries

## Public Constraint

Synthetic experiment schemas are not canonical GoblinFlash production schemas. They may be discussed as process examples only when scrubbed of generated artifacts and private details.
