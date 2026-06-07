# Contributing to Sounds & Recreation

Thanks for taking a look! **Sounds & Recreation** is an open-source toolkit and AI
agent that listens to a song, reverse-engineers its keyboard sound, and recreates it
on real hardware synths over MIDI.

It's a small project built in the open, and it's most fun to build with people who are
into **audio analysis, DSP, synthesis, ML, or MIDI tooling**. You don't need to be an
expert in all of those — pick the corner that interests you.

- 🌐 Site: https://uribrecher.github.io/sounds-and-recreation/
- 💬 Discussions (start here): https://github.com/uribrecher/sounds-and-recreation/discussions

## Start with a conversation

The lowest-friction way in is the
[Discussions](https://github.com/uribrecher/sounds-and-recreation/discussions) tab:

- 👋 [**Introduce yourself**](https://github.com/uribrecher/sounds-and-recreation/discussions/30) — what synths you own, your background, what brought you here.
- 🗺️ [**Where we need help right now**](https://github.com/uribrecher/sounds-and-recreation/discussions/31) — a curated list of tasks grouped by interest.
- 💡 [**Open research questions**](https://github.com/uribrecher/sounds-and-recreation/discussions/32) — the unsolved DSP/ML problems, discussion-first.

Rule of thumb: open-ended ideas, questions, and "is anyone working on X?" belong in
**Discussions**. Use **issues** for concrete, actionable bugs and tasks.

## The repos

The project is split into focused repos. Pick the one that matches what you're into —
each repo's own `README` has its setup and run instructions.

| Repo | What it is | Stack | Good if you like |
|------|------------|-------|------------------|
| [keyboards-mcp](https://github.com/uribrecher/keyboards-mcp) | MCP server that drives MIDI keyboards (Nord Electro 5D, JUNO-X, Prophet-6) + a mock-device runner | TypeScript | MIDI, synthesis, FM/wavetable engines |
| [audio-analysis-mcp](https://github.com/uribrecher/audio-analysis-mcp) | Stem separation, spectrum analysis, transcription, note isolation — as MCP tools | Python | DSP, ML / audio, feature extraction |
| [sound-recreation-agent](https://github.com/uribrecher/sound-recreation-agent) | The AI agent (Vercel AI SDK) that orchestrates the MCP servers end to end | TypeScript | agents, orchestration, LLM tooling |
| [reverse-synth-research](https://github.com/uribrecher/reverse-synth-research) | Design notes for the ML analysis pipeline — amplitude/ADSR, modulation, tone-generation | Research / docs | research, schema design, writing |
| [macos-packager](https://github.com/uribrecher/macos-packager) | Will bundle the runtime into a one-click macOS app | Tooling | packaging, build tooling |
| [sounds-and-recreation](https://github.com/uribrecher/sounds-and-recreation) | Project home — the website and cross-repo issues | HTML / docs | docs, web, project glue |

## Picking something up

1. Browse open issues, especially those labeled **`good first issue`**, **`help wanted`**,
   or **`research`** — on any repo.
2. **Comment on the issue** (or reply in the "Where we need help" thread) to say you're on
   it, so two people don't build the same thing.
3. No issue for what you have in mind? Open one — or float it in Discussions first for
   anything open-ended.

## Submitting a change

You **don't** need to be a collaborator. The standard open-source flow works for anyone:

1. **Fork** the relevant repo.
2. Create a branch: `git checkout -b my-change`.
3. Make your change; keep it focused. Match the existing code style and add/update tests
   where the repo has them.
4. Push to your fork and open a **pull request** against `main`, referencing the issue
   (e.g. "Fixes #123").
5. CI runs automatically; a maintainer reviews and merges.

Small, focused PRs get reviewed fastest. Planning something larger? Open an issue or
Discussion first so we can agree on the shape before you write a lot of code.

## A few conventions

- **License:** everything is **GPL-3.0**. By contributing, you agree your contribution is
  licensed under it.
- **Be decent.** Assume good faith, keep it friendly and on-topic. This is a hobby project —
  kindness goes a long way.
- **Questions?** Open a thread in
  [Discussions](https://github.com/uribrecher/sounds-and-recreation/discussions) — no
  question is too basic.

Welcome aboard. 🎹
