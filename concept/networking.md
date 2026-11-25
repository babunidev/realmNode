# Networking, privacy and availability

**Status:** Concept. Connection preferences and role-control scope were established; transport choices and precise protocols are open.

## Discovery and connectivity

Combine a distributed hash table, cached peers, several bootstrap peers, manual entry, LAN discovery and introductions through existing connections. Bootstrap nodes introduce peers and have no gameplay authority. A new node still needs some reachable discovery path; operation after bootstrap loss must be tested.

Support direct connections, NAT traversal, reachable IPv6, port mapping and relay fallback. Possible mapping mechanisms include manual forwarding, UPnP, NAT-PMP or PCP; a reachable tunnel can also provide a public endpoint. These are candidates, not automatic permission to alter router settings. NAT and carrier-grade NAT can prevent inbound connections even when outgoing connections work.

A volunteer relay must have usable reachability and spare capacity. Test eligibility automatically; enforce opt-in bandwidth and connection ceilings (the earlier 50 Mbps/100 connections illustration is not a default). Relays forward encrypted traffic and gain no authority over game state.

## Privacy modes

| Mode | Behaviour |
| --- | --- |
| Direct | Prefer direct connectivity; peers may see each other's network addresses |
| Prefer Relay | Prefer relayed paths, with direct fallback where allowed |
| Relay Only / Strict Relay | Connect only using acceptable relays; no direct fallback to ordinary game peers |

Allow selection of trusted or community relay providers. Strict mode should fail visibly if a permitted relay is unavailable, rather than silently exposing the user's address. Discovery, diagnostics and reconnect paths need to respect the same privacy policy. A relay may observe source addresses, destination relationships, timing and volume even when it cannot read the payload. This does not promise anonymity against relays or traffic correlation.

Authenticated end-to-end encryption protects the payload between peers even over relays. Transport, identity verification, replay protection and key management remain implementation work.

## Availability and DDoS

Design for any single machine disappearing. Replace simulators, validators and relays; recover storage from replicas, archives from alternative archives, and bootstrap from cached or alternative discovery paths. Avoid a mandatory master, login, simulation, relay, database, archive or discovery machine in the final community architecture.

A targeted attack can still disconnect a home connection if its address is exposed. Distributed infrastructure and relays reduce permanent single points of failure, but do not guarantee availability against coordinated attacks, exhausted relay pools, insufficient validators or access-network disruption.

## Network health

Expose peer count, eligible authorities and validators, relay availability, redundancy, archive reachability, regional latency, stability, ruleset agreement and verification status. More peers may improve redundancy, but verified community progression stops when safe participation is lost. Connection success, latency, failover time, bandwidth, partition behaviour and strict-mode leak prevention need independent-machine tests.
