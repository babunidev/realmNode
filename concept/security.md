# Security, identities and validation

**Status:** Concept. Security properties are goals until demonstrated under explicit assumptions.

## Trust boundaries

Every remote peer may lie, cheat, collude, impersonate, send malformed or stale packets, exhaust CPU/memory/bandwidth, disconnect or use incompatible rules. Authenticate node and player identities using cryptographic keys. Keep private keys local. A signature identifies the signing key and detects unauthorized modification; it does not prove truthful simulation or independent ownership.

Character ownership gives permission to submit authenticated requests, not direct permission to alter durable state. Account key loss, recovery, rotation, revocation and protection against theft are open. A decentralized identity does not require an indispensable login database.

## Input and validation

Validate intentions against authoritative state: action known and permitted, resources available, range and target valid, cooldown and timing correct, and result computed using the rules. The node reports an attempted action; it cannot simply award itself damage, currency, items or progression. Validators independently reproduce relevant execution. Prediction is provisional, and durable effects require the stronger commit path.

Eligibility and selection may use longevity, history, uptime, behaviour, resource contribution, CPU, bandwidth, latency, current load, compatibility, diverse network paths, reputation and randomized selection. Rate-limiting new identities can help. These are potential signals, not proof of independent operators. A participant must not choose or control its own validating majority. Sybil and collusion resistance, adversarial assumptions, admission and punishment remain open.

## Protocol and host isolation

Use a narrow typed protocol for player inputs, state updates/hashes, authority handoffs, validation requests/results, shard and snapshot transfers, discovery, and transaction proposals/commits. Validate size, shape, authentication, context and authorization before expensive processing. A gameplay message must not request shell commands, arbitrary files, DLL loading, or arbitrary remote code execution.

Run with least privilege and isolate network handling and executable rules from unrelated documents, browser credentials, SSH keys and other applications. Signed releases are authenticated content, not automatically safe code. Rule execution, update installation and publisher compromise require a defined trust and sandbox model.

Limit connections, request rates, message sizes, bandwidth, memory, CPU, shard retrieval and validation work. Apply both per-peer and global budgets. Resource caps and consent must remain effective under hostile load.

## Confidential state

Encryption protects data in transit, not from an endpoint authorized to simulate it. A simulator or storage peer may learn hidden world state. Fog-of-war, private information and selective state disclosure require a separate design. Sharding alone does not solve confidentiality. Keep sensitive data out of public diagnostics and test artifacts.

Security tests should include forged inputs, invalid signatures, incompatible rules, conflicting state, spam, validator collusion, abrupt disconnects, stale authority and network partitions. No attack-resistance result is claimed.
