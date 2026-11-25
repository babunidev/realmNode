# RealmNode

An experiment in peer-to-peer gaming: a runtime in which the players' own machines calculate, validate and store a persistent online world together, so that no single server owns it. The server is not one computer; it is the network of participating nodes.

**Status: concept and brainstorming. Nothing here is implemented yet.**

## Start here

| Document | What it covers |
| --- | --- |
| [Concept index](concept/README.md) | Subsystem architecture, companion app, rules, networking, security and legacy integration |
| [Game-native concept](concept/game-native-concept.md) | The full architecture: node roles, temporary authority, deterministic simulation, validation, replication, identity, networking and security invariants |
| [Brainstorm](ideas/BRAINSTORM.md) | Open collection of ideas: the companion app, rewards for contributors, Analubia as the first game |
| [Concept audit](docs/CONCEPT_AUDIT.md) | Recovered design history, original architecture coverage and limitations |
| [Open engineering questions](ideas/ENGINEERING_QUESTIONS.md) | Unresolved protocols, implementation choices and evidence requirements |
| [Roadmap](docs/ROADMAP.md) | Proposed milestones from a central server to a public peer network |
| [Decisions](docs/DECISIONS.md) | What has been decided, by whom and why |
| [Development log](docs/DEVLOG.md) | How the project is taking shape |
| [Project structure](docs/PROJECT_STRUCTURE.md) | Where everything lives |

Contributors, human or AI, read [AGENTS.md](AGENTS.md) and the [documentation standard](docs/DOCUMENTATION.md) first.

## The idea in one picture

```text
        PLAYER A
        Game + Node
            │
PLAYER B ───┼─── PLAYER C
Game + Node │    Game + Node
            │
        PLAYER D
        Game + Node

The lines between them are the server.
```

Each node carries the complete rules of the game. Authority over a region moves between nodes, results are reproduced and checked by independent validators, and persistent state is replicated so that no machine holds the only copy of the world.

## First game: Analubia

Analubia, a browser-based roleplaying world, is the first intended integration. It starts with a **central game server** that is built along RealmNode's rules (inputs as requests, seeded randomness, stable identities, regions as the unit of simulation), so that parts of its work can later move to player nodes. RealmNode itself, together with a companion app that players run alongside the game, is the future direction and is meant to be tried as soon as possible. See [Decisions](docs/DECISIONS.md).

## Origin

RealmNode first appeared as a general runtime meant to wrap existing games, then as the proposed network for the Morkahja concept, and is now written up as a game-native architecture. Earlier versions live in my local Morkahja concept archive and are not published here.

## License

No license has been chosen yet. Until one is added, all rights are reserved.
