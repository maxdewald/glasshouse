# Glasshouse Home wallpaper-drift benchmark

Alternative View + Pictures, 1920×1080, official Landscape wallpaper, Glasshouse C2 emulator. Baseline: `8fcf08cf0b98df086c1c52703e21f67c599784f0`. The only runtime difference in the comparison is the wallpaper CSS patch.

Headless Chromium with SwiftShader, 4× CDP CPU slowdown. Two baseline/patch pairs in alternating order. The horizontal test sent 34 arrow presses over five seconds across an overflowing 23-tile Apps row and checked that it scrolled. Frame times are intervals between `requestAnimationFrame` callbacks, not frames presented by a display. The JSON files contain the raw intervals and pooled summary. No physical TV was tested.

- [Frame-time chart](frame-times.svg) and [wallpaper motion comparison](wallpaper-motion.svg)
- [Emulator screenshot](alternative-view.png)
- [Raw frame intervals](timings.json) and [summary statistics](summary.json)
