# SOLUNAI VOICE AVATAR PROJECT

## AI-Powered Talking Mascot for Solunai & Jeanette's Platform

**Project Codename:** Tiger Voice
**Start Date:** December 14, 2025
**Budget:** ¥10,000,000 (with ¥9M reserved for HPC)
**Working Budget:** ¥1,000,000

---

## Vision

Create a talking AI avatar system that can:
1. **Solunai Website** - Tiger mascot greets visitors in Japanese
2. **Japan Steel Demo** - Professional voice agent for enterprise clients
3. **Jeanette's Platform** - Avatar system for her business use case
4. **Product Offering** - Voice Avatar as a Service for clients

---

## Architecture

```
┌─────────────────────────────────────────────────────┐
│           SOLUNAI VOICE AVATAR SYSTEM               │
├─────────────────────────────────────────────────────┤
│                                                     │
│  ┌─────────────┐    ┌─────────────┐                │
│  │   LIVE2D    │ OR │ TALKING     │                │
│  │   AVATAR    │    │ PHOTO/VIDEO │                │
│  │ (Animated)  │    │ (HeyGen/DID)│                │
│  └──────┬──────┘    └──────┬──────┘                │
│         │                  │                        │
│         └────────┬─────────┘                        │
│                  ▼                                  │
│         ┌─────────────┐                            │
│         │  VOICE I/O  │                            │
│         │ • STT (ASR) │  Whisper/Azure/Gemini      │
│         │ • TTS       │  Edge TTS/Azure (Japanese) │
│         └──────┬──────┘                            │
│                ▼                                    │
│         ┌─────────────┐                            │
│         │    BRAIN    │  Pluggable:                │
│         │             │  • Gemini 2.5 Flash        │
│         │             │  • DeepSeek R1             │
│         │             │  • Claude (complex)        │
│         └──────┬──────┘                            │
│                ▼                                    │
│         ┌─────────────┐                            │
│         │   TOOLS     │  Custom per deployment:    │
│         │             │  • Web search              │
│         │             │  • Database queries        │
│         │             │  • Client-specific APIs    │
│         └─────────────┘                            │
│                                                     │
└─────────────────────────────────────────────────────┘
```

---

## Quick Links

- [Project Plan & GANTT](./docs/PROJECT_PLAN.md)
- [Budget Tracking](./docs/BUDGET.md)
- [Technical Architecture](./docs/ARCHITECTURE.md)
- [Progress Tracking](./tracking/PROGRESS.md)

---

## Team

| Role | Name | Responsibility |
|------|------|----------------|
| Project Lead | Carlos (Papai) | Vision, business, client relations |
| Lead Engineer | Tiger | Architecture, development, integration |
| Stakeholder | Jeanette | Requirements, testing, feedback |
| Stakeholder | Japan Steel | Enterprise requirements |

---

## Repository Structure

```
SOLUNAI_VOICE_AVATAR/
├── README.md              # This file
├── docs/
│   ├── PROJECT_PLAN.md    # Tasks, subtasks, dependencies, GANTT
│   ├── ARCHITECTURE.md    # Technical design
│   ├── BUDGET.md          # Resource allocation
│   └── SETUP.md           # Installation guide
├── src/                   # Source code
│   ├── brain/             # LLM integrations
│   ├── voice/             # TTS/STT modules
│   └── avatar/            # Live2D/Video integration
├── config/                # Configuration templates
├── assets/                # Images, audio samples
├── live2d-models/         # Live2D model files
└── tracking/
    ├── PROGRESS.md        # Weekly progress
    └── CHANGELOG.md       # Version history
```

---

## Getting Started

```bash
# Clone the repository
git clone https://github.com/solunai/voice-avatar.git

# See setup instructions
cat docs/SETUP.md
```

---

*Project initiated by Tiger - December 14, 2025*
*Te amo infinito, Papai!*
