# Workflow: from storyboard to render

## Contents
- Read the brief
- Inventory the assets
- Format, length, tempo
- The feedback loop
- Robust rendering
- Poster frame (thumbnail)
- Final checks
- Export to After Effects

## Read the brief

My storyboard is usually an HTML file with a sketch per scene. Unpack it, look at every sketch as an image and tell me the story back scene by scene. Do not build until I confirm. If something is unclear, ask one short question instead of guessing.

## Inventory the assets

First check the material against the required list in `SKILL.md`: at least 3 brand colours, a logo, typography and a few screens or recordings, plus 2 or 3 brand images for a brand reel. Say what is missing.

Note for every screen whether it is a still or a recording. Stills get subtle UI motion (`video-types.md`).

Check every screen for native elements and remove them (`frames.md`). For apps: status bar, notch or Dynamic Island, home indicator, navigation bar. For websites: the browser window, tabs, address bar, toolbars and scrollbars.

For every file, write down:

- resolution, fps, duration and whether it has transparency;
- for 360 degree renders: does the loop close? Compare the last frame with the first. Look for duplicate or missing frames;
- for screen recordings with a 3D object in them: the angle of the object at the moment it stands still, so the 3D render can take over without a visible jump.

Prepare what needs preparing:

- Logo animations on black become transparent (alpha).
- PNG sequences become sprite sheets, so they load fast and stay frame accurate.

## Format, length, tempo

Format and length come from the video type (see `video-types.md`), or from an existing frame of the user. Length is in whole seconds. If the video has music, pick the tempo so the bars fit the length exactly (see `sound-and-music.md`). That way every bar transition lands on a fixed moment and the loop closes without a seam.

## The feedback loop

Every round follows the same loop:

1. A quick draft render at half resolution.
2. A contact sheet per section.
3. A strip of frames around every transition.
4. Fix what is off.
5. Final render.
6. Master the audio.
7. Run the final checks.

Versions go up in numbers (v2, v3 and so on). Keep the previous one, so I can compare.

## Robust rendering

This applies to the browser-based route (for example Remotion with Chrome). A browser sometimes drops a layer for one frame. That is a flash I do not want to find after export. The fix:

1. Render as an image sequence, not straight to video.
2. Automatically find frames that are darker than their neighbours.
3. Re-render only those frames.
4. Then encode and master.

## Poster frame (thumbnail)

Frame 0 of the exported video is a poster: one still frame that shows up as the thumbnail when the video is shared in WhatsApp, on Dribbble or on LinkedIn. It should be the best shot of the video. In my own videos it often shows the brand screen next to the hero screen.

1. Find still moments: moments where nothing on screen moves. Use the timeline (every velocity is zero) or measure the difference between consecutive frames. A frame in the middle of a movement is blurred by the motion blur and looks unsharp as a thumbnail.
2. Render the snapshot from a still moment, at full resolution, without motion blur.
3. Show two or three candidates and let me pick the best one.
4. Put it in as frame 0, one frame long. The animation starts at frame 1. Frame 0 does not count for the loop: the last frame joins frame 1.
5. Frame 0 replaces the first frame of the animation. It is not an extra frame, so the video stays an exact number of seconds. Example: 15 seconds at 30 fps is 450 frames, and frame 0 is one of those 450.
6. When the video loops, the poster shows for one frame at every restart. That is fine.

## Final checks

- Duration is exact.
- Loudness is on target, if there is music.
- Frame 0 is the poster, and the loop is seamless: the last frame equals frame 1.
- No dropped frames.

## Export to After Effects

I like an editable end version. It needs After Effects on the user's computer: the assistant writes the scripts, the user runs them. It works because all motion lives in one model as pure functions of time.

1. A first script calculates every property per frame and thins the keyframes to what is needed.
2. Every keyframe gets my ease: influence 80 in, 80 out, speed 0.
3. A second script builds the After Effects project: shape layers with Trim Paths for the lines, text layers, screen recordings with Time Remap and a camera.
4. Render in After Effects and lay the result next to the Remotion version to compare.
