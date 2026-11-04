<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="Logos/Pixel%20Transparency%20Logo%20-%20White.png">
    <source media="(prefers-color-scheme: light)" srcset="Logos/Pixel%20Transparency%20Logo%20-%20Black.png">
    <img src="Logos/Pixel%20Transparency%20Logo%20-%20Grey.png" alt="Pixel Transparency" width="200">
  </picture>
</p>

# Pixel Transparency for RetroArch
_v3.0 by mattakins · Copyright (C) 2025–2026 Matt Akins._

<img width="2240" height="1008" alt="image (28)" src="https://github.com/user-attachments/assets/226d963a-0a63-4959-a64f-4f16d45d55f4" />

Pixel Transparency recreates the reflective look of a Game Boy Color LCD. Bright pixels reveal a textured backing, with adjustable tint, transparency, and pixel shadows.

**Sunlight Shimmer** adds moving glare and rainbow shimmer. Motion follows device tilt when supported by the device and RetroArch build; lighting and shadows also have manual controls.

## What’s new in v3.0

- LCD grids are integrated into the shader pipeline.
- Pixel Transparency and Sunlight Shimmer each include six grid styles.
- Soft and Accurate modes control how the grid combines with the screen effects.
- Shared cache passes handle shadows, film noise, and lighting.

## Install and load

1. Download this repository and copy the contents of [`pixel_transparency-slang/`](pixel_transparency-slang/) into RetroArch’s Slang shader directory. Keep the folder structure intact.
2. Load a game with a video driver that supports Slang shaders.
3. Open **Quick Menu → Shaders → Load Preset** and choose:

   - [`handheld/pixel_transparency.slangp`](pixel_transparency-slang/handheld/pixel_transparency.slangp) for transparency and shadows.
   - [`handheld/sunlight_shimmer.slangp`](pixel_transparency-slang/handheld/sunlight_shimmer.slangp) to add glare and rainbow shimmer.
4. Enable the core’s color correction and interframe blending options where available.
5. Adjust the effect under **Shader Parameters**.

Both handheld presets use the Authentic GBC grid. The v3.0 presets include their own grid passes; load them directly instead of appending them to another LCD shader.

## Choose a grid

Find the alternatives in [`presets/pixel_transparency/`](pixel_transparency-slang/presets/pixel_transparency/). Each style has a `pixel_transparency-` and a `sunlight_shimmer-` preset:

- `authentic_gbc_fast`
- `lcd1x`
- `lcd3x`
- `lcd-grid-v2`
- `simpletex_lcd`
- `zfast_lcd`

The grid section in **Shader Parameters** offers two modes:

- **Soft (0):** applies transparency and lighting over the grid.
- **Accurate (1):** applies the grid after the screen effects.

The `pixel_transparency-accurate.slangp` and `sunlight_shimmer-accurate.slangp` shortcuts select Authentic GBC with Accurate mode enabled. The other presets default to Soft mode.

## Other downloads

The [`pixel_transparency-glsl/`](pixel_transparency-glsl/) folder contains the older GLSL release. It has not been updated to the v3.0 pipeline.

## Earlier release comparison

![Pixel Transparency with LCD1x](Screenshots/lcd1x%20-%202.png)
