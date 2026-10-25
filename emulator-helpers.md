# Emulator helpers

Patches, cheats, texture packs and mods you load into an emulator to alter or improve a game. Legend in
[README.md](README.md#legend). *Quality* reviews the code where there is code; data, packs and how-tos get `–`.

Rule of thumb for the legal tag: a **cheat code or pnach** is a handful of addresses and values, 🟢. A **texture
pack** redistributes Sony's art, upscaled, 🟠. A **patched ISO or xdelta that embeds DLC** carries
Sony's content, 🔴, even when the repo itself holds no ISO.

## PS1 (DuckStation, Beetle PSX HW)

| Project | Quality | Game | Type | Signals | Legal | Notes |
|---------|---------|------|------|----------|-------|-------|
| [duckstation/chtdb](https://github.com/duckstation/chtdb) | – | WipEout, 2097 / XL, Wip3out / 3 SE | 🩹 DuckStation's official cheat database (GameShark `.cht`) | 🕒👥🏷️⚙️ | 🟢 | Ships with DuckStation. One file per serial, covering every US/EU/JP release plus Wip3out SE: Rapier/Phantom unlocks, infinite weapons and energy, Wip3out SE prototype mode. No 60 fps or widescreen patches for the series yet. CI validates submissions |
| [Yash-Singh1/wipeout-xl-60fps](https://github.com/Yash-Singh1/wipeout-xl-60fps) | 🥈 Careful hash-checked patch generator; one 816-line script, backup cruft | 2097 | 🩹 DuckStation `.cht` 60 fps patch, USA (SCUS-94351) | 🕒🤖 | 🟢 | Gameplay renders at 60 fps while physics, race clock, weapons and AI stay at 30 Hz through gated code caves. Menus stay at 30. Requests a 250% CPU overclock. A Python builder regenerates the patch from your own exe and refuses any other hash. The author says it is AI-written and buggy: some objects run at 2x because binary space ran out. No game data, no licence |
| [hueponik/wip3out-patches](https://codeberg.org/hueponik/wip3out-patches) | – | Wip3out SE | 💿 xdelta3 patches vs PAL SCES-02845 (single-bin or track 01): 25/30/50/60/100 fps, in-game options menu (Start+Select in pause) saved to memory card, extended draw distance and detail on 8 MB RAM | – | 🟢 diff only | Small code diffs against your own image with no Sony assets embedded, but the patch source is not published so this cannot be verified. NTSC variants give 30/60 and PAL 25/50/100. 8 MB mode needs DuckStation/GooseStation/Beetle with overclock, and 100 fps needs GooseStation PAL x2. Also runs on real hardware and MiSTer at stock rates. Author says it is lightly tested. Codeberg, 2026 |
| [ShaolinAssassin/PSOne-Dithering-OFF-patches](https://github.com/ShaolinAssassin/PSOne-Dithering-OFF-patches) | – | WipEout, 2097/XL | 🩹 GameShark/AR codes: disable dithering | 🏷️ | 🟢 | Codes by krHACKen for WipEout US (SCUS-94301) and UK v1.0/1.1, Wipeout XL US, WipEout 2097 UK (SLES-00327). Generic multi-game repo. Mostly redundant with the emulators' own dithering toggles, useful on software renderers or real hardware |
| [Wip3out SE NTSC 30 fps conversion (archive.org)](https://archive.org/details/wipeout-3-s.-e.-pal-2-ntsc.chd.-7z) | – | Wip3out SE | 💿 PAL-to-NTSC conversion (30 fps), shipped as a full CHD disc image | – | 🔴 full ISO | Anonymous upload (2025-03), updated 2026-08 to centre the picture. No patch file or list of changes, only the whole disc. Aimed at Batocera. A patch-only version (xdelta) would make this 🟢 |
| [princepeter64/Wip3out-HD-Texture-Pack](https://github.com/princepeter64/Wip3out-HD-Texture-Pack) | – | Wip3out / 3 SE | 🖼️ texture pack, Beetle PSX HW | – | 🟠 derivative | |
| [Matsilagi/WO3-Beta-Texturepack](https://github.com/Matsilagi/WO3-Beta-Texturepack) | – | Wip3out SE | 🖼️ beta-look texture pack, Beetle PSX HW | – | 🟠 derivative | |
| [tigrouind/wipeout-autopilot](https://github.com/tigrouind/wipeout-autopilot) | 🚧 Neat 159-line Lua PID hack; hardcoded Feisar/PAL addresses | 2097 | 🧰 BizHawk Lua autopilot | 📜 | 🟢 MIT | Curiosity. Feisar only, PAL only, steering only (no throttle or weapons) |
| [tre3qwerty/Wipeout-2097-Auto-Splitter](https://github.com/tre3qwerty/Wipeout-2097-Auto-Splitter) | 🥉 Right emu-help approach; NTSC-only addresses, copy-paste lap watchers | 2097 | 🧰 LiveSplit autosplitter | – | 🟢 | Speedrunning. NTSC (Wipeout XL) only, needs emu-help-v2 |
| [suXinjke/RAScripts: Wipeout.ts](https://github.com/suXinjke/RAScripts/blob/master/js/Duckstation/Wipeout.ts) | 🥈 Compact data-driven achievement script; magic RAM addresses undocumented | WipEout | 🧰 RetroAchievements set source (cruncheevos, TypeScript) | 🕒🤖 | 🟢 | Source of the 14 Time Trial achievements of RA set [11378](https://retroachievements.org/game/11378), played through RetroAchievements in DuckStation or Beetle. Doubles as a map of useful RAM addresses (track ID, race state, timer). Part of a multi-game repo, no licence |

## Saturn (Kronos, Beetle Saturn, Ymir)

| Project | Quality | Game | Type | Signals | Legal | Notes |
|---------|---------|------|------|----------|-------|-------|
| [SegaXtreme: resolution hacks thread, p.7](https://segaxtreme.net/threads/screeen-resolution-hacks.24034/page-7) | – | 2097 (Saturn PAL) | 🩹 CEP / Action Replay codes: widescreen, transparent shadows/HUD, 20 fps cap removal | – | 🟢 | Post #126 (Esppiral, Aug 2020) gives the CEP codes. AR conversions are in #133–#135. One tester got transparent HUD and shadows working, but the rear-light code breaks lighting and the others crashed. Uncapped runs at 'sometimes 60, mostly ~30 fps'. Untested in emulators, so treat it as experimental. Codes only |

## PC originals (Windows 9x releases, wrappers, VMs)

| Project | Quality | Game | Type | Signals | Legal | Notes |
|---------|---------|------|------|----------|-------|-------|
| [ata4/glrage](https://github.com/ata4/glrage) | 🥇 Clean modular C++ wrapper; VS2015-only, external SDK, no tests | WipEout (ATI 3D Rage Edition) | 🧰 OpenGL wrapper for ATI 3D CIF + DirectDraw 2, with runtime memory patches | 👥🏷️📜 | 🟢 LGPL-3.0 | Runs the ATI Rage edition of PC WipEout (bundled with Sony Vaio PCV) on modern Windows at high resolutions. Forced patches stop the game from changing key-repeat and screensaver settings and remove a bugged alt+tab check. Title screen and intro skips are optional. Wobbly polygons at high resolution (low subpixel precision). The DOS version is not supported. Recommended by PCGamingWiki. Dormant since 2018 |
| [PCGamingWiki: Wipeout 2097](https://www.pcgamingwiki.com/wiki/Wipeout_2097) · [Wipeout](https://www.pcgamingwiki.com/wiki/Wipeout) | – | WipEout, 2097 (Windows 1996-97) | 📖 how-to | – | 🟢 how-to only | 2097: hex-edit widescreen fix for `Wipeout2.exe`, and forcing a 30 Hz refresh rate with Special K (other rates run too fast or become unplayable). WipEout page: GLRage for the ATI Rage edition, plus pointers to Phantom Edition and wipEout Rewrite |
| [WipeoutZone: Running 2097/XL on Windows 8.1](https://www.wipeoutzone.com/forum/archive/index.php/t-9964.html) | – | 2097 / XL (PC) | 📖 how-to: dgVoodoo2 in place of 3dfx/Glide | – | 🟢 how-to only | Demos work, retail flaky, game runs too fast. dgVoodoo 2.63+ crashes after PRESS START ([Vogons](https://www.vogons.org/viewtopic.php?t=73450)), so use an older build. Overspeed above 30 Hz is documented on [PCGamingWiki](https://www.pcgamingwiki.com/wiki/Wipeout_2097) (Special K 30 Hz). See also the [speed patch thread](https://www.wipeoutzone.com/forum/archive/index.php/t-1963.html). Site often returns HTTP 500 |
| [WipEout XL Network Patch v0.9 beta (archive.org)](https://archive.org/details/WOXLN1) | – | 2097 / XL (PC) | 🩹 official Psygnosis 1997 patch: IPX, TCP/IP, direct-link and modem multiplayer | – | 🔴 Sony binary | Psygnosis gave it away for free at the time; preserved on archive.org since 2016 (456 KB zip and readme). Works with both the XL and 2097 PC releases. IPX over DOSBox or a VM LAN is the realistic way to use it today. For an open-source lobby replacement see VidyaGod in [tools.md](tools.md) |

## PS2 (PCSX2)

| Project | Quality | Game | Type | Signals | Legal | Notes |
|---------|---------|------|------|----------|-------|-------|
| [fvhcookie-bit/wipeout-fusion-arcade-settings](https://github.com/fvhcookie-bit/wipeout-fusion-arcade-settings) | 🥈 Superb RE notes and pnach generator; script is an override palimpsest | Fusion | 🩹 pnach | 🕒🏷️📜🤖 | 🟢 MIT | Adds a race set-up screen to single-player Arcade (laps, up to 16 ships, shields, AI level, respawn) and fixes the final-lap slowdown. PAL + NTSC-U, PCSX2 2.8. The generator script covers PAL only; the NTSC-U pnach was relocated by hand. Optional skip-intro and FINAL LAP cheats |
| [PCSX2 built-in](https://github.com/PCSX2/pcsx2_patches/blob/main/patches/SLUS-20462_4C2D1E6D.pnach) | – | Fusion | 🩹 built-in pnach: widescreen 16:9 with improved chase-cam baked in (No.47), no-interlace | 🕒👥🏷️⚙️ | 🟢 | NTSC-U (SLUS-20462) only. Turning on widescreen also gives the 'whole ship visible' chase-cam for all 8 ships, with no separate toggle. There is no PAL (SCES-50005) entry, so PAL users still need the [2014 forum attachment](https://forums.pcsx2.net/Thread-PCSX2-Widescreen-Game-Patches) |
| [PCSX2/pcsx2_patches: SCES-54748](https://github.com/PCSX2/pcsx2_patches/blob/main/patches/SCES-54748_F8AE6FF2.pnach) | – | Pulse (PS2, EU only) | 🩹 pnach: 50/60 FPS (asasega) | 🕒👥🏷️⚙️ | 🟢 | First index entry for the 2009 PS2 port of Pulse (SCES-54748, CRC F8AE6FF2). Ships with PCSX2's built-in patch list: just enable it per game. A single EE NOP. Its author says it may need a 130% EE overclock to stay stable. Also mirrored in Gabominated/PCSX2 and Saramagrean/NetherSX2-cheats |
| [sethvm/WipEout-Fusion-HD-Texture-Pack](https://github.com/sethvm/WipEout-Fusion-HD-Texture-Pack) | – | Fusion | 🖼️ texture pack | – | 🟠 derivative | |

## PSP (PPSSPP)

Both Pure and Pulse run at 60 fps but fall back to 30 whenever effects pile up (explosions, Zone mode late stages).
The fix is a CWCheat that forces the 60 fps path. See [PPSSPP issue 12273](https://github.com/hrydgard/ppsspp/issues/12273)
for the mechanism. Codes are per region and per disc revision (Pure USA has v1 and v2 BINs).

| Project | Quality | Game | Type | Signals | Legal | Notes |
|---------|---------|------|------|----------|-------|-------|
| [NR74W/WipEout-Mods](https://github.com/NR74W/WipEout-Mods), *CWCheat section* | – | Pure, Pulse | 🩹 cheats: Force 60FPS (All) for Pure and Pulse, Force 60FPS (In-Game Only) for Pure | 🕒 | 🟢 | The codes themselves are fine. See the next table for the rest of that repo |
| [PPSSPP forum: 60 FPS patches thread](https://forums.ppsspp.org/showthread.php?tid=4799) | – | Pulse EU (UCES-00465) | 🩹 cheat: 60 FPS Always / 30-60 Default | – | 🟢 | Also explains how to find the address yourself to port to another region |
| [kabutokun.github.io](https://kabutokun.github.io/) | – | Pure, Pulse | 🩹 60 fps CWCheat master list (link index) | – | 🟢 | 2017 snapshot of GamerzHell9137's forum list. Links the tid=4799 posts for Pure USA (v1.04 and v2.0 share one link) and EUR, and Pulse USA. Pulse EUR and Pure JAP are marked as having no code. The codes themselves stay in the forum thread |
| [Saramagrean/CWCheat-Database-Plus-](https://github.com/Saramagrean/CWCheat-Database-Plus-) | – | all PSP | 🩹 cheat database with a 60 fps collection | 🕒👥 | 🟢 | Generic. Has WipEout Pure (EU/US/JP) and Pulse (EU/US/CN, demo, promo) entries: 60 fps codes (Pulse per UMD v1.04/v2.00) and a 'Remove DLC Signature Check' code |
| [LunaMoo/PPSSPP_workarounds](https://github.com/LunaMoo/PPSSPP_workarounds) | – | all PSP | 🩹 CWCheat fixes | 🕒 | 🟢 | Author warns 60 fps patches often break timing. Worth reading before trusting any of the above |
| [0xf0xx0/WipEout-Pure-HD-Texture-Pack](https://github.com/0xf0xx0/WipEout-Pure-HD-Texture-Pack) | – | Pure | 🖼️ texture pack (NR74W, Update #33, 2022) | – | 🟠 derivative | Reupload preserving NR74W's full history through Update #33 (adds track textures). The reTokyo repo below is the same author's older account, frozen at Update #5 (2020). Prefer this one |
| [reTokyo/WipEout-Pure-HD-Texture-Pack](https://github.com/reTokyo/WipEout-Pure-HD-Texture-Pack) | – | Pure | 🖼️ texture pack | – | 🟠 derivative | UI-focused, partial: UI, HUD and fonts, plus a few track textures (Vineta K, Pro Tozo). Older NR74W snapshot. [Forum thread](https://forums.ppsspp.org/showthread.php?tid=26291) |
| [reTokyo/WipEout-Pulse-Upscale-Version](https://github.com/reTokyo/WipEout-Pulse-Upscale-Version) | – | Pulse | 🖼️ texture pack | – | 🟠 derivative | |
| [archive.org: NR74W PSP HD texture packs](https://archive.org/details/nr74w-wipeout-psp-hd-texture-packs) | – | Pure, Pulse | 🖼️ texture packs, original NR74W release | – | 🟠 derivative | 2023 mirror of the original packs, whose PPSSPP forum thread ([archived](https://web.archive.org/web/20210802013022/https://forums.ppsspp.org/showthread.php?tid=26335)) is gone. Pulse 1.05 GB, Pure 440 MB. The uploader says re-upscaled mirrors break Pulse fonts. NR74W's mods are mirrored at [nr74w-wo-mods](https://archive.org/details/nr74w-wo-mods) (🔴, the same xdelta patches) |
| [Litiser PT-BR translation](https://github.com/romhackersbr/romhackersbr-db/blob/main/_traducoes/portatil/playstation-portable/wipeout-pure-litiser.md) (romhackers.org database) | – | Pure EU (UCES-00001) | 💿 xdelta3 patch: Brazilian Portuguese translation, v1.0 (2009), 99% | – | 🟢 diff only | Texts translated with accents, a few untranslated bits remain. Database entry only; download location not verified |
| [PPSSPP docs: custom background music](https://www.ppsspp.org/docs/reference/custom-background-music/) | – | Pulse | 📖 how-to | – | 🟢 | Put your own MP3s in `ms:/MUSIC/WIPEOUT` (memory stick root), then edit the playlist in-game. MP3s must be 44.1 kHz. Pure has no custom-music support |

In-game unlock without any patch: both games have a main-menu button sequence that unlocks all tracks and leagues
([32bits write-up](https://32bits.substack.com/p/under-the-microscope-wipeout-pure)).

### DLC and "all content" mods

Pure's DLC packs (Classic 1-3, Delta 1-2, Gamma 1-3, Omega, promo skins) were free downloads Sony no longer hosts.
Pulse's four packs were paid and EU-only. Neither is redistributable, so every "all DLC" mod is 🔴.

| Project | Quality | Game | Type | Signals | Legal | Notes |
|---------|---------|------|------|----------|-------|-------|
| [NR74W/WipEout-Mods](https://github.com/NR74W/WipEout-Mods), *patches* | – | Pure, Pulse | 💿 xdelta patches vs EU ISOs (README v3.0): *WipEout Pure*, *WipEout Pulse*, *WipEout Portable Collection* (both games in one ISO). Patches hosted on MEGA | 🕒 | 🔴 embeds DLC | All DLC, everything unlocked, built-in 60 fps, Japanese language, Head-to-Head and Eliminator restored in Pulse, AI fixes. The de-facto community reference. Changes the game ID, so saves are incompatible |
| [PPSSPP forum: Pure DLC install](https://forums.ppsspp.org/showthread.php?tid=18516) | – | Pure | 📖 how-to | – | 🟢 how-to only | One top-level folder per pack under `PSP/SAVEDATA`, region must match the disc (UCUS vs UCES IDs). Says nothing about where to get the packs |

## PS3 (RPCS3)

| Project | Quality | Game | Type | Signals | Legal | Notes |
|---------|---------|------|------|----------|-------|-------|
| [RPCS3 wiki: WipEout HD](https://wiki.rpcs3.net/index.php?title=WipEout_HD) | – | HD / Fury | 🩹 built-in patches: *High FPS Fixes* (Lex6s, NPUA80105 / NPEA00057), *21:9* (Esppiral) | – | 🟢 | Above 60 fps alters camera, ship fall speed, Zone scoring and EMP range. The high-fps patch resyncs shield glow. 21:9 needs *Stretch To Display Area*. Install updates before the Fury DLC |
| [hookmanuk/rpcs3-vr-plans](https://github.com/hookmanuk/rpcs3-vr-plans) · [fork (openxr branch)](https://github.com/hookmanuk/rpcs3/tree/openxr) | 🥈 Data-driven VR profiles, great evidence; scratch scripts, 6k-line files | HD / Fury (BCES00664) | 🧰 OpenXR VR fork of RPCS3 with per-game stereo profiles | 🕒🤖 | 🟢 | WipEout is the reference title: its released profile was fitted against the game's own native stereo-3D output. Fork has tagged builds (v0.0.43-vr11, 2026-10-14); the 2.51 update is not required. Open regression since 2026-10-15: late frames in the race test at 120 Hz. Vulkan only. The plans repo is notes plus scripts, the emulator code is in the fork |
| [bucanero/apollo-saves](https://github.com/bucanero/apollo-saves) | – | HD / Fury, 2048, Pulse | 🧰 save database for Apollo Save Tool | 🕒👥📜 | 🟠 save files | HD EU digital (NPEA00057): HD and Fury campaign 100%, all ships and tracks unlocked (may need Fury DLC), platinum save. 2048 (PCSF00007): 100% career including online and Elite passes, all liveries. Pulse EU (UCES00465): ghosts and custom grids. Load through Apollo on CFW or import into RPCS3/Vita3K. Player data, but the game's ICON0.PNG is bundled as is |

## Vita (Vita3K)

| Project | Quality | Game | Type | Signals | Legal | Notes |
|---------|---------|------|------|----------|-------|-------|
| [Vita3K/vita3k-patches](https://github.com/Vita3K/vita3k-patches) | – | 2048 | 🩹 Patch Manager patch *60FPS* (v1.04: EU/US PCSF00007/PCSA00015, JP/Asia PCSC00006/PCSD00005) + VitaCheat file | 🕒🏷️⚙️🤖 | 🟢 | Official Vita3K patch repo, fetched via *Manage > Patch Manager > Download latest patches*. As of 2026-10-25 the EU/US block has an empty NID, which Vita3K never applies, so only JP/Asia works out of the box. The only cheat is a joke *Mess up Race* |
| [Scirvir/game-patches: WipEout2048.md](https://github.com/Scirvir/game-patches/blob/main/other/WipEout2048.md) | – | 2048 | 🩹 eboot hex patch: 60 fps | 🕒 | 🟢 | EU/US 1.04 only (PCSF00007, PCSA00015). Two variants: Scirvir's single patch at ELF offset 0x2F6B6C, and u/Azrael1981's two-site patch, which writes the same bytes as VitaGrafix's FPS block. Offsets only: apply them yourself to a decrypted eboot, for Vita3K or hardware. The same repo has an RPCS3 photo-mode unlock for HD (BCES00664 02.00) |
| [60 fps eboot by Mike_Chester92 (archive.org)](https://archive.org/details/eboot_60-fps) | – | 2048 | 🩹 modded `eboot.bin` (PCSF00007), 60 fps in Vita3K | – | 🔴 patched Sony exe | The whole 5.5 MB executable is replaced, not shipped as a diff. Install the 1.04 update and the HD + Fury DLC first, then overwrite `eboot.bin` in the app folder. Uploaded 2026-07 with no notes on what was patched, so it cannot be reproduced |
| [cousteauche/Vita3K `wipeout_fps_hack`](https://github.com/cousteauche/Vita3K/tree/wipeout_fps_hack) ([commit](https://github.com/Vita3K/Vita3K/commit/9e920bd1ec86af0ff56dde973cfe2ff9f9cc6aff)) | 🚧 Unmerged fork debug hack with hardcoded title IDs | 2048 | 🩹 Vita3K fork branch: 60 fps by skipping display waits | 👥🏷️⚙️📜 | 🟢 GPL-2.0 | Unmerged fork hack (2025-06), not in Vita3K master. Hardcodes EU/US title IDs in SceDisplay and needs fps_hack on. Signals are inherited from upstream. The upstream route is open PR [#4315](https://github.com/Vita3K/Vita3K/pull/4315) (per-game vblank rate, tested on 2048 at 60/240 Hz). Compat issues: #357, #556, #2852 |

### Vita real hardware (HENkaku / PS TV plugins)

These do nothing in Vita3K.

| Project | Quality | Game | Type | Signals | Legal | Notes |
|---------|---------|------|------|----------|-------|-------|
| [Electry/VitaGrafixPatchlist](https://github.com/Electry/VitaGrafixPatchlist) (for the [VitaGrafix](https://github.com/Electry/VitaGrafix) plugin) | – | 2048 | 🩹 taiHEN plugin patchlist: fixed internal resolution (overrides the 14 dynamic-res steps), FPS cap | 🕒👥🏷️ | 🟢 | EU/US/JP/ASIA 1.04 (PCSF00007, PCSA00015, PCSC00006, PCSD00005), matched by eboot hash. Configure in `ux0:data/VitaGrafix/config.txt` or with [VitaGrafixConfigurator](https://github.com/Kirezar/VitaGrafixConfigurator). The plugin is GPL-3.0; the patchlist has no licence |
| [Thekenbaum/Vita-Thread-Optimizer-Profiles](https://github.com/Thekenbaum/Vita-Thread-Optimizer-Profiles) | – | 2048 (US, PCSA00015) | 🧰 Thread Optimizer plugin profiles: *Final Version* (steadier fps) and *High Intensity* (higher peak fps) | – | 🟢 | Tested at a 444 MHz overclock and native resolution. Opaque binary `config.dat` with no explanation of what was changed |
| [OperationNT414C/DSMotion](https://github.com/OperationNT414C/DSMotion) | 🥈 Small sensible kernel/user split, clean shared header; no tests | 2048 | 🧰 taiHEN plugin that feeds DualShock 3/4 motion to the Vita motion API | 🏷️📜 | 🟢 MIT | PS TV, or a Vita with ds3vita/ds4vita. Makes 2048's motion-steering option usable on PS TV |
| [OperationNT414C/FakeCamera](https://github.com/OperationNT414C/FakeCamera) | 🥉 Works, but 1.5k-line single file with 39 hand-unrolled hooks | 2048 | 🧰 taiHEN plugin that fakes the camera API | 🏷️📜 | 🟢 MIT | PS TV. Stops 2048 (PCSF00007) crashing when a multiplayer session starts, caused by the camera picture feature. BMP image mode works at low resolution (64x64 tested) |
| [r0ah/vitacheat](https://github.com/r0ah/vitacheat) | – | 2048 | 🩹 VitaCheat database + closed-source `WipeOut_2048.suprx` cheat plugin | 👥 | 🟢 | VitaCheat on HENkaku. The 2048 .psv has a single *Mess up Race* code. The plugin is a 2019 binary with no source or docs. Low value, listed for completeness |

## Cross-platform

| Project | Quality | Game | Type | Signals | Legal | Notes |
|---------|---------|------|------|----------|-------|-------|
| [RetroAchievements: Wipeout Pure](https://retroachievements.org/game/3224) | – | WipEout, 2097, WipEout 64, Fusion, Pure | 🧰 achievement sets (RetroArch, DuckStation, PCSX2, PPSSPP) | – | 🟢 | Sets: Pure PSP 237 / 1,283 pts (largest), Fusion PS2 [88 / 620](https://retroachievements.org/game/3294), 2097 PS1 [42 / 364](https://retroachievements.org/game/13913), WipEout PS1 [44 / 466](https://retroachievements.org/game/11378), [Wipeout 64](https://retroachievements.org/game/10532). Pulse and 2097 Saturn have no set yet. Hash-matched, so your dump must match a supported revision. Something to do with the game, not a quality signal |

## Gaps worth filling

- A clean, WipEout-only CWCheat collection per region/revision (60 fps, unlocks) instead of forum threads and generic databases.
- Fusion PAL (SCES-50005): the widescreen + chase-cam pnach in pcsx2_patches (only NTSC-U has it).
- 2048: a working Vita3K 60 fps patch for EU/US (the vita3k-patches block has an empty NID) or a clean xdelta of the eboot instead of the full patched exe.
- Wip3out SE PAL-to-NTSC conversion as an xdelta instead of a full CHD; published source for hueponik's patches.
- 2097 / XL: 60 fps for the PAL and JP releases (Yash-Singh1's patch is USA only).
