# MORF-X: find your tone

Blend one block on your Line 6 unit between five tones on an X-Y pad, live over USB. Drag the crosshair and every
parameter of the block moves with it: knobs blend, switches change at the halfway point, and a short glide turns a
fast move into a smooth sweep. Every model starts with five ready-made tones, and you can make and save your own.

**Home page, with all the downloads:** https://tavishrox.github.io/morf-x/
**Use it in the browser** (Chrome or Edge on a computer): https://tavishrox.github.io/morf-x/app/
**Or download the app** for Mac, Windows or Linux from [Releases](https://github.com/tavishrox/morf-x/releases).

## Works with

| Unit | Status |
|---|---|
| POD Go / POD Go Wireless | Tested |
| Helix Floor | Tested |
| HX Effects | Tested |
| Helix LT | Tested (on Windows) |
| Helix Rack | Recognised by name; not tried yet: Save stays hidden. Please [report how it goes](https://github.com/tavishrox/morf-x/issues). |
| HX Stomp, HX Stomp XL | Not tried yet: Save stays hidden. Please [report how it goes](https://github.com/tavishrox/morf-x/issues). |

Close POD Go Edit or HX Edit first: only one program can talk to the unit at a time.

## What it does

- Finds the unit, its firmware, its setlists and presets, and the blocks in the loaded preset; starts on the amp.
- Follows the unit: change preset, setlist or a block's on/off on the unit and MORF-X keeps up.
- Pick a setlist and preset from the app; **Save** to the loaded preset or **Save as** into any setlist and slot.
- Nothing is saved until you press Save: until then, reloading the preset on the unit puts everything back.
- Edit the five tones per model, rename them, and keep them in your own file.

## The apps

| Download | Notes |
|---|---|
| `MORF-X-…-Mac-Apple-Silicon.zip` | Macs with an M1, M2, M3, M4 or later chip. Not notarised: the first time, right-click the app and choose Open. |
| `MORF-X-…-Mac-Intel.zip` | Older Macs with an Intel processor. Same first-time step. |
| `MORF-X-…-Windows-64-bit.zip` | Windows 10 and 11. Tested with a Helix LT. |
| `MORF-X-…-Linux-64-bit-Intel-AMD.tar.gz` | Most Linux PCs. Not yet tried; install the included USB rule once (see `README-linux.txt`). |
| `MORF-X-…-Linux-ARM-64-bit.tar.gz` | 64-bit ARM Linux, such as a Raspberry Pi 4 or 5 on 64-bit Raspberry Pi OS. Not yet tried. |

Not sure which Mac you have? Apple menu › About This Mac: "Chip" means Apple Silicon, "Processor" means Intel.

## The website

`web/index.html` is the home page and `web/app/` is MORF-X itself; GitHub Pages publishes `web/` on every push.

## Building

    cd app
    npm ci
    npm start              # run from source (copies ../web/app in first)
    npm run pack-all       # Mac (arm64, x64), Windows (x64), Linux (x64, arm64), then the zips in app/dist

`MORFX_SELFTEST=1 npx electron .` connects, prints what MORF-X finds and quits (reads only).

The tone data (`web/app/focus-defaults.json`, `web/app/focus-helix.json`) is made by `tools/focus_extras.py` and
`tools/make_focus_helix.py` from Line 6's Focus View presets and the model lists in your own POD Go Edit / HX Edit
install.

## Licence and credits

GPL-3.0-or-later; see [LICENSE](LICENSE) and [NOTICE](NOTICE).

Default tones: Line 6's Focus View presets, © Line 6 / Yamaha Guitar Group, used with credit; the EQ and two delay
sets are ours. Line 6, POD Go, Helix and HX are trademarks of Yamaha Guitar Group, Inc., shown only to say what
MORF-X works with. MORF-X is not made or endorsed by Line 6. The unit pictures are our own renders.

By [ToneShift](https://www.youtube.com/channel/UC8Fy07TKY0txLxOgj7edHCA). Also from ToneShift:
[NAM A2 Lite for POD Go](https://tavishrox.github.io/pod-go-nam-lite/web/pod-go/).
