# Video types

## Contents
- Formats
- Interface video
- Brand reel

## Formats

| Ratio | Use | Size |
| --- | --- | --- |
| 9:16 | Reels | 1080x1920 |
| 16:9 | YouTube, brand reel | 1920x1080 |
| 1:1 | Square feed video | 1080x1080 |
| 4:3 | My portfolio frame | 1600x1200 |

Interface videos run at 30 fps. Brand reels run at 25 or 30 fps. When the user already has a frame or template, take the format from that.

## Interface video

**Purpose.** Show an app or a website in motion. The product is the hero. Use one of my frames (`frames.md`).

**Two shapes.**

- **Flow video (my usual).** One realistic flow through the product in a static frame. Aim for around 15 seconds (mine run 9 to 20). Never more than 30, and only when it cannot be shorter. Details in `interface-flow-video.md`. Use this by default.
- **System piece (bigger).** With camera moves, token lines and a brand switch. Use it when the point is to show a design system or theming. Keep it as short as the story allows, 30 seconds at most. My example runs 25. See `example-white-label-piece.md`.

Both have a seamless loop, a poster frame as frame 0 (see `workflow.md`) and motion blur on everything that moves.

**Building blocks of the system piece.** Pick 3 to 5 and put them in a clear order. Not every project needs all of them.

1. **Open on real screens.** Always. Real screens and screen recordings, never mock-ups when the real thing exists.
2. **Camera over the interface.** Move across the screens to point at details.
   - **Subtle UI motion.** When the screens are static, bring the interface to life: entrances, state changes, toggles, buttons, list items. Keep it subtle, so it still looks like the real product. See `ui-motion.md`. Recordings stay as they are.
3. **System reveal (optional).** Design tokens drawn as lines with label pills, when the project has a token or theme system. Use the project's own token names. Never reuse names from another project. If the names are unknown, ask for them or skip this block.
4. **Brand or theme switch (optional).** Only when the project has more than one brand or theme.
5. **Object moment (optional).** 3D or product objects turning, or a grid of them.
6. **Logo close.** The logos come in and fold back, so the end joins the start.

When a project has no tokens and one brand, skip blocks 3 and 4 and put the weight on screen recordings, camera and rhythm.

## Brand reel

**Purpose.** Tell the story of a brand or project as a motion graphic piece.

**Format and length.** 16:9, 1920x1080, 25 or 30 fps, usually 60 to 80 seconds. Build it on whole bars, so the length is exact. Examples: 132 BPM x 44 bars = 80 seconds, 120 BPM x 30 bars = 60 seconds. It may end on a seamless loop.

**Material.** Brand colours, logo, typography, real screens, plus 2 or 3 images that fit the brand.

**Story pattern.**

1. A statement, typed or revealed word by word.
2. The brand or product reveal, with its logo animation.
3. The explanation in parts, one part per scene. For a brand identity: voice, typography, colour, motion, icons, photography, illustration and layouts. For a product: the problem, how it works and the answer.
4. The brand applied: layouts, mockups, a phone in a hand, a screen on a wall.
5. A finale: the logo animates or morphs, then an end card.

**Rhythm.** Calm scenes with long holds first, then cuts that accelerate towards a climax (in one of my reels the gap between cuts shrinks from about 0.9 seconds to 0.1 seconds). Or no hard cuts at all: one stream of morphs where each element turns into the next. Scenes overlap, so the next one starts while the last one is still leaving.

**Section breaks.** A switch from a dark scene to a full-bleed brand colour can mark a new part of the story.

**Small touches.** A button that morphs into a smiley and then into the logo. Statements that are typed out.

**Music.** If there is music, it starts with a hook and ends for real, with a stinger (a bass hit or a whoosh) as the final logo animates. See `sound-and-music.md`.

**Principles.** The same ones as in `SKILL.md`: understand first, overlap, music as the clock, one timeline, text stays readable.

Ask the user whether they have earlier brand reels or motion pieces to share. Study them before designing: look at the cut rhythm, how type and images move, and how the story is paced. This needs a file the assistant can open and frames it can extract (for example with ffmpeg). A link to a streaming page is not enough: ask for the file.
