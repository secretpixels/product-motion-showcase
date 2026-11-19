# Storyboard

After the questions, I show the story as a storyboard before I build anything. It is cheap: one small HTML file and no rendering.

## Contents
- How to make it
- Card
- Scene snippets
- Music strip
- Rules

## How to make it

1. Copy `assets/storyboard-template.html` to `storyboard.html` in the project folder. The template holds all the styling and the ratio control (16:9, 9:16, 1:1, 4:3 and 4:5). Do not rewrite it.
2. Replace `{{TITLE}}` and `{{META}}` (length, tempo, frame rate). Put one card per scene at `<!-- SCENES -->`. Make these as small edits, not by rewriting the file.
3. Tell the user to open the file in a browser and try the ratio buttons.

If the environment cannot make files, tell the story in text instead.

## Card

```
<section class="card"><h2>1 Hook</h2><p class="when">0 to 4 s | bars 1-2</p><div class="frame">CONTENT</div><p class="cap">One sentence.</p></section>
```

Add the class `two` to the section when the frame holds two devices. In a tall ratio the template then shows a note that there is no two-device frame.

## Scene snippets

Paste one of these as CONTENT. Add the extra class to `frame` where it says so.

- **One device:** `<div class="device"><div class="hd"></div><div class="cards"><i></i><i></i><i></i></div></div>`
- **Two devices** (card class `two`): `<div class="device d1"><div class="hd"></div></div><div class="device d2"><div class="hd"></div></div>`
- **Web:** `<div class="web"><div class="bar"></div><div class="body"><div class="img"></div><div class="t"><i></i><i></i><i></i></div></div></div>`
- **Text** (frame class `frame txt`): `<p class="big">Line one<br>line two</p><p class="sub">Second text</p>`
- **Grid of cards or logos** (frame class `frame cf`): `<div class="cells"><i>1</i><i>2</i><i>3</i> ...</div>`. The numbers show the order they pop in.
- **Gallery panels** (frame class `frame pn`): `<div class="pan" style="left:3.7cqh;width:66cqw"><i class="d"></i><i class="d w"></i></div><div class="pan" style="left:calc(7.4cqh + 66cqw);width:66cqw"><i class="d"></i><i class="d p"></i></div>`
- **Cover mosaic** (frame class `frame mo`): `<div class="p t"><b>Title</b></div><div class="p"><i class="d"></i><i class="d w"></i></div>` and three more panels like the second one.
- **End** (frame class `frame end`): `<div class="mark">logo</div><div class="name">Name</div>`

## Music strip

Only when the video has music. One more section after the cards, with the bars as columns:

```
<section class="music" style="--bars:15"><h2>Music and timing</h2><p class="when">120 BPM | 1 bar = 2 s</p><div class="track"><div style="grid-column:1/3">Hook</div><div style="grid-column:3/5;--c:var(--purple)">Statement</div></div><p class="note">Hook beat, no fade-in. Stinger at the end.</p></section>
```

## Rules

- Five to nine cards, one per scene. An interface video gets one per screen of the flow. Never more than nine.
- Wireframes only. Do not embed assets. Name the assets in the caption.
- One sentence per caption, and only the words that matter inside a frame.
- It is a sketch, not the design. The header says so.
- Follow the rest of the skill in the sketch: a mosaic as the cover for a promo or a brand reel, and text in its own scene, never next to a device.
