# Rules, releases and world compatibility

**Status:** Concept. Minimal verified module downloads, preferably from peers, were established in the general-runtime discussions. The publisher-oriented format below is an optional integration proposal.

## Compatibility identity

Nodes only execute together when world identity, client compatibility where applicable, network protocol, ruleset version/hash, world generation and persistent-state generation agree. For external rules packages, include relevant game-data and executable/script hashes. Names alone are insufficient to identify a realm.

The core remains neutral toward individual game mechanics. The runtime defines spells, creatures, quests, combat, items, AI and world behaviour. Runtime packages are additional cached downloads rather than mandatory parts of every RealmNode installation. Fetch only required data/modules; prefer peer exchange where available, with repositories, mirrors or other distribution sources as fallback.

## Package integrity

A manifest can identify the world, release, author/publisher key where applicable, minimum supported RealmNode protocol/software, client build, ruleset generation, content hashes, migration and activation point. Verify manifest authenticity against the selected trust anchor and verify every content-addressed file/chunk before acceptance. Download sources need not be trusted to supply authentic bytes. The current game-native integration does not require a generic publisher directory or launcher.

Runtime updates and content releases can be independently versioned. Crash fixes, UI changes, diagnostic and networking improvements may remain compatible if they do not change the rules or required protocol. Changed spell behaviour, loot, quests, item rules, stats or formulas generally require a new rules generation.

## Activation and migration

A signed release can propose scheduled activation. Nodes may download and verify packages before that point. Older and newer incompatible networks can coexist as distinct histories, never silently share simulation state. The exact time/height activation protocol is open.

A deterministic migration transforms a known accepted state into a new generation. Examples include new profession or entity fields, retired item/spell IDs, altered quest and talent structures. Independent validation should reproduce the resulting state root. Activation during partitions, partial migration, failed release recovery and rollback require an explicit policy.

A publisher identity can distinguish an official release and a community fork, with separate keys and hashes even where client technology is shared. This preserves authenticity without making a download host the game server. Publisher key custody, revocation, rotation, forks and trust establishment remain proposals for deployments that need them.

See [legacy integration](legacy-integration.md) for the original publisher/adapter model and [persistence](persistence.md) for durable history.
