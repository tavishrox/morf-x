# Changelog

## 0.2.5 (24 Nov 2026)

- Helix LT: working with MORF-X (tested on Windows); Save and Save as are switched on for it.
- Windows: confirmed working with a unit. Only one program can talk to the unit at a time, so close MORF-X before
  running the device check.

## 0.2.4 (24 Nov 2026)

- Helix LT: recognised by its own USB ID (0x424A; it calls itself "HELIX"), named Helix LT with its own picture.
  Thanks to the LT owner who ran the device check. Still not tried with MORF-X, so Save stays hidden.
- A device check page (check.html): shows which Line 6 unit is plugged in, its USB ID and whether MORF-X can reach it,
  with a button to email the results.

## 0.2.3 (24 Nov 2026)

- Helix LT and Helix Rack: MORF-X now offers any Line 6 unit and recognises these by the name they give over USB,
  so they no longer show "no compatible devices". Not yet tried on either: Save stays hidden until someone reports back.

## 0.2.2 (24 Nov 2026)

- HX Effects: all 9 blocks on each path are found. The 9th block on path A (1A9) was missed before, and path B's
  9th block was labelled "2A0"; it now reads 1B9. Other units are unchanged.

## 0.2.1 (24 Nov 2026)

- HX Stomp: presets are named as the unit shows them, in banks of 3 (01A to 42C), in the preset picker and Save as.
  Thanks to the Stomp owner who reported it. Every other unit keeps banks of 4.
- Double-clicking the pad no longer opens the tone editor by accident: double-click a tone's dot to edit it.
- A home page with every download: https://tavishrox.github.io/morf-x/ (the web app is now at /app/).

## 0.2.0 (22 Nov 2026)

- A new look: the block's knobs shown like the POD Go's screen, every knob at once, in the MORF-X theme.
- Setlists: a setlist picker (Factory and User on the POD Go), and Save as into any setlist (POD Go Factory tested).
- Follows the unit: preset and setlist changes made on the unit, and blocks turned on or off.
- Starts on the amp whenever a preset loads.
- Shows the unit's firmware version.
- Every POD Go model is named out of the box: no need to load POD Go Edit's model list any more.
- Glide 0 to 1 s, 0.1 s to start. Edit tones moved next to the knobs. A dark title bar in the app.
- Apps for Mac, Windows and Linux (Windows and Linux not yet tried with a unit).

## 0.1.0 (18 Nov 2026)

- First release: POD Go, Helix and HX Effects; Mac app.
