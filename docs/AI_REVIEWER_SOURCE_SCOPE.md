# AI Reviewer Source Scope

GoblinFlash treats AI reviewer output as an evidence candidate, not as authority.

A reviewer may produce useful observations, but every source-level claim must declare what source access was actually available before the claim can be trusted.

## Core rule

AI confidence is not evidence.
Tool logs are provenance.
Source scope is mandatory.
Implementation claims require source verification.

This applies to praise, criticism, architecture reviews, and security findings.

## Source scope labels

Use one of these labels when evaluating AI reviewer output:

```text
NO_SOURCE_ACCESS
  The reviewer had no source file access.
  Source-level claims are unverified by default.

DOCS_ONLY
  The reviewer saw documentation only.
  Architecture summaries may be useful, but implementation claims remain unverified.

REPO_SEARCH_ONLY
  The reviewer used search over the repository, but did not inspect the full relevant file.
  Symbol existence may be plausible, but behavior claims require verification.

PARTIAL_FILE_READ
  The reviewer read only selected ranges or snippets.
  Claims are limited to the inspected range.

FULL_FILE_READ
  The reviewer read the full relevant file.
  Claims may be evaluated against that file.

VERIFIER_OUTPUT
  The reviewer used a separate grep, AST, test, or source-verifier output.
  Claims may be classified against that verifier result.
```

## Claim levels

Every reviewer statement should be classified before acceptance:

```text
SOURCE_FACT
  A concrete file, symbol, function, class, enum, test, or line-level behavior.

FILE_ATTRIBUTION
  A claim that a symbol or behavior exists in a specific file.

SEMANTIC_BEHAVIOR
  A claim about what the code actually does.

ARCHITECTURE_INFERENCE
  A higher-level interpretation based on source shape or project structure.

RECOMMENDATION
  A proposed design, refactor, policy, or future direction.

SPECULATION
  A plausible idea without enough evidence to treat as fact.
```

## Verification status

Use one of these statuses after review:

```text
SOURCE_CONFIRMED
  The symbol, file attribution, and behavior match inspected source.

SOURCE_UNVERIFIED
  The reviewer did not have enough source access for the claim.

SYMBOL_EXISTS_WRONG_FILE
  The symbol exists, but not in the claimed file.

DOMAIN_TOKEN_ONLY
  The token exists only in tests, demos, documentation, or examples.

ILLUSTRATIVE_NOT_IMPLEMENTED
  The reviewer described a useful model or rule, but it is not implemented as stated.

NOT_FOUND
  The claimed symbol, relation, or behavior was not found.

SEMANTIC_MISMATCH
  The symbol exists, but its behavior differs from the claim.

OVERSTATED
  The claim is directionally useful but too broad for the available evidence.
```

## Acceptance rules

```text
A source-level claim without source scope is not accepted.

A repo search is not a full audit.

A useful architecture inference is not an implementation fact.

A model's confidence does not upgrade evidence strength.

Praise is also untrusted input until decomposed.

A reviewer may assist, but does not grant authority.
```

## Examples

```text
Claim:
  "File X contains function Y."

Required:
  source scope proving file X was inspected.

If Y exists in another file:
  SYMBOL_EXISTS_WRONG_FILE

If Y appears only in tests:
  DOMAIN_TOKEN_ONLY

If Y is a proposed rule, not implemented behavior:
  ILLUSTRATIVE_NOT_IMPLEMENTED
```

## GoblinFlash posture

GoblinFlash uses AI reviewers as assistants in a controlled review process.

The reviewer may discover, summarize, compare, or challenge.
The reviewer does not decide truth.
The reviewer does not grant write authority.
The reviewer does not replace source verification.

Evidence remains evidence.
Authorization remains separate.
Unknown remains unknown.
