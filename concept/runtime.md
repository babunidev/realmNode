# Runtime and game integration

**Status:** Concept; the central-server-first integration and companion application are established directions. API signatures and deployment boundaries are proposed.

## Responsibilities

RealmNode is the distributed server infrastructure. The game supplies its authoritative rules and state; RealmNode coordinates who executes, validates, replicates and recovers them. One node has sufficient game logic to execute the whole world locally. Several nodes can share work without every node computing every entity.

| Layer | Responsibility |
| --- | --- |
| Presentation | Rendering, UI, sound, animation, local input and prediction |
| Gameplay interface | Converts intentions into typed commands and accepted events into presentation updates |
| Deterministic game runtime | Movement, interactions, gameplay physics, combat, spells, NPC AI, spawning, items, quests, resources, progression, maps and game-specific systems |
| RealmNode core | Discovery, transport, identity, authority assignment, validation, state replication, persistence, version agreement, recovery |
| Durable state | Stable entity identities, shards, transactions, snapshots, history |

The same rules and canonical state representation must work in a single process, an authoritative server, a player simulator and a validator. UI state and scene objects are never evidence of a successful action. IDs survive restart, migration, transfer, replication and reconnect.

## Runtime contract (illustrative)

The baseline proposes initialize_world, load_state, apply_input, simulate_step, calculate_event, validate_event, serialize_state, deserialize_state, hash_state, create_snapshot, apply_transaction and migrate_state. These describe responsibilities rather than fixed language-level signatures. Commands must carry authenticated actor identity, relevant entity IDs and sufficient context for deterministic execution. A simulator produces consequences; the caller cannot directly write them.

Rules may include executable logic, scripts, configuration, formulas, item definitions, behaviour and tables. A repository or mirror can distribute a package but is not a live rules engine. A node executes the verified cached package locally.

## Native integration

A game-native integration uses the runtime contract directly. The node may be embedded in the game or run in a companion application with a local game-facing interface. The latter is the current deployment direction; the interface, process isolation and lifecycle are open. The game need not implement peer networking inside its rendering code. An independent headless node should eventually be possible.

Analubia is the first intended integration. The established starting point is a central authoritative Node.js server using shared game logic, seeded randomness, stable IDs and regions. Introduce witnesses and distributed responsibilities gradually. The existing game-native concept remains applicable; a temporary central server is a development stage, not proof of decentralization.

An earlier integration discussion explored a presentation-only engine with authoritative rules moved to a shared deterministic Rust runtime later. That choice applied to its earlier game context; it does not establish Rust as the universal RealmNode runtime. A fixed simulation tick, authored data for interaction results, and headless deterministic validation remain proposals worth evaluating. Current TypeScript interoperability and native app language are open.

See [legacy integration](legacy-integration.md) for the earlier adapter approach, [roadmap](../docs/ROADMAP.md) for milestones, and [engineering questions](../ideas/ENGINEERING_QUESTIONS.md) for unresolved contracts.
