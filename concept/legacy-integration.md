# External-client integration and historical runtime approach

**Status:** Retained earlier design and proposed integration path. This is optional, not the current first-game architecture.

The initial RealmNode concept was a neutral runtime capable of hosting compatible existing game clients. The current game-native direction extracts the same core without requiring legacy client translation or a multi-game launcher. This document preserves the earlier technical design for future reference.

## Local gateway and adapters

A compatible client connects to localhost as it would connect to a traditional server. A client adapter handles its authentication and world protocol, then translates into the neutral encrypted RealmNode protocol. A separate game runtime module implements the actual game rules. The gateway is an interface; the long-term simulation authority belongs to the participating nodes. The core need not know the meaning of any particular spell.

Original illustrative client families included Vanilla 1.12, TBC 2.4.3, Wrath 3.3.5a and custom clients. Compatible client build, publisher/world identity, ruleset generation, data and script hashes, and protocol identity distinguish networks. Different expansions or custom rulesets cannot accidentally simulate together.

An optional launcher flow: select an existing game installation, detect its compatible build, list compatible worlds, verify the chosen release, obtain missing verified modules, join the peer network, launch the client and connect it locally. A browser could show world name, publisher identity/signature status, ruleset, client version, peer/player estimate, relay count, network health and verification status. Official worlds and forks can use distinct publisher identities. This is an historical UX proposal rather than a required native-game feature.

## Transport-only development test

The earlier testbed discussion used an existing WoW-compatible server (Tortoise-WoW/Turtle WoW terminology appears in the recovered discussions). The explicit constraint was to use the existing workload unchanged for private development and testing, not distribute or rewrite it as part of RealmNode.

The first test was a two-machine peer connection:

    Game client -> local node -> encrypted P2P link -> remote node -> unchanged test server

The remote server is still authoritative at this stage. This tests the transport only; it does not demonstrate distributed simulation or make that server part of RealmNode. Both computers run nodes. Authentication and subsequent world connections must traverse the gateway without changing the existing client's behaviour; address/connection handoff, bidirectional traffic and reconnect are explicit test cases.

Proposed sequence: simple TCP workload, authentication, world entry, movement/combat traffic, discovery and NAT traversal, relay fallback, reconnect, multiple players. No distribution of third-party client or server files is implied; licenses and rights must be reviewed before any public integration.

## From test workload to distributed runtime

The earlier accepted development direction was to wrap an existing workload first, define a formal game-runtime interface, extract responsibilities incrementally and eventually distribute simulation and validation. An emulator could supply rule logic through an adapter where technically and legally appropriate. Converting centralized logic into deterministic distributed execution is substantial work, and the unchanged transport test must remain separate from later extraction experiments.

A native game can directly implement the runtime contract without legacy adapters. The current [roadmap](../docs/ROADMAP.md) follows the native integration, with the transport-only experiment retained as an optional test track.
