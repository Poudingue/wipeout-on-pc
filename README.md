# wipeout-on-pc

A curated index of open-source projects to run, port, mod or study the **WipEout** games on PC.

Nothing is hosted here, only links. Every entry carries a **legal exposure** tag so you know what you are
downloading before you click. Most projects expect you to bring your own legally dumped disc image or PKG.

## Legend

**Quality**: the maintainer's opinionated review of each repository's code (structure, genericity, build, tests,
hygiene). This is the primary quality verdict of the index. The Signals badges below are secondary activity facts
and never a quality verdict by themselves.

| Tier | Meaning |
|------|---------|
| 💎 | Exemplary: a model codebase, clean architecture, tests and CI, worth learning from |
| 🥇 | Solid: well structured and maintainable, with minor gaps (tests, CI or docs) |
| 🥈 | Decent: works and reads fine, but carries real structural debt (monoliths, patch stacks, magic numbers) |
| 🥉 | Rough: works or worked, but hacks, god files, hardcoded paths or committed binaries |
| 🚧 | Prototype, stub or abandoned: not usable as a base |
| – | Not code (data, cheats, texture pack, how-to, link page) or not reviewed |

The cell reads tier first, then a one-line verdict, e.g. `🥇 lean C, clean platform split, no tests`.

**Legal exposure**: how much Sony material the project itself distributes or executes.

| Tag | Level | Meaning |
|-----|-------|---------|
| 🟢 | Low | Nothing of Sony's in the repo and none executed by it. Clean-room code, format tools, cheat codes, emulators. |
| 🟡 | Moderate | Distributes nothing of Sony's, but **executes Sony's code** from your own dump: static recompilation, native-runtime ports. Also faithful recreations (fonts redrawn by hand). Untested in court. |
| 🟠 | Grey | **Redistributes transformed Sony material**: code derived from the 2022 source leak (author claims fair use, no takedown since 2023), upscaled or repainted textures from the game. |
| 🔴 | High | **Redistributes Sony material as is**: ISOs, DLC content, extracted assets, patches that embed them. |

**Signals**: factual badges about the repository, collected from the GitHub API on 2026-10-25. Each one is a
single piece of information, never a quality verdict on its own: a repo untouched for years can be clean, a busy
one can be a mess. Quality (above) is the verdict. Non-GitHub entries get `–`.

| Badge | Earned when |
|-------|-------------|
| 🕒 | Pushed within the last 12 months |
| 👥 | At least 3 contributors |
| 🏷️ | Has tagged releases |
| ⚙️ | Has CI (GitHub Actions workflows) |
| 🧪 | Has a test suite (test directory or test files, vendored code excluded) |
| 📜 | Has an explicit licence (SPDX-recognised) |
| 🤖 | AI-assisted: agent config in the repo (CLAUDE.md, AGENTS.md, Cursor/Copilot rules...), AI co-author commit trailers, or stated in the README. No badge means no evidence found, not a guarantee |

**Approach and parity** (reimplementations): 🖊️ rewrite · 🔬 decompilation · 🔁 static recompilation ·
🧬 native runtime · 🍴 fork · 👁️ viewer · 🎯 byte-exact · ✅ behaviour-exact · ✨ enhanced.

**Helper type** (emulator helpers): 🩹 cheat or patch · 🖼️ texture pack · 💿 ISO patch · 📖 how-to · 🧰 misc tool.

## Index

Filterable view of everything below: **[poudingue.github.io/wipeout-on-pc](https://poudingue.github.io/wipeout-on-pc/)**
(a single static page that reads the markdown files, no build step).

Every table has a *Quality* column right after *Project*.

| File | Content |
|------|---------|
| [reimplementations.md](reimplementations.md) | Source ports, rewrites, decompilations, static recompilations, plus open-source spiritual successors. One game each. Includes a *parity* column (byte-exact / behaviour-exact / enhanced). |
| [emulators.md](emulators.md) | Open-source emulators per platform, with a WipEout-specific playability rating (🏁 👍 ⚠️ ⛔ ❓) per game, verified against compat lists and recent reports. |
| [emulator-helpers.md](emulator-helpers.md) | Things you load into an emulator (or the original PC release) to improve a game: cheats (60 fps, unlocks), pnach/RPCS3/Vita patches, texture packs, DLC and "all content" mods, achievements. |
| [tools.md](tools.md) | Format tools, extractors, editors, viewers, mod managers, reverse-engineering documentation, online-play revival infrastructure. |

## Start here

The ⭐ **canon** picks: the absolute go-to for each game, what a fan should try first. Chosen for how well they play
today, then for code quality. Everything else, with ratings, is in the category files and the
[filterable view](https://poudingue.github.io/wipeout-on-pc/) (Canon facet).

| Game | ⭐ Canon | Why |
|------|---------|-----|
| WipEout (1995) | [wipeout-rewrite](https://github.com/phoboslab/wipeout-rewrite) · [DuckStation](https://github.com/stenzek/duckstation) | The native PC rewrite everyone builds on; DuckStation for the untouched original |
| 2097 / XL | [wipeout-xl-rewrite](https://github.com/Yash-Singh1/wipeout-xl-rewrite) · [DuckStation](https://github.com/stenzek/duckstation) | Rewrite on top of a byte-exact decomp, lockstep-tested; DuckStation for the original |
| WipEout 64 | [RMG](https://github.com/Rosalie241/RMG) | Maintained Mupen64Plus frontend, playable |
| Wip3out / SE | [DuckStation](https://github.com/stenzek/duckstation) | Perfect in every region; add hueponik's 60 fps patches for SE (see [emulators.md](emulators.md)) |
| Fusion | [PCSX2](https://github.com/PCSX2/pcsx2) | Perfect; NTSC-U disc for 60 Hz, built-in widescreen patch |
| Pure | [pure-recomp](https://github.com/erreib/pure-recomp) · [PPSSPP](https://github.com/hrydgard/ppsspp) | Native recomp if you have the US v2.00 dump; PPSSPP for every other edition |
| Pulse | [PPSSPP](https://github.com/hrydgard/ppsspp) | Playable, online through AGRF (see [tools.md](tools.md)) |
| HD / Fury | [RPCS3](https://github.com/RPCS3/rpcs3) | Playable with the built-in high-fps and 21:9 patches |
| 2048 | [Vita3K](https://github.com/Vita3K/Vita3K) | Playable in EU/US/Asia releases; JP still has issues |
| Omega Collection | [shadPS4](https://github.com/shadps4-emu/shadPS4) · [wipeout_pc](https://github.com/AbdelmoumenDeghbouche/wipeout_pc) | shadPS4 plays the EU release; wipeout_pc is the most advanced native port (early, sound unfinished) |

## Legal landscape in one paragraph

🟢 An emulator plus your own dump, format tools, cheat codes and clean-room fan code distribute and execute nothing
of Sony's. 🟡 Static recompilation and native-runtime ports distribute no Sony bytes and regenerate the game code on
your machine from your dump, but you still execute Sony's copyrighted code, and no court has ruled on it.
🟠 wipeout-rewrite and its derivatives "may or may not" derive from the 2022 leaked PC source according to the author,
who argues fair use; online without takedown since 2023. Texture packs redistribute Sony's art, upscaled.
🔴 Anything embedding DLC, ISOs or extracted assets is plain redistribution, however convenient.

## Contributing

PR a row in the right file. Required: link, one-line description, Signals badges, legal tag with a sentence of
justification in *Notes*. Read the README and the release assets of a project before tagging it. Leave *Quality*
as `–`: the maintainer fills it in after reviewing the code.
