# Brainstorm

Open collection. Contradictions, half-finished thoughts and alternatives may stand here. Newest entries first. Quotations are translated from German.

## 2026-11-25 — A companion app as the node, and rewards for taking part

*Added by Babuni on 2026-11-25.*

**The idea:** A dedicated app, native on the computer or the phone, that runs alongside the game. It is the RealmNode: it calculates, validates, stores or relays for the world, between the players. The network no longer depends on open browser tabs, or on there being any. People who want to support the project, or who play a lot, are asked to install the app and keep it running while they play. In return they receive a **contributor reward**. One hand washes the other, and that is good for the community.

Babuni: “that we don't just count on people having tabs open, or maybe none at all, but that people who want to support the project, and people who play a lot, are prompted to install the thing and keep it running while they play” – “I definitely want to integrate and implement that as soon as possible.”

**Why an app rather than only the browser (notes by Claude Code, Claude Opus 5.5; proposal):**
- An app can accept connections, runs in the background without throttling and stays on when the tab is closed. A browser can only connect through WebRTC with a signalling service.
- It fits the roles in the concept (simulator, validator, storage, archive, relay) and the “Allow / Ask / Never” controls with limits for CPU, memory and bandwidth.
- On a phone, more likely relay or witness than simulator (battery, background rules on Android and iOS).
- An always-on machine (a server or a community machine) is still needed, because Analubia's world keeps running on real time even when no player is online.

**Open questions:**
- What is the reward? Something in the game (standing, a title, adornments), something outside it, or recognition only? It must not let anyone buy or cheat their way to advantages in the game.
- How is contribution measured (uptime, validated work, stored data) without being faked?
- Which role does the app take first? Proposal: relay and storage first, then witness or validator, simulator of a region last.
- How do players learn about it in the game without it becoming intrusive?
- Which language and runtime does the app use? The concept names Rust with rust-libp2p and SQLite; Analubia's game logic is TypeScript. These have to fit together, for example through an embedded JavaScript runtime or a second implementation of the rules.

## Analubia as the first game

*Proposal by Claude Code (Claude Opus 5.5), 2026-11-25; not a decision.*

What Analubia already brings: world state separate from presentation, the same game logic in the browser and on the server, individuals with stable identities, and the city of Undor as a region with its own simulator.

What it still needs: inputs as requests instead of results, seeded randomness, regions as the unit of simulation, results that another machine can reproduce exactly (watch floating-point maths in browsers), and an answer to hidden knowledge: whoever simulates a region knows everything in it, including what lies behind the fog.

The steps that follow from this are in the [roadmap](../docs/ROADMAP.md).
