# Demo Commentary Script — *"I want my keyboard to sound like that"*

**Purpose:** the gating demo screen-capture for the press site + promotion ([#11](https://github.com/uribrecher/sounds-and-recreation/issues/11)). Sell the product, excite people, recruit collaborators.
**Format:** ~80 seconds · first-person VO (you, the keyboardist-builder) · on-screen subtitles · screen-capture + b-roll of you playing hardware.
**Principle:** the visuals carry; the VO stays out of their way. The song is the hook.

---

## ⚠️ Honesty / "under active development" framing

Part of the flow below — **the audio-analysis panel, click-a-section → keyboard-picker popup, and the agent auto-applying parameters** — is **not implemented yet**. We sell the *vision*, but we do **not** mislead. Handle it like this:

- **Persistent on-screen badge** from the first frame: `🚧 concept demo · under active development`.
- Frame the unbuilt beats as **"the workflow we're building"**, not a shipped feature. This is a recruitment pitch, not a product launch — *being early is the ask.*
- **What's real today** (safe to show as-is): the MCP servers (`keyboards-mcp`, `audio-analysis-mcp`), the **Sounds and Recreation app** + model picker, MIDI parameter control (`set_parameters`), and the audio-analysis tools (import, stem-separate, spectrum, transcribe, isolate).
- **What's target / to be staged as mockup or b-roll:** the in-UI audio-analysis panel, the section-click → JUNO-X/Prophet-6/Nord popup, and the agent's reverse-synth auto-patching. Keep VO loose over these beats so it covers cuts/mockups.
- **The "humbler hardware" angle (intentional):** the b-roll synth is a **Sequential FourM** — a 4-voice poly, more affordable and portable than (and less capable than) the Prophet-5/6, *not* the synth from the record. That's a feature, not a caveat on two fronts: (1) it proves the tool adapts the sound to whatever gear you actually own, and (2) it widens the appeal to hobbyist/budget players who can't drop Prophet-5 (vintage, very pricey) or even Prophet-6 (modern reissue, still not cheap) money. The payoff line leans into this (*"your gear, your sound"*). The tool's selected profile is the **Prophet-6** (its closest supported model); the lower-third names the **actual board played — confirmed Sequential FourM, not a placeholder.**
- The CTA already says "it's just getting started" — let the `🚧` badge + "come build it with me" carry the disclosure honestly.

---

## Script (beat-by-beat)

### `[0:00–0:05]` COLD OPEN — the song does the hook
**Visual:** moody shot / title card. The track swells background → foreground; the lead synth is unmistakable for ~3s, then ducks back.
**VO** (lands as the synth peaks):
> "Hear that sound? I want my keyboard to do **that**."

**On-screen:** `I want my keyboard to sound like THAT.`

### `[0:05–0:13]` THE PROBLEM (relatable pain)
**Visual:** you at the keys, stuck; or a quick knob-twiddling montage.
**VO:**
> "Normally that's hours on forums, guessing at knobs, chasing one patch. So I built an AI that does the listening for me."

### `[0:13–0:20]` THE TURN — open the tool
**Visual:** focus on the **Sounds and Recreation app** → click the **waveform icon** → audio-analysis panel slides in. Click **Import**, pick the mp3.
**VO:**
> "I drop in the track—and hit **Analyze**."

**On-screen:** `1 · Import the song`

### `[0:20–0:30]` ANALYSIS — let it breathe
**Visual:** slight focus on the progress bar.
**VO** (while it runs):
> "It splits the stems and reads the synth itself—the envelope, the movement, the tone. It's not transcribing notes. It's reverse-engineering the **sound**."

**On-screen:** `2 · It analyzes the actual synth`

### `[0:30–0:42]` STEMS → PICK THE CHORUS
**Visual:** stem waveforms + song sections appear; zoom into the **keyboard stem**; select the **chorus**.
**VO:**
> "There's the keyboard, isolated. This chorus—that's the part I want. Sounds like a subtractive synth to me."

**On-screen:** `3 · Pick the part you love`

### `[0:42–0:52]` CHOOSE HARDWARE → AGENT WORKS
**Visual:** click chorus → popup **JUNO-X · Prophet-6 · Nord Electro 5D** → pick **Prophet-6**. UI shifts to the Prophet-6 mock; chat box scrolls (agent calls the reverse-synth tool); zoom on a slider that races and settles.
**VO:**
> "I pick the Prophet-6. The agent dials in the patch for me—live, over MIDI. Watch the on-screen controls move."

**On-screen:** `4 · It sets up YOUR synth — over MIDI`

### `[0:52–1:05]` THE PAYOFF — play it
**Visual:** b-roll of you playing the hardware; A/B the original track vs. your keyboard on the chorus line — they match.
**VO:**
> "And now…" *(play — let the sound carry 2–3s)* "…that's it. And it's not even the synth from the record—it's my own simpler board, and it **still** nails it. Your gear, your sound—under a minute."

**On-screen:** `played live on a Sequential FourM — a 4-voice, budget-friendly poly` (small lower-third)

### `[1:05–1:20]` CTA — recruit collaborators
**Visual:** project title / repo URL / the 6-repo toolkit; GitHub ⭐ button.
**VO:**
> "It's open source, built on **MCP**—and it's just getting started. I want it to know every synth, every sound. If you're into synths, audio ML, or AI agents: come build it with me."

**On-screen:** `⭐ github.com/uribrecher/sounds-and-recreation · built on MCP · 🚧 early & contributors welcome`

---

**Budget:** ~200 words VO ≈ 80s. The CTA names the project's "triple identity" audience on purpose (synths / audio ML / AI agents) so all three feel invited.

---

## Alternate hooks (the first 5s do the most work)

The script uses **Hook A**. Kept here as alternatives if A doesn't land in edit:

- **A (in use):** "Hear that sound? I want my keyboard to do **that**."
- **B (problem-first):** "Every keyboardist knows this feeling: you hear a sound… and you have no idea how to make it."
- **C (provocative):** "What if you could just **ask** your synth to sound like the record?"
