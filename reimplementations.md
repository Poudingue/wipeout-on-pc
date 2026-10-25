# Reimplementations, decompilations and recompilations

One game per project. Legend in [README.md](README.md#legend).

**Parity column**

| Value | Meaning |
|-------|---------|
| byte-exact | Decompilation that rebuilds the original executable bit for bit |
| behaviour-exact | Original game code executes (static recomp / native runtime), so behaviour is identical by construction |
| enhanced | Rewrite that deliberately changes behaviour (widescreen, fps, QoL). May or may not track the original closely |

**Approach column**

- *rewrite*: hand-written reimplementation of the engine
- *decomp*: matching decompilation to C
- *recomp*: static recompilation of the PS1/PSP executable to native code ([psxrecomp](https://github.com/mstan/psxrecomp) ecosystem)
- *native-runtime*: the PS4 x86-64 binary runs on the host CPU with a replacement system library layer

## WipEout (1995, PS1 / PC)

| Project | Approach | Parity | Activity | Legal | Notes |
|---------|----------|--------|----------|-------|-------|
| [phoboslab/wipeout-rewrite](https://github.com/phoboslab/wipeout-rewrite) | rewrite, C, SDL2/Sokol, also runs in a browser | enhanced | 🟢 | 🟠 leaked-src | The reference (~3k stars). Needs PSX NTSC data plus a few PC-version menu models. Non-commercial clause, no SPDX licence. [Blog](https://phoboslab.org/log/2023/08/rewriting-wipeout) |
| [wipeout-phantom-edition](https://github.com/wipeout-phantom-edition/wipeout-phantom-edition) | fork of wipeout-rewrite | enhanced | ⚫ (2024-08) | 🟠 leaked-src | Easiest "just play": feed it the USA multi-bin `.cue`, it extracts data and music itself. Widescreen, QoL |
| [alexbeavs-ps1-ports/wipeout-recomp](https://github.com/alexbeavs-ps1-ports/wipeout-recomp) | recomp | behaviour-exact | 🟢 | 🟡 orig-code | Europe disc + SCPH-5502 BIOS, code generated locally. GPL-3.0 on project files only |
| [phoboslab/wipeout](https://github.com/phoboslab/wipeout) | WebGL model and track viewer | n/a | 🟡 | 🟢 | 2015 reverse-engineering work the rewrite grew out of |

Ports of wipeout-rewrite, same legal status as upstream:
[Dreamcast](https://github.com/jnmartin84/wipeout-dc) 🟡 ·
[Saturn](https://github.com/FCare/WipeoutSaturn) 🟡 ·
[Switch homebrew](https://github.com/emuman100/wipeout-rewrite-nintendo-switch-homebrew) 🟡 ·
[Playdate](https://github.com/pastasfuture/PastaWipeoutPD) 🟡 ·
[Quest / PICO VR](https://github.com/SgtBilko76/Wipeout-Rewrite-VR) 🟢 ·
[Steam Frame VR](https://github.com/astromaddie/wipeout-vr) 🟢 ·
[Flatpak](https://github.com/leuc/org.phoboslab.wipeout) 🟡 ·
[AppImage](https://github.com/pkgforge-dev/wipEout-Rewrite-AppImage) 🟢

## WipEout 2097 / XL (1996, PS1 / PC)

| Project | Approach | Parity | Activity | Legal | Notes |
|---------|----------|--------|----------|-------|-------|
| [Yash-Singh1/wipeout-xl-decomp](https://github.com/Yash-Singh1/wipeout-xl-decomp) | decomp | byte-exact | 🟢 | 🟡 orig-code | Rebuilds US, EU and JP executables with the original compiler. Partial decomp of the PC release too. PsyQ libs taken from retail exe as asm |
| [Yash-Singh1/wipeout-xl-rewrite](https://github.com/Yash-Singh1/wipeout-xl-rewrite) | rewrite built on the decomp | enhanced, lockstep-tested against recordings | 🟢 | 🟡 orig-code | HD, widescreen, uncapped fps, split-screen, loads WipEout 1 and Wipeout 64 tracks, custom music. Win/mac/web/iOS. Point it at your `.cue` |
| [NJH-1001/Wipeout2K97XL](https://github.com/NJH-1001/Wipeout2K97XL) | recomp, setup kit | behaviour-exact | 🟢 | 🟡 orig-code | USA SCUS-94351, 12-track Redump cue. Win/Linux/mac, OpenBIOS + SDL3, Steam Deck tested |
| [alexbeavs-ps1-ports/wipeout-xl-recomp](https://github.com/alexbeavs-ps1-ports/wipeout-xl-recomp) | recomp | behaviour-exact | 🟢 | 🟡 orig-code | Release candidate, needs retail BIOS |

## Wip3out / WipEout 3 Special Edition (1999-2000, PS1)

| Project | Approach | Parity | Activity | Legal | Notes |
|---------|----------|--------|----------|-------|-------|
| [RetroPortingToolKit/Wipeout-3-Special-Edition-Recomp](https://github.com/RetroPortingToolKit/Wipeout-3-Special-Edition-Recomp) | recomp | behaviour-exact | 🟢 | 🟡 orig-code | WIP, no release builds yet |

No rewrite or decomp found for Wip3out. Gap.

## WipEout Fusion (2002, PS2)

Nothing beyond emulation. See [emulator-helpers.md](emulator-helpers.md) and [tools.md](tools.md). Gap.

## WipEout Pure / Pulse (2005-2007, PSP)

| Project | Approach | Parity | Activity | Legal | Notes |
|---------|----------|--------|----------|-------|-------|
| [erreib/pure-recomp](https://github.com/erreib/pure-recomp) | recomp, Metal (macOS) / Vulkan (Windows) | behaviour-exact | 🟢 | 🟡 orig-code | GPL-2.0. Requires UCUS-98612 v2.00 dump, refuses other editions. Apple Silicon or Win x64 |

No Pulse port found. Gap.

## WipEout HD / Fury (PS3) and 2048 (Vita)

Emulation only. Gap.

## WipEout Omega Collection (2017, PS4)

| Project | Approach | Parity | Activity | Legal | Notes |
|---------|----------|--------|----------|-------|-------|
| [AbdelmoumenDeghbouche/wipeout_pc](https://github.com/AbdelmoumenDeghbouche/wipeout_pc) | native-runtime, shadPS4 video core | behaviour-exact | 🟢 | 🟡 orig-code | GPL-2.0, early. Menus and HD/2048 races above 60 fps, sound unfinished. Needs your PKG dump (`eboot.bin` folder). Same model as bloodborne_pc |
| [jshodanVR/revive-psvr1-wipeout](https://github.com/jshodanVR/revive-psvr1-wipeout) | native-runtime, OpenXR output | behaviour-exact | 🟢 | 🟡 orig-code | GPL-2.0. Base CUSA05670 + 1.07 update PKG. Experimental, visual glitches on some tracks |

## Open-source spiritual successors (not WipEout code)

| Project | Engine | Activity | Legal | Notes |
|---------|--------|----------|-------|-------|
| [Synert/WipeoutClone](https://github.com/Synert/WipeoutClone) | Unity | 🟡 | 🟢 MIT | |
| [Corruptinator/G-Zero](https://github.com/Corruptinator/G-Zero) | Godot | 🟡 | 🟢 | Demo project |
| [fishfolk/drifty](https://github.com/fishfolk/drifty) | Rust / Bevy | 🟢 | 🟢 Apache-2.0 | Arcade racer inspired by several games |

BallisticNG is commercial and closed-source, so not listed.
