# AI Engineering Stack

A multi-agent AI engineering system built for production. 7 specialized agents, 3 orchestrated workflows, and a complete model routing configuration — designed to ship enterprise-grade AI work across consulting, content, trading, and product development.

This isn't a framework. It's a working system deployed on real projects worth $10M+.

---

## Architecture

```
                    ┌─────────────────────────────────┐
                    │       ORCHESTRATION LAYER        │
                    │   Claude Code + oh-my-claudecode │
                    │      (32 engineering agents)     │
                    └──────────┬──────────────────────┘
                               │
          ┌────────────────────┼────────────────────┐
          │                    │                    │
    ┌─────▼─────┐      ┌──────▼──────┐     ┌──────▼──────┐
    │ CONSULTING │      │   CONTENT   │     │  PRODUCTION │
    │   LANE     │      │    LANE     │     │    LANE     │
    └─────┬─────┘      └──────┬──────┘     └──────┬──────┘
          │                    │                    │
  ┌───────┴───────┐   ┌───────┴───────┐   ┌───────┴───────┐
  │ Forensic      │   │ Content       │   │ Video         │
  │ Analyst       │   │ Strategist    │   │ Director      │
  │               │   │               │   │               │
  │ Pitch         │   │ Image         │   │ Music         │
  │ Architect     │   │ Architect     │   │ Producer      │
  └───────────────┘   └───────────────┘   └───────────────┘
                              │
                      ┌───────▼───────┐
                      │   TRADING     │
                      │    LANE       │
                      ├───────────────┤
                      │ Trading       │
                      │ Analyst       │
                      │ (IFVG + CRT)  │
                      └───────────────┘
```

## Agents

| Agent | Domain | What It Does |
|-------|--------|-------------|
| **Consulting Forensic** | Intelligence | PE-grade competitive teardowns with funding reality checks |
| **Pitch Architect** | Presentations | Investor decks, enterprise sales decks, luxury brand presentations |
| **Content Strategist** | Writing | X threads, LinkedIn posts, long-form — zero AI slop |
| **Image Architect** | Visual | Production-ready prompts for Nano Banana Pro, Higgsfield, Seedream |
| **Video Director** | Motion | Hyper-realistic short-form video prompts for Kling, Sora, Veo |
| **Music Producer** | Audio | Suno prompt engineering across 40+ genres and 10 Indian languages |
| **Trading Analyst** | Finance | MNQ futures analysis using IFVG Turtle Soup + numerology filtering |

## Workflows

### Forensic Teardown
```
consulting-forensic → pitch-architect → content-strategist
```
Input: Company name. Output: Full competitive intelligence report + presentation deck + social content.

### Content Pipeline
```
content-strategist → image-architect → video-director
```
Input: Topic or idea. Output: Thread copy + image prompts + video prompts. Ready to publish.

### Product Launch
```
consulting-forensic → pitch-architect → content-strategist → image-architect → video-director
```
Input: Product concept. Output: Market analysis + pitch deck + launch content + visual assets.

## Model Routing

Smart routing across 15+ AI models based on task requirements:

| Layer | Models |
|-------|--------|
| **Language** | Claude Opus, Claude Haiku, GPT-4o, Qwen 3.5 Coder, Gemini 2.0 |
| **Image** | Nano Banana Pro, Higgsfield Soul, Seedream 4.5, FLUX.2 |
| **Video** | Kling O1 Edit, Kling 2.6, Sora 2, Veo 3.1 |
| **Music** | Suno v3/v3.5/v4/v5 |

See [`configs/model-routing.md`](configs/model-routing.md) for the full decision matrix.

## Setup

### Prerequisites
- [Claude Code](https://claude.ai/code) (v2.0+)
- [oh-my-claudecode](https://github.com/Yeachan-Heo/oh-my-claudecode) (optional, for 32-agent orchestration)
- [Ollama](https://ollama.com) (optional, for local Qwen 3.5)

### Install

```bash
# Clone this repo
git clone https://github.com/Tashi/ai-engineering-stack.git

# Copy agents to your Claude Code config
cp ai-engineering-stack/agents/*.md ~/.claude/agents/

# (Optional) Install oh-my-claudecode for full orchestration
npm i -g oh-my-claude-sisyphus@latest
omc setup
```

### Quick Start

```bash
# In Claude Code — agents are available immediately
# Use any agent by name in your prompts

# Forensic teardown
"Use consulting-forensic to tear down [Company X]"

# Content creation
"Use content-strategist to write a thread about [topic]"

# Full workflow
"Run the product-launch workflow for [product]"
```

## Project Structure

```
ai-engineering-stack/
├── agents/                    # Specialized AI agent definitions
│   ├── consulting-forensic.md # PE-grade competitive intelligence
│   ├── pitch-architect.md     # Investor and enterprise decks
│   ├── content-strategist.md  # Zero-slop content creation
│   ├── image-architect.md     # AI image prompt engineering
│   ├── video-director.md      # AI video prompt engineering
│   ├── music-producer.md      # AI music production (Suno)
│   └── trading-analyst.md     # MNQ futures (IFVG + CRT)
├── workflows/                 # Multi-agent orchestration pipelines
│   ├── forensic-teardown.md   # Research → Deck → Content
│   ├── content-pipeline.md    # Write → Image → Video
│   └── product-launch.md      # Full launch sequence
├── configs/                   # System configuration
│   ├── model-routing.md       # AI model selection matrix
│   └── tool-ecosystem.md      # Complete tool stack
└── docs/                      # Documentation
```

## Philosophy

**Production-ready over academic.** Every agent in this stack was built to ship work that enterprise clients pay for. Not prototypes. Not demos. Deployed systems.

**Stakes, specifics, friction.** Content must answer "why should anyone care?", name real numbers, and have edges. This principle runs through every agent.

**Architecture first, then detail.** Start with structure. Fill content. Iterate aggressively until it's 10/10.

## Built With

- [Claude Code](https://claude.ai/code) — Primary AI engineering environment
- [oh-my-claudecode](https://github.com/Yeachan-Heo/oh-my-claudecode) — Multi-agent orchestration (32 agents)
- [Ollama](https://ollama.com) + Qwen 3.5 — Local LLM for offline coding
- [python-pptx](https://python-pptx.readthedocs.io) — Presentation automation
- [Instrumenta](https://github.com/iappyx/Instrumenta) — McKinsey-grade PowerPoint toolbar

## License

MIT

---

*Built by Tashi. Deployed on $10M+ enterprise AI projects.*
