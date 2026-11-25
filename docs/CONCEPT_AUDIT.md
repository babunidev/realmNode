# Concept consolidation and source coverage

**Date:** 2026-11-25. **Status:** Documentation audit; no code or tests.

The objective of this pass was to recover the earlier questions, design choices and proposals into the repository without turning assistant suggestions into established decisions. ChatGPT (GPT-6.2) reviewed the existing repository, the available 79-section original architecture document, and retrieved project conversation excerpts and summaries. The original historical text and private conversations are not reproduced here. The repository's game-native concept remains intact.

## Retrieved conversation coverage

| Period | Recovered themes | Destination |
| --- | --- | --- |
| 2026-09-08 | Neutral runtime and rename; external client gateway, publisher identity, compatible world networks, updates, prototype sequence; positive concept framing | Runtime, rules and versions, legacy integration, roadmap, decisions |
| 2026-09-12 | Two-machine P2P test; unchanged legacy server workload; distinction between transport test and nodes collectively executing game rules | Legacy integration, runtime, decisions |
| 2026-09-13 | Minimal verified downloads, three isolated save categories, six-node threshold, privacy settings and chosen relays, contribution controls, abrupt failover, locality, fast/strong validation, accepted staged integration | Simulation, networking, security, companion node, rules and versions, decisions |
| 2026-09-21 | Native architecture extraction; saved Markdown; prior shared-runtime and presentation separation discussion | Runtime, concept baseline, engineering questions |
| 2026-11-18 | Revisited concept and open finality, partition and authority issues | Persistence, engineering questions |
| 2026-11-25 | Existing repository records of central-server-first integration, companion app, rewards, contribution and documentation standard | Companion node, runtime, roadmap, existing decision register |

These rows describe retrieved material, not a complete chat inventory. The available conversation search returned excerpts/summaries rather than full transcripts; deleted, archived or unindexed chats and individual turns may be missing. Exact historical technical parameters beyond recovered evidence remain open. No private messages, personal data or private game project source paths were copied into this public repository.

## Original architecture coverage

The source used the earlier AzerothNode name. The mapping below covers all numbered sections of that document. Names, example builds, node counts, quorum illustrations and sample release values were not treated as binding defaults.

| Original sections | Topics | Current location |
| --- | --- | --- |
| 1–3 | Scope, layers, local gateway | Runtime; legacy integration |
| 4–12 | World/publisher identity, releases, patch distribution, compatible/breaking changes, activation and migrations | Rules and versions; legacy integration |
| 13–17 | Regions, roles, temporary authority, isolated player, single-node mode | Simulation; companion node; baseline |
| 18–23 | Fast/strong validation, two truths, determinism, anti-cheat, identity | Simulation; security; persistence |
| 24–26 | Replicas, snapshots, archives | Persistence |
| 27–33 | Discovery, direct connections, relays, volunteer capacity, NAT, privacy, encryption | Networking; companion node |
| 34–39 | Hostile peers, protocol, sandbox, limits, Sybil resistance, validators | Security |
| 40–44 | Locality, adaptive capacity, instances, events and handoff | Simulation; companion node |
| 45–48 | DDoS, failover, central dependencies and limits | Networking |
| 49–53 | Player/character identity, social services, economy, ledger | Security; persistence |
| 54–56 | Neutral core, runtime modules, emulator integration | Runtime; legacy integration |
| 57–61 | Player experience, browser, forks, health, degradation | Legacy integration; networking; simulation |
| 62–67 | Security, availability, version, update and latency invariants | Baseline; subsystem documents |
| 68–74 | Staged prototypes, malicious peers, relays, client integration | Roadmap; engineering questions; legacy integration |
| 75–79 | Publisher example, DDoS motivation, scope, overall architecture | Rules and versions; legacy integration; baseline |

## Remaining uncertainty

This consolidation is intentionally additive: the existing baseline and brainstorm are preserved. The subsystem layout and open-question grouping are editorial choices. The companion-app deployment supersedes an exclusively embedded-process reading of the baseline without changing the native runtime contract. Historical external-client and publisher concepts are retained as optional approaches, not current priorities. The current architecture still lacks a specified finality and authority protocol, transport implementation and test evidence.

The [decision register](DECISIONS.md) distinguishes recovered explicit decisions from proposals. The [engineering register](../ideas/ENGINEERING_QUESTIONS.md) keeps unresolved issues visible.
