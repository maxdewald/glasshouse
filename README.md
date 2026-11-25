# Glasshouse Home wallpaper-drift benchmark

Alternative View + Pictures, 1920×1080, official Landscape wallpaper, Glasshouse C2 emulator. Baseline: `8fcf08cf0b98df086c1c52703e21f67c599784f0`. The patch moves the picture sideways by one device pixel every 3.75 seconds, using the browser's pixel density and the Home stage scale. It reverses at the end of its travel without zooming.

Headless Chromium with SwiftShader, 4× CDP CPU slowdown. Two baseline/patch pairs in alternating order. The horizontal test sent 34 arrow presses over five seconds across an overflowing 23-tile Apps row and checked that it scrolled. Frame times are intervals between `requestAnimationFrame` callbacks, not frames presented by a display. The JSON files contain the raw intervals and pooled summary. No physical TV was tested.

The device-pixel check covers a native 1080p viewport, a 1920×1080 CSS viewport at 2× pixel density, a native 3840×2160 viewport, and scaled/letterboxed windows. Comparing the pixels in before/after captures at 1× and 2× density confirmed a one-pixel horizontal shift in both. Browser-reported device pixels may differ from panel pixels if the system scales the browser output again.

- [Frame-time chart](frame-times.svg) and [wallpaper motion comparison](wallpaper-motion.svg)
- [Emulator screenshot](alternative-view.png)
- [Raw frame intervals](timings.json) and [summary statistics](summary.json)
