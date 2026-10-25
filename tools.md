# Tools, formats and documentation

Extractors, editors, viewers and reverse-engineering notes. Legend in [README.md](README.md#legend).
Tools are 🟢 unless they bundle game data.

## Cross-series

| Project | Covers | What | Activity | Legal | Notes |
|---------|--------|------|----------|-------|-------|
| [PierreBelmondo/vscode-wipeout](https://github.com/PierreBelmondo/vscode-wipeout) | PSX to PS5 | VS Code extension: unpack WAD (LZSS/zlib, XTEA-encrypted DLC), WAC, PSARC, BNK (SCREAM audio to WAV); view VEXX and RCS models with animation | 🟢 | 🟢 MIT | The Swiss-army knife of the series |
| [NR74W/WipEout-Fonts](https://github.com/NR74W/WipEout-Fonts) | all | Series fonts remade in OpenType | ⚫ archived | 🟠 derivative | |

## PS1 (WipEout, 2097, Wip3out)

| Project | Covers | What | Activity | Legal | Notes |
|---------|--------|------|----------|-------|-------|
| [phoboslab/wipeout](https://github.com/phoboslab/wipeout) | WO1, 2097 | WebGL / Three.js model and track viewer | 🟡 | 🟢 | Reads PRM, CMP, TIM, TRV/TRF directly |
| [ficool2/wipeout_ripper](https://github.com/ficool2/wipeout_ripper) | WO1, 2097 | Texture and geometry ripper | 🟡 | 🟢 | Author flags it as early learning code |
| [IsPeG/wip3out-showroom](https://github.com/IsPeG/wip3out-showroom) | Wip3out | Three.js ship showroom | ⚫ | 🟢 | |
| [puargamer/Wip3out-Menu](https://github.com/puargamer/Wip3out-Menu) | Wip3out | Main menu recreation | 🟡 | 🟢 | |
| [devhowyalike/wipeout3-react](https://github.com/devhowyalike/wipeout3-react) | Wip3out | Recreation of the 1999 Designers Republic Flash site | 🟢 | 🟢 | |

Format notes:

- [Reverse Engineering WipEout (PSX)](https://phoboslab.org/log/2015/04/reverse-engineering-wipeout-psx), phoboslab 2015. CMP = LZ77-compressed bundle of TIM textures, PRM = dumps of PSX GPU primitive structs, TRV/TRF = track vertices and faces.
- [Rewriting wipEout](https://phoboslab.org/log/2023/08/rewriting-wipeout), phoboslab 2023. Engine architecture and what the leaked source looked like.
- [WipeoutZone: Reverse engineering of Wipeout](https://www.wipeoutzone.com/forum/archive/index.php/t-9959.html) and [of Wipeout 3 SE](https://www.wipeoutzone.com/forum/archive/index.php/t-9955.html). Community threads, 2010s.
- [Qhimm wiki: TIM](https://qhimm-modding.fandom.com/wiki/PSX/TIM_file). Generic PSX texture format.

## PS2 (Fusion)

| Project | What | Activity | Legal | Notes |
|---------|------|----------|-------|-------|
| [neko68k/FusionTool](https://github.com/neko68k/FusionTool) | Archive explorer and editor | ⚫ (2014) | 🟢 | |
| [aybe/WipeoutFusion](https://github.com/aybe/WipeoutFusion) | Reverse-engineering attempt | ⚫ (2016) | 🟢 | Stub |

## PSP (Pure, Pulse)

| Project | What | Activity | Legal | Notes |
|---------|------|----------|-------|-------|
| [thp/wipeout-pulse-shipedit](https://gitlab.com/thp/wipeout-pulse-shipedit) ([GitHub mirror](https://github.com/CommanderCRM/wipeout-pulse-shipedit), [free fork](https://gitlab.com/tommasoclini/wipeout-pulse-shipedit-free)) | Pulse ship skin / livery editor. C + OpenGL 1.1, 256x256 PNG in and out, 16-colour quantizer, reads the `16034453` save format | 🟡 (1.0.4, 2024-11) | 🟢 | By Thomas Perl. Windows builds on [itch.io](https://thp.itch.io/shipedit) (pay what you want, source included). DLC ships need lowercase, unencrypted files next to the exe |
| [wlfn1116/PureWADTool](https://github.com/wlfn1116/PureWADTool) | Decrypt and extract Pure `.WAD` | 🟡 | 🟢 | |

## PS4 (Omega Collection)

Archive and model support (PSARC, RCS) is in [vscode-wipeout](https://github.com/PierreBelmondo/vscode-wipeout). No standalone tool found.

## Related infrastructure

| Project | What | Legal |
|---------|------|-------|
| [mstan/psxrecomp](https://github.com/mstan/psxrecomp) · [recomp-ui](https://github.com/mstan/recomp-ui) | PS1 static recompiler and launcher behind the `*-recomp` projects | 🟢 |
| [alexbeavs-ps1-ports/psxrecomp-ports](https://github.com/alexbeavs-ps1-ports/psxrecomp-ports) | Index of PS1 recomp releases (WipEout, XL and ~30 other titles) | 🟢 |
| [marco-calautti/DeltaPatcher](https://github.com/marco-calautti/DeltaPatcher) | xdelta GUI used by the PSP mods | 🟢 |
