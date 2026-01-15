# Arcade TTV Roadmap

## Phase 1: Research & Testing

- [ ] Evaluate text-to-video models for 8GB VRAM compatibility
  - [ ] AnimateDiff
  - [ ] Zeroscope
  - [ ] ModelScope
  - [ ] CogVideoX-2B
- [ ] Test generation times and quality on RunPod
- [ ] Determine optimal GPU tier for cost/performance balance

## Phase 2: Core Development

- [ ] Video generation pipeline
  - [ ] Text prompt processing
  - [ ] Style/mood modifiers
  - [ ] Video generation with AnimateDiff (or selected model)
  - [ ] Output formatting (resolution, framerate, codec)
- [ ] Integration with arcade-tts
  - [ ] HTTP call to arcade-tts `/speak` endpoint (yelling voice)
  - [ ] Audio/video synchronization
  - [ ] Combined output file
- [ ] Flask API server
  - [ ] `/jumpscare` endpoint (video + TTS)
  - [ ] `/video` endpoint (video only)
  - [ ] `/health` endpoint
  - [ ] Error handling and logging

## Phase 3: Streamer.bot Integration

- [ ] Document Streamer.bot action setup
- [ ] Handle async generation (webhook callback or polling)
- [ ] Queue management for multiple redemptions

## Phase 4: Containerization

- [ ] Dockerfile with GPU support
- [ ] docker-compose for local testing
- [ ] Optimize image size (multi-stage build)
- [ ] Pre-download models in container

## Phase 5: Cloud Deployment

- [ ] RunPod Serverless configuration
- [ ] Cold start optimization
- [ ] Cost monitoring and alerts
- [ ] Documentation for DEPLOYMENT.md

## Phase 6: Polish & Features

- [ ] Style presets
  - [ ] Horror/creepy
  - [ ] Absurd/surreal
  - [ ] Glitch/distortion
  - [ ] Retro/VHS
- [ ] Configurable video length (3-5 seconds)
- [ ] Optional text overlay on video
- [ ] Volume/audio mixing controls

## Future Ideas

- Integration with arcade-stream-tools unified suite
- Custom LoRA support for specific visual styles
- Viewer voting on generated clips
- Clip archive/gallery feature
