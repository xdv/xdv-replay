# XDV Replay

Version: 0.1.0
Status: active
Language: Dust Programming Language (DPL)

## Specification Alignment

Primary specification: XDV-071 in `xdv-spec`.

Implemented focus for this milestone:

1. Trace entry format and hash-chain verification.
2. Deterministic reconstruction of scheduler/resource/capability/fault decisions.
3. Replay equivalence suite for local and distributed paths.

## Purpose

Deterministic replay engine for orchestration-faithful reconstruction.

## Modules

- `src/replay_contracts.ds`
  Replay invariants, domain/event/mode validation, capability and isolation guards.

- `src/replay_trace.ds`
  Trace hash chaining, entry token format, ordering keys, and chain/order verification.

- `src/replay_reconstruct.ds`
  Deterministic scheduler/resource/capability/fault reconstruction and verification.

- `src/replay_distributed.ds`
  Deterministic multi-node trace merge and distributed ordering verification.

- `src/replay_tests.ds`
  Replay equivalence suite for trace/hash, reconstruction, and distributed parity.

- `src/main.ds`
  Startup checks, smoke paths, and self-test entrypoints.

## Design Notes

- Replay is orchestration-faithful and excludes raw Q/Phi internal state.
- Q/Phi trace metadata requires structured exposure mode.
- Hash-chain verification is deterministic and tamper-evident.
- Distributed merge uses stable order keys and deterministic tie-breaks.

## Build

```bash
dust check xdv-replay/src
```

## Test

```bash
dust check xdv-replay/src/replay_tests.ds
dust check xdv-replay/tests/replay_e2e.ds
```

## Integration Contracts

- Preserve global logical ordering semantics.
- Preserve scheduler/resource decision equivalence.
- Detect hash/order/resource/capability invariant violations deterministically.
- Preserve isolation constraints by rejecting raw Q/Phi trace metadata.
