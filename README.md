# gstack-simplified

A stripped-down, debloated version of the [gstack](https://github.com/garrytan/gstack) framework. Optimized for Hermes Agent and OpenCode — no Claude Code, no Codex, no iOS, no OpenClaw.

## What Changed (vs original gstack)

**Removed (not relevant to Hermes/OpenCode):**
- Agent-specific: codex, claude, connect-chrome, open-gstack-browser, openclaw
- iOS: ios-clean, ios-design-review, ios-fix, ios-qa, ios-sync
- Infra: setup-gbrain, sync-gbrain, supabase, extension, model-overlays, contrib
- Redundant with Hermes: scrape, skillify, learn, investigate, careful, guard
- Not relevant: benchmark-models, plan-tune, pair-agent, landing-report, CLAUDE.md
- CLI-replaceable: cso, health, benchmark, diagram, make-pdf, document-generate, setup-deploy

**Trimmed (preamble bloat removed):**
- Removed 750+ lines of telemetry, upgrade checks, session tracking, feature discovery, CLAUDE.md routing, Conductor detection, gbrain integration, AskUserQuestion format docs, and other Claude Code-specific infrastructure from every skill.
- Each skill now contains only: frontmatter + voice guidelines + core methodology.

**De-branded:**
- "Garry-shaped product and engineering judgment" → "Product and engineering judgment"
- "YC Office Hours" → "Product Diagnostics"
- All personal stats, YC recruitment CTAs, and promotional content removed

## Available Skills

### Core Workflow
| Skill | What it does |
|-------|-------------|
| `/office-hours` | Product diagnostics — reframe your idea before writing code |
| `/plan-ceo-review` | CEO-level review: scope challenge, strategic alignment |
| `/plan-eng-review` | Architecture review: data flow, edge cases, test plan |
| `/plan-design-review` | Design scoring: rate each dimension 0-10 |
| `/autoplan` | Orchestrator: runs CEO → design → eng reviews |
| `/review` | Pre-landing PR review with confidence calibration |
| `/qa` | Browser QA with diff-aware testing and fix loop |
| `/qa-only` | Browser QA report only (no code changes) |
| `/ship` | Run tests, review, bump version, create PR |
| `/canary` | Post-deploy monitoring with baseline comparison |
| `/land-and-deploy` | Merge PR, wait for CI, verify production |
| `/document-release` | Update docs after shipping with Diataxis coverage map |

### Safety
| Skill | What it does |
|-------|-------------|
| `/freeze` | Lock edits to one directory |
| `/unfreeze` | Remove directory restrictions |

### Browser
| Skill | What it does |
|-------|-------------|
| `/browse` | Headless browser for QA and testing |
| `/setup-browser-cookies` | Import cookies from real browser |

### Unique Value (no standalone alternatives)
| Skill | What it does |
|-------|-------------|
| `/retro` | Git-powered engineering retrospective with trend tracking |
| `/spec` | Intent → structured spec → GitHub issues (5-phase pipeline) |
| `/design-consultation` | Build complete design system from scratch |
| `/design-review` | 80-item visual audit with atomic commit fix loop |
| `/design-html` | Framework detection + AI HTML/CSS generation |
| `/design-shotgun` | Multi-variant AI design comparison workflow |
| `/plan-devex-review` | DX review at plan stage (TTHW, friction points) |
| `/devex-review` | Live developer experience audit |
| `/gstack-upgrade` | Self-update mechanism |

## CLI Tools (recommended companions)

The following skills were replaced by direct CLI tool usage:

| Skill removed | CLI tools | Install |
|---------------|-----------|---------|
| `cso` | semgrep + trivy + gitleaks | `pip install semgrep` + `dnf install trivy gitleaks` |
| `health` | ruff + mypy + vulture + radon | `pip install ruff mypy vulture radon` |
| `benchmark` | Lighthouse CLI | `npm i -g lighthouse` |
| `diagram` | mermaid-cli | `npx @mermaid-js/mermaid-cli` |
| `make-pdf` | pandoc | `dnf install pandoc` |
| `document-generate` | Diataxis framework | Manual methodology |
| `setup-deploy` | Platform CLIs | `flyctl`, `vercel`, `render` etc. |

## Install

```bash
git clone --depth 1 https://github.com/jimmyliuzg/gstack-simplified.git
cd gstack-simplified
./setup --host hermes   # or --host opencode
```

## License

MIT. Free forever.
