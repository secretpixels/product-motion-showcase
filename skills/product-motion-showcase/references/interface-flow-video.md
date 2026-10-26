# Interface flow video

My usual interface video: one realistic flow through an app or a website, in a static frame, made to loop.

## Format

- 1600x1200 (4:3), 30 fps. Aim for around 15 seconds (mine run 9 to 20). Never more than 30, and only when it cannot be shorter.
- One of my frames (`frames.md`). The device and the background stay still. All the motion happens inside the screen.
- A second device can come in when it makes something clearer. For example the brand splash on one device and the flow on the other.

## Material

Static screens are best: I animate them myself (`ui-motion.md`). If the user cannot do that, a screen recording works.

## Structure

1. **A brand moment.** A logo animation inside the screen or full-bleed on black: shapes that morph into the logo, a wordmark, a welcome line, a 3D object that spins in. Skip it only when the product has no logo moment.
2. **One realistic flow, in real time.** Three to six screens, used the way a real person would use them. Show every tap with a tap indicator.
3. **Back to the start.** The last frame equals frame 1 of the animation, so the loop has no seam. Frame 0 is the poster (see `workflow.md`).

## Tap indicator

A white circle with a soft shadow where the finger lands. On a website I have used a ring in the accent colour.

## Timing

- A page slide between steps: about 0.65 seconds (20 frames). The same kind of step gets the same duration over the same distance.
- A long scroll: 1.0 to 1.3 seconds.
- A small shift: 0.3 to 0.4 seconds.
- Ease: my 80/80 (`timing-and-easing.md`). Motion blur on everything that moves.

## Details I like

- Text that is typed live: amounts and words appear as they are typed.
- Text that is revealed line by line with a mask.
- Blur when items swap, for example in a carousel.
- A little blur on spinning 3D objects, on top of the motion blur.
- Static screens get subtle UI motion (`ui-motion.md`). Recordings stay as they are.

## Unisex

Apps are unisex: no status bar, notch, Dynamic Island, home indicator or navigation bar. Websites have no browser around them: no tabs, address bar, toolbars or scrollbars. See `frames.md`.

## Background

See `frames.md`.
