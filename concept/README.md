# RealmNode concept

This is the navigable architecture of RealmNode. The [game-native concept](game-native-concept.md) remains the consolidated baseline; the following documents develop its subsystems and recover requirements that were not explicit in that baseline.

The current direction is a game-native runtime, with a companion application as a deployment option and an incremental transition from a central server. The older external-client approach is retained separately as an integration proposal, not a prerequisite for the first game.

| Area | Document |
| --- | --- |
| Runtime boundaries and integration | [Runtime](runtime.md) |
| World modes, simulation and authority | [Simulation](simulation.md) |
| Durable state and recovery | [Persistence](persistence.md) |
| Connectivity, privacy and resilience | [Networking](networking.md) |
| Verification and threat model | [Security](security.md) |
| Rules, releases and migration | [Rules and versions](rules-and-versions.md) |
| Companion application and contribution | [Companion node](companion-node.md) |
| Historical external-client approach | [Legacy integration](legacy-integration.md) |
| Evidence and open questions | [Source coverage](../docs/CONCEPT_AUDIT.md), [open engineering questions](../ideas/ENGINEERING_QUESTIONS.md) |

All architecture here is **Concept**, not evidence of implementation. Established decisions are identified in the [decision register](../docs/DECISIONS.md). Examples and proposed mechanisms remain illustrative unless separately established.
