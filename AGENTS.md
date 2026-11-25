# Agent and Contributor Instructions

Follow [the documentation standard](docs/DOCUMENTATION.md) for first-person author voice, factual changelogs, and naming the AI tool and verified model for each contribution.

## Before every change

1. Read this file and [docs/DOCUMENTATION.md](docs/DOCUMENTATION.md).
2. Check the [README](README.md), the [project structure](docs/PROJECT_STRUCTURE.md) and the files affected.
3. Place existing statements, decisions and sources as they are before adding new material.

## Project role

RealmNode is an architecture and, later, software for running a persistent online world across the players' machines. It is reusable infrastructure. Games define their rules; RealmNode decides who calculates, who validates, where state lives and when authority moves.

The human creative owns the concept, scope, priorities and final decisions. AI may assist with research, organization, drafting, review, implementation, testing and documentation when requested.

## Keep the areas separate

- **`concept/`** holds the architecture. Change it deliberately and record substantial changes in the development log.
- **`ideas/`** is an open inbox. Contradictions, repetitions, half-finished thoughts and alternatives may stand there. Never silently delete an idea or turn it into a decision.
- **`docs/`** holds working rules, decisions, the development log, the roadmap and the structure overview. Concept content does not belong there as a substitute.
- **Game projects** such as Analubia keep their own documentation. Their repositories may be private: do not copy their content, file paths or links into this public repository beyond what the creative has approved.

## Status precision

An idea is not a proposal, a proposal is not a decision, and a decision is not an implementation. A model's answer is never a project decision. Something is **implemented** only with evidence, and **verified** only when the test actually ran. Use the labels from the [documentation standard](docs/DOCUMENTATION.md).

## Security and privacy

This repository is public. Never commit credentials, keys, private conversations, personal contact details, network addresses of real machines or other sensitive data. The concept assumes every remote node may be hostile; code written here must assume the same.

## Maintenance

- Decisions go into [docs/DECISIONS.md](docs/DECISIONS.md), meaningful progress into [docs/DEVLOG.md](docs/DEVLOG.md), and repository changes into [CHANGELOG.md](CHANGELOG.md).
- Update [docs/PROJECT_STRUCTURE.md](docs/PROJECT_STRUCTURE.md) when folders or key files change.
- Prefer small, reviewable commits. Do not add frameworks, dependencies or automation without being asked.
- Do not assume a license or rights to third-party material.
