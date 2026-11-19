# Portfolio frames

The frames I use for app and web videos. They are in `assets/frames/`. The red areas are placeholders: replace them with the real screens or screen recordings.

All frames: 1600x1200 (4:3), 30 fps, flat background `#3D424D` in my templates, a soft shadow under every device (see Shadow below).

| Frame | File | Device | Position |
| --- | --- | --- | --- |
| App, 1 device | `app-1-device.png` | 486x984, corner radius 48 | Centered. Top left at x 557, y 108 |
| App, 2 devices | `app-2-devices.png` | Two devices of 486x984, corner radius 48 | Side by side with an 80 px gap. Left one top left at x 274, y 80. Right one top left at x 840, y 136 |
| Web, 1 device | `web-1-device.png` | 1380x880, small corner radius (about 20) | Centered. Top left at x 110, y 160 |

In the two-device frame the devices are staggered: the left one sits 28 px above the middle, the right one 28 px below it. The pair as a whole is centered.

## Shadow

The shadow is a flattened, blurred black ellipse, not a box shadow. It sits centered under the device, mostly hidden behind it, so only a soft edge shows below. There is no shadow on the sides or on top. Every device gets its own shadow.

Proportions, measured on my 1600x1200 frames and written relative to the canvas, so they scale to any ratio:

- **Size at half strength:** 47 percent of the device width for a phone, 72 percent for the web device. The height is about 8 percent of the canvas height for both.
- **Blur:** about 2 to 3 percent of the canvas height, a wide soft falloff.
- **Position:** the middle of the ellipse sits about 4 percent of the canvas height above the bottom edge of the device. The top half is hidden and about 3 percent shows below the edge.

The intensity follows the background. These are starting values for the peak opacity of the black:

| Background | Peak opacity |
| --- | --- |
| Dark, like `#3D424D` | about 65 percent |
| Mid grey | about 45 percent |
| White | about 35 percent |

Between these, follow the lightness of the background. Judge it by eye: the contrast stays in balance, so the shadow is felt and not seen as a shape.

Ready-made layers for each frame are in `assets/frames/`: `shadow-app-1-device.png`, `shadow-app-2-devices.png` and `shadow-web-1-device.png`. They are black with the shadow as transparency, at 1600x1200 and aligned with the frames, with the peak at 100 percent. Put the layer behind the device and set its opacity to the value above. For another ratio, rebuild the shadow from the proportions.

## Clean corners

Where a screen sits in a rounded device, the edge of the screen can show as a light rim or as stair-steps along the rounded corners. To avoid it:

- Make the screen about 2 px larger than the device on every side, at 1920 px wide. Scale that with the canvas, about 0.1 percent of the width. Clip it with the rounded mask of the device, so the edge of the source falls outside the mask.
- Not more than that. A bigger scale cuts the UI off.
- Check the corners at 4 times zoom in a frame of every device, also in the draft.

## Unisex: no operating system, no browser

The device is a plain rounded rectangle: no notch, no Dynamic Island, no camera hole, no side buttons. The web frame is a plain rounded rectangle too, without a browser window. The screens show only the interface itself. For apps, remove:

- the status bar (time, signal, battery);
- the notch, the Dynamic Island or a camera cut-out;
- the home indicator;
- the Android navigation bar or gesture bar.

For websites, remove the browser:

- the window controls (the three dots at the top left);
- the tab bar, the address bar, the toolbar and the bookmarks bar;
- native scrollbars;
- anything from the operating system around the window, like a menu bar or a dock.

How:

1. Ask for screens exported without these elements.
2. If that is not possible, remove them yourself: crop the strips at the top and bottom (and the sides for a scrollbar), extend the app's own background colour or header over the freed space, and check the top and bottom padding so the screen still looks balanced. Show me the result before you build.
3. The system keyboard and system pop-ups (share sheets, permission alerts) are native too. Ask me whether to show a neutral version in the app's own style, or to leave them out.

## How I use them

- **App videos:** I usually show one device. I use two side by side only when it makes something clearer, for example two brands of a white-label product next to each other. The second device comes in with my ease and overlap.
- **Web videos:** one device, centered.

## Notes

- Keep device sizes, radius and positions as they are. Only the background colour changes.
- **Background colour.** In a finished video I use a flat neutral grey. Calculate the contrast between the screens and the background, and make sure the edges of the device read clearly. It is usually a dark colour, for example `#424242`. A light or warm grey is fine when it suits the brand and the device still separates from it.
- **Other ratios.** Keep the proportions of my 4:3 frame. In the app frame the device is 82 percent of the canvas height (984 of 1200), centered, and the corner radius scales with the device.
  - 9:16, 1080x1920: device about 777x1574, radius about 77. Two devices do not fit side by side, so use one.
  - 1:1, 1080x1080: device about 437x886, radius about 43.
  - 16:9, 1920x1080: device about 437x886, radius about 43.
  - For the web device, fit it inside 86 percent of the canvas width and 73 percent of the canvas height (my 4:3 frame), keeping its 1380:880 proportions.
