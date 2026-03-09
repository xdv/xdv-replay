# Changelog

## 0.1.1 - XDV-071 Replay Core Implementation

- Implemented replay invariants and validators in `src/replay_contracts.ds`.
- Implemented trace format, order keys, and hash-chain verification in `src/replay_trace.ds`.
- Implemented deterministic scheduler/resource/capability/fault reconstruction in `src/replay_reconstruct.ds`.
- Implemented deterministic distributed trace merge in `src/replay_distributed.ds`.
- Added replay equivalence suite in `src/replay_tests.ds`.
- Added aggregate test entrypoint `tests/replay_e2e.ds`.
- Updated README/docs/test docs for delivered XDV-071 behavior.

## 0.1.0 - Initial Skeleton

- Created project scaffold for XDV Replay.
- Added State.toml, README.md, and docs/test placeholders.
- Imported LICENSE from xdv-os/LICENSE.
