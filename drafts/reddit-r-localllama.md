# r/LocalLLaMA

**Venue:** [r/LocalLLaMA](https://www.reddit.com/r/LocalLLaMA/) · local-model builders · **Following weeks (opportunistic)**

### Before you post
- This sub is local-model-first and allergic to cloud-only marketing. **Be upfront** that it currently runs through a hosted gateway, and frame the post around the *agent/tooling* angle and the open invitation to point it at a local model.
- Only post if it's genuinely additive — don't force it. Lead with the tool-use architecture, not a model.
- Disclose authorship; respect the ~10% rule.

### Title
```
Agent + two MCP servers that recreate a song's synth patch on hardware — model-agnostic, want to wire it to a local model
```

### Paste-ready body
```
I built an open-source agent that analyzes a song and recreates its keyboard sound on a real
hardware synth over MIDI. It's an MCP setup: one server for audio analysis (stem separation
with Demucs, spectral analysis, note transcription) and one that controls the synth over USB
MIDI, with an agent running the tool loop between them.

Honesty up front: right now the agent talks to an LLM through a hosted AI gateway. But the
MCP servers are just stdio tool providers — nothing about them is cloud-specific — so the
interesting (to me, and hopefully here) question is swapping in a local model as the
reasoner. The task is a nice agent benchmark, actually: lots of tool calls, structured
numeric feedback (spectral comparison), and a clear success signal (does it sound closer?).

If you've had luck with local models doing multi-step tool loops with numeric feedback, I'd
genuinely like to hear which ones and how you structured the context. Repo:
https://github.com/uribrecher/sounds-and-recreation
[DEMO]

GPL-3.0.
```

### After you post
- Lean into the local-model swap discussion; that's the only reason this belongs here.
- If the reception is "this is cloud, not local" — acknowledge it, don't argue.
