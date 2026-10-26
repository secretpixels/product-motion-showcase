# Timing and easing

## Contents
- One time table
- Overlap (overlapping action)
- Speeding up screen recordings
- Easing: my 80/80 rule
- Subtle bounce
- Motion blur

## One time table

Keep one table with named moments, such as logos in, lines start, toggle, zoom out, take-over and drop. Every animation refers to that table. When I change one moment, everything else moves with it. Never hard-code a time inside an animation.

## Overlap (overlapping action)

Do not play animations one after another. When a move is nearly done, about 70 percent, the next one starts. The name for this is *overlapping action*, in short *overlap*.

The moves overlap in time but not in view: they flow into each other, they do not collide.

When the same move repeats over several items, each one starting a little after the last, that is a *stagger*. My stagger: each next item starts when the previous one is about halfway, so they come in half after each other. Use it for grids, lists and rings of objects, and use overlap for the main story beats.

## Speeding up screen recordings

Screen recordings are sped up with a slow, fast, slow curve. You see more in the same time, and the important moments (a picker that closes, a panel that opens) land exactly on the beat. Recordings keep running through the scene instead of restarting.

## Easing: my 80/80 rule

Every move gets ease in and ease out at **80**, linked. In After Effects I set ease in to 80 and ease out to 80, linked, for example with an ease panel. That is an influence of 80 percent with a speed of 0 on both sides of every keyframe.

In code the same curve is `cubic-bezier(0.8, 0, 0.2, 1)`. In Remotion: `Easing.bezier(0.8, 0, 0.2, 1)`.

The feel: a slow start, a fast middle and a long, soft landing. Use it for everything: entering, camera moves, repositioning and leaving. Do not fall back on the default easy ease or on linear. Only constant motion, like a continuous rotation or a scrolling recording, is linear.

Leaving is still shorter than entering. Things that exit should not linger.

Every move is either this 80/80 ease or a subtle bounce. I do not use other curves.

When exporting to After Effects, write this ease onto every keyframe: influence 80 in, 80 out, speed 0.

## Subtle bounce

Not everything bounces. Alternate: some elements move with the 80/80 ease, others arrive with a subtle bounce. That mix gives the piece rhythm and personality. If everything bounces, nothing does.

| Feel | Spring damping (Remotion) |
| --- | --- |
| Subtle bounce | 13 to 18 |
| Playful bounce (a heart, a button) | 11 to 12 |

In After Effects, build the same feel as a small overshoot that settles, by hand on the keyframes or with an expression.

Use a spring where something has weight or personality. Use the 80/80 ease for everything that should feel calm and precise.

## Motion blur

Motion blur is on for everything that moves. It makes the movement look smoother, especially at 30 fps.

- In After Effects: switch motion blur on for every moving layer and for the composition. Start with a shutter angle of 180 degrees and adjust by eye.
- In Remotion: use its motion blur component, so the moving layers get extra sub-frames and the blur matches.
- Spinning 3D objects and fast carousels get it too.
- A frame taken in the middle of a movement is blurred, so it is never used as a thumbnail. See the poster frame in `workflow.md`.
