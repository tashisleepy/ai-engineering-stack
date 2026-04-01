# AI Engineering Stack

A multi-agent AI system for content production. 4 specialized agents, orchestrated workflows, and smart model routing across 15+ AI tools — built for shipping production-grade creative work at scale.

Built on [oh-my-claudecode](https://github.com/Yeachan-Heo/oh-my-claudecode) (32-agent orchestration framework for Claude Code).

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
│  CONTENT   │      │   VISUAL    │     │   AUDIO     │
│   LANE     │      │    LANE     │     │    LANE     │
├────────────┤      ├─────────────┤     ├─────────────┤
│ Content    │      │ Image       │     │ Music       │
│ Strategist │      │ Architect   │     │ Producer    │
│            │      │             │     │             │
│            │      │ Video       │     │             │
│            │      │ Director    │     │             │
└────────────┘      └─────────────┘     └─────────────┘
```

## Agents

| Agent | Domain | What It Does |
|-------|--------|-------------|
| **Content Strategist** | Writing | X threads, LinkedIn posts, long-form — zero AI slop |
| **Image Architect** | Visual | Production-ready prompts for Nano Banana Pro, Higgsfield, Seedream |
| **Video Director** | Motion | Hyper-realistic short-form video prompts for Kling, Sora, Veo |
| **Music Producer** | Audio | Suno prompt engineering across 40+ genres and 10 Indian languages |

Additional proprietary agents (consulting, research, trading) are maintained privately for enterprise client work.

## Workflow

### Content Pipeline
```
content-strategist → image-architect → video-director
```
Input: Topic or idea. Output: Thread copy + image prompts + video prompts. Ready to publish.

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
git clone https://github.com/tashisleepy/ai-engineering-stack.git

# Copy agents to your Claude Code config
cp ai-engineering-stack/agents/*.md ~/.claude/agents/

# (Optional) Install oh-my-claudecode for full orchestration
npm i -g oh-my-claude-sisyphus@latest
omc setup
```

## Project Structure

```
ai-engineering-stack/
├── agents/                    # Specialized AI agent definitions
│   ├── content-strategist.md  # Zero-slop content creation
│   ├── image-architect.md     # AI image prompt engineering
│   ├── video-director.md      # AI video prompt engineering
│   └── music-producer.md      # AI music production (Suno)
├── workflows/                 # Multi-agent orchestration pipelines
│   └── content-pipeline.md    # Write → Image → Video
├── configs/                   # System configuration
│   ├── model-routing.md       # AI model selection matrix
│   └── tool-ecosystem.md      # Complete tool stack
└── docs/                      # Documentation
```

## Philosophy

**Production-ready over academic.** Every agent ships work that enterprise clients pay for. Not prototypes. Not demos. Deployed systems.

**Stakes, specifics, friction.** Content must answer "why should anyone care?", name real numbers, and have edges. This runs through every agent.

**Architecture first, then detail.** Start with structure. Fill content. Iterate aggressively until it's 10/10.

## Built With

- [Claude Code](https://claude.ai/code) — Primary AI engineering environment
- [oh-my-claudecode](https://github.com/Yeachan-Heo/oh-my-claudecode) — Multi-agent orchestration (32 agents)
- [Ollama](https://ollama.com) + Qwen 3.5 — Local LLM for offline coding
- [Instrumenta](https://github.com/iappyx/Instrumenta) — McKinsey-grade PowerPoint toolbar

## License

MIT

---

*Built by Tashi. Part of a larger system deployed on enterprise AI projects.*
