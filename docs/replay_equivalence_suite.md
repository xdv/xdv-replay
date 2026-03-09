# Replay Equivalence Suite

## Scope

`src/replay_tests.ds` implements the XDV-071 equivalence suite.

## Test Blocks

1. Trace format + hash chain integrity
2. Deterministic reconstruction parity
3. Replay mode/distributed merge equivalence

## Assertions

- hash chain verification succeeds for valid entries
- ordering checks are monotonic
- reconstructed scheduler/resource/capability/fault decisions match recorded outputs
- distributed merge output is stable for identical inputs
- mismatch paths are detected deterministically

## Entrypoint

`tests/replay_e2e.ds` delegates to `XdvReplayTests::K::run_all_tests()`.
