# Distributed Replay Ordering

## Scope

`src/replay_distributed.ds` provides deterministic merge ordering for node traces.

## Merge Semantics

- Build order keys from logical timestamp + node id + event id.
- Choose earliest key first.
- If keys tie, choose lower node id first.

## APIs

- `distributed_merge_choice`
- `distributed_merge_token`
- `verify_distributed_order`

## Determinism Goal

For identical distributed inputs, merge choice and token are stable and replay-equivalent.
