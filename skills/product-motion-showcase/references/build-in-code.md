# Building in code

Lessons for building the video in code. I use React with Remotion; the same rules hold for any renderer that draws the video frame by frame. This needs an environment that can run code.

## Contents
- Everything is a function of time
- Structure
- Loading before the first frame
- Video and audio
- Preview and drafts
- Motion blur

## Everything is a function of time

- Every value on screen is calculated from the current frame or time. No CSS transitions or animations, no animation classes, no timers, no clock time and no unseeded randomness. A renderer draws each frame on its own, so anything that depends on the previous frame breaks.
- Write timing in seconds and convert with the frame rate of the composition (seconds x fps). Never hard-code frame numbers, so a change of frame rate keeps the timing.
- Clamp every interpolation at both ends, so values do not run past their range before or after the move.
- Interpolate scale geometrically (multiply by the same factor per step) and apply the 80/80 ease to the progress. A linear scale looks slower as it grows.
- Easing and springs are in `timing-and-easing.md`. A spring is calculated from the time since it started, so every frame can be drawn on its own.

## Structure

- One component per scene, one shared time table with named moments, and one model file that holds all motion as pure functions of time. The scenes draw from the model, and the same model can be baked into keyframes for After Effects.
- Put assets in the project's static folder and reference them through the framework's static-file helper.
- Install add-on packages with the framework's own add command, so all versions match.

## Loading before the first frame

- Fonts: load them through a font loader that holds the render until they are ready. Otherwise the first frames show a fallback font.
- Images and sprite sheets: preload and decode them all before frame 1, and keep a reference so they stay decoded.
- Anything that loads (fonts, images, data) holds the render until it is ready (delay the render, then continue it).

## Video and audio

- Screen recordings: show them at an exact source time per frame, by freezing a frame-accurate video at the frame you calculate. That gives full control: speed ramps with the slow, fast, slow curve, holds, and a recording that continues across scenes.
- For a speed ramp, compute the source time per frame from a smooth speed curve (the sum of the speed per frame), so the speed never jumps. Use a source with at least the frame rate of the output, so no frame repeats.
- In simple cases, trim the start, limit the duration and set a playback rate on the video itself.
- Audio per layer: music, the effects track and the one-shots are separate audio layers, each with its own start. Ducking is a volume that is calculated per frame.

## Preview and drafts

- If the environment can open a local preview (this needs the user's own computer), open it as soon as the project runs and keep it open while working, so the user can watch and steer.
- Drafts are cheap: half scale, a range of frames around a transition, or a single still. Make a draft after the user says yes to it, show it, and ask before the final render.
- Final renders: see `pitfalls.md` (one tab, an image sequence, repairing dropped frames).

## Motion blur

- Motion blur stays on (see `SKILL.md`). In Remotion, `@remotion/motion-blur` offers `HtmlInCanvasMotionBlur` (experimental, needs HTML-in-canvas enabled in the preview) and `CameraMotionBlur` (works everywhere, with `shutterAngle` and `samples`). Call the frame hook inside the child component, not outside the blur wrapper.
- Use enough samples. Ghost copies or a stepped trail at a fast move mean too few samples.
- A frame in the middle of a movement is blurred, so it is never the poster frame.
