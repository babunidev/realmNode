# Decisions

A concise record of meaningful decisions. Each entry names who decided. A proposal from an AI is recorded only once the creative has confirmed it.

Entries are listed newest first.

## 2026-11-25 — English, and the documentation standard of my other repositories

**Decision:** The repository is written in English and follows the same documentation structure as my other projects: README, AGENTS.md, changelog, and in `docs/` the documentation standard, collaboration record, decisions, development log, roadmap and project structure.

**Who:** Babuni (translated): “Translate everything into English in the RealmNode project, and make sure you follow the complete documentation like in the other repositories.”

## 2026-11-25 — A companion app as the node

**Decision:** RealmNode is pursued with a companion app, native on computer or phone, that players run alongside the game and that takes over server work between the players. Players who support the project or play a lot are asked to install it and keep it running while they play, and are rewarded as contributors. This is to be integrated and tried as soon as possible. What the reward is, how contribution is measured and which roles the app takes first are **open**; see the [brainstorm](../ideas/BRAINSTORM.md).

**Who:** Babuni (translated): “that people who want to support the project, and people who play a lot, are prompted to install the thing and keep it running while they play, so they get their contributor reward, and one hand washes the other” – “I definitely want to integrate and implement that as soon as possible.”

## 2026-11-25 — Analubia first runs on a central server built for RealmNode

**Decision:** Analubia, the first intended game, calculates its world on a central game server (Node.js, with the same game logic as the browser) for now. The server is built along RealmNode's rules so that peers can take over parts of it later: inputs as requests, seeded randomness, stable identities, regions as the unit of simulation. RealmNode stays the explicit future direction. Recorded in the Analubia prototype as decision P-017.

**Who:** Babuni (translated): “Until then, of course, we do it exactly as your proposal says.” The proposal for a central server first came from Claude Code (Claude Opus 5.5).

**Why:** The open engineering problems of a peer network (consensus, fake identities, network splits, determinism across browsers, hidden knowledge under fog of war) are each substantial, and Analubia's world keeps running on real time even when nobody is online, which needs an always-on machine anyway.

## 2026-09-21 — Extract the game-native core

**Decision:** Use the core distributed simulation, validation, networking, persistence and recovery architecture for direct game integration, without requiring WoW compatibility, the multi-game ecosystem or publisher discovery. Retain the earlier external-client approach as a separate historical integration track.

**Who:** Babuni. Recovered from the game-native concept discussion and its accepted Markdown consolidation.

## 2026-09-13 — Separate play modes and verified progression

**Decision:** Solo/offline (one node), cooperative (two to five) and community realm (six or more participating nodes) have separate save/world branches; do not mix their progression. Community verification cannot continue below the minimum participation threshold. Movement/combat remain responsive with parallel checking; durable loot, currency, inventory, trade, quests and progression require validation.

**Who:** Babuni. Recovered from earlier discussion; exact finality and validator-independence protocols remain open.

## 2026-09-13 — Privacy, contribution and failure

**Decision:** Offer direct, prefer-relayed and strict relay-only connectivity, with selectable trusted/community relays. Contribution controls have global defaults and per-realm overrides, with consent and playing/background timing policies. Support automatic background node operation subject to permissions. Sudden node loss must be survivable without graceful handoff; handoff is an optimization. Distribute fine-grained work, favor latency-local simulation and independent external validators.

**Who:** Babuni. Recovered from earlier networking and contribution discussions.

## 2026-09-13 — Verified modules and staged integration

**Decision:** Game modules remain additional, minimal cached downloads; prefer peer distribution with repository/mirror fallback, always verify authenticity and hashes. The earlier external-client path starts by wrapping the existing workload, then defining a runtime API, extracting responsibilities and distributing them incrementally.

**Who:** Babuni. Recovered from earlier development discussion. The current native-game roadmap is separate.

## 2026-09-12 — Keep the legacy test workload unchanged

**Decision:** Both machines run RealmNode in the peer-to-peer transport test. The existing game server is an unchanged test workload, not software to distribute as RealmNode. The long-term RealmNode itself is the server: participating nodes collectively execute the rules; one node can run the world locally.

**Who:** Babuni. Recovered from the two-machine test and subsequent clarification.

## 2026-09-08 — Name and neutral scope

**Decision:** Rename the original AzerothNode concept to realmNode and adapt it to neutral runtime infrastructure. Describe the architecture positively as a coherent concept rather than a series of corrections.

**Who:** Babuni. Recovered from the original concept revision discussion.
