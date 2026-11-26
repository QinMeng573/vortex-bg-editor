# Demo: a 60-second tour of the 18 presets

Open `index.html` in any browser. No install, no build.

## The tour

Pick each preset from the dropdown, in this order — it tells a story:

| # | Preset | Mode | What to notice |
|---|---|---|---|
| 1 | Cathedral Blue-White | vortex | The original. Contrast 3.0, silky pixels (2000). A game main menu that shipped like this. |
| 2 | Mint Battle A2 | ripple | Same engine, battle variant: mint + lemon on deep teal, contrast dropped to 1.5 so it sits *behind* gameplay. |
| 3 | Crimson Ripple | ripple | The A2's predecessor — crimson + gold. Kept for comparison; it lost to mint in playtesting. |
| 4 | Rose Window | rose | Rose mode: the vortex opens into a cathedral rose window. |
| 5 | Solar Eclipse | kaleido | Dark core, golden rim — a kaleidoscopic eclipse. |
| 6 | Violet Void | rose | High warp (0.9) — the rose pattern starts to breathe. |
| 7 | Blood Moon | vortex | Spin 0.75: noticeably faster rotation, same shader. |
| 8 | Ink & Paper | kaleido | Greyscale. Proof the effect is structure, not color. |

Then drag the **contrast**, **spin**, and **pixel factor** sliders on any preset:
pixel factor 700 turns the same image into chunky retro grain; 2000 makes it silk.

## For developers

Every stop on this tour is one row of [`presets.json`](presets.json).
The demo you just clicked through is data, not code — port the shader once, ship all 18 looks.

## Recording a GIF for your own project

1. Full-screen the editor (hide the panel), pick a preset.
2. Screen-record 4 seconds — one full breathing cycle is 12s at speed 0.5, so record at speed 1.0+ for a snappier loop.
3. That GIF is your menu background *and* your store-page banner.
