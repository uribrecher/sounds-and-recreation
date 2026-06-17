# r/synthdiy

**Venue:** [r/synthdiy](https://www.reddit.com/r/synthdiy/) · builder / hacker ethos · **Following weeks · 🎬 demo-gated**

### Before you post
- This sub respects open tooling and "show your work." Emphasize the open toolchain, MIDI control, and the in-progress research — not a polished product.
- Lead with the demo, but it's fine to go deeper on the *how* here than in r/synthesizers.
- Disclose authorship. ~10% rule.

### Title
```
Open-source toolchain that analyzes a song and sets a hardware synth's parameters over MIDI to match
```

### Paste-ready body
```
Sharing a project I've been building in the open: a toolchain that takes a song, analyzes the
keyboard/synth part, and drives a real synth's parameters over MIDI to recreate the sound.

[DEMO]

How it's built (all open, GPL-3.0):
- Audio analysis is a Python MCP server — stem separation (Demucs), spectral analysis, note
  transcription (Basic Pitch), sound isolation and comparison.
- Hardware control is a TypeScript MCP server speaking USB MIDI to a Nord Electro 5D, Roland
  JUNO-X, or Prophet-6. Adding a synth is basically writing a device module that owns its own
  parameter map — the tool layer stays thin.
- An agent runs the loop between them: analyze → set parameters → compare → adjust.

The genuinely unsolved part (and where I'd love builder input): mapping measured audio
features to specific synth parameters — ADSR, modulation, oscillator/tone settings. I'm
writing that up as open research in the repo rather than hiding it. If you've thought about
audio-feature → synth-parameter inversion, I want to hear it.

Repo + research notes: https://github.com/uribrecher/sounds-and-recreation
You can run the whole thing against an on-screen mock synth with no hardware — the mock
device is in keyboards-mcp: https://github.com/uribrecher/keyboards-mcp
```

### After you post
- Point people at `reverse-synth-research` for the parameter-mapping design notes; invite critique.
