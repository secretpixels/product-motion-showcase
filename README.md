# Product motion showcase

My way of making motion videos for apps, websites and brands: real screen recordings, camera moves, overlapping animation, a music-driven edit and a perfect loop.

Built from my own work as a freelance UI/UX and product motion designer. I use it to speed up my workflow, and now you can too.

By [Secretpixels](https://github.com/secretpixels).

## Two kinds of video

- **Interface video** (portfolio video): shows an app or website in motion. Around 15 seconds, never more than 30, made to loop perfectly.
- **Brand reel** (showreel): tells the story of a brand or project as a motion graphic piece. Usually 16:9 and longer.

Formats: 9:16 (Reels), 16:9 (YouTube, brand reel), 1:1 and 4:3.

## What it gives your AI assistant

- Questions, asked one at a time, so it starts with the right brief.
- How I bring static screens to life with subtle interface motion.
- My three portfolio frames (app with one or two devices, web with one device), with exact sizes.
- A list of required material: at least 3 brand colours, a logo, typography and a few screens or recordings.
- How my usual interface video is built: a brand moment, one realistic flow and a seamless loop.
- A poster frame for the thumbnail, taken from a moment where nothing moves.
- Motion blur on everything that moves, for smoother motion.
- My timing rules: overlapping action, stagger, my 80/80 ease and a subtle bounce on some elements.
- How I handle the camera, token lines, labels, a brand switch and 3D objects.
- How I tie everything to the music, with the tempo math.
- A robust render and check routine.
- Music that starts with a hook and ends for real, not with a fade-out.
- The prompts and feedback style that work for me.

## Install

It is one skill folder in the open Agent Skills format. Install it as a folder in Claude Code or Codex, and upload it in the Claude app and in ChatGPT where Skills are available. Availability and exact steps vary by product and workspace. Step by step: see [INSTALL.md](INSTALL.md). The ready-made ZIP is on the Releases page.

## Requirements

- An AI assistant that supports Agent Skills.
- The method (questions, story, timing, prompts) needs nothing else. Rendering a video needs an environment that can run code and create files. After Effects is optional, for an editable version.

## Use it

Ask your AI assistant for an interface video or a brand reel, or share a storyboard and say "make this into a motion video". The skill asks its questions one by one, tells your story back and only builds after you say yes.

## What is inside

```
INSTALL.md
skills/product-motion-showcase/
  SKILL.md
  agents/openai.yaml
  assets/frames/
  references/
    video-types.md
    interface-flow-video.md
    frames.md
    ui-motion.md
    example-white-label-piece.md
    workflow.md
    timing-and-easing.md
    camera-tokens-and-3d.md
    sound-and-music.md
    prompts-and-feedback.md
```

It is plain text and three images, with no scripts. `agents/openai.yaml` is optional metadata for ChatGPT and Codex.

## About me

I'm a freelance digital product designer (UX/UI, design systems and motion), working as Secretpixels. I use AI to set up and speed up design workflows.

- Portfolio: https://www.secretpixels.com
- X: https://x.com/hugonoorlander
- GitHub: https://github.com/secretpixels

## License

MIT
