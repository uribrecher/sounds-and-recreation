# r/midi

**Venue:** [r/midi](https://www.reddit.com/r/midi/) · MIDI tinkerers · **Following weeks**

### Before you post
- Focus on the MIDI control + parameter-mapping story — that's what this sub cares about, more than the AI.
- Disclose authorship. ~10% rule.

### Title
```
Controlling a hardware synth's full parameter set over MIDI from an MCP server (open source)
```

### Paste-ready body
```
Part of a larger project, but the MIDI piece might be useful on its own: an open-source MCP
server that exposes a hardware synth's parameters over USB MIDI and lets you read and set them
programmatically.

It currently speaks to a Nord Electro 5D, Roland JUNO-X, and Prophet-6. Each device owns its
own parameter map (CC numbers, SysEx, value ranges), and the server exposes a small, uniform
set of tools on top: list_parameters, set_parameters, load_program, get_current_state,
extract_backup. There's also an on-screen mock device with a per-model UI, so you can develop
and test without the hardware plugged in.

The wider project uses this to recreate a song's keyboard sound automatically (an agent
analyzes the track and sets the parameters), but the MIDI layer is a clean standalone thing if
you just want scripted control of these synths.

Repo: https://github.com/uribrecher/keyboards-mcp  (umbrella project:
https://github.com/uribrecher/sounds-and-recreation)
[DEMO]

GPL-3.0. Curious whether anyone wants device modules for other synths — the pattern is
designed to make that straightforward.
```

### After you post
- Field questions about CC/SysEx mapping and which synths could be added next.
