# Arcade TTV

A Twitch Channel Point jumpscare video generator powered by AI text-to-video and voice cloning.

> **Status: In Development**
> This project is currently a placeholder. Core functionality is planned but not yet implemented.

## Concept

Viewers redeem channel points with a text prompt. The system generates:
1. A short (3-5 second) AI-generated video based on their prompt
2. A yelling TTS voice reading their message
3. Combined audio/video jumpscare that plays on stream

**Example:**
- Viewer redeems with: "giant rubber duck attacks the city"
- System generates surreal AI video of the concept
- Bot voice screams the message over the video
- Chaos ensues on stream

## Planned Features

- **Text-to-Video Generation** — AI-generated surreal/absurd video clips
- **Yelling TTS Integration** — Uses [arcade-tts](https://github.com/elchalupa/arcade-tts) for voice
- **Streamer.bot Integration** — HTTP API for channel point redemptions
- **Cloud Deployment** — RunPod Serverless for GPU-heavy generation
- **Customizable Styles** — Different video generation presets

## Planned Tech Stack

| Component | Technology |
|-----------|------------|
| Video Generation | AnimateDiff / Stable Diffusion |
| Voice Synthesis | Chatterbox-Turbo (via arcade-tts) |
| Web Server | Flask |
| Deployment | Docker / RunPod Serverless |

## Requirements (Planned)

- Python 3.11
- NVIDIA GPU with 8GB+ VRAM (local) or cloud GPU
- [arcade-tts](https://github.com/elchalupa/arcade-tts) for voice generation
- [Streamer.bot](https://streamer.bot/) v1.0.3+

## Project Structure (Planned)

```
arcade-ttv/
├── video_server.py         # Main Flask server
├── video_generator.py      # Text-to-video generation
├── requirements.txt        # Python dependencies
├── Dockerfile              # Container definition
├── docker-compose.yml      # Local Docker setup
├── prompts/                # Video style presets
├── video_output/           # Generated videos (gitignored)
└── README.md
```

## API Endpoints (Planned)

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/jumpscare?text=...` | GET/POST | Generate video + yelling TTS |
| `/video?text=...` | GET/POST | Generate video only |
| `/health` | GET | Health check |

## Related Projects

- [arcade-tts](https://github.com/elchalupa/arcade-tts) — Channel point TTS system
- arcade-stream-tools (coming soon) — Unified suite

## Estimated Cloud Costs

Video generation is GPU-intensive. Estimated RunPod Serverless costs:

| Usage | Monthly Cost |
|-------|-------------|
| 10 jumpscares/month | $1 - $3 |
| 50 jumpscares/month | $5 - $15 |

Generation time: ~30-90 seconds per video (varies by GPU tier).

## Roadmap

- [ ] Core video generation pipeline
- [ ] Integration with arcade-tts for yelling voice
- [ ] Streamer.bot HTTP API
- [ ] Docker containerization
- [ ] RunPod Serverless deployment
- [ ] Style presets (horror, absurd, glitch, etc.)

## Contributing

This project is in early development. Feel free to open issues with ideas or feature requests.

## License

MIT License — See [LICENSE](LICENSE) for details.

---

Part of the Arcade Stream Tools ecosystem
