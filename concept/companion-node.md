# Companion node and contribution

**Status:** Established direction (2026-11-25); user controls from the September discussions are established requirements. UI details, incentives and platform implementation are open.

## Deployment and lifecycle

A dedicated native computer or phone application can run alongside the game and contribute simulation, validation, storage, archives or relay capacity. Its role is a RealmNode process, not a mandatory browser tab. The earlier runtime discussion called for automatic background startup; startup and background contribution must honor the user's explicit role permissions and platform controls. A headless or always-on community node can also contribute.

The game and node may be one process in a native implementation or separate processes with a local interface. The browser game can continue to use a central server while the companion initially takes on low-risk responsibilities. On phones, witness or relay roles were suggested as a lighter starting point, subject to mobile background restrictions and battery limits; this is not a proven platform capability.

## Contribution settings

Provide global defaults plus per-realm overrides. For each simulator, validator, storage, archive and relay role, offer Allow / Ask / Never; distinguish while playing, background and both/always as timing policies. An Ask setting requires consent before taking the role. A role may be refused or relinquished; sudden loss must still be survivable.

Resource controls include CPU, memory, disk space, upload/download bandwidth, simultaneous connections, and storage duration. Adapt work to machine capability and current load. A weak laptop or battery-powered phone may take lighter work; a stable desktop or dedicated community device may contribute more. A machine can perform several roles if permitted. Privacy settings remain independent of contribution.

## Recognition and onboarding

The established idea is to invite frequent players and community supporters to install the application, run it while playing and earn a contributor reward. The relationship should benefit the world and the contributor. The reward type, measurement, eligibility, anti-fraud rules and presentation are open. Possible non-power recognition includes titles, standing or cosmetics; these are proposals, not decisions.

Contribution reporting should distinguish offered capacity from useful verified work. Uptime alone is not proof of service; resource usage and privacy need to be understandable to the user. Avoid assuming a verified measurement mechanism exists.

## First integration

The proposed sequence is known-peer relay/storage, witnessing a central simulator, independent validation, then simulation authority and eventual public participation. The first app's language, operating systems, install/update mechanism, local interface and TypeScript/Rust interoperability remain undecided. Always-on game execution and archive availability are distinct responsibilities.
