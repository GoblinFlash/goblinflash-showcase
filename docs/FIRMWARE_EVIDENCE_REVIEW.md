# Firmware Evidence Review

GoblinFlash treats firmware-related data as untrusted evidence until deterministic validation says otherwise.

## Evidence Is Not Authorization

A strong-looking signal does not grant authority to modify firmware. A parser finding, model summary, report row, or simulated result can support review, but it cannot authorize a write path.

## Parser Output

Parsers are evidence producers. They can report bounded observations, failure reasons, and uncertainty. They are not oracles and must not convert parse failure into negative evidence.

Expected parser posture:

- validate declared byte ranges before reads
- fail closed on malformed structures
- preserve provenance
- keep raw payloads out of trusted metadata
- avoid fallback-to-success behavior
- keep outputs deterministic and bounded

## Evidence Review Flow

At a high level, evidence review asks:

1. What produced this evidence?
2. What exact input was observed?
3. What validation accepted it?
4. What uncertainty remains?
5. Is this suitable for display, triage, or further review?

The answer may still be candidate-only, blocked, or insufficient. Absence of evidence is not proof of absence.

## Out-of-Scope Requests

The public showcase does not provide firmware modification recipes, exploit chains, bypass instructions, private-case analysis, or device-specific support.
