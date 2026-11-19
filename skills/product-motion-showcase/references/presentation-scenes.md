# Presentation scenes

For a brand reel, when the user supplies assets (pieces of a UI, images, illustrations, icons), I present them in two kinds of scene: a component grid and a gallery. Use only the assets that are delivered. Never invent assets.

## Contents
- What to ask for
- Cover mosaic
- Component grid
- Zoom-out reveal
- Card wall (subtle)
- Assemble into a mosaic (fast)
- Responsive morph
- Wall reveal
- Device with a grid around it
- Gallery
- Examples inside the panels
- Logo grid
- Timing
- Background and cards

## What to ask for

- **For a component grid:** pieces of the UI as separate elements, like a button, a price card, a toggle, a step indicator or a type scale. If they are not delivered as separate files, crop them from the screens or ask. Six to twelve pieces make a full grid. With fewer, make a smaller grid.
- **For a gallery:** images, illustrations or product cards. At least three, in different sizes if possible.
- **For an icon set:** the whole set, as one image or as separate icons.
- **For the card wall:** a dozen or more portrait cards (text cards, photos, screens).
- **For assembling into a mosaic:** the icons, and the content of every tile.
- **For the responsive morph:** the page as a responsive build, or the desktop and the mobile layout of the same page.
- **For the wall reveal:** many layouts or screens, a dozen or more.
- **For a device with a grid around it:** the pieces of one screen (UI pieces, illustrations, icons, a logo tile).

Ask for these when you choose the scene, as part of the material question. Use the scene only when the user supplies what it needs.

## Cover mosaic

The cover (frame 0) is a mosaic of panels. It is not a scene with text and logos, and it never shows a block of text next to a grid of logos.

- A dark neutral background and slightly lighter rounded panels. In my examples `#14161a` and `#292c33`.
- The margin and the gaps between the panels are equal, about 3.7 percent of the canvas height.
- Every panel holds a device pair: the brand splash next to a screen, with the shadow from `frames.md`. One panel can hold the title (big text, two lines at most) or a web frame.
- The panels differ in size, for example a big panel next to a 2 x 2 grid, or three columns with one tall panel.
- For a light brand the cover can be the component grid below: white cards on a light tint of the brand colour.

## Component grid

- Pull the elements out of the interface and present each one as its own card in a tight grid with small gaps. One element per card, large enough to read.
- The cards differ in size, like a bento grid, so the rhythm varies. The grid fills the frame.
- Every card has its own quiet loop: a button that changes colour, a toggle that slides, steps that light up one after another. Small and slow, and not all in sync.
- The cards come in with a subtle animation, my 80/80 ease and a small stagger.
- Let the grid hold long enough to see the loops, about 1 to 2.5 seconds.

## Zoom-out reveal

- Start on one card or one element that fills the frame, for example a colour swatch card or a single component.
- Then the camera zooms out and the rest of the grid is revealed around it. About 0.5 seconds, with the 80/80 ease. Start it on a beat and let it land on a beat.
- After a grid appears, a small extra zoom-out of about 7 percent in about a quarter of a second settles it.

## Card wall (subtle)

- Five columns of tall portrait cards (three in a tall ratio) with an equal gap. The cards are text cards, photo cards and cards with a screen, mixed. In this scene text may sit in cards next to screens.
- All columns scroll upward by the same distance: the length of the content pattern. The last frame then equals the first, and the loop closes.
- The centre column starts first. The next pair follows 5 frames later (about 0.2 seconds at 24 fps), and the outer pair 5 frames after that.
- Every column takes about 2 seconds with the 80/80 ease. Hold about 0.5 seconds before the move and about 1 second after it.

## Assemble into a mosaic (fast)

- A row of round icons pops in one after another within 0.2 to 0.3 seconds, and holds for about 0.4 seconds.
- The icons scatter to loose positions, with motion blur, in about 0.6 seconds.
- Every icon becomes one tile of the mosaic: the circle turns into a rounded rectangle in the place of its tile, in a few tenths of a second.
- The tiles fill with their content: type is typed, a logo is drawn, colour bars slide in. About 0.8 seconds.
- In total about 2.5 seconds, with two brand colours and one corner radius for all the tiles. Then it holds.

## Responsive morph

A web page morphs into its mobile layout. Use it only when the assets allow it:

- Best: the page as a responsive build (HTML, or a frame with real constraints), so the content reflows while the width changes. The heading rewraps and the picture recrops.
- Otherwise: the desktop and the mobile layout of the same page. The frame changes width while the two layouts cross-dissolve.
- With neither, skip it.

The width goes from the desktop width to the mobile width in about 0.6 seconds with the 80/80 ease. Start it on a bar line. Then the mobile page holds for about 1.2 seconds, with a small movement inside. The frame is the plain shape from `frames.md`, with no browser around it.

## Wall reveal

After the responsive morph, or after any single layout, the page shrinks and a wall of layouts pops in around it. The page shrinks with an ease-in in about 0.2 seconds. Then the wall comes in within about 0.15 seconds and fills the frame. It holds after that. It needs a dozen or more layouts. With fewer, make a smaller wall or use the component grid.

## Device with a grid around it

- A plain device shape sits in the middle: no notch, no island, no buttons, so nobody can see whether it is iOS or Android. Around it sit cards pulled out of the screen: UI pieces, illustrations, icons and a logo tile, in a bento arrangement on a light tint of the brand colour.
- The screen builds itself. A colour fills it, a gradient grows, elements appear and a card grows up from the bottom. A logo tile can morph: a dot, then an oval, then the shapes of the logo.
- The cards have quiet loops. Hold the scene for about 1.1 to 1.8 seconds.
- The scene lands on a bar line, and the cut into it comes a couple of frames before the downbeat.

## Gallery

- A row of equal-size panels in the style of the cover: a darker background, lighter rounded panels, and a margin and gap of about 3.7 percent of the canvas height. Every panel holds one example, a device pair or a web frame.
- Balance: all panels have the same height, and every example fits inside its panel with room around it. The next panel shows at the edge of the frame, cut off, at full brightness. Never dim the neighbours.
- The camera moves from panel to panel with a horizontal slide of about 0.6 to 1.2 seconds with the 80/80 ease. Hold about 1.3 seconds between the moves.
- A small pill with dots at the bottom shows where you are, when it fits the story. The active dot moves along with every slide.
- It can open with an icon set that zooms out from a handful of icons to the whole set, followed by a cut into the first panel.

## Examples inside the panels

- The examples (screen recordings or animated screens) play inside their panels while the gallery rests and while it moves. Speed them up: about 1.5 to 2 times at the fastest point, with a slow, fast, slow curve. Keep it subtle.
- Remap the time with a smooth speed curve, so the speed never jumps and nothing stutters. At the fastest point, check that no frame repeats or jumps.
- This speed-up belongs to the examples. It is separate from the slide of the gallery.
- Let an important moment (a tap, a screen change) land on a slow part of the curve, so it stays readable.

## Logo grid

- The text comes first and the logos follow while the text is settling. They never start at the same moment.
- Use the finished state of every logo, the last frame of its animation. A logo's own build-up shows partial shapes and dots, and that reads as flicker.
- The logos come in playfully, not row by row. Each one scales up from about 85 percent with its opacity, some with a subtle bounce and some with the plain 80/80 ease. The order is loose, for example from the middle outward or scattered, with heavy overlap and a small stagger. The whole grid is in within about 1.5 to 2 seconds.
- No blinking: a logo never goes on, off and on again.
- Then the grid holds, with the logos as finished stills.

## Timing

The same rules as everywhere. Music is the clock: a grid appears on a bar line, a zoom-out starts on a beat, and a slide lands on a beat. The camera uses my 80/80 ease only.

## Background and cards

- **Component grid:** a light tint of the brand colour as the background, with white cards that have rounded corners and a clear gap between them.
- **Cover and gallery:** a dark neutral background with lighter rounded panels.
- Use the colours, the logo and the typography from the material.
