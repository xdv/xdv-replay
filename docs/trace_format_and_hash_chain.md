# Trace Format and Hash Chain

## Scope

`src/replay_trace.ds` implements the deterministic trace format and hash chaining requirements.

## Trace Entry Elements

Trace token and hash functions encode these logical elements:

- event id
- domain
- process id
- VHM id
- capability id
- resource id
- event type
- event metadata
- logical timestamp
- previous hash

## Hash Chain

`trace_hash_next` computes next-link hash deterministically from previous hash and entry payload.

`verify_trace_chain_pair` recomputes and validates link integrity.

## Ordering

`trace_order_key` and `verify_trace_order` enforce global deterministic ordering by logical timestamp and node/event identity.

## Isolation Constraint

Q/Phi trace entries require structured metadata mode; raw-state mode is rejected.
