# Portfolio frames

The frames I use for app and web videos. They are in `assets/frames/`. The red areas are placeholders: replace them with the real screens or screen recordings.

All frames: 1600x1200 (4:3), 30 fps, flat background `#3D424D` in my templates, a soft shadow under every device.

| Frame | File | Device | Position |
| --- | --- | --- | --- |
| App, 1 device | `app-1-device.png` | 486x984, corner radius 48 | Centered. Top left at x 557, y 108 |
| App, 2 devices | `app-2-devices.png` | Two devices of 486x984, corner radius 48 | Side by side with an 80 px gap. Left one top left at x 274, y 80. Right one top left at x 840, y 136 |
| Web, 1 device | `web-1-device.png` | 1380x880, small corner radius (about 20) | Centered. Top left at x 110, y 160 |

In the two-device frame the devices are staggered: the left one sits 28 px above the middle, the right one 28 px below it. The pair as a whole is centered.

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
