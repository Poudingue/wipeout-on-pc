# wipeout-on-pc

A curated index of open-source projects to run, port, mod or study the **WipEout** games on PC.

**Rule of the house:** we only reference projects that ship **no copyrighted game material**. Every entry expects
you to bring your own legally dumped disc image or PKG. Projects that redistribute ISOs, extracted assets or DLC
are pointed at, tagged 🔴, and never mirrored.

## Legend

**Legal exposure**

| Tag | Meaning |
|-----|---------|
| 🟢 | Low risk. Clean-room code, tooling, cheat codes, emulators. No Sony bytes, no leaked code. |
| 🟠 | Grey zone. Either derived from the 2022 WipEout source leak (author claims fair use, no takedown so far), or runs/recompiles the game's original executable from *your* dump (no Sony bytes distributed, but Sony code executes), or upscaled/derivative textures. |
| 🔴 | Ships copyrighted material (ISOs, DLC content, extracted assets, patches that embed them). Listed for completeness only. |

**Activity** (last push, as of 2026-10)

| Tag | Meaning |
|-----|---------|
| 🟢 | Active: pushed within the last 3 months |
| 🟡 | Slow: 3 to 18 months |
| ⚫ | Dormant or archived: older than 18 months |

## Index

| File | Content |
|------|---------|
| [reimplementations.md](reimplementations.md) | Source ports, rewrites, decompilations, static recompilations. One game each. Includes a *parity* column (byte-exact / behaviour-exact / enhanced). |
| [emulator-helpers.md](emulator-helpers.md) | Things you load into an emulator to improve a game: cheats (60 fps, unlocks), pnach/RPCS3 patches, texture packs, DLC and "all content" mods. |
| [tools.md](tools.md) | Format tools, extractors, editors, viewers, reverse-engineering documentation. |

## Which emulator for which game

| Game | Platform | Emulator | Notes |
|------|----------|----------|-------|
| WipEout, 2097/XL, Wip3out / 3 SE | PS1 | [DuckStation](https://github.com/stenzek/duckstation), Beetle PSX HW (RetroArch), [PCSX-Redux](https://github.com/grumpycoders/pcsx-redux) | Or skip the emulator: see [reimplementations.md](reimplementations.md) |
| Fusion | PS2 | [PCSX2](https://github.com/PCSX2/pcsx2) | Use the NTSC-U disc for 60 Hz. Widescreen and no-interlace are built-in patches |
| Pure, Pulse | PSP | [PPSSPP](https://github.com/hrydgard/ppsspp) | Both drop to 30 fps under load. Fix in [emulator-helpers.md](emulator-helpers.md) |
| HD / Fury | PS3 | [RPCS3](https://github.com/RPCS3/rpcs3) · [wiki](https://wiki.rpcs3.net/index.php?title=WipEout_HD) | Install game updates before the Fury DLC |
| 2048 | Vita | [Vita3K](https://github.com/Vita3K/Vita3K) · [compat](https://github.com/Vita3K/compatibility/issues/556) | Playable in recent builds, 30 fps cap patchable |
| Omega Collection | PS4 | [shadPS4](https://github.com/shadps4-emu/shadPS4) | Or the native runtime ports in [reimplementations.md](reimplementations.md) |

## Legal landscape in one paragraph

Three tiers. **Lowest risk:** an emulator plus your own dump, format tools, cheat codes, clean-room fan code.
**Middle:** static recompilation and native-runtime ports. They distribute no Sony bytes and regenerate the game
code on your machine from your dump, but you still execute Sony's copyrighted code, and no court has ruled on it.
**Grey:** wipeout-rewrite and its derivatives, which the author says "may or may not" derive from the 2022 leaked PC
source and argues fair use; online without takedown since 2023.
**Excluded:** anything embedding DLC, ISOs or extracted assets, however convenient.

## Contributing

PR a row in the right file. Required: link, one-line description, activity tag, legal tag with a sentence of
justification in *Notes*. Read the README and the release assets of a project before proposing it.
