# Open engineering questions

This register separates unsettled mechanisms from established architecture. All items below are **Open** or **Proposed**; none implies implementation.

| Area | Open question / proposed experiment |
| --- | --- |
| Authority | How are authority epochs, leases, membership, handoff acknowledgement and stale-owner fencing defined? Recover without a graceful shutdown. |
| Consensus | Which finality/quorum protocol prevents conflicting commits when both partitions have six or more nodes? How do validator sets change safely? The 3-of-5 example is illustrative. |
| Determinism | Define canonical state encoding, tick/input ordering, cross-runtime arithmetic and shared seed derivation that prevents manipulable loot. Compare identical replays across machines. |
| Independence | Define validator admission, Sybil resistance, collusion assumptions, unpredictable selection, disputes and evidence-based penalties. |
| Transactions | Specify atomic trade, multi-shard commits, idempotency, duplicate requests, pending rewards and disconnect behaviour. |
| Recovery | Define snapshot eligibility, retention, replica targets, accepted history discovery, corruption repair and restore after total downtime. |
| Game modes | Define exact minimum-participation accounting, community pause/resume UI, handling of a transient partition and separate save IDs. Do not merge branches. |
| World time | Define dormant-region elapsed-time calculation and active real-time executor requirements per game. |
| Privacy | Verify strict relay mode across discovery, reconnection and telemetry; determine relay trust, metadata exposure and no-relay UX. |
| Transport | Choose transport/protocol library, DHT, bootstrap strategy, NAT traversal, relay admission and congestion/DoS controls. |
| Security | Define message schemas, key lifecycle, replay prevention, permissions, sandbox, budgets, safe update execution and compromised publisher recovery. |
| Hidden knowledge | Explore how simulators, validators and storage nodes can work without exposing undiscovered or private game data. Encryption alone does not solve this. |
| Runtime | Decide companion language and shared game-rule execution strategy. Rust, rust-libp2p and SQLite were mentioned in prior project notes as candidates; current architecture does not establish them. Evaluate TypeScript compatibility without assuming deterministic equivalence. |
| Releases | Define manifest schema, trust anchors, verified chunks, dependency minimization, version negotiation, activation and migration/rollback safety. |
| Contribution | Choose recognition, reliable measurement, fraud resistance, CPU/memory/storage/bandwidth budgets, startup consent, and mobile lifecycle. |
| Scaling | Establish tests for hot-region splitting, cross-region interactions, validator lag and actual capacity under churn. |
| External clients | Optional legacy workload test: address handoff, session routing, module rights, unchanged client/server, and eventual runtime extraction. No third-party distribution authorization is assumed. |

## Evidence expectations

Start with known independent machines and record topology, versions, configuration, input logs and expected results. Measure correctness, latency, recovery, resource use and privacy behaviour before asserting network verification. Include invalid input/signature, impossible state, spam, rules mismatch, primary loss, relay loss and partition scenarios. An offline single-node demo and an opaque TCP tunnel prove only their respective scope.

See the [roadmap](../docs/ROADMAP.md) and [concept index](../concept/README.md).
