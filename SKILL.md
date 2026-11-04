---
name: portal-x-trace
description: Create PORTAL-X TRACE visuals with tracking boxes, evidence labels, scientific grids, surveillance overlays, glitch and film grain. Prepare Seedance image-to-video prompts and use an available authorized model tool or web workflow for AI video without requiring API setup; use the bundled browser compositor for static PNG artwork. Preserve the model-native video format. Trigger for cyberpunk visuals, technical data overlays, found-footage graphics, motion tracking aesthetics, experimental posters, social-media covers, or processed image and video artwork.
---

# PORTAL-X TRACE Visual Compositor

This edition requires no API configuration. Route by the requested deliverable: video requests use a Seedance prompt and an available authorized model tool or web workflow; static artwork uses `assets/webapp/index.html`. If no video-generation capability is available, deliver a ready-to-use prompt and a short manual handoff, clearly labeled as preparation rather than a generated video. Do not request an API key or model endpoint as a prerequisite.

## Launch the compositor

1. Check that `assets/webapp/index.html` exists.
2. Start a local static-file server rooted at `assets/webapp/`. Prefer an available built-in server such as `python3 -m http.server`.
3. Open the local URL in a modern Chromium-based browser for the broadest video-recording compatibility.
4. If the environment cannot launch a browser, give the user the path to `assets/webapp/index.html` and concise local-serving instructions.

If a distribution platform removed the HTML asset, explain that the complete Skill package is required; `SKILL.md` describes the workflow but cannot reproduce the interactive compositor by itself.

## Output selection

- An explicit request for video, animation, image-to-video, or moving footage takes precedence over the input file type: follow the Seedance workflow even when the input is a static photograph.
- For a static artwork request, or a photo without any motion request, default to a separate static PNG and preserve the original file.
- Preserve the video format returned by Seedance. Do not require MP4, transcode automatically, or rename an extension to imply conversion.
- Browser canvas recording is only for an explicit request to record the local effects preview. Never substitute it for AI video generation, including after a Seedance failure.

## AI video with Seedance — no API required

1. Read `references/seedance-no-api.md`. Inspect the supplied image and resolve the requested motion. If an image is missing, request it; do not invent its visual details. Choose modest motion and a short single shot unless the user specifies otherwise.
2. Produce a complete, image-specific Chinese prompt: source identity and composition, subject motion, camera movement, one TRACE style, overlay behavior, color, and constraints. Preserve a still subject only when the user requests it; a static input alone does not prohibit motion.
3. Check for an already available Seedance-capable tool or authorized web workflow. Do not assume this skill supplies a model, account, credits, or credentials. Do not invoke an unrelated image model as a video substitute.
4. If a usable tool exists, use its actual schema. For a web workflow, inspect the current page and available options rather than inventing model names or controls. Use the user's selected account and source image; if login or a required account action needs the user, hand off that step. Do not purchase credits or subscriptions automatically.
5. If model access is unavailable, deliver the prompt with concise instructions to upload the photo to the user's Seedance-capable interface, choose image-to-video and supported settings, then generate. Label the result “视频生成提示词（尚未生成视频）”. Do not repeatedly ask for an API key, block prompt preparation on setup, or claim that a prompt is a finished video.
6. After a real generation, inspect available playback for identity, intended motion, stable overlays and visual artifacts. Deliver through the host's media preview when supported, otherwise provide the actual result link. Preserve the returned format, including WebM or MP4; the format does not determine whether it was AI-generated. Clearly distinguish submitted, still generating, failed, and completed states. Check existing task status before retrying an uncertain submission.

## Local compositor: static artwork or explicit preview recording

1. Use this workflow for static artwork or an explicit local-preview recording request. Resolve the source and necessary composition choices (ratio, style, theme color). AI video requests use the Seedance workflow above.
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
- Only when local preview recording is explicitly requested, click `REC Video (.WebM)`, let the desired segment play, then click `STOP RECORDING...` to finish and save it.
- Keep the browser tab active while recording when possible because background-tab throttling can affect animation timing.
- If WebM recording is unavailable, use a current Chromium-based browser or export still PNG frames instead.

## Design guidance

- Keep tracking labels short to prevent overflow around small target boxes.
- Use white or a bright accent color over dark footage; use black or deep red over bright imagery.
- Reduce tracker count and glow when the source is visually busy.
- Use moderate grain and glitch coverage for readable editorial work; increase them only for intentionally degraded visuals.
- Treat motion tracking as an aesthetic approximation rather than measurement-grade computer vision.
- Local compositor processing stays in the browser. Actual AI generation through a model tool or web service sends the selected image and prompt to that service; use only the media supplied for this task and disclose that remote processing when starting generation.

## Preserve and deploy

Copy the entire `assets/webapp/` directory when moving or deploying the tool. Publish it on any static host without a build step. Serve only the web-app directory when possible instead of exposing the whole Skill package.
