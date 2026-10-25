# Emulators

Open-source emulators that run the original games from your own dump, one row per emulator and game, with a
WipEout-specific playability rating. Closed-source emulators (ePSXe and the like) are only mentioned in notes.
Legend for *Quality*, *Signals* and *Legal* in [README.md](README.md#legend); *Quality* rates the emulator's
codebase, not how well it runs WipEout.

**Playability**: 🏁 perfect · 👍 playable (minor glitches or needs a setting/patch) · ⚠️ serious issues ·
⛔ unplayable · ❓ no usable evidence. Ratings verified against compat lists and recent reports, 2026-10.

## PlayStation (WipEout, 2097 / XL, Wip3out)

| Project | Quality | Game | Playability | Signals | Legal | Notes |
|---------|---------|------|-------------|---------|-------|-------|
| [DuckStation](https://github.com/stenzek/duckstation) ⭐ | 💎 Clean modular core/util split, CMake, unit and regression tests. | WipEout (1995) | 🏁 | 🕒👥🏷️⚙️🧪🤖 | 🟢 BIOS needed, NC-ND licence | Gamedb NoIssues in all regions, PGXP fixes auto-applied. Widescreen hack stretches the HUD and culls track edges. Prefer US/JP for 60 Hz. Closed-source ePSXe also works, not rated. [compat](https://github.com/stenzek/duckstation/blob/master/data/resources/gamedb.yaml) |
| [DuckStation](https://github.com/stenzek/duckstation) ⭐ | 💎 | 2097 / XL | 🏁 | 🕒👥🏷️⚙️🧪🤖 | 🟢 BIOS needed, NC-ND licence | Gamedb NoIssues (2097 EU, XL US/JP), same PGXP traits. No 60 fps or widescreen cheat in chtdb. [compat](https://github.com/stenzek/duckstation/blob/master/data/resources/gamedb.yaml) |
| [DuckStation](https://github.com/stenzek/duckstation) ⭐ | 💎 | Wip3out | 🏁 | 🕒👥🏷️⚙️🧪🤖 | 🟢 BIOS needed, NC-ND licence | EU SCES-01909 is LibCrypt: needs the .sbi, and set PGXP CPU mode manually. US/JP: upscaling breaks the position counter. Use the native 16:9 mode. [compat](https://github.com/stenzek/duckstation/blob/master/data/resources/gamedb.yaml) |
| [DuckStation](https://github.com/stenzek/duckstation) ⭐ | 💎 | Wip3out SE | 🏁 | 🕒👥🏷️⚙️🧪🤖 | 🟢 BIOS needed, NC-ND licence | Stock game clean. hueponik's 60 fps xdelta patches recommend it; 8 MB mode needs the 8 MB RAM option plus an overclock. Patches self-described as not thoroughly tested. [compat](https://github.com/stenzek/duckstation/blob/master/data/resources/gamedb.yaml) |
| [SwanStation](https://github.com/libretro/swanstation) | 🥇 2021 DuckStation architecture, now hardened with save-state validation tests. | 2097 / XL | 👍 | 🕒👥⚙️🧪📜 | 🟢 BIOS recommended | Indirect: the working reference in the last-CD-track loop bug reports. No per-game settings, set PGXP CPU mode manually. [issue](https://github.com/libretro/pcsx_rearmed/issues/887) |
| [SwanStation](https://github.com/libretro/swanstation) | 🥇 | Wip3out | 👍 | 🕒👥⚙️🧪📜 | 🟢 BIOS recommended | Loops the final 'Xpander' CD track correctly where Beetle fails (US, 2025 and 2026-06). EU needs the .sbi. Use the native 16:9 mode. [issue](https://github.com/libretro/beetle-psx-libretro/issues/924) |
| [PCSX-Redux](https://github.com/grumpycoders/pcsx-redux) | 🥇 Modern C++ dev/debug emulator, sanitizer and coverage CI, legacy core. | WipEout (1995) | 👍 | 🕒👥⚙️🧪📜🤖 | 🟢 OpenBIOS bundled | US hung at the title screen under OpenBIOS until PR #2272 (2026-10-10); a real BIOS always worked. No PGXP, widescreen or 60 fps: a debugging tool. [issue](https://github.com/grumpycoders/pcsx-redux/issues/1913) |
| [PCSX-Redux](https://github.com/grumpycoders/pcsx-redux) | 🥇 | Wip3out SE | 👍 | 🕒👥⚙️🧪📜🤖 | 🟢 OpenBIOS bundled | First-loading-screen freeze from cue/bin fixed 2023-08. Boot confirmed, full races not reported: a weak 👍. [issue](https://github.com/grumpycoders/pcsx-redux/issues/1395) |
| [Beetle PSX / PSX HW](https://github.com/libretro/beetle-psx-libretro) | 🥈 Accurate Mednafen core, flat libretro glue, heavy 2026 AI-driven churn. | WipEout (1995) | 👍 | 🕒👥⚙️🧪📜🤖 | 🟢 BIOS recommended | Last CD track 'Transvaal' does not loop: set CD access method = Precache. Toggling fullscreen during FMVs garbles them. [issue](https://github.com/libretro/beetle-psx-libretro/issues/924) |
| [Beetle PSX / PSX HW](https://github.com/libretro/beetle-psx-libretro) | 🥈 | 2097 / XL | 👍 | 🕒👥⚙️🧪📜🤖 | 🟢 BIOS recommended | Last track 'Body in Motion' goes silent instead of looping; Precache still fixes it on current cores. Standalone Mednafen is unaffected. [issue](https://github.com/libretro/beetle-psx-libretro/issues/924) |
| [Beetle PSX / PSX HW](https://github.com/libretro/beetle-psx-libretro) | 🥈 | Wip3out | 👍 | 🕒👥⚙️🧪📜🤖 | 🟢 BIOS recommended | Same 'Xpander' loop bug, Precache fixes it. EU needs the .sbi. The texture packs in [emulator-helpers.md](emulator-helpers.md) target Beetle PSX HW. [issue](https://github.com/libretro/beetle-psx-libretro/issues/924) |
| [Beetle PSX / PSX HW](https://github.com/libretro/beetle-psx-libretro) | 🥈 | Wip3out SE | 👍 | 🕒👥⚙️🧪📜🤖 | 🟢 BIOS recommended | Recommended by hueponik's 60 fps patches (8 MB RAM option plus overclock). Loop bug inferred, Precache. No direct gameplay report. [compat](https://codeberg.org/hueponik/wip3out-patches) |
| [PCSX-ReARMed](https://github.com/notaz/pcsx_rearmed) | 🥈 Fast legacy PCSX plugin design, ARM dynarec, actively maintained by notaz. | WipEout (1995) | 👍 | 🕒👥🏷️⚙️🧪📜 | 🟢 HLE BIOS built in | Music crackling fixed 2022, last-track loop fixed 2025-12-14. No PGXP. Load cue/chd, not a bare .bin. Good on weak ARM devices. [issue](https://github.com/libretro/pcsx_rearmed/issues/593) |
| [PCSX-ReARMed](https://github.com/notaz/pcsx_rearmed) | 🥈 | 2097 / XL | 👍 | 🕒👥🏷️⚙️🧪📜 | 🟢 HLE BIOS built in | Final track loop fixed 2025-12-14 (940f8ac): use a newer core. No PGXP. [issue](https://github.com/libretro/pcsx_rearmed/issues/887) |
| [PCSX-ReARMed](https://github.com/notaz/pcsx_rearmed) | 🥈 | Wip3out | 👍 | 🕒👥🏷️⚙️🧪📜 | 🟢 HLE BIOS built in | 'Xpander' loop fixed 2025-12-14. EU needs the LibCrypt .sbi. [issue](https://github.com/libretro/pcsx_rearmed/issues/887) |
| [PCSX-ReARMed](https://github.com/notaz/pcsx_rearmed) | 🥈 | Wip3out SE | 👍 | 🕒👥🏷️⚙️🧪📜 | 🟢 HLE BIOS built in | Mid-race softlock with arm32 dynarec plus NEON GPU fixed 2022-01. On old arm32 builds, update or disable the dynarec. [issue](https://github.com/libretro/pcsx_rearmed/issues/589) |
| [SwanStation](https://github.com/libretro/swanstation) | 🥇 | WipEout (1995) | ❓ | 🕒👥⚙️🧪📜 | 🟢 BIOS recommended | No direct report; the 2021 DuckStation core should work. Set PGXP CPU mode manually. Use a Sony BIOS: OpenBIOS hung the US release in Redux. [issue](https://github.com/grumpycoders/pcsx-redux/issues/1913) |
| [SwanStation](https://github.com/libretro/swanstation) | 🥇 | Wip3out SE | ❓ | 🕒👥⚙️🧪📜 | 🟢 BIOS recommended | No report. The core exposes 'Enable 8MB RAM', so hueponik's 8 MB 60 fps mode is possible with an overclock. |
| [PCSX-Redux](https://github.com/grumpycoders/pcsx-redux) | 🥇 | 2097 / XL | ❓ | 🕒👥⚙️🧪📜🤖 | 🟢 OpenBIOS bundled | No issue or report found. |
| [PCSX-Redux](https://github.com/grumpycoders/pcsx-redux) | 🥇 | Wip3out | ❓ | 🕒👥⚙️🧪📜🤖 | 🟢 OpenBIOS bundled | No issue or report found. |

## Sega Saturn (WipEout, 2097)

| Project | Quality | Game | Playability | Signals | Legal | Notes |
|---------|---------|------|-------------|---------|-------|-------|
| [Ymir](https://github.com/ymir-emu/Ymir) | 💎 Modern C++20, clean core/app split, tests, docs, presets. Exemplary. | WipEout (1995) | 👍 | 🕒👥🏷️⚙️🧪📜 | 🟢 BIOS needed | Saturn version. Official list: Playable in US, EU and JP. Menu input bug fixed June 2025: use 0.1.6+ (current 0.4.1). [compat](https://docs.google.com/spreadsheets/d/1SLZzL9LelSlpEmTKy8cjaQnE7mew2uW1rfCgcekO58Q/edit?usp=sharing) |
| [Ymir](https://github.com/ymir-emu/Ymir) | 💎 | 2097 / XL | 👍 | 🕒👥🏷️⚙️🧪📜 | 🟢 BIOS needed | Saturn version (2097 EU, XL JP; no US release). Playable since 0.1.7. Accurate SCU DSP timing is CPU-heavy, a DSP JIT is planned. [compat](https://docs.google.com/spreadsheets/d/1SLZzL9LelSlpEmTKy8cjaQnE7mew2uW1rfCgcekO58Q/edit?usp=sharing) |
| [Mednafen](https://mednafen.github.io/) | 🥇 Accuracy-first, per-game cache DB; monolithic, tarball-only, no tests. | WipEout (1995) | 👍 | – | 🟢 BIOS needed | Saturn version. The built-in DB auto-applies a cache-emulation fix for the hang when exiting a race, all regions. No playthrough report. [compat](https://mednafen.github.io/documentation/ss.html) |
| [Mednafen](https://mednafen.github.io/) | 🥇 | 2097 / XL | 👍 | – | 🟢 BIOS needed | Saturn version. No known issue in the fix DB; only a gameplay test video. Low confidence. [video](https://www.youtube.com/watch?v=5-EJyW85qRY) |
| [Beetle Saturn](https://github.com/libretro/beetle-saturn-libretro) | 🥈 Mednafen core plus libretro glue; inherits accuracy, little structure of its own. | WipEout (1995) | 👍 | 🕒👥🧪📜🤖 | 🟢 BIOS needed | Saturn version. Ships Mednafen's DB entries, so the race-exit hang fix applies automatically. No core-specific issues. [compat](https://github.com/libretro/beetle-saturn-libretro/blob/master/mednafen/ss/db.c) |
| [Beetle Saturn](https://github.com/libretro/beetle-saturn-libretro) | 🥈 | 2097 / XL | 👍 | 🕒👥🧪📜🤖 | 🟢 BIOS needed | Saturn version. Inferred from upstream Mednafen, no core-specific report. Low confidence. |
| [Kronos](https://github.com/FCare/Kronos) | 🥉 Sprawling Yabause fork; odd default branch, no root licence. | WipEout (1995) | 👍 | 🕒👥🏷️⚙️ | 🟢 BIOS recommended | Saturn version. Archived community list: Playable in EU, JP and US on 2.1.5 (around 2021). Needs an OpenGL 4.3 GPU. [compat](https://web.archive.org/web/20211201101710/http://tradu-france.com/tfwiki-1.28.2/index.php?title=Compatibility_list_of_Kronos) |
| [Kronos](https://github.com/FCare/Kronos) | 🥉 | 2097 / XL | 👍 | 🕒👥🏷️⚙️ | 🟢 BIOS recommended | Saturn version. Only XL JP listed, Playable on 2.1.5 (around 2021); EU untested. [compat](https://web.archive.org/web/20211201101710/http://tradu-france.com/tfwiki-1.28.2/index.php?title=Compatibility_list_of_Kronos) |
| [Yaba Sanshiro](https://github.com/libretro/yabause/tree/yabasanshiro) | 🥉 Aging Yabause codebase; upstream source repo gone from GitHub. | WipEout (1995) | 👍 | 🕒👥⚙️ | 🟢 BIOS recommended | Saturn version. Only gameplay videos of the Android app, none of the libretro core. Low confidence, prefer Ymir or Mednafen. [video](https://www.youtube.com/watch?v=LbeNnL2kcWE) |
| [Yaba Sanshiro](https://github.com/libretro/yabause/tree/yabasanshiro) | 🥉 | 2097 / XL | ❓ | 🕒👥⚙️ | 🟢 BIOS recommended | Saturn version. No usable report. |

## Nintendo 64 (WipEout 64)

| Project | Quality | Game | Playability | Signals | Legal | Notes |
|---------|---------|------|-------------|---------|-------|-------|
| [Mupen64Plus](https://github.com/mupen64plus/mupen64plus-core) | 🥈 Venerable plugin-based C core; dated structure, no tests. | WipEout 64 | 👍 | 🕒👥🏷️⚙️🤖 | 🟢 | USA ROM registers several inputs per press (CountPerOp=1). Fixed in master 2025-12, not in 2.6.0: use --set Core[CountPerOp]=2. GLideN64 rates it Perfect. [issue](https://github.com/mupen64plus/mupen64plus-core/issues/1160) |
| [RMG](https://github.com/Rosalie241/RMG) ⭐ | 🥈 Tidy Qt frontend over bundled Mupen64Plus core and plugins. | WipEout 64 | 👍 | 🕒👥🏷️⚙️📜 | 🟢 | Same USA multi-input bug: v0.9.0 still sets CountPerOp=1, only master after 2026-09-28 is fixed. Set CountPerOp to 2 in the game settings. [issue](https://github.com/Rosalie241/RMG/issues/376) |
| [simple64](https://github.com/simple64/simple64) | 🥈 Accurate m64p bundle (parallel-RDP/RSP); archived Feb 2025. | WipEout 64 | 👍 | 👥🏷️⚙️📜 | 🟢 | Controller Pak saves fail on USA and the repo is archived: use savestates. Races and input are fine. [issue](https://github.com/simple64/simple64/issues/471) |
| [Project64](https://github.com/project64/project64) | 🥈 Windows-centric MSVC codebase; mature RDB, no Actions CI. | WipEout 64 | 👍 | 🕒👥🏷️📜 | 🟢 | RDB marks E and U Compatible. Counter Factor=1 on U may cause the multi-input menu bug (unverified): try 2. Time-trial freezes also happen on real hardware. [compat](https://github.com/project64/project64/blob/develop/Config/Project64.rdb) |
| [Mupen64Plus-Next](https://github.com/libretro/mupen64plus-libretro-nx) | 🥈 Well-kept libretro port of Mupen64Plus with GLideN64/parallel-RDP. | WipEout 64 | 👍 | 🕒👥🏷️⚙️📜 | 🟢 | Embedded ini still has CountPerOp=1 for USA: set the 'Count Per Op' core option to 2. Europe is fine as is. [compat](https://github.com/libretro/mupen64plus-libretro-nx/blob/develop/custom/mupen64plus-core/main/mupen64plus.ini.h) |
| [ParaLLEl N64](https://github.com/libretro/parallel-n64) | 🥉 Kitchen-sink of old plugins plus parallel-RDP; hard to navigate. | WipEout 64 | 👍 | 🕒👥⚙️🧪🤖 | 🟢 | Old Glide64/Rice bugs fixed. Ini still sets CountPerOp=1 for USA, multi-input likely (untested): use the EU ROM. Prefer the parallel-RDP renderer. [compat](https://github.com/libretro/parallel-n64/blob/master/mupen64plus-core/src/main/mupen64plus.ini.h) |
| [ares](https://github.com/ares-emulator/ares) | 🥇 Accuracy-focused multi-system; custom nall/hiro stack, CPU test suites. | WipEout 64 | ⚠️ | 🕒👥🏷️⚙️🧪 | 🟢 | EU: menu glitches fixed in v148, random hangs within minutes still open. The game crashes on real hardware too, but more often here. Savestate often. [issue](https://github.com/ares-emulator/ares/issues/2326) |
| [gopher64](https://github.com/gopher64/gopher64) | 🥇 Compact, readable Rust LLE emulator; good CI, few tests. | WipEout 64 | ❓ | 🕒👥🏷️⚙️📜 | 🟢 | No report. LLE with parallel-RDP should behave like simple64, unverified. |

## PC, MS-DOS and Windows 9x (WipEout, 2097 / XL)

| Project | Quality | Game | Playability | Signals | Legal | Notes |
|---------|---------|------|-------------|---------|-------|-------|
| [DOSBox Staging](https://github.com/dosbox-staging/dosbox-staging) | 💎 Modern C++, tests, linters, static analysis, strict review culture. | WipEout (1995) | 👍 | 🕒👥🏷️⚙️🧪🤖 | 🟢 | MS-DOS CD version, full speed. The in-game SFX slider is an SFX/CD balance. If CD audio drowns effects: sbmixer=false, then 'mixer sb 80 cdaudio 70' after imgmount. [issue](https://github.com/dosbox-staging/dosbox-staging/issues/474) |
| [86Box](https://github.com/86Box/86Box) | 🥇 Accurate, well-organised device model; C legacy from PCem. | 2097 / XL | 👍 | 🕒👥🏷️⚙️📜🤖 | 🟢 BIOS ROMs, own Win9x | Windows 95 Direct3D version. S3 Trio plus emulated Voodoo2, DirectX 7a and the reference Voodoo2 driver, not the bundled DX3. Fullscreen only. 2017 guide. [compat](https://virtuallyfun.com/2017/06/23/using-voodoo-2-emulation-pcem-86box/) |
| [DOSBox-X](https://github.com/joncampbell123/dosbox-x) | 🥈 Feature-maximal, sprawling codebase; strong CI, uneven structure. | WipEout (1995) | 👍 | 🕒👥🏷️⚙️🧪📜🤖 | 🟢 | MS-DOS CD version. 'Works fine' (one tester, 2020). Missing effects come from the in-game music/SFX balance. Mount a CD image for the music. [issue](https://github.com/joncampbell123/dosbox-x/issues/1809) |
| [PCem](https://github.com/sarah-walker-pcem/pcem) | 🥈 Solid pioneer, slow cadence, largely superseded by 86Box. | 2097 / XL | 👍 | 🕒👥🏷️⚙️📜 | 🟢 BIOS ROMs, own Win9x | Windows 95 Direct3D version. Same 2017 guide: Pentium Overdrive 166, Voodoo2, DirectX 7a. 86Box is the better-maintained choice. [compat](https://virtuallyfun.com/2017/06/23/using-voodoo-2-emulation-pcem-86box/) |
| [GLRage](https://github.com/ata4/glrage) | 🥈 Small focused ATI3DCIF/DDraw-to-OpenGL wrapper with exe patching. | WipEout (1995) | 👍 | 👥🏷️📜 | 🟢 | Wrapper for the Win95 ATI 3D Rage Edition (Sony Vaio OEM) only, no DOS support. 'Runs mostly stable', polygons wobble at high resolutions. Inactive since 2018. [compat](https://github.com/ata4/glrage) |
| [DOSBox](https://sourceforge.net/projects/dosbox/) | 🥉 Venerable reference, legacy codebase, stagnant since 0.74-3. | WipEout (1995) | 👍 | – | 🟢 | MS-DOS CD version, 100% on 0.70. Cap cycles (about 80000) or it runs too fast; imgmount the CD to avoid crashes when CD audio starts. No Win9x, so no 2097 PC. [compat](https://www.dosbox.com/comp_list.php?showID=724&letter=W) |
| [DOSBox Staging](https://github.com/dosbox-staging/dosbox-staging) | 💎 | 2097 / XL | ❓ | 🕒👥🏷️⚙️🧪🤖 | 🟢 own Win9x | Windows 95 version needs an unofficial Win9x guest; Voodoo emulation had stability problems. Direct3D only, so Glide wrappers do not apply. No report. |
| [86Box](https://github.com/86Box/86Box) | 🥇 | WipEout (1995) | ❓ | 🕒👥🏷️⚙️📜🤖 | 🟢 BIOS ROMs, own Win9x | No report for the DOS CD version (Pentium plus SB16 should do) or the ATI Rage Edition (needs ATI3DCIF drivers, unconfirmed). |
| [DOSBox-X](https://github.com/joncampbell123/dosbox-x) | 🥈 | 2097 / XL | ❓ | 🕒👥🏷️⚙️🧪📜🤖 | 🟢 own Win9x | Windows 95 version possible in theory with a Win9x guest and Voodoo emulation. No report. |
| [PCem](https://github.com/sarah-walker-pcem/pcem) | 🥈 | WipEout (1995) | ❓ | 🕒👥🏷️⚙️📜 | 🟢 BIOS ROMs | MS-DOS CD version: no report. |

## PlayStation 2 (Fusion)

| Project | Quality | Game | Playability | Signals | Legal | Notes |
|---------|---------|------|-------------|---------|-------|-------|
| [PCSX2](https://github.com/PCSX2/pcsx2) ⭐ | 🥇 Huge legacy core, heavily modernized; Qt frontend, CI, regression tests | Fusion | 🏁 | 🕒👥🏷️⚙️🧪📜🤖 | 🟢 BIOS needed | GameIndex Perfect, PAL and NTSC-U. Use NTSC-U for 60 Hz and built-in widescreen/no-interlace patches. Dolby intro FMV is silent, keep stereo. NeGcon needs 2.6. PAL demo unrated. [compat](https://raw.githubusercontent.com/PCSX2/pcsx2/master/bin/resources/GameIndex.yaml) |
| [Play!](https://github.com/jpd002/Play-) | 🥇 Clean portable C++ HLE design, many frontends, ctest in CI | Fusion | ⛔ | 🕒👥🏷️⚙️🧪📜 | 🟢 no BIOS (HLE) | Compat 'ingame'. 2024 report (v0.66): crashes at the start of lap 3 in every race, Vulkan and GL, still open. Needs a re-test on 0.77. [issue](https://github.com/jpd002/Play-/issues/1409) |
| [DobieStation](https://github.com/PSI-Rockin/DobieStation) | 🥈 Readable young core, dormant since 2021, not for general use | Fusion | ❓ | 👥⚙️📜 | 🟢 BIOS needed | No report. Dormant since 2021, use PCSX2. |

## PSP (Pure, Pulse)

| Project | Quality | Game | Playability | Signals | Legal | Notes |
|---------|---------|------|-------------|---------|-------|-------|
| [PPSSPP](https://github.com/hrydgard/ppsspp) ⭐ | 💎 Reference PSP emulator: modular Core/GPU/Common, many backends, headless test harness. | Pure | 👍 | 🕒👥🏷️⚙️🧪🤖 | 🟢 no firmware (HLE) | Game drops itself to 30 fps on explosions: NR74W 60 fps CWCheat (EU addresses) fixes it. Effects auto-fixed via compat.ini. No online racing ever existed; ad hoc untested. [issue](https://github.com/hrydgard/ppsspp/issues/12273) |
| [PPSSPP](https://github.com/hrydgard/ppsspp) ⭐ | 💎 | Pulse | 👍 | 🕒👥🏷️⚙️🧪🤖 | 🟢 no firmware (HLE) | Smoother than Pure. DLC needs v1.20.2+, matching region. Online works on the AGRF server (DNS auto since v1.19); opponent ship textures corrupted. Ad hoc untested. [compat](https://www.ppsspp.org/docs/multiplayer/infrastructure-servers/) |
| [JPCSP](https://github.com/jpcsp/jpcsp) | 🥈 Accurate-leaning Java HLE emulator: monolithic, Ant build, slow, barely maintained. | Pure | ❓ | 🕒👥🏷️⚙️🧪📜🤖 | 🟢 no firmware (HLE) | Only old HLE tickets naming the game, no play reports. Much heavier than PPSSPP. [issue](https://github.com/jpcsp/jpcsp/issues/9) |
| [JPCSP](https://github.com/jpcsp/jpcsp) | 🥈 | Pulse | ❓ | 🕒👥🏷️⚙️🧪📜🤖 | 🟢 no firmware (HLE) | No report. |

## PlayStation 3 (HD / Fury)

| Project | Quality | Game | Playability | Signals | Legal | Notes |
|---------|---------|------|-------------|---------|-------|-------|
| [RPCS3](https://github.com/RPCS3/rpcs3) ⭐ | 🥇 Mature, well-structured LLVM-based emulator; strong CI, thin test suite. | HD / Fury | 👍 | 🕒👥🏷️⚙️🧪📜🤖 | 🟢 firmware needed (free from Sony) | Playable (PSN HD, Fury disc). Write color buffers ON, avoid Relaxed XFloat. Update to 2.51 before the Fury DLC. Medals missing on AMD. Asia PSN untested. [compat](https://rpcs3.net/compatibility?api=v1&g=wipeout) |

## PS Vita (2048)

| Project | Quality | Game | Playability | Signals | Legal | Notes |
|---------|---------|------|-------------|---------|-------|-------|
| [Vita3K](https://github.com/Vita3K/Vita3K) ⭐ | 🥈 Modular HLE codebase, active, but still maturing with regressions. | 2048 | 👍 | 🕒👥🏷️⚙️🧪📜🤖 | 🟢 firmware needed (free from Sony) | EU/US v1.04 on desktop Vulkan. Audio dropouts, dark lighting. Remove PSN sign-in if loading hangs. 30 fps cap: FPS hack. JP PCSC00006: ⚠️ load hang. Flaky on macOS/Android. [compat](https://github.com/Vita3K/compatibility/issues/556) |

## PlayStation 4 (Omega Collection)

| Project | Quality | Game | Playability | Signals | Legal | Notes |
|---------|---------|------|-------------|---------|-------|-------|
| [shadPS4](https://github.com/shadps4-emu/shadPS4) ⭐ | 🥇 Clean modular C++20 core, real shader recompiler, very active. | Omega Collection | 👍 | 🕒👥🏷️⚙️🧪📜🤖 | 🟢 firmware modules needed | EU CUSA05670: enable Readback Linear Images, firmware .prx in sys_modules; Intel may need Red zone Static Patching. Wrong lighting. US CUSA07671: ⚠️ missing graphics or crashes. [compat](https://github.com/shadps4-compatibility/shadps4-game-compatibility/issues/487) |
| [Obliteration](https://github.com/obhq/obliteration) | 🥇 Careful Rust kernel + VMM design, but runs no games yet. | Omega Collection | ⛔ | 🕒👥⚙️📜 | 🟢 system software needed | README: 'Currently we cannot run any games yet'. |
| [fpPS4](https://github.com/red-prig/fpPS4) | 🥉 Pascal, mostly one-man, core rewrite pending; no tests. | Omega Collection | ⛔ | 🕒👥🏷️⚙️📜 | 🟢 | Never boots (EU out of device memory, US format assert, 2024). No per-game support until the core rewrite. [compat](https://github.com/red-prig/fpps4-game-compatibility/issues/1055) |
| [Kyty](https://github.com/InoriRus/Kyty) | 🥈 Tidy C++ with unit tests, abandoned since 2022. | Omega Collection | ❓ | 🏷️⚙️🧪📜 | 🟢 | No report. Only simple PS4 games run, no audio or video. Abandoned 2022. |

## Gaps

Pairs with no usable evidence that are worth a test run (PR a report or a compat link):

- **SwanStation**: WipEout (1995) with a real BIOS vs OpenBIOS, Wip3out SE with the 8 MB 60 fps patch.
- **PCSX-Redux**: 2097 / XL, Wip3out.
- **Yaba Sanshiro** (libretro core): 2097 / XL on Saturn, and WipEout itself (only Android app videos so far).
- **gopher64**: WipEout 64.
- **86Box / PCem**: WipEout MS-DOS CD; 86Box with the ATI 3D Rage Edition.
- **DOSBox-X / DOSBox Staging**: 2097 / XL Windows 95 in a Win9x guest with Voodoo emulation.
- **PCSX2**: Fusion PAL demo (SCED-50768). **Play!**: Fusion re-test on 0.77.
- **PPSSPP**: Pure and Pulse ad hoc local multiplayer.
- **JPCSP**: Pure, Pulse.
- **RPCS3**: HD Asia PSN (NPHA80039).
- **Vita3K**: 2048 JP (PCSC00006) with PSN signed out.
