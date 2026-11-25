# Roadmap

Proposed milestones, from a central server to a public peer network. **Status: proposed** (draft by Claude Code, Claude Opus 5.5, 2026-11-25), based on the milestones in the earlier Morkahja-era chapter and on the [brainstorm](../ideas/BRAINSTORM.md). The order may change; nothing here is implemented.

## Milestones

1. **Central server built for RealmNode (in Analubia).** One authoritative server with regions as the unit of simulation and WebSocket connections. Inputs are requests, randomness is seeded, every entity has a stable identity. The client predicts its own movement and accepts corrections.
2. **Second simulator, same results.** A second instance on another machine recalculates one region from the same state and inputs and compares state hashes. This proves determinism before any trust question arises.
3. **Companion app as relay and storage, known peers.** A first native app that relays traffic and stores replicas for a small group of known testers, with the contribution controls from the concept (Allow / Ask / Never, resource limits).
4. **Companion app as witness and validator.** The app checks results of the central server's regions and reports disagreements.
5. **Companion app as region simulator.** A player node simulates a region; the server and other nodes validate it. Authority handoff and recovery when the node disappears.
6. **Independent machines over the internet.** Relays, NAT traversal, latency, bandwidth and recovery tested across real connections.
7. **Open participation.** Public validator admission, Sybil resistance, hostile-peer protection, multiple regions, signed releases and scalability measurements.

## Open before milestone 3

- What the contributor reward is and how contribution is measured without being faked.
- Which language and runtime the app uses, given that Analubia's rules are TypeScript (embedded JavaScript runtime or a second implementation of the rules).
- How hidden knowledge is protected when a node simulates a region its player has not explored.
