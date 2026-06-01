# Analytics

How we measure the project on a **$0 budget** — two surfaces, no pipelines, everything free and hosted.

| Surface | Tool | What it tells you |
|---|---|---|
| Press-site traffic | GoatCounter | visitors, **referrers**, spikes |
| Repo health | star-history.com + OSS Insight | star growth, contributors/PRs/issues |

## Web traffic — GoatCounter

- **Dashboard:** https://soundsrec.goatcounter.com
- Cookieless, no consent banner. One `<script>` tag lives before `</body>` on every landing page (`docs/index.html`) across all 6 repos; the single dashboard separates them by URL path.
- **Retention:** indefinite (free hosted tier) — durable history, unlike GitHub's 14-day traffic window.
- **How to read it — treat counts as a _lower bound_, not truth.** Technical audiences block analytics beacons heavily (~half of HN/Reddit/dev traffic), and no free tool beats ad-blockers on a static GitHub Pages site without a first-party proxy (out of scope). So the absolute visitor number is a floor. The **trustworthy signals are referrers** (where people came from) and **relative spikes** (e.g. a Show HN or Reddit bump) — which is exactly what we need to judge whether promotion is working.

## Repo health — free hosted dashboards (zero setup, zero maintenance)

These cover what web analytics can't see.

### Star growth — star-history.com
All 6 repos on one chart, full history:

https://star-history.com/#uribrecher/keyboards-mcp&uribrecher/audio-analysis-mcp&uribrecher/sound-recreation-agent&uribrecher/reverse-synth-research&uribrecher/macos-packager&uribrecher/sounds-and-recreation&Date

### Contributors / PRs / issues — OSS Insight
Per-repo community & contribution depth.

> ⚠️ **These links return 404 while the repos are brand-new.** OSS Insight only covers repos already in its GitHub-events dataset (8B+ rows from GH Archive). With ~0 stars and almost no history, our repos aren't indexed yet, so the per-repo pages return *not found*. They start working once the repos accumulate public activity. (The URL format is correct — verified against indexed repos like `facebook/react`.)

- keyboards-mcp — https://ossinsight.io/analyze/uribrecher/keyboards-mcp
- audio-analysis-mcp — https://ossinsight.io/analyze/uribrecher/audio-analysis-mcp
- sound-recreation-agent — https://ossinsight.io/analyze/uribrecher/sound-recreation-agent
- reverse-synth-research — https://ossinsight.io/analyze/uribrecher/reverse-synth-research
- macos-packager — https://ossinsight.io/analyze/uribrecher/macos-packager
- sounds-and-recreation — https://ossinsight.io/analyze/uribrecher/sounds-and-recreation

## Deliberately excluded

- **GitHub native Insights → Traffic** (clones/views/referrers): 14-day retention only, and overlaps GoatCounter — not worth persisting. It's a built-in tab on each repo if ever needed.
- **GA4** (most ad-blocked + forces a cookie banner/CMP), **Cloudflare Web Analytics** (free tier keeps only ~30 days), self-hosted analytics, and any GitHub Action / cron / CSV metrics pipeline.

_Design rationale lives in the project's analytics design spec (kept with the project planning docs, outside this repo)._
