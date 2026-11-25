# Persistence, history and recovery

**Status:** Concept. The data formats, consensus protocol and replication factors are open.

## Durable state

Replicate character and entity state, inventories, item ownership, resources, currency, settlements, guilds, mail, market state, quests, professions and progression across independent storage nodes. Shards may follow geography, entity groups, ownership, systems or historical ranges. Nodes keep relevant simulation data plus replicas they consent to store; the full database need not exist on every device.

Persistent events have an ordered, cryptographically verifiable history. Ledger-like records can protect ownership, provenance and tamper detection without putting movement or ordinary spells on a cryptocurrency blockchain.

An economic change is a validated state transition. Creation, destruction, vendor exchanges, crafting, trades, auctions and currency changes must preserve the game's invariants and ownership history. Trade should be atomic; delayed mail can be represented as signed transactions; guild membership and market changes favor consistency over input-loop latency. Cross-shard atomicity, double-spend prevention, retries and idempotency remain open.

## Commit path

1. An authenticated input is submitted.
2. Authority calculates the result under the active rules.
3. A durable transaction is proposed with enough evidence for independent verification.
4. Eligible validators check the result and required agreement is obtained.
5. The transaction commits to the accepted history and replicas store it.
6. Presentation reflects final durable ownership/progression.

A pending pickup or reward may be shown as provisional before commitment; the UI must distinguish pending, validating, committed and rejected outcomes. This is a proposed interaction pattern, not an implemented feature. Unfinished interactions interrupted by disconnect need explicit cancellation or resumption rules.

## Snapshots and archives

A snapshot identifies world/state generation, history position, state root and validator signatures. Recovery verifies the snapshot's authorization and content, downloads newer accepted changes and checks the resulting state before rejoining. A signature alone does not prove that the signer was eligible or that the snapshot is canonical.

Archives can retain manifests, rules versions, migrations, snapshots, shards and historical transactions. Volunteers, community machines, mirrors and headless nodes may preserve data. Multiple independent copies are needed; loss of every replica or archive means state may be unrecoverable. If nobody is online, archived state can remain dormant; active real-time simulation requires an executor.

## Reconnection and partitions

A node compares its local state to the current world identity, generation, accepted snapshot and subsequent history. Outdated local copies do not overwrite accepted state. Separate solo/cooperative histories are never merged into community history.

A minimum node count is not enough to prevent conflicting commits: two partitions may each have six nodes. Safe membership changes, authority fencing, quorum intersection, finality and recovery must be designed before unrestricted public durable progression. Until a safe decision can be demonstrated, community writes should fail closed as a proposed safety policy. No partition merge algorithm is established.
