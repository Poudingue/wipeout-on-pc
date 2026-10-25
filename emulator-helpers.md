# Emulator helpers

Patches, cheats, texture packs and mods you load into an emulator to alter or improve a game. Legend in
[README.md](README.md#legend).

Rule of thumb for the legal tag: a **cheat code or pnach** is a handful of addresses and values, 🟢. A **texture
pack** redistributes Sony's art, upscaled, 🟠. A **patched ISO or xdelta that embeds DLC** carries
Sony's content, 🔴, even when the repo itself holds no ISO.

## PS1 (DuckStation, Beetle PSX HW)

| Project | Game | Type | Signals | Legal | Notes |
|---------|------|------|----------|-------|-------|
| [princepeter64/Wip3out-HD-Texture-Pack](https://github.com/princepeter64/Wip3out-HD-Texture-Pack) | Wip3out / 3 SE | 🖼️ texture pack, Beetle PSX HW | – | 🟠 derivative | |
| [Matsilagi/WO3-Beta-Texturepack](https://github.com/Matsilagi/WO3-Beta-Texturepack) | Wip3out SE | 🖼️ beta-look texture pack, Beetle PSX HW | – | 🟠 derivative | |
| [tigrouind/wipeout-autopilot](https://github.com/tigrouind/wipeout-autopilot) | 2097 | 🧰 BizHawk Lua autopilot | 📜 | 🟢 MIT | Curiosity |
| [tre3qwerty/Wipeout-2097-Auto-Splitter](https://github.com/tre3qwerty/Wipeout-2097-Auto-Splitter) | 2097 | 🧰 LiveSplit autosplitter | – | 🟢 | Speedrunning |

## PS2 (PCSX2)

| Project | Game | Type | Signals | Legal | Notes |
|---------|------|------|----------|-------|-------|
| [fvhcookie-bit/wipeout-fusion-arcade-settings](https://github.com/fvhcookie-bit/wipeout-fusion-arcade-settings) | Fusion | 🩹 pnach | 🕒🏷️📜🤖 | 🟢 MIT | Adds a race set-up screen to single-player Arcade (laps, up to 16 ships, shields, AI level, respawn) and fixes the final-lap slowdown. PAL + NTSC-U, PCSX2 2.8 |
| [sethvm/WipEout-Fusion-HD-Texture-Pack](https://github.com/sethvm/WipEout-Fusion-HD-Texture-Pack) | Fusion | 🖼️ texture pack | – | 🟠 derivative | |
| PCSX2 built-in | Fusion | widescreen 16:9, no-interlace | – | 🟢 | Enable in the per-game patch list. A chase-cam fix pnach exists on the [PCSX2 forums](https://forums.pcsx2.net/Thread-PCSX2-Widescreen-Game-Patches) (2014 attachment) |

## PSP (PPSSPP)

Both Pure and Pulse run at 60 fps but fall back to 30 whenever effects pile up (explosions, Zone mode late stages).
The fix is a CWCheat that forces the 60 fps path. See [PPSSPP issue 12273](https://github.com/hrydgard/ppsspp/issues/12273)
for the mechanism. Codes are per region and per disc revision (Pure USA has v1 and v2 BINs).

| Project | Game | Type | Signals | Legal | Notes |
|---------|------|------|----------|-------|-------|
| [NR74W/WipEout-Mods](https://github.com/NR74W/WipEout-Mods), *CWCheat section* | Pure, Pulse | 🩹 cheats: Force 60FPS (All), Force 60FPS in-game only | 🕒 | 🟢 | The codes themselves are fine. See the next table for the rest of that repo |
| [PPSSPP forum: 60 FPS patches thread](https://forums.ppsspp.org/showthread.php?tid=4799) | Pulse EU (UCES-00465) | 🩹 cheat: 60 FPS Always / 30-60 Default | – | 🟢 | Also explains how to find the address yourself to port to another region |
| [Saramagrean/CWCheat-Database-Plus-](https://github.com/Saramagrean/CWCheat-Database-Plus-) | all PSP | 🩹 cheat database with a 60 fps collection | 🕒👥 | 🟢 | Generic. Check for WipEout entries |
| [LunaMoo/PPSSPP_workarounds](https://github.com/LunaMoo/PPSSPP_workarounds) | all PSP | 🩹 CWCheat fixes | 🕒 | 🟢 | Author warns 60 fps patches often break timing. Worth reading before trusting any of the above |
| [reTokyo/WipEout-Pure-HD-Texture-Pack](https://github.com/reTokyo/WipEout-Pure-HD-Texture-Pack) | Pure | 🖼️ texture pack | – | 🟠 derivative | |
| [reTokyo/WipEout-Pulse-Upscale-Version](https://github.com/reTokyo/WipEout-Pulse-Upscale-Version) | Pulse | 🖼️ texture pack | – | 🟠 derivative | |

In-game unlock without any patch: both games have a main-menu button sequence that unlocks all tracks and leagues
([32bits write-up](https://32bits.substack.com/p/under-the-microscope-wipeout-pure)).

### DLC and "all content" mods

Pure's DLC packs (Classic 1-3, Delta 1-2, Gamma 1-3, Omega, promo skins) were free downloads Sony no longer hosts.
Pulse's four packs were paid and EU-only. Neither is redistributable, so every "all DLC" mod is 🔴.

| Project | Game | Type | Signals | Legal | Notes |
|---------|------|------|----------|-------|-------|
| [NR74W/WipEout-Mods](https://github.com/NR74W/WipEout-Mods), *patches* | Pure, Pulse | 💿 xdelta patches vs EU ISOs: *Pure Special Edition*, *Pulse FX350 Edition*, *WipEout Portable Collection* (both games in one ISO) | 🕒 | 🔴 embeds DLC | All DLC, everything unlocked, DLC signature check disabled, built-in 60 fps, Japanese language, Head-to-Head and Eliminator restored in Pulse, AI fixes. The de-facto community reference. Changes the game ID, so saves are incompatible |
| [PPSSPP forum: Pure DLC install](https://forums.ppsspp.org/showthread.php?tid=18516) | Pure | 📖 how-to | – | 🟢 how-to only | One top-level folder per pack under `PSP/SAVEDATA`, region must match the disc (UCUS vs UCES IDs). Says nothing about where to get the packs |

## PS3 (RPCS3)

| Project | Game | Type | Signals | Legal | Notes |
|---------|------|------|----------|-------|-------|
| [RPCS3 wiki: WipEout HD](https://wiki.rpcs3.net/index.php?title=WipEout_HD) | HD / Fury | 🩹 built-in patches: *High FPS Fixes* (Lex6s, NPUA80105 / NPEA00057), *21:9* (Esppiral) | – | 🟢 | Above 60 fps alters camera, ship fall speed, Zone scoring and EMP range. The high-fps patch resyncs shield glow. 21:9 needs *Stretch To Display Area*. Install updates before the Fury DLC |

## Vita (Vita3K)

| Project | Game | Type | Signals | Legal | Notes |
|---------|------|------|----------|-------|-------|
| community eboot patch | 2048 | 60 fps unlock | – | 🟢 | Circulates as a how-to, no repo found yet. Gap |

## Gaps worth filling

- A clean repo collecting WipEout CWCheats per region/revision (60 fps, unlocks) instead of forum threads.
- Fusion: a maintained widescreen + chase-cam pnach on GitHub.
- 2048: the 60 fps eboot patch as a reproducible script.
