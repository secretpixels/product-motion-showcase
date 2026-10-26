# Sound and music

Music is optional. When the video has no music, skip this file and the tempo math.

## Contents
- Tempo math
- Music as the clock
- How the music starts and ends
- Self-made music
- Sound design
- Mixing

## Tempo math

Length and tempo are chosen together so that whole bars fill the video exactly.

`seconds = bars x 4 x 60 / BPM` and so `BPM = bars x 240 / seconds`

Examples:

- 128 BPM x 16 bars = 30 seconds.
- 134.4 BPM x 14 bars = 25 seconds.

Every bar transition then falls on a fixed moment, and the loop closes exactly on the downbeat.

## Music as the clock

All important moments land on a bar or a beat: the toggle, the drop, the objects falling and the final hit. If the timing changes, regenerate the music instead of nudging the picture. Measure per bar whether the build-up still fits.

When I give a reference video, use it. Measuring its tempo and structure works better than a description.

## How the music starts and ends

**The start is a hook.** The music is catchy from the first beat. No slow fade-in, no warming up.

**The end is a real ending.** The music does not fade out. It stops on purpose, with a stinger (a bass hit or a whoosh) as the final logo animates, as in my brand reels.

In a loop, the ending lands on the downbeat where the video joins its start, so the loop still feels intentional.

## Self-made music

When no track exists and the environment can run code, I make the music in code with a small synthesizer: kick, clap, hats, 808 bass, plucks, pads, risers, blobs, swishes and sliding beeps. A small library of free effects (whoosh, whip, click, switch) sits next to it. Writing it in code means I can change the tempo and regenerate in seconds. If code cannot be run, ask the user for a track instead.

## Sound design

Every effect has a cause on screen:

- A whoosh on a camera move.
- A blob for every ring of objects, rising in pitch.
- A swish while lines grow.
- A whirr while things rotate.
- A stack of click, switch, whip and bloop on the switch.

## Mixing

- Master the music to about -14 LUFS, for every video, brand reels included. LUFS is how loud the audio is on average, and -14 is a safe level for platforms.
- Effects sit a few dB above the music.
- The music ducks briefly under important moments.
- Measure loudness per bar and check the final file.
- Always ask me to listen. Measuring is not hearing.
