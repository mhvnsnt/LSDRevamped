# HANDOFF — LSDRevamped

**Last updated: 2026-11-22 (America/New_York).**
**Repo:** `mhvnsnt/LSDRevamped` (PUBLIC), default branch `master` (not `main` — use this branch as the PR base).
**Purpose of this file:** any agent that picks up work here reads this FIRST, then the linked docs. It states what we've done, where we're at, and what we're working toward — so the owner can say "go to this repo, pick up the work" and you just know. Update this file in the same PR whenever the state changes (add, don't delete).

## 1. What this repo is

A remake of the cult-classic game LSD: Dream Emulator — mirrored into the owner's account 2026-11-20. This is Figglewatts' Unity remake (not a decompilation): the game rebuilt in Unity 2021.3.45f2, using libLSD to load the original data files. ~184 MB in the tree (Git LFS).

How it relates to the owner's other LSD repos:
- `mhvnsnt/lsd-decomp` — the matching decomp, actively documented (1,447/1,447 functions read).
- `mhvnsnt/lsddecomp` — the brian-oblivion lineage complete matching decomp (CC0).
- `mhvnsnt/lsd_decompiled` — the cawfee lineage, early-stage WIP decomp.
- `mhvnsnt/lsddecomp-1` — the FirecatFG first attempt from 2024.
- `mhvnsnt/libLSD` — Figglewatts' C# library for loading LSD data files — the same library this remake builds on.

## 2. Where we're at

### DONE
- **1.0 release changes (2026-10-20, `e4d5bfe`):** the most recent upstream commit — changes for the 1.0 release. Last push into this account's mirror 2026-10-23.
- **Mirrored into this account 2026-11-20** (repo created here that day; history carried over). Upstream history before that runs back to 2024-10-15 (credit names, journal-select fix, video-dream-end freeze fix, control-binding fix).
- **Upstream state:** the remake reached 1.0. This mirror is a reference copy, not a fork under active development here.

### IN PROGRESS
- Nothing in progress. No open PRs, no releases in this mirror.

### BLOCKED
- Nothing blocked. Nothing is being built here.

## 3. What we're working toward

Reference, not development — for now. For the owner's Sato games work (Western Heart pulls LSD in as a main Eastern Mind pair), this repo is the playable-remake reference: how the dream plays in a modern engine, what the remake kept and changed, and the libLSD data formats it runs on. If the owner ever wants remake work (a port, a mod, a Unity-side change), it starts from this mirror — but that is his call, not a lane's.

## 4. Standing rules that apply here

- **Branch → PR → merge, always.** Never push to `master` directly. Add-only, zero-conflict PRs, no force pushes. (This is a public mirror — a bad merge breaks the remake for everyone downstream.)
- **Checkpoint-and-save law:** CHECKPOINT.md first, update after every step; the repo is the save; resume, never restart.
- **No-temp-storage law:** nothing in /tmp or any wipeable location, ever. Everything goes straight into the repo or a durable folder the second it exists.
- **Real-source-only:** the remake is built from the real LSD data via libLSD and the real Unity project here. No hand-tooled lookalikes.
- **Licence/source logged honestly:** this is Figglewatts' work (see upstream `Figglewatts/LSDRevamped`); the game itself is Asmik Ace / Osamu Sato's. You need your own copy of the game data to run it. Nothing built from it is distributed without respecting that.
- **Never kill in-progress work.** Never delete game files or other lanes' work without the standing verification rules.

## 5. Key files and paths

| What | Where |
|---|---|
| Unity project | `LSDR/` |
| Quick start | `README.md` (Git LFS, Unity 2021.3.45f2, nuget.exe restore, `move-packages`, open `LSDR/` in Unity) |
| Data-file library it builds on | `mhvnsnt/libLSD` (also in this batch) |
| Upstream | `Figglewatts/LSDRevamped` |
| Related repos (NOT this one) | `mhvnsnt/lsd-decomp`, `mhvnsnt/lsddecomp`, `mhvnsnt/lsd_decompiled`, `mhvnsnt/lsddecomp-1`, `mhvnsnt/libLSD` |

## 6. Open decisions needing the owner

- **Is this a reference or a project?** Right now it is a reference mirror. Any remake work (port, mod, Unity change) is his call — do not start it in a lane.
- **Which LSD source is canonical for the Sato-games pull?** This remake vs the `lsd-decomp` / `lsddecomp` decomps. His call, not a lane's.

## 7. How to pick up

1. Read this HANDOFF.md first, then `README.md`.
2. To run it: Git LFS, Unity 2021.3.45f2 via Unity Hub, nuget.exe; clone, `nuget.exe restore`, run the `move-packages` script in `LSDR/`, open `LSDR/` in Unity. You need your own game data — none is in the repo.
3. Never commit game data. Never push to `master` directly.
4. Land work branch → PR → merge, add-only, base branch `master`.
5. Update this HANDOFF.md in the same PR when the state changes.
