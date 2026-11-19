# Known pitfalls

Problems I ran into before, and how to avoid them. Read this before the first render.

## Contents
- Rendering
- 360 renders and sprites
- Layout
- Screens and logos
- After Effects scripting
- Working together

## Rendering

- In Remotion, the bundled headless browser can hang on "Waiting for root component". If you see it, set the installed Chrome as the browser in the Remotion config.
- Render with one browser tab (concurrency 1). With several tabs, Chrome dropped whole layers (a phone, a row of objects) for a single frame.
- Render to an image sequence, find frames that are much darker than both neighbours (more than 15 percent), re-render only those, then encode. Run this check on every final render.
- Motion blur with too few samples leaves ghost copies or a stepped trail at fast moves. Raise the samples.
- A render on the command line clashes with a running preview on the same port. Render on another port.
- Paint sprites as background images and decode all sheets before the first frame. A large transformed image per sprite made Chrome skip rows.

## 360 renders and sprites

- The last frame of a 360 render often equals the first. Drop it, or the turn stutters once per rotation.
- Check every sequence for missing or duplicate frames: compare each frame with the next one.
- Turning and taking over an object from a recording are in `camera-tokens-and-3d.md`.

## Layout

- Check that no two labels touch over the whole move, not just at one frame.
- Measure text and interface positions in a real browser before rebuilding them in another tool.

## Screens and logos

- A light rim or stair-steps along the rounded corners of a device: the edge of the screen shows. See "Clean corners" in `frames.md`.
- A logo animation that plays its own build-up shows fragments and dots, and that reads as flicker. Use the finished state.

## After Effects scripting

This is the optional route to an editable version. It needs After Effects on the user's computer, and the user's permission before any script runs.

- The first launch of After Effects often shows a dialog (sign-in, welcome, recovery). Ask the user to click it away.
- On macOS, a script started through AppleScript returns nothing. Report errors another way, for example by saving a file whose name holds the error message.
- New shape layers have their origin in the middle of the composition. Set the anchor and the position to 0,0, so the shape coordinates are composition coordinates.
- Adding a property to a shape group makes earlier references to its siblings invalid. Look them up again.
- Time Remap cannot lose all its keyframes and cannot go past the last frame of its source.
- Separate the position dimensions (X, Y, Z), so keyframes do not curve between each other.
- Write the 80/80 ease onto every keyframe (influence 80 in, 80 out, speed 0).
- Install the fonts before building, and put them in the project folder too.
- Render the project with `aerender` and lay it next to the original, frame by frame, at every transition.

## Working together

- Users often dictate their feedback. Expect transcription typos and read for the intent.
- After a feedback list, confirm briefly and make the next draft straight away. Ask before the final render.
