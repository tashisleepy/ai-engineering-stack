# Model Routing Configuration

## AI Model Selection Matrix

### Language Models
| Task | Primary | Fallback | Reasoning |
|------|---------|----------|-----------|
| Complex architecture | Claude Opus | GPT-4o | Depth of reasoning |
| Fast iteration | Claude Haiku | Claude Sonnet | Speed + cost |
| Code generation | Claude Opus / Qwen 3.5 Coder | Codex | Accuracy |
| Content writing | Claude Opus | GPT-4o | Voice control |
| Data analysis | Claude Opus | Gemini 2.0 | Context window |

### Image Generation
| Task | Primary | Fallback |
|------|---------|----------|
| 4K hero shots | Nano Banana Pro | Seedream 4.5 |
| Fashion/editorial | Higgsfield Soul | Nano Banana Pro |
| Product texture | Seedream 4.5 | GPT Image 1.5 |
| True color accuracy | GPT Image 1.5 | Nano Banana Pro |
| Artistic/creative | FLUX.2 | Nano Banana Pro |

### Video Generation
| Task | Primary | Fallback |
|------|---------|----------|
| Product commercials | Kling O1 Edit | Sora 2 |
| Native audio | Kling 2.6 | Veo 3.1 |
| DOP presets | Higgsfield DOP | Kling O1 Edit |
| Complex scenes | Sora 2 | Veo 3.1 |
| Cinematic quality | Veo 3.1 | Kling O1 Edit |

### Music Generation
| Style | Suno Model |
|-------|-----------|
| Raw/gritty/lo-fi | v3 |
| Commercial hooks | v3.5 (default) |
| Modern polish | v4/v4.5 |
| Cinematic/orchestral | v5 |

## Cost Optimization
- Use Haiku for classification, routing, and simple tasks
- Use Opus only for complex reasoning, architecture, and creative direction
- Local models (Qwen 3.5) for iterative coding and testing
- Batch similar tasks to minimize context switching costs
