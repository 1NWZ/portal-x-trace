---
name: portal-x-trace
description: Use the bundled PORTAL-X TRACE browser compositor to add tracking boxes, evidence labels, scientific grids, surveillance overlays, glitch effects, and film grain to images or videos, then export PNG frames or WebM recordings. Static image input defaults to a static PNG output. Trigger for cyberpunk visuals, technical data overlays, found-footage graphics, motion tracking aesthetics, experimental posters, social-media covers, or processed image and video artwork.
---

# PORTAL-X TRACE Visual Compositor

Use the self-contained static app in `assets/webapp/index.html`. The app processes user media locally in the browser and does not require external libraries or CDN access.

## Launch the compositor

1. Check that `assets/webapp/index.html` exists.
2. Start a local static-file server rooted at `assets/webapp/`. Prefer an available built-in server such as `python3 -m http.server`.
3. Open the local URL in a modern Chromium-based browser for the broadest video-recording compatibility.
4. If the environment cannot launch a browser, give the user the path to `assets/webapp/index.html` and concise local-serving instructions.

If a distribution platform removed the HTML asset, explain that the complete Skill package is required; `SKILL.md` describes the workflow but cannot reproduce the interactive compositor by itself.

## Output selection

- For a static source image, default to one static PNG. Preserve the source photograph as a still image within the composition; capture overlays and effects in a single frame.
- Do not infer an animation or video request from tracking, glitch, grain, or cyberpunk styling. The live preview may animate, but the delivered PNG must remain a single still image.
- Use WebM recording for a static source only when the user explicitly requests animation or video.
- Preserve the original input file unchanged and save the processed PNG as a separate file.

## Compose an image or video

1. Ask for the source image or video and any necessary missing composition choices (output ratio, visual style, theme color). For static image input, use PNG without asking the user to choose between still and video. For video input, clarify still PNG versus WebM when the requested deliverable is unclear.
2. Upload one image or video through `Media & Ratio`.
3. Select the output ratio. Use `3:4` for a Xiaohongshu portrait image, `9:16` for vertical video, `1:1` for square artwork, or `Original Ratio` when preservation matters.
4. Choose one master style:
   - Use `Evidence Tree` for archival labels, coordinates, timestamps, connected targets, and documentary evidence aesthetics.
   - Use `Red Machine` for alert blocks, bold tracking boxes, motion-reactive fragments, and aggressive warning graphics.
   - Use `Biotech Grid` for crosshair grids, intersection nodes, coordinates, and scientific-interface aesthetics.
   - Use `Surveillance` for target identifiers, edge-linked boxes, and dark monitoring-system aesthetics.
5. Set the global theme color and edit the style-specific labels, density, target size, timestamps, and coordinates.
6. Combine image effects as needed: black and white, hard contrast, inversion, ASCII rendering, deep glow, film grain, and glitch-mask coverage.
7. Click the canvas to add a tracker manually. Use `Randomize Positions` to regenerate tracker placement or `Clear` to remove trackers.
8. Inspect label contrast, cropping, tracker placement, text overflow, and motion readability before export.

## Export

- Click `Export Frame (.PNG)` to save the current canvas as a still image.
- Only when video output is requested, click `REC Video (.WebM)`, let the desired segment play, then click `STOP RECORDING...` to finish and save it.
- Keep the browser tab active while recording when possible because background-tab throttling can affect animation timing.
- If WebM recording is unavailable, use a current Chromium-based browser or export still PNG frames instead.

## Design guidance

- Keep tracking labels short to prevent overflow around small target boxes.
- Use white or a bright accent color over dark footage; use black or deep red over bright imagery.
- Reduce tracker count and glow when the source is visually busy.
- Use moderate grain and glitch coverage for readable editorial work; increase them only for intentionally degraded visuals.
- Treat motion tracking as an aesthetic approximation rather than measurement-grade computer vision.
- Do not upload private media to external services: processing and export happen locally in the browser.

## Preserve and deploy

Copy the entire `assets/webapp/` directory when moving or deploying the tool. Publish it on any static host without a build step. Serve only the web-app directory when possible instead of exposing the whole Skill package.
