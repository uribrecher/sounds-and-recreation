# r/ClaudeAI

**Venue:** [r/ClaudeAI](https://www.reddit.com/r/ClaudeAI/) · Claude-tooling users · **Following weeks**

### Before you post
- This sub likes concrete "what I built with Claude" posts — show the tool-use flow.
- Lead with the agent loop, not the music theory.
- Disclose authorship; respect the ~10% rule.

### Title
```
I used Claude as a tool-using agent to recreate a song's synth patch on real hardware
```

### Paste-ready body
```
I built an open-source agent where Claude drives two MCP servers to recreate a song's
keyboard sound on a physical synth.

The flow is a Vercel AI SDK tool loop: Claude gets tools from an audio-analysis server
(import a track, separate stems with Demucs, run spectral analysis, transcribe notes) and
from a keyboards server (set parameters / load programs over USB MIDI on a Nord, Roland
JUNO-X, or Prophet-6). It analyzes the target sound, reasons about which parameters to
change, sets them on the hardware, compares the result, and iterates.

What I found interesting working with Claude here:
- The "model-delegated" design — the MCP tools are deliberately thin, and the model does
  the reasoning about *which* synth parameters matter. The tools don't encode the music
  knowledge; Claude supplies it.
- Tool-loop ergonomics: keeping each tool result small and structured matters a lot for how
  well the loop converges.

You can run it against an on-screen mock synth with no hardware. Repo:
https://github.com/uribrecher/sounds-and-recreation
[DEMO]

GPL-3.0. Happy to share how the tool loop and prompts are structured if anyone's building
something similar.
```

### After you post
- Be ready for prompt/architecture questions — share specifics, that's the value here.
