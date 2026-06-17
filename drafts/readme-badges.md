# README badges

**Venue:** the 6 repo READMEs · **Do-first / ongoing**

Paste-ready badge snippets. Put them in a single row right under the repo's H1. Swap
`<repo>` for the actual repo name (`keyboards-mcp`, `audio-analysis-mcp`, etc.).

### License (GPL-3.0)
```markdown
[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](./LICENSE)
```

### Stars
```markdown
[![GitHub stars](https://img.shields.io/github/stars/uribrecher/<repo>?style=flat&logo=github)](https://github.com/uribrecher/<repo>/stargazers)
```

### MCP registry (MCP-server repos only: `keyboards-mcp`, `audio-analysis-mcp`)
Add once the listing is live (issue #9 — verify the registry/badge URL at publish time):
```markdown
[![MCP Registry](https://img.shields.io/badge/MCP-Registry-000000?logo=modelcontextprotocol)](https://registry.modelcontextprotocol.io/)
```

### Claude Code plugin (per #9 — `keyboards-mcp` first)
**Gated:** `keyboards-mcp` is submitted to the community marketplace and **in review** — add this
once the listing is live.

Badge:
```markdown
[![Claude Code Plugin](https://img.shields.io/badge/Claude%20Code-Plugin-d97757?logo=anthropic)](https://github.com/anthropics/claude-plugins-community)
```

Install snippet (paste into the README under an `## Install` heading):
````markdown
## Install (Claude Code)

```
/plugin marketplace add anthropics/claude-plugins-community
/plugin install keyboards-mcp@claude-community
```
````

### Suggested full row (umbrella `sounds-and-recreation`)
```markdown
[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](./LICENSE)
[![GitHub stars](https://img.shields.io/github/stars/uribrecher/sounds-and-recreation?style=flat&logo=github)](https://github.com/uribrecher/sounds-and-recreation/stargazers)
```

### Notes
- shields.io renders these live — no setup, no maintenance.
- Keep it to one row; badge spam reads as noise to the technical audiences we're courting.
- Verify each badge actually resolves before committing (shields occasionally changes logo slugs).
