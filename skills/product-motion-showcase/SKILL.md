---
name: product-motion-showcase
description: Make short, looping motion videos for apps, websites and brands in the Secretpixels style. An interface video (portfolio video) shows an app or website in motion. A brand reel (showreel) tells the story of a brand or project as motion graphics. Use when the user asks for a portfolio video, showreel, app or web presentation video, UI or screen-recording animation, a looping LinkedIn video or brand motion, or wants to go from a storyboard to a rendered video, even without naming a tool or style. Not for static designs, slide decks or edits of an existing finished video.
---

# Product motion showcase

This is how I make motion videos for apps, websites and brands. It is my style and my way of working. Use it as a method, not as a template to copy frame by frame. It works for any brand, so never carry names, colours or content over from another project.

This skill is written in my voice. "I" and "my" describe my way of working. "Me" in "tell me", "ask me" and "show me" means the person you are working with, the user. It is written for any AI assistant: where a step needs a tool, a file or a person, the text says so (see "What the environment must provide").

## Two kinds of video

**Interface video** (for an app or a website, what I also call a portfolio video). Shows the interface in motion, built from real screens and screen recordings in one of my frames. Short: aim for around 15 seconds, never more than 30, made to loop perfectly.

**Brand reel** (for a brand, what I also call a showreel). Tells the story of a brand or project as a motion graphic piece, with more room. Usually 16:9 and longer than 30 seconds.

Both can end on a seamless loop: the last frame joins the first frame of the animation. Details in `references/video-types.md`.

## Before you start: ask, one question at a time

Ask one question per message and wait for the answer. Skip what the user already told you. Offer a default with every question. Where the environment can show tappable options (for example a multiple-choice question tool), use them for questions with a few fixed answers. If it cannot, write the options in plain text and name the default. For open questions the user has to type, suggest the answer you would pick, so a short yes or a small correction is enough.

1. **What is the video for: an app, a website or a brand?** An app or a website becomes an interface video. A brand, a service or a person becomes a brand reel. Ask this first, because it decides everything after it.
2. **Which frame?** Only for an app or a website. App with one device (my default), app with two devices (only when two things side by side make it clearer, for example two brands of a white-label product), or web with one device. See `references/frames.md`.
3. **Which aspect ratio?** My frames are 4:3. Other options: 16:9 (YouTube, brand reel), 9:16 (Reels) and 1:1. Defaults: 4:3 for an interface video, 16:9 for a brand reel, 9:16 if it is for Reels.
4. **The feel: subtle or fast?** Subtle is my usual calm motion. Fast is quick and kinetic: short scenes, kinetic text and cuts on the beat (`references/fast-style.md`). Default: subtle for an interface video. For a brand reel, ask.
5. **The brand and project.** Which brand, and which app, website or project is it? This is an open question, so suggest what you can already tell from the material.
6. **The material.** Ask for the required material below. Do not start until the minimum is there. If you plan a presentation scene (see `references/presentation-scenes.md`), ask now for the assets it needs.
7. **The music.** Music is optional. Does the video get music? If yes: a reference track or video to match, or music made from scratch? A reference works best as a file, so it can be measured instead of described. Without a reference, use my beeps and 808 style as the starting point, and let it differ per video. Only use a paid tool (Suno, ElevenLabs, a licensed library) when the user asks for it, since it spends their credits or budget. Offer two variants to choose from, for example with a different hook. If there is music, the sound design (whooshes, blobs, swishes) comes with it as a separate track.
8. **Tools and end result.** Which tools can you use here (Node.js, ffmpeg, Remotion, After Effects)? Only the rendered video, or also an editable After Effects file?

State the length and the loop as defaults instead of asking: an interface video of around 15 seconds, a longer brand reel, both with a seamless loop. Change them only if the user objects.

Choose the shape of an interface video yourself: when the story is about a design system or theming, make a system piece. Otherwise make a flow video.

When the answers are in, show the story as a storyboard (`references/storyboard.md`): one card per scene in a small `storyboard.html`, with a ratio control. In the reply, add one line with the one thing the viewer should remember. Propose that thing yourself, based on the material, and let the user correct it. If the environment cannot make files, tell the story in text instead. Then ask: "Shall I make a draft?" Build nothing before that yes. A note on the storyboard is not a yes: update it, show it again and wait for a clear "yes" or "go ahead".

## Required material

Minimum, for every video:

- **At least 3 brand colours** (hex values), ideally as a full light-to-dark scale with the rule for using it (for example: dark shades for backgrounds, light shades for text).
- **A logo**, ideally as SVG or a PNG with a transparent background.
- **Typography**: font names, or the font files.
- **A few app or web screens** of the real product. Static screens are best, because I animate them myself. If that is not possible, screen recordings work.

Extra for a brand reel:

- **2 or 3 images that fit the brand**, such as photography or key visuals.

Optional but helpful: a storyboard, 3D renders, a music reference, and pieces of the UI, images or icons to present in a grid or a gallery, and the desktop and the mobile layout of the same page.

If the screens are static (stills instead of recordings), bring the interface elements to life subtly. See `references/ui-motion.md`.

If something is missing, say what is missing and why it matters. Continue with placeholders only if the user agrees.

## Unisex apps and websites

I show apps unisex: not iOS, not Android. Remove every native element from the screens: the status bar (time, signal, battery), the notch or Dynamic Island, a camera cut-out, the home indicator and the Android navigation bar. For websites, remove the browser (Chrome, Safari and so on): the window controls, tabs, address bar, toolbars and scrollbars. Only the interface itself stays. My device frames are plain rounded rectangles for the same reason. How to do it is in `references/frames.md`.

## Text

Text has its own scene between the screens. It never sits next to, above or below a device. At most two lines are on screen at a time, so a longer text is split into steps that follow each other, unless the user explicitly asks for more. Text and a group of other elements never start at the same moment: the text comes first. With a voice-over, the text is on screen as long as the voice speaks it. How I animate it is in `references/text-animation.md`.

## How I think

1. **Understand before building.** Read the storyboard and the material first. Show me the story back, as a storyboard, and wait for my "yes, that's it". This saves rounds.
2. **Overlap, never one after another.** Do not play animations in a row. When a move is nearly done, about 70 percent, the next one starts. The proper name is *overlapping action*, in short *overlap*. Moves flow into each other but never collide in view. When the same move repeats over several items, that is a *stagger*: each next item starts when the previous one is about halfway.
3. **Every shot turns into the next.** No cross dissolves. The outgoing shot's key object (a card, a logo, a frame, a device) grows, morphs or slides into what the next shot needs. Ask yourself: how does this shape become that shape? Hard cuts are only for a short, speeding-up sequence, always on the beat, never between two calm shots.
4. **Keep the subject centred.** The eye should never have to go looking for it. Build an invisible crosshair into every shot. Presentation scenes (mosaic, gallery, card wall) are the exception.
5. **Something is always moving.** Even a slow drift or a gentle push is enough. A still frame feels stale.
6. **Direction never reverses.** No zoom in then out on the same subject, no orbit that turns back. Drive each move on one continuous curve. The loop closing is the only exception.
7. **Ease 80/80, and bounce some things.** Every move uses ease in 80 and ease out 80, linked, or has a subtle bounce. No other curves. Not everything bounces. See `references/timing-and-easing.md`.
8. **Motion blur on.** Everything that moves gets motion blur, so the movement runs smoother.
9. **If there is music, it is the clock.** Format, length and tempo are fixed early, and every key moment lands on a bar or a beat. Make the music before the picture is final, and regenerate it whenever the timing changes. Music and sound effects are two separate tracks. Music is optional.
10. **One timeline, one model.** All motion is a pure function of time, driven by one table of named moments. Change one moment and everything shifts with it. This also makes exporting to other tools possible.
11. **Text stays readable.** Labels and titles sit in a flat layer above everything else, never touch each other and leave before something covers them.
12. **Every sound has a cause on screen.** No decoration.
13. **Loop on purpose, and a poster up front.** The last frame joins frame 1 of the animation, and frame 0 is a poster for the thumbnail, taken from a moment where nothing moves. Check both.
14. **Check every transition frame by frame.** A contact sheet hides small jolts.
15. **One light source, shallow depth of field.** For 3D and product shots: light from one direction and a soft, out-of-focus background. That alone makes it read as filmed, not rendered.
16. **A delivered animation stays exactly as delivered.** When I hand over a finished logo animation or brand video, place and scale it, nothing more: no re-animating, re-timing or recreating it. On a dark background, screen- or add-blend it rather than redrawing it.
17. **Compare against the real product.** Put the actual app, logo or product next to the render and check that every detail is there before showing it to me.
18. **I judge the music, if there is any.** You can measure loudness and tempo, but you cannot hear. Ask me to listen before you call the audio done.

## Workflow

1. Ask the questions, read the material, show the story as a storyboard, and ask "Shall I make a draft?" Build nothing before the yes.
2. Inventory the assets and check them against the required material (`references/workflow.md`).
3. Fix format and length, and the tempo too if there is music (`references/sound-and-music.md`).
4. Build the timeline model and the first version (`references/timing-and-easing.md`, `references/camera-tokens-and-3d.md`).
5. Make a cheap draft (half resolution, a range of frames or a few stills) and check each section and transition. Show it, then ask: "Shall I render the final version?"
6. Iterate with my feedback (`references/prompts-and-feedback.md`).
7. After that yes, render robustly, master the audio, pick the poster frame and run the final checks.
8. If I want an editable version, export the model to After Effects (`references/workflow.md`).

So the user says yes three times: to the story, to a draft and to the final render. Each answer ends with the next question, so nobody has to ask where the video is.

## Reference files

Read only what the current step needs.

- `references/video-types.md`: interface video and brand reel, formats, lengths and story patterns.
- `references/interface-flow-video.md`: how my usual interface video is built, with timing numbers and details.
- `references/presentation-scenes.md`: how I present supplied assets: the cover mosaic, a component grid, a responsive morph, a wall reveal, a device with a grid around it, a gallery and a logo grid.
- `references/text-animation.md`: how I animate text, where it lives, how much of it at once and how long it stays.
- `references/ui-motion.md`: how I bring static screens to life with subtle interface motion.
- `references/frames.md` and `assets/frames/`: my three portfolio frames with exact sizes and positions, the shadow that follows the background, and how to make apps and websites unisex.
- `references/example-white-label-piece.md`: one finished interface video, as an example of the building blocks.
- `references/workflow.md`: assets, the feedback loop, robust rendering, the poster frame and export.
- `references/timing-and-easing.md`: the time table, overlap, sped-up recordings, my 80/80 easing, subtle bounce, motion blur.
- `references/camera-tokens-and-3d.md`: camera, token lines, brand switch, 3D objects, the grid, the loop.
- `references/fast-style.md`: the fast feel next to my subtle one: kinetic text, an image cloud, assembling a mosaic and keyword scenes.
- `references/storyboard.md` and `assets/storyboard-template.html`: how to show the story as a cheap HTML storyboard with a ratio control, before building.
- `references/build-in-code.md`: how to build the video in code so every frame renders correctly: time-driven motion, loading, video and audio, preview and drafts, motion blur.
- `references/pitfalls.md`: problems I ran into before (rendering, 360 renders, layout, After Effects) and how to avoid them. Read it before the first render.
- `references/sound-and-music.md`: tempo math, self-made music, sound design, mixing.
- `references/prompts-and-feedback.md`: prompts that worked for me and how I like to give feedback.

## What the environment must provide

The method works in any AI assistant. Building the video needs more, and not every environment has it. Say what you can and cannot do, and what the user has to do.

- **Needs nothing special:** the questions, the story, the storyboard, the timing table and the prompts.
- **Needs code execution and file creation:** rendering the video, taking the poster snapshot, measuring loudness, cropping screens, looking at frames of a reference video. If you cannot run code, deliver the plan, the timing table and the scripts, and tell the user exactly what to run.
- **Needs software on the user's computer:** After Effects, for the optional editable version. The user runs the project script there.
- **Needs macOS and the user's permission (optional):** on macOS the assistant can also run the After Effects build script itself through AppleScript and check the result with `aerender`. Ask first. The first launch of After Effects often shows a dialog that the user must click away.
- **Needs the user:** brand colours, logo, typography and screens, listening to the music, picking the poster frame and a yes before building.

## Tools I use (swap in the user's own)

Node.js, ffmpeg and ffprobe for analysis and encoding, and Chrome as the render engine. A quick HTML and GSAP prototype for the first draft. React with Remotion for the final build, because it has real springs, per-layer audio and time control. After Effects for an editable end version. Swap in the user's own tools when they differ, but keep the principles above.

## About me

I'm Hugo Noorlander, a freelance digital product designer (UX/UI, design systems and motion), working as Secretpixels. I use AI to set up and speed up design workflows.

- Portfolio: https://www.secretpixels.com
- X: https://x.com/hugonoorlander
- GitHub: https://github.com/secretpixels
