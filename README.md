# Motion Studio Ultra V8 — Creative Edition

A browser-based motion-graphics editor you can host on **GitHub Pages**. Includes the original 114 editable templates plus 24 new cinematic, editorial, data, and social motion scenes (**138 total**).

## Try it locally

The easiest preview is the separate **single-file HTML build** (`Motion_Studio_ULTRA_V8_138_Layouts.html`), which opens directly in Chrome/Edge. For this GitHub project, use a local HTTP server when testing video export:

```bash
python -m http.server 8000
```

Open `http://localhost:8000`.

## Publish on GitHub Pages

1. Create a repository on GitHub, such as `motion-studio-ultra`.
2. Upload the contents of this folder **at the repository root** (`index.html`, `assets/`, `README.md`, `.nojekyll`).
3. In **Settings → Pages → Build and deployment**, choose **Deploy from a branch**, branch **main**, folder **/(root)**, then save.
4. Once deployed, open `https://YOUR-USERNAME.github.io/REPO-NAME/`.

No build step, API key, database, or paid backend is required.

## Features

- 138 editable canvas templates, including cinematic geometry, typography, data dashboards, explainer scenes, editorial cards, and maps.
- 16:9, 9:16, and 1:1 layouts, with full-size 1920×1080 / 1080×1920 / 1080×1080 PNG and video export.
- Quick-edit headline and figure fields, including +/− controls when the value is numeric; all per-scene fields remain available below.
- 30+ font choices including Anek Kannada, Noto Sans Kannada, Noto Serif Kannada, Baloo Tamma 2, Tiro Kannada, Hind Mysuru, and installed system Kannada fonts.
- Text entrances: rise, slide, zoom, type-on, glitch and float; optional particles, light sweep, film grain, scanlines and sparks; metric count-up.
- Custom colors, backgrounds, editable map route stops, field-level size/position/color controls, save/load project JSON.
- PNG, transparent PNG, browser WebM, and MP4 (where supported) export. MP4 encodes H.264 via WebCodecs and dynamically imports mp4-muxer from jsDelivr.

## Limitations / dependencies

- **Fonts:** Google Fonts require network access (or must be installed locally). System fonts such as Nirmala UI / Tunga depend on the viewer’s OS.
- **MP4:** Requires an H.264-capable WebCodecs-enabled browser and HTTPS or localhost. The current MP4 muxer is fetched from a third-party CDN, so MP4 is *not* completely offline. Use WebM if unavailable.
- **WebM:** Export is real-time and uses `MediaRecorder`; leaving the tab or heavy system load can affect recording timing.
- **Maps:** Existing built-in geometry is general-purpose illustration, **not legal/administrative boundary authority**. Geographic routes are lines through user-entered coordinates, not road navigation.
- **No audio timeline:** Exports are silent videos. This is a browser motion-graphics editor, not a complete After Effects replacement.
- **Existing third-party sources / licenses:** Review all assets, source-data, font and dependency licenses before publishing publicly. This package does not grant rights over third-party material.

## Source layout

```
index.html              Page and controls
assets/studio.css       Styling, responsive UI, V8 polish
assets/world.js         Bundled generalized geographic outlines
assets/studio.js        Template data, rendering, exports and V8 features
README.md               Setup and usage
.nojekyll               Static hosting compatibility
```

## Quick guide

1. Select a template or search by topic; the **Surprise me** button reveals another layout.
2. Use the **Content** tab for your headline and numbers. Use the +/− buttons to tweak numeric figures.
3. Choose your colors and Kannada/English font under **Design**.
4. Choose text entrances and an atmosphere under **Motion**, and edit duration, playback speed and framing.
5. Save your editable project JSON, export a frame as PNG, or render MP4/WebM.

**Production tip:** Wait until your chosen web font has loaded before exporting. Browser encoder support can vary by device.
