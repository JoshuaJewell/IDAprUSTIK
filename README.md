<div align="center">

# IDAprUSTIK

### *If you have to ask, you're already compromised.*

**Invisible Door: Actionpointrun Uplink ShadowTrauma, Inc. Kickers**

An asymmetric two-player infiltration game. One of you goes in. The other keeps you alive from a screen. Neither of you is fully in control, and that is the point.

</div>

---

## What this is

IDAprUSTIK is a game about infiltration, deception, and trust, usually misplaced.

One player is the **infiltrator**: moving through the world, dodging obstacles, bypassing security, staying unseen. The other is the **hacker**: watching remotely, opening doors, timing elevators, rewiring electronics, cutting the lights, and generally trying to keep the infiltrator breathing.

Control is not shared. It is asymmetric. The infiltrator moves; the hacker watches. If they do not work together, someone gets caught. The recurring problem is that the hacker's competence and the infiltrator's survival are loosely correlated at best.

> *"Breaking in is easy. Getting back out is harder. Especially when your escape route depends on a hacker who swears he knows what he's doing, right up until he accidentally reboots the entire security grid."*

## A new era (attempt four)

This is the fourth incarnation of the project. The lineage:

| # | Codebase | Stack |
|---|----------|-------|
| 1 | IDApTIK | TypeScript / Excalibur |
| 2 | IDApixiTIK | ReScript / PixiJS |
| 3 | idaptik | AffineScript / PixiJS |
| 4 | **IDAprUSTIK** | **Rust** / **Elixir** |

Rust owns gameplay truth; Elixir owns multiplayer/session life.

## How it plays

Underneath the platforming sits a grounded network simulation, so the hacker is solving a real, legible network rather than pressing a "hack" button.

- **Grounded access.** The hacker starts from a specific device and sees only what is reachable from where they are.
- **Real topology.** Star networks, subnets, zones (LAN / VLAN / External), routing, DNS resolution, traceroute hop paths.
- **Movement through the network.** SSH between devices, session chaining, and pivoting so you attack from a compromised machine's perspective.
- **Pressure.** Active trace timers during intrusions, action-based alerts (failed logins, port scans), and passive logging for post-incident investigation. Bounce through intermediate machines to slow the trace.
- **The physical layer bites back.** Power grids, signal strength, cut cables, and physical location all affect what the hacker can do, and the infiltrator can open doors the hacker cannot reach remotely.

The two roles share one world. The hacker has a physical presence and real discovery risk; this is not a disembodied support role.

## Roadmap

Development runs in vehicle-named phases, smallest viable thing first:

**Envelope** &rarr; **Wheel** &rarr; **Skateboard** &rarr; **Bicycle** &rarr; **Chassis** &rarr; **Motorcycle** &rarr; **Computer Game**

- **Envelope (v0.1)** — minimum viable game: core movement, basic hacker interactions (doors, elevators, overrides), first art, documented mechanics.
- **Wheel** — refined movement and interaction; stealth responsiveness; expanded hacker capabilities (security loop manipulation, timed overrides, sabotage).
- **Skateboard** — deeper asymmetric multiplayer; multi-phase infiltration; infiltrator/hacker communication.
- **Bicycle** — strategic depth; AI countermeasures that react to interference.
- **Chassis** — richer environmental mechanics (terrain, sound sensitivity, misdirection); first non-linear missions.
- **Motorcycle** — the full experience: adaptive security AI, emergent tension, the complete multiplayer framework.
- **Computer Game** — beyond proof of concept.

## Tech

- **Language:** Rust.

The wider stack (rendering, multiplayer transport, persistence) is being settled as part of this rewrite and is intentionally not pinned here yet. Architecture decisions for the Rust era will be recorded as ADRs under `docs/` as they are made, rather than asserted up front and quietly contradicted later.

## Licensing

IDAprUSTIK is layered, and each layer is licensed for what it is. The whole project is open and is built to stay open.

| Layer | License |
|-------|---------|
| **Engine & code** | [AGPL-3.0-or-later](https://www.gnu.org/licenses/agpl-3.0.html) |
| **Game content** (art, levels, narrative, character designs, audio) | [CC-BY-SA-4.0](https://creativecommons.org/licenses/by-sa/4.0/) |
| **Names & marks** (IDAprUSTIK, IDApTIK, Moletaire) | Trademark, all rights reserved |

The engine is strong copyleft: anyone who builds on it, including as a hosted service, must share their entire derivative source. The content is free culture: you may use, modify, and even sell derivatives, provided you attribute and keep them under the same share-alike terms.

## Contributing

Contributions come in under the Developer Certificate of Origin (DCO 1.1); sign your commits with `git commit -s`. See `CONTRIBUTING.md`.

## Status

Early. This is a `git init`-era repository for the Rust rewrite.

---

<div align="center">

*The infiltrator moves. The hacker watches. Try to leave together.*

</div>
