# r/synthesizers

**Venue:** [r/synthesizers](https://www.reddit.com/r/synthesizers/) (~209k) · your exact hardware owners · **Launch week · 🎬 demo-gated**

### Before you post
- **Do not post without the demo video.** This is a musician audience — they want to *hear* it, not read about architecture.
- Lead with the sound: "here's a song, here's the patch my tool built on a real [synth]."
- Light on code, heavy on gear and result. Mention the specific hardware (Nord Electro 5D / Roland JUNO-X / Prophet-6) — owners will perk up.
- Read the rules — some self-promo lands better as a comment in a relevant thread first. Disclose authorship. ~10% rule.

### Title
```
I made a tool that listens to a song and recreates the patch on my [synth] — here's how close it got
```
(Replace `[synth]` with whichever hardware is in the demo, e.g. "Prophet-6".)

### Paste-ready body
```
I've been building an open-source tool that listens to a track, figures out how the
keyboard/synth part was made, and dials in a matching patch on a real hardware synth over
MIDI — no presets, it sets the parameters itself.

[DEMO]

In the clip it's working on [SONG], recreating the sound on a [synth]. It separates the
stems, isolates the keyboard part, analyzes it, then drives the synth's parameters over MIDI
and compares its result back against the original, adjusting until it's close.

I'd really value ears better than mine on this: where does it nail the patch and where does
it obviously miss? The hard part is going from "what the sound is" to "which knobs to turn,"
and that's exactly where I want feedback.

It's free and open source (GPL-3.0), and you can try it on an on-screen mock synth if you
don't want to hook up hardware: https://github.com/uribrecher/sounds-and-recreation
```

### After you post
- Answer gear/sound questions; this crowd will get specific about the patch. Be humble about misses.
