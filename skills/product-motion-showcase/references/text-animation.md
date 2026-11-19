# Text animation

How I animate text. Treat it as a method, not as exact numbers. The timing follows the text, and the voice-over if there is one.

## Contents
- Where text lives
- How much text at once
- How a line comes in
- How a line goes out
- How long text stays
- Two sentences in a row
- Text and other elements
- Playful text

## Where text lives

Text never sits next to, above or below a device. If text is needed, it gets its own scene between the screens, and nothing else is in that frame.

## How much text at once

- Two lines at most on screen at the same time. Never ten text fields stacked.
- A longer text is split into steps that follow each other. Split where the sentence naturally pauses.
- Only show more than two lines when the user explicitly asks for it.

## How a line comes in

- Every line has its own mask: a box with the height of the line. The words rise from below the bottom edge of that box into place. No fade and no scale.
- The words follow each other with a very small stagger. In my example it is about 1 frame per word, and it continues from the first line into the second.
- No typewriter effect for sentences: no letter by letter typing with a cursor. The line reveal is my standard.
- Every word moves about one line height, in about 0.8 seconds, with my 80/80 ease.
- These numbers are a starting point. A long text or a slow video can use a bigger stagger.

## How a line goes out

- A line leaves as a whole, not word by word. All words of the line move up out of the top edge of the box together.
- The next line follows a few frames later (about 4 frames in my example).
- It takes about as long as coming in, with the same ease.

## How long text stays

- With a voice-over, the text is on screen as long as the voice is speaking it. A long sentence stays longer. It comes in with the first words of the voice and leaves after the last.
- With music, text lands on a bar or a beat and stays for whole bars.
- Without either, it stays long enough to read once, calmly.

## Two sentences in a row

Sentences can follow each other directly. While the first sentence leaves, the next one is already coming in, so they overlap in time. Do not wait until the first one is gone. Both together stay within the limit of two lines.

## Text and other elements

Text and a group of other elements (logos, cards) never start at the same moment. The text comes first. The group follows while the text is settling, with a stagger.

## Playful text

For short labels and call-to-action text in a playful scene, use the same pop as the logos: scale up from about 85 percent with opacity and a subtle bounce, with a small stagger. A command that is typed live (in a terminal block) keeps its typing, inside a block that pops in with that same animation. Sentences keep the masked line reveal.
