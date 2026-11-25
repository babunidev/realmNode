# Development Log

A concise account of meaningful project development, written from the human creative's perspective. Newest entries first.

## 2026-11-25 — A repository of its own

RealmNode now lives in its own public repository, [babunidev/realmNode](https://github.com/babunidev/realmNode), written in English and organized like my other projects. Claude Code (Claude Opus 5.5) translated the brainstorm, moved the existing English concept into `concept/`, wrote the agent instructions and the documentation standard after the pattern of my other repositories, and set up the decisions, development log, roadmap, collaboration record and structure overview. References to Analubia stay by name only, because that repository is private.

**Result:** Documentation only, no code.

## 2026-11-25 — From Analubia back to RealmNode

While working on Analubia's 3D experiment, the question came up of where the world is actually calculated. An MMORPG needs one place that decides what really happens, and my RealmNode concept was the obvious candidate. Claude Code (Claude Opus 5.5) took stock: Analubia's non-player characters already run on a central Node.js service with the same code as the game, while each player's own character is still calculated by the browser and trusted as reported. It weighed this against the concept and proposed starting with a central server that follows RealmNode's rules, so that the move to peers stays open. That is how we do it for now.

On top of that came my idea of a companion app: something people run next to the game on their computer or phone, which takes over the server work between players and earns them a contributor reward. Relying on open browser tabs alone is too fragile, and this turns contribution into something the community gives and gets back. Claude Code set up the project folder with a copy of the existing concept and a first brainstorm with open questions and steps.

**Result:** Documentation only, no code. The game-native concept itself was written earlier with AI assistance; tool and model were not recorded.
