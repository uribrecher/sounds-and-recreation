# Show HN

**Venue:** Hacker News — Show HN · **🎬 strongest variant demo-gated**

### Before you post
- **Title:** plain and factual — no superlatives, no "revolutionary", no emoji. "Show HN:" prefix is required.
- **Try-able without signup:** the linked repo must let someone clone-and-run (or watch the demo) without an account. Put the run steps near the top of the README.
- **Submit the repo URL** (the umbrella repo or the agent), not a blog post. Use the text box for context.
- **Timing:** weekday morning US time tends to do best, but it's noisy — don't overthink it.
- **You answer comments all day.** This is the single biggest factor. Be present, technical, humble.
- **One repost** is acceptable later if it gets no traction the first time.

### Title (pick one — all plain/factual)
```
Show HN: An AI agent that recreates a song's keyboard sound on real synths
```
Alternates:
```
Show HN: Open-source agent that reverse-engineers a song's synth patch over MIDI
Show HN: Two MCP servers + an agent that matches a song's keyboard sound on hardware
```

### Paste-ready body (the "context" text box)
```
I've been building an open-source toolkit that listens to a song, works out how its
keyboard/synth part was made, and recreates that sound on a real hardware synth over MIDI.

It's three pieces wired together with the Model Context Protocol:

- audio-analysis-mcp (Python): import a track, separate stems (Demucs), run spectral
  analysis, transcribe notes (Basic Pitch), isolate and compare sounds.
- keyboards-mcp (TypeScript): drives real hardware — Nord Electro 5D, Roland JUNO-X,
  Prophet-6 — over USB MIDI, or an on-screen mock device if you don't have the gear.
- sound-recreation-agent (TypeScript): an agent (Vercel AI SDK tool loop) that
  orchestrates both servers — analyze, reason about the patch, set parameters, compare,
  iterate.

What works today: the full analyze → reason → set-MIDI-params → compare loop, against the
mock device or real hardware. What's still research: the deeper "reverse-synth" ML that
maps audio features to specific ADSR/modulation/tone-generation parameters — that part is
in-progress and documented in the open.

You can run it without any hardware or an account — there's a mock keyboard with a
model-specific UI. Run it / try it: https://github.com/uribrecher/sound-recreation-agent
(the no-hardware mock synth lives in https://github.com/uribrecher/keyboards-mcp; project
overview: https://github.com/uribrecher/sounds-and-recreation)
[DEMO]

It's GPL-3.0. I'd love feedback on the analysis→parameter mapping especially — that's the
hard part and where I'm least sure I've got the right approach.
```

### After you post
- Refresh and reply to every comment, especially the skeptical ones.
- If someone asks "does it actually sound right?", point them at the demo and be honest about limits.
- Don't vote-beg or share the link asking for upvotes (fast track to a ban).
