# XDV Replay Tests

Deterministic tests and fixtures for `xdv-replay`.

## Covered Behaviors

- Trace format/hash-chain generation and verification.
- Scheduler/resource/capability/fault deterministic reconstruction.
- Replay equivalence across local and distributed ordering paths.

## Entrypoints

- `xdv-replay/src/replay_tests.ds` : core behavior checks.
- `xdv-replay/tests/replay_e2e.ds` : aggregate test entrypoint.

## Run

```bash
dust check xdv-replay/src
dust check xdv-replay/tests/replay_e2e.ds
```
