# vortex-bg-collection

**18 hand-tuned, animated shader backgrounds for games — in one single HTML file.**

A Balatro-style vortex background editor with 7 motion modes and 18 ready-to-use presets.
Open `index.html`, pick a preset, tweak, export. No build step, no dependencies.

## Live demo

The v1 editor is already live: https://qinmeng573.github.io/vortex-bg-editor/
(This collection is the v2 upgrade: 13 → 18 presets, plus a machine-readable `presets.json`.)

**Guided tour:** [DEMO.md](DEMO.md) — 8 presets in 60 seconds, in the order that tells the story.

## What's new in the collection

- **18 presets** (5 new): Mint Battle A2, Solar Eclipse, Glacier, Violet Void, Matcha Garden — alongside the original Cathedral Blue-White, Crimson Ripple, Rose Window, Black-Gold Throne, Blood Moon and more
- **`presets.json`** — every preset as data (mode, 3 colors, contrast, spin, speed, scale, warp, pixel factor), ready to drop into your own engine or shader port
- **7 motion modes**: vortex · ripple · wave · tide · rays · kaleido · splash

## Use the presets in your game

Each entry in `presets.json` maps 1:1 to the shader uniforms in `index.html`:

```json
{
  "name": "薄荷战斗 A2（定版）",
  "mode": 1,
  "colors": ["#35b09b", "#ffe066", "#0e352f"],
  "contrast": 1.5, "spin": 0.6, "speed": 0.5,
  "scale": 1.0, "warp": 0.6, "pixelFac": 800
}
```

Port the fragment shader, feed it a preset, done.

## Rules we learned the hard way

- Colors 1 and 2 must not both be blue at the same time (the vortex collapses visually). Both white is fine.
- `pixelFac` trades retro pixel grain against smoothness: 700 = chunky, 2000 = silky.

## Disclaimer

An original clean-room editor inspired by a well-known card game's menu background.
Not affiliated with LocalThunk or Playstack. No original game code or assets included.

## License

MIT
