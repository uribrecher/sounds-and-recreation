# r/mcp

**Venue:** [r/mcp](https://www.reddit.com/r/mcp/) (~89k) · MCP builders · **Launch week**

### Before you post
- Read the sidebar/rules first. Standalone project posts are fine here if they're substantive.
- Lead with the demo and the architecture — this audience wants to see *how* the MCP wiring works.
- **Disclose you're the author** ("I built…").
- Respect the ~10% self-promo rule across your overall Reddit activity.

### Title
```
Two MCP servers + an agent that recreates a song's synth sound on real hardware
```

### Paste-ready body
```
I built an open-source project that uses MCP to go from a song to a recreated synth patch
on real hardware. Two servers do the work, and an agent orchestrates them:

**audio-analysis-mcp** (Python / FastMCP, stdio)
Tools: import_audio, stem_separate (Demucs), spectrum_analyze, note_transcribe (Basic Pitch),
note_isolate, note_triage, audio_compare, audio_render.

**keyboards-mcp** (TypeScript)
Tools: connect_to_keyboard, list_parameters, set_parameters, load_program, get_current_state,
extract_backup… It talks to a Nord Electro 5D, Roland JUNO-X, or Prophet-6 over USB MIDI — or
an Electron mock device with a per-model UI so you can try it with no gear.

The agent (sound-recreation-agent, Vercel AI SDK tool loop) connects to both over stdio and
runs the loop: analyze the track → reason about the patch → set parameters over MIDI →
compare → iterate.

A design detail I liked: the keyboards server is "model-delegated" — the MCP tools are thin
wrappers and each device owns its own parameter logic, so adding a synth is mostly a device
module, not new tools.

Repo (all servers + the agent): https://github.com/uribrecher/sounds-and-recreation
[DEMO]

Happy to talk about the MCP design — especially the thin-tool / device-owns-logic split, and
how the agent decides when the recreated sound is "close enough". GPL-3.0.
```

### After you post
- Engage on the MCP-design questions; that's what this sub rewards.
- Cross-link to the official MCP registry listing once it's live (see issue #9).
