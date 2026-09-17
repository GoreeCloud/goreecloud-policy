# GoreeCloud Policy

GoreeCloud Policy is the shared policy-definition, evaluation, decision, distribution, enforcement-coordination, explanation, precedence, freshness, and policy-evidence framework for the GoreeCloud ecosystem.

## Current state

**Lifecycle:** Development  
**Runtime contract:** `v0.1` draft foundation  
**Platform Contract:** `0.4`  
**Implementation status:** Contract and schema foundation only; production runtime implementation and cross-repository acceptance evidence are not yet established.

GoreeCloud Policy is one of the nine Integral Platform Systems defined by **Instructions — Integral Platform Systems v3.0**. It provides common policy machinery without absorbing the substantive authority of domain systems:

- Privacy Shield remains authoritative for privacy requirements.
- Wardveil Security remains authoritative for security requirements.
- GoreeCloud Identity remains authoritative for identity and authentication facts.
- Everkeep remains authoritative for continuity and preservation requirements.
- GoreeCloud Manager remains authoritative for administration and control.
- Other approved domain systems remain authoritative within their defined scopes.

GoreeCloud Policy represents, evaluates, composes, distributes, explains, and coordinates enforcement of approved rules. A policy engine does not become the owner of a rule merely because it evaluates that rule.

## Repository contents

- [`CONTRACT.md`](CONTRACT.md) — normative runtime and authority-boundary contract.
- [`schemas/policy.definition.schema.json`](schemas/policy.definition.schema.json) — policy definition envelope.
- [`schemas/policy.evaluation-request.schema.json`](schemas/policy.evaluation-request.schema.json) — runtime evaluation request.
- [`schemas/policy.decision.schema.json`](schemas/policy.decision.schema.json) — policy decision and explanation/provenance envelope.
- [`schemas/policy.enforcement-evidence.schema.json`](schemas/policy.enforcement-evidence.schema.json) — enforcement-result evidence.
- [`examples/`](examples/) — non-production contract examples.
- [`goreecloud.platform.yaml`](goreecloud.platform.yaml) — truthful Platform Contract `0.4` repository declaration.

## Decision outcomes

Contract `v0.1` defines six policy outcomes:

- `allow`
- `deny`
- `conditional`
- `defer`
- `indeterminate`
- `error`

Only `allow` is an unconditional positive policy decision. `conditional`, `defer`, `indeterminate`, and `error` must never be silently upgraded to `allow`. Missing, stale, conflicting, unauthenticated, unverifiable, or unavailable required authority input fails closed into an explicit non-allow state.

## Development rule

The presence of schemas, examples, documentation, or a passing CI workflow does **not** establish production runtime implementation, Stable maturity, or component-level Policy conformance. Those claims require substantive implementation, tests, exact-revision evidence, and accepted integration results under the current GoreeCloud governance and Platform Contract.
