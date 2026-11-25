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
