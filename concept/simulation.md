# Simulation, world modes and authority

**Status:** Concept. The three save categories, minimum community participation, responsive gameplay with parallel checks, and survival of abrupt node loss were established in earlier discussions.

## World modes and save isolation

| Mode | Participants | State |
| --- | --- | --- |
| Solo/offline | 1 | Local, unverified by independent witnesses |
| Small cooperative | 2–5 | Shared cooperative branch; witnessed where possible |
| Community realm | 6+ eligible participating nodes | Community branch; durable progression requires sufficient independent validation |

Offline operation uses already downloaded required rules and data. Solo, cooperative and community state are separate save/world branches. Local loot, characters and progression do not migrate into the verified community history. The six-node threshold is a minimum participation policy, not a proof of independence or a sufficient consensus protocol. Six identities controlled by one participant are not six independent validators.

When community participation falls below the minimum, verified progression stops. Degraded transient play may be possible, subject to policy; it must not create durable community rewards. The exact pause/rejoin experience remains open. A returning node recovers the accepted branch, not an automatically merged local save.

## Work distribution

Simulation regions are logical units that can be split or merged according to population, entity density, AI, combat, computational cost and latency. Fine-grained tasks may be delegated within a region, but their order, dependencies and authority must remain explicit. A group activity should use a simulator close to its players, and independent validators can be elsewhere. A lone player in a quiet area does not need physically nearby players to receive independent validation.

A region has a temporary primary simulator and a set of eligible independent validators. Role eligibility depends on resources, latency, reliability, compatibility, independence and consent. Authority can follow the geographic population. Instances such as dungeons or raids can recruit temporary authority groups and discard transient state after their durable effects are committed. Large gatherings can recruit extra capacity and partition work; capacity gains must be measured, not assumed.

## Execution and validation

The deterministic contract is same starting state + ordered inputs + same rules + same random seed = same result. Seeds cover loot, hits, AI and generated events. Stable tick ordering, canonical serialization, numerical behaviour across runtimes and unpredictable yet reproducible randomness require engineering validation.

Movement and combat use prediction, authoritative regional results and validation alongside the experience. The local client can respond before every check completes, then reconcile, interpolate or roll back where appropriate. Persistent item creation, inventory, currency, trade, experience, quests and progression are committed only after stronger validation. The earlier 3-of-5 example is illustrative, not the chosen quorum protocol.

## Handoff and abrupt failure

A normal handoff transfers signed state with entity ID, position, velocity, health, resources, effects/auras, cooldowns, inventory references, current action, combat and quest context, relevant AI and world references. The receiver verifies the state before assuming authority; the old owner relinquishes it.

Abrupt disappearance is a normal condition. A successful graceful shutdown is never a prerequisite for recovery. Replicas and validated history must provide a recoverable starting point; an eligible replacement takes over, and validators are replenished. Graceful handoff is an optimization. Authority epochs, fencing stale owners, recovery of uncommitted inputs and partition safety are unresolved protocol details.

Dormant areas can save state and resolve elapsed time abstractly upon reactivation when game rules permit. A real-time game requiring progress in the absence of players needs a reachable active executor; an archive alone stores data and does not perform simulation.
