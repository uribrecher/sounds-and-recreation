# dev.to build-log

**Venue:** [dev.to](https://dev.to/) · long-form build-log · **Following weeks**

### Before you post
- Set `canonical_url` so SEO credit flows to your own repo/site, not dev.to.
- dev.to uses the frontmatter below; `cover_image` is optional (use the social card once available).
- Long-form is fine here — tell the build story, show code, be honest about what's unsolved.

### Paste-ready (dev.to article, frontmatter + body)
```markdown
---
title: "Teaching an AI agent to recreate a song's synth sound on real hardware"
published: false
tags: ai, mcp, audio, midi
canonical_url: https://uribrecher.github.io/sounds-and-recreation/
cover_image:
---

I wanted to answer a specific question: could an AI agent listen to a song, work out how its
keyboard part was made, and dial in a matching patch on a *real* hardware synth — not a
plugin, an actual box with knobs?

This is a build-log of where I've gotten. It's open source (GPL-3.0); links at the end.

## The shape of the problem

"Recreate the sound" breaks into three jobs:

1. **Hear it** — isolate the keyboard/synth part from a full mix and measure it.
2. **Reason about it** — decide which synth parameters would produce that sound.
3. **Make it** — set those parameters on hardware and check the result.

I built each as a separate, reusable piece, connected with the Model Context Protocol (MCP).

## Hearing it — `audio-analysis-mcp` (Python)

A FastMCP server that wraps the audio pipeline as tools: `import_audio`, `stem_separate`
(Demucs), `spectrum_analyze`, `note_transcribe` (Basic Pitch), `note_isolate`, `audio_compare`.
Each tool is small and returns structured data, because that data becomes context for the
agent — verbose tool output makes the loop worse, not better.

## Making it — `keyboards-mcp` (TypeScript)

A server that drives real synths over USB MIDI: Nord Electro 5D, Roland JUNO-X, Prophet-6.
The design choice I'm happiest with is "model-delegated": the MCP tools are thin
(`set_parameters`, `load_program`, `get_current_state`…) and each *device* owns its parameter
map. Adding a synth is a device module, not new tools. There's also an Electron mock device so
you can develop with no hardware.

## Reasoning about it — `sound-recreation-agent` (TypeScript)

An agent built on the Vercel AI SDK tool loop. It connects to both MCP servers over stdio and
runs: analyze → propose parameters → set them → compare → adjust.

## What works, and what doesn't (yet)

The loop runs end to end against the mock device and real hardware. The honest gap is step 2:
mapping measured audio features to *specific* ADSR/modulation/tone parameters is hard, and
that's the part I'm still treating as research rather than a solved feature. I'm writing that
design up in the open.

## Try it / read more

- Project + all repos: https://github.com/uribrecher/sounds-and-recreation
- Site: https://uribrecher.github.io/sounds-and-recreation/
- [DEMO]

If you've worked on audio-feature → synth-parameter inversion, I'd love to compare notes.
```

### After you post
- Flip `published: true` when ready. Reply to comments; cross-post the link to Mastodon (see `mastodon.md`).
