# Sound and music

Music is optional. When the video has no music, skip this file and the tempo math.

When it does have music, this is my starting point. Adapt it to the story of each video, so no two videos sound the same.

## Contents
- Tempo math
- Music as the clock
- Arrangement per bar
- How the music starts and ends
- Self-made music
- My style: beeps and 808
- Measuring a reference
- Sound design
- Two tracks: music and effects
- Mixing and mastering
- The loop
- Checks

## Tempo math

Length and tempo are chosen together so that whole bars fill the video exactly.

`seconds = bars x 4 x 60 / BPM` and so `BPM = bars x 240 / seconds`

Examples:

- 128 BPM x 16 bars = 30 seconds.
- 134.4 BPM x 14 bars = 25 seconds.

Every bar transition then falls on a fixed moment, and the loop closes exactly on the downbeat. Length is always whole seconds.

## Music as the clock

All important moments land on a bar or a beat: the switch, the drop, the objects falling and the final hit. Keep them in the time table as bar and beat numbers, not as loose seconds. If the timing changes, regenerate the music instead of nudging the picture. Measure per bar whether the build-up still fits.

## Arrangement per bar

Map the storyboard onto the bars before writing any music. This is a starting point for 14 to 16 bars. Stretch or shrink it to the story. Every video gets its own arrangement.

| Bars | Picture | Music |
| --- | --- | --- |
| 1 | A logo or title animates in | A soft sting on beat 3, sparse |
| 2 to 3 | The first screens | The hook: gliding beeps on the beat, a soft 808 on the first beat of the bar |
| 4 to 6 | The story builds | Kick on 1 and 3, clap from bar 5, the 808 pattern, a riser into the main moment |
| Main moment | A switch or a reveal | Impact plus a stack of click, switch, whip and bloop |
| 7 to 8 | The story continues | Groove: four on the floor, hats, a soft arpeggio |
| 9 | The camera pulls back | Breathe: sparse, long 808 |
| 10 | Build to the payoff | Snare roll, then one eighth of silence |
| 11 to 12 | The payoff | The drop: full beat, the hook an octave up, the 808 jumps an octave |
| 13 | Outro | Riser into the final hit |
| Last | The logos, back to the start | Final hit, then a reverse swell into the loop point (loop) or a stinger (end card) |

## How the music starts and ends

**The start is a hook.** The music is catchy from the first beat. No slow fade-in, no warming up. Small moments, like a heart or an icon, get a soft sting: a big one feels too intense.

**The end is a real ending.** The music does not fade out. There are two ways, depending on the video:

- **End card:** a stinger (a bass hit or a whoosh) as the final logo animates, then it stops.
- **Loop:** the ending lands on the downbeat where the video joins its start, with a reverse swell into it (see "The loop").

## Self-made music

When no track exists and the environment can run code, I make the music in code with a small synthesizer. Writing it in code means I can change the tempo and regenerate in seconds. If code cannot be run, ask the user for a track instead.

The instruments and how they sound:

- **Kick, clap, hats, shaker:** a short, tight beat.
- **808 bass:** a deep sine with a pitch drop at the start and a little distortion. A pattern I use per bar, "dum-dum ... dum": hits on the 1st, 4th and 11th sixteenth note. In the drop the last hit jumps an octave. Change the pattern per video.
- **Gliding beeps:** start about 7 semitones high and drop to their note in 60 to 90 ms, short decay (about 0.1 s), through a ping-pong delay of a dotted eighth.
- **Blip bursts:** short square blips between 3 and 5.6 kHz on sixteenth notes, at the end of a phrase.
- **Pad and soft arpeggio:** in the background, the filter opens towards the drop.
- **Riser, reverse crash, impact:** for build-ups and hits.
- **Pump:** the music bed ducks on every beat (sidechain), also in bars without a kick.

A small library of free one-shots (whoosh, whip, click, switch) sits next to it, each normalised to a peak of -1 dB.

## My style: beeps and 808

My style is beeps and 808, in a minor key: gliding beeps, blip bursts and the "dum-dum ... dum" 808. Modern and product-like.

Use it as the starting point for every video with music, and let it differ per video: another hook, another bass pattern, another tempo. If a reference asks for another style, follow the reference. Offer two variants to choose from, for example with a different hook.

## Measuring a reference

When I give a reference video or track, measure it instead of guessing from words:

1. **Tempo:** detect the onsets (where sounds start) and find the BPM with autocorrelation.
2. **Structure:** loudness per few seconds, to find the intro, the build-up and the drop.
3. **The sounds:** a spectrogram of the intro (high frequencies: beeps, blips) and of the low end (the bass and its pattern).
4. **Loudness:** integrated LUFS and the peak.

Then describe what you found in numbers (for example "beeps that glide down about 7 semitones in 0.1 s, on every beat" or "a bass on the 1st, 4th and 11th sixteenth note"), build those, and never copy samples from the reference.

## Sound design

Every effect has a cause on screen:

- A soft whoosh on a camera move.
- A blob for every ring of objects that comes in, rising in pitch through a scale, 0.125 to 0.2 s apart.
- A swish while lines grow: filtered noise that sweeps up from about 500 Hz to 4 kHz over the growth.
- A whirr while things rotate: band-passed noise with a fast tremolo, about 0.5 s.
- A stack of click, switch, whip and bloop on the switch.
- A whip and a whoosh when objects fall or fly out.

## Two tracks: music and effects

Render the music and the made sound effects (blobs, swishes, whirrs) as two separate files with the same gain. Then they can be balanced, ducked and exported to other tools on their own. One-shots (whoosh, click) are placed as separate layers on top.

## Mixing and mastering

- **Music bed (starting values):** -4 dB, a high-pass at 28 Hz, gentle compression (ratio about 1.6, attack 15 ms, release 160 ms) and a limiter at about -1.5 dB.
- **Effects:** a repeated effect, like a whoosh on every slide, sits at the level of the music or 0 to 3 dB below it, with a softer top end. A whoosh is mostly high noise, and the music has little up there, so it stands out fast. Only a single big moment, like the main switch or the final hit, may sit above the music, by up to about 3 dB. No repeated effect is ever the loudest part of the mix.
- **Ducking:** the music drops to about 40 percent under the main moment (from 0.14 s before to 0.35 s after it) and to about 75 percent under camera moves. It goes down in 0.08 s and comes back in 0.25 s.
- **Final mix of the video:** about -14 LUFS, true peak at -1 dB or lower. LUFS is how loud the audio is on average, and -14 is a safe level for platforms.

## The loop

Render a few seconds of tail after the last bar and add that tail onto the start. Reverb and delays then carry over the loop point, and the loop has no hole in it. End with a reverse swell into the downbeat.

## Checks

- The duration is exactly the number of bars.
- Loudness per bar: the build-up rises and the drop is the loudest part.
- Effects are audible but balanced: measure the level at each cue with and without effects, and check that no repeated effect is the loudest part of the mix.
- Integrated loudness and peak of the final file.
- Always ask me to listen. You can measure, you cannot hear. Say so when you deliver.

Paid tools (Suno, ElevenLabs, a licensed library) are only used when the user asks for them, since they spend credits or budget. Self-made music in code is the default.
