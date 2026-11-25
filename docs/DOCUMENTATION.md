# Documentation Guide

## Author voice and AI attribution

Write project documentation in Babuni’s first-person voice. Tell readers what prompted the work, which choices shaped it, and how the experience unfolded from Babuni’s point of view. Recast third-person author narration such as “Babuni requested” as first-person prose. Use “I” and “my” naturally within sentences and vary the openings. Never begin a narrative sentence with “I” or “My.” Use **creative** as the role label. Keep technical facts, commands, and tables direct. Keep changelogs neutral and limited to what actually changed. Retain original quotations and credits.

Whenever AI contributed, identify the tool or product by name and give the exact model name or version when it can be verified. Say what each tool and model actually did, including research, proposals, drafting, coding, or testing as applicable. If the tool is known but the model is undocumented, say the model was not recorded. If the tool itself cannot be verified, say it was not recorded. Never guess or infer a model from the date, provider, or product name. Keep the human creative’s ideas, decisions, and firsthand observations distinct from AI contributions and distinguish proposals, implementation, and verified results. Put this attribution in the relevant narrative or collaboration record so the changelog can stay focused on changes.

## Purpose

This guide defines how material is organized and maintained in the RealmNode repository.

## Language

English is the language of this repository, for documentation, code, comments and commit messages. Quotations from conversations held in another language are translated and marked as translations.

## Status labels

- **Idea** — an untested thought in the collection.
- **Proposed** — a solution or direction open for discussion.
- **Developing** — actively being worked out; details may change.
- **Established** — explicitly decided by the creative and recorded in [DECISIONS.md](DECISIONS.md).
- **Open** — unresolved or intentionally undecided.
- **Retired** — superseded material retained for historical context.

## Technical evidence labels

Use explicit evidence labels in technical research and implementation records:

- **Concept** — described in the architecture; no code exists.
- **Documented** — a library or platform officially documents the capability relied on.
- **Inferred** — follows from documented behavior, but the exact runtime behavior has not been verified.
- **Locally verified** — tested on one machine, with versions and reproduction steps recorded.
- **Network verified** — tested across independent machines and real internet connections, with the setup recorded.
- **Unverified** — not yet confirmed or tested.

A design property such as “resilient to node loss” or “Sybil-resistant” is a goal until a test shows it under stated conditions. More peers do not by themselves prove scalability, and a signature proves who sent a message, not that its content is true.

## Where things belong

- **`concept/`:** the architecture, written as a coherent description.
- **`ideas/`:** raw, dated thoughts and brainstorming. Originals stay, even when later decisions differ.
- **`docs/`:** working rules, decisions, development history, roadmap and structure.
- **Repository root:** entry point, agent instructions and changelog.

## From idea to decision

1. Record the idea without changing its content or authorship.
2. Discuss it and keep contradictions visible.
3. Fold it into the concept as a draft, linking to where it came from.
4. Record a decision only after explicit confirmation, in [DECISIONS.md](DECISIONS.md), with date, subject, decision and who decided.
5. Update affected concept sections, the structure overview and the roadmap where needed.

## Readability

Every file starts with a short statement of its purpose. Prefer paragraphs and precise headings to long disconnected lists. Use relative links between files and check them when renaming.

## Privacy

This repository is public. Related game projects may be private: refer to them by name, without copying their content, paths or links. No passwords, keys, private communication or personal contact details.
