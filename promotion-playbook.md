# Organic Promotion Playbook

How we drive traffic to the repos and the [press site](https://uribrecher.github.io/sounds-and-recreation/) on a **strictly $0 budget**, fully organic, with **no auto-posting**. Community etiquette (Reddit/HN/Lobsters) keys off a real human account with history, so the division of labour is fixed:

> **Claude drafts; the user posts.** Claude may directly apply only safe, reversible, identity-neutral repo metadata (GitHub Topics, descriptions) — and only on the user's OK. Everything that touches an external community account is posted by a human.

Ready-to-paste, channel-tailored content lives in the companion **`drafts/`** folder (separate deliverable). This file is the *map and the schedule*; `drafts/` is the *copy*.

## The triple identity

The project sits at the intersection of three communities. Every venue below is sorted into the one it serves; a few span two.

| Cluster | Who they are | What hooks them |
|---|---|---|
| **AI / MCP devs** | People building agents, MCP servers, LLM tooling | Two real MCP servers; an agent that drives hardware via tool-calls |
| **Audio-ML / MIR** | Audio DSP, music-information-retrieval, ML-audio folks | Stem separation, transcription, spectral comparison, the reverse-synth research |
| **Synth / MIDI musicians** | Owners of Nord / JUNO-X / Prophet-6, synth-DIY, MIDI tinkerers | "AI recreates a song's patch on *my* hardware" |

**Fit legend:** ⭐ great · ✓ good · ◦ marginal.

## Do first — free & automatic wins (no human-account risk)

These build passive discoverability and carry **zero etiquette risk**, so they happen before any "launch" post. They run in parallel with Week 1.

| Win | Action | Who |
|---|---|---|
| **GitHub Topics** | Tag all 6 repos (`mcp`, `model-context-protocol`, `midi`, `synthesizer`, `audio-analysis`, `music-information-retrieval`, `ai-agents`, `demucs`) via `gh` | Claude applies, on user OK |
| **Repo descriptions** | Fill the 3 empty ones (`audio-analysis-mcp`, `sound-recreation-agent`, `macos-packager`) via `gh` | Claude drafts, applies on OK |
| **MCP registry** | Publish `keyboards-mcp` + `audio-analysis-mcp` to the official registry via `mcp-publisher` → auto-propagates to the GitHub MCP Registry + Glama | **User runs** (domain/identity verification). *Verify `mcp-publisher` GA status at execution time — was preview in late 2025.* |
| **MCP aggregators** | Submit to PulseMCP, Smithery, mcpservers.org | User submits |
| **Awesome-lists** | PRs to [`punkpeye/awesome-mcp-servers`](https://github.com/punkpeye/awesome-mcp-servers) (~88k★) and `awesome-musicdsp` | Claude drafts entries, **user opens** PRs |
| **README badges** | License / stars / MCP-registry badges on repo READMEs | Claude drafts |

## Full targeting map

### AI / MCP devs

| Venue | Audience / size | Engagement approach | Fit |
|---|---|---|---|
| **Hacker News — Show HN** | The launch's single best fit (hardware + AI angle) | Plain factual title; try-it/hear-it without signup; author answers all day | ⭐ |
| **r/mcp** | ~89k MCP builders | Lead with the demo; frame as "two MCP servers + an agent that plays hardware" | ⭐ |
| **r/LocalLLaMA** | Large AI-builder sub | Only if genuinely additive; agent angle, not a model drop | ✓ |
| **r/ClaudeAI** | Claude-tooling users | Built on Claude + Vercel AI SDK tool-loop — show the tool-call flow | ✓ |
| **Lobsters** | Invite-only, high-signal | `show` tag; keep self-promo <~25% of your activity | ✓ |
| **dev.to** | Dev blog audience | Long-form build-log, canonical link back to the repo | ✓ |
| **Mastodon (fosstodon etc.)** | FOSS/dev instance | `#AudioDev #MCP`; conversational, not announcement-only | ✓ |

### Audio-ML / MIR

| Venue | Audience / size | Engagement approach | Fit |
|---|---|---|---|
| **The Audio Programmer Discord** | ~11.7k, **self-promo-tolerant** | Share freely in the right channel; it welcomes projects | ⭐ |
| **`awesome-musicdsp`** | Curated DSP list | PR a one-line entry | ✓ |
| **lines (llllllll.co)** | Sound/experimental-tools community | Genuine, thoughtful post — quality bar is high | ✓ |
| **CDM (cdm.link)** | Music-tech editorial | Earned-media **long shot**: pitch "AI recreates a song's synth patch on real hardware" | ◦ |
| **music-dsp mailing list** | Legacy / quiet | Low priority — largely dormant | ◦ |

### Synth / MIDI musicians

| Venue | Audience / size | Engagement approach | Fit |
|---|---|---|---|
| **r/synthesizers** | ~209k — your exact hardware owners | **Demo-gated.** Lead with the video; "AI matched this patch on a real Nord/JUNO/Prophet" | ⭐ |
| **r/synthdiy** | Builder ethos | **Demo-gated.** Emphasize the open toolchain + MIDI control | ✓ |
| **r/midi** | MIDI tinkerers | Focus on the MIDI-control + parameter-mapping story | ✓ |
| **VCV Rack Community** | OSS-friendly | Post in the **Announcements** category; OSS framing resonates | ✓ |
| **r/edmproduction** | ~452k | **Designated/weekend self-promo thread only**; participate first | ◦ |
| **r/WeAreTheMusicMakers** | ~2M | **Designated self-promo thread only** | ◦ |
| **KVR / Gearspace** | Large, **ban-sensitive** | Strictly on-topic; these gate vendor/self-promo posts — tread carefully | ◦ |
| **ModWiggler** | Modular-only | Skip — audience mismatch with hardware-synth focus | ◦ |

### Avoid / low-priority

- **r/programming** — high removal risk for project self-promo.
- **ModWiggler** — modular-only, mismatched.
- **music-dsp mailing list** — legacy and quiet.
- **KVR / Gearspace** — only if a genuinely on-topic thread invites it; never a cold vendor post.

## Self-promotion etiquette

The single rule behind all of this: **be a community member who happens to have built something, not a marketer who happens to be in the community.** Participate genuinely first, disclose authorship, lead with a demo, answer every reply.

**Reddit.** The **~10% rule** — no more than ~1 in 10 of your posts/comments should be your own project; the rest is genuine participation. Each sub has its own rules — read the sidebar before posting:
- r/edmproduction (~452k) and r/WeAreTheMusicMakers (~2M): self-promo **only** in the designated/weekend threads.
- r/synthesizers, r/synthdiy, r/mcp: a standalone post is fine *if* it leads with the demo and you're already a participant.
- Always disclose that you're the author.

**Hacker News (Show HN).** Plain, factual title — **no superlatives, no hype**. The project must be **try-able without signup** (repo + hear-it/try-it demo). The **author answers comments all day** — this is the single biggest driver of a good thread. If it gets no traction, **one repost** later is acceptable.

**Lobsters.** **Invite-only** — you need an account first. Self-promo should stay **<~25%** of your total activity. Use the **`show` tag** for your own project.

**Audio forums.** **KVR and Gearspace are ban-sensitive** and gate vendor/self-promo posts — stay *strictly* on-topic and never cold-drop a project. The **self-promo-tolerant** venues are **The Audio Programmer Discord** and the **VCV Rack Community** — share there freely.

## Demo dependency

A **demo screen-capture asset** (user-produced, with commentary/subtitles) gates the channels where seeing-and-hearing it is the whole pitch:

> **Demo-gated:** r/synthesizers · r/synthdiy · the *strongest* Show HN · the CDM pitch.

Everything else proceeds **without** the demo. If the demo slips, the AI/MCP launch (Show HN repo-only version, r/mcp) still runs on schedule, and the demo-gated channels shift to whichever week the asset lands.

## 4-week cadence

Spacing matters more than exact dates — the Reddit ~10% rule means you can't blast every venue in one week. Sequence, don't stack.

| Week | Theme | Venues | Notes |
|---|---|---|---|
| **0 / ongoing** | Free & automatic wins | GitHub Topics · descriptions · MCP registry + aggregators · awesome-list PRs · README badges | Runs alongside Week 1; zero etiquette risk |
| **1** | **Launch** | **Show HN** → **r/mcp** (~89k) → **r/synthesizers** (~209k) | The three-punch launch, same week. r/synthesizers + strongest Show HN are **demo-gated** |
| **2** | Seed the verticals | r/synthdiy *(demo-gated)* · The Audio Programmer Discord · VCV Rack (Announcements) · r/midi | Builder/audio-dev crowd; self-promo-tolerant venues |
| **3** | Broaden + build-log | dev.to build-log · Mastodon (tech + music instance) · lines (llllllll.co) · Lobsters (`show`) · r/LocalLLaMA / r/ClaudeAI | Long-form + adjacent AI; opportunistic |
| **4** | Earned-media long shot | **CDM pitch** *(demo-gated)* · r/edmproduction & r/WeAreTheMusicMakers (designated threads only) | The CDM swing; big-but-marginal subs via their self-promo threads |

### The launch sequence (the spine of Week 1)

1. **Show HN** — the single best fit (hardware + AI). Try-it/hear-it demo, author answers all day.
2. **r/mcp** + **r/synthesizers** — **same week**, each led with the demo video.
3. **Seed the verticals** (Weeks 2–3) — synth-DIY, audio-dev, MIDI, build-log, Mastodon.
4. **CDM long shot** (Week 4) — the earned-media pitch, once the demo is polished.

---

_Design rationale lives in the project's organic-promotion design spec (kept with the project planning docs, outside this repo). Companion ready-to-paste content lives in `drafts/`._
