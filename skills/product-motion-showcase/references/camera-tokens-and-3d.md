# Camera, tokens and 3D

These are building blocks, not a fixed script. Use only what the project has. No tokens, one brand, no 3D objects: skip those parts and lean on camera and screen recordings.

## Contents
- Camera
- Token lines and labels
- The switch
- 3D objects from 360 degree renders
- The grid
- The loop

## Camera

- The world is wider than the frame. The camera follows the tips of the growing lines.
- Add depth while travelling: tilt the world slightly while the camera moves.
- Zoom out elastically. The whole chain (app, lines, switch, app) pulls together like a rubber band, so the overview stays compact.
- Do the zoom out and the final arrangement in one move. In the same motion both phones slide into their end position, with a small bounce.

## Token lines and labels

**Use the project's own token names.** Never reuse names from another brand. If you do not know them, ask for a token export or a few real names. If there are none, skip the token lines.

**Lines**
- S-shaped bezier curves that get drawn. In the browser use dash-offset, in After Effects use Trim Paths.
- Put lines at different depths so they pass each other without tangling.

**Labels**
- They sit at a fixed place on screen and slide along their line while the camera moves. That keeps them readable.
- They spring in the moment their line exists.
- They disappear before a card or screen reaches their spot.
- They live in a flat layer above the 3D world. This stopped flickering.
- Give them a solid background with a shadow.
- Pick positions with a small search so labels never touch each other.

**Finish**
- At the end the lines retract into the switch instead of fading out.
- Then the card bounces briefly and disappears.

## The switch

Only use this when the project has more than one brand or theme.

- The knob squishes first, then flips.
- The card gives a small punch.
- The colours flow over to the new brand.
- Sound: a stack of click, switch, whip and bloop. The music dips under it for a moment.
- Token names stay the same after the switch. Only the values change. That is the whole point of the piece.

## 3D objects from 360 degree renders

Only use this when the user has 360 degree renders or a 3D model.

- Rotating means choosing the render frame: exactly one render frame per video frame.
- Never cross-fade between frames. It gives double edges and a flickering shadow.
- Take over from the screen recording at the moment the object stands still in it.
- Measure the angle by comparing the recording with all renders, so the hand-over is invisible.

## The grid

- Make the grid bigger than the frame, so it feels like there are more objects than you see.
- Objects arrive from the outside in, ring by ring, half staggered, partly outside the frame.
- On the beat a wave of half turns runs through the grid, with a small swell.
- To close: the camera zooms in slowly, the objects hop and fall.
- The logos come in while the last objects are still falling.

## The loop

- The logos animate in like their original splash and fold back to empty at the end.
- The last frame equals frame 1 of the animation. Frame 0 is the poster (see `workflow.md`).
