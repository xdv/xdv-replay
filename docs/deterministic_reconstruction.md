# Deterministic Reconstruction

## Scope

`src/replay_reconstruct.ds` reconstructs and verifies deterministic control decisions.

## Covered Decisions

- Scheduler winner reconstruction with stable tie-break.
- Resource allocation allow/deny reconstruction with conservation checks.
- Capability validation reconstruction per domain scope.
- Fault escalation action reconstruction by severity.
- Domain transition ordering checks.

## Verification Model

Each verification API recomputes the decision and compares against recorded value.

Mismatch returns deterministic replay invariant error codes.

## Invariants

- scheduler decision equivalence
- resource conservation
- capability outcome equivalence
- fault escalation equivalence
- monotonic transition ordering
