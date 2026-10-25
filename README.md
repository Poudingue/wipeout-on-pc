# wipeout-on-pc

A curated index of open-source projects to run, port, mod or study the **WipEout** games on PC.

Nothing is hosted here, only links. Every entry carries a **legal exposure** tag so you know what you are
downloading before you click. Most projects expect you to bring your own legally dumped disc image or PKG.

## Legend

**Legal exposure**: how much Sony material the project itself distributes or executes.

| Tag | Level | Meaning |
|-----|-------|---------|
| 🟢 | Low | Nothing of Sony's in the repo and none executed by it. Clean-room code, format tools, cheat codes, emulators. |
| 🟡 | Moderate | Distributes nothing of Sony's, but **executes Sony's code** from your own dump: static recompilation, native-runtime ports. Also faithful recreations (fonts redrawn by hand). Untested in court. |
| 🟠 | Grey | **Redistributes transformed Sony material**: code derived from the 2022 source leak (author claims fair use, no takedown since 2023), upscaled or repainted textures from the game. |
| 🔴 | High | **Redistributes Sony material as is**: ISOs, DLC content, extracted assets, patches that embed them. |

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

🟢 An emulator plus your own dump, format tools, cheat codes and clean-room fan code distribute and execute nothing
of Sony's. 🟡 Static recompilation and native-runtime ports distribute no Sony bytes and regenerate the game code on
your machine from your dump, but you still execute Sony's copyrighted code, and no court has ruled on it.
🟠 wipeout-rewrite and its derivatives "may or may not" derive from the 2022 leaked PC source according to the author,
who argues fair use; online without takedown since 2023. Texture packs redistribute Sony's art, upscaled.
🔴 Anything embedding DLC, ISOs or extracted assets is plain redistribution, however convenient.

## Contributing

PR a row in the right file. Required: link, one-line description, activity tag, legal tag with a sentence of
justification in *Notes*. Read the README and the release assets of a project before tagging it.
