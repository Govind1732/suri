# Suri

Suri Core is a personal AI orchestration runtime built in Python. It is designed to coordinate specialized workers, AI models, browser automation, and messaging interfaces to automate useful workflows while keeping humans in control.

## What it is

- A FastAPI backend for orchestration and agent integration
- A project focused on Telegram + Gemini AI assistant integration
- An event-driven runtime layer on top of Linux/macOS
- A coordinator that uses external AI services rather than replacing them

## Current focus

This repository is currently in Phase 1, building the core foundation:

- FastAPI application
- Gemini/AI service abstraction
- Telegram bot integration
- Memory storage support
- Browser automation via Playwright
- Intent routing and tool dispatching

## Tech stack

- Python
- FastAPI
- asyncio
- Uvicorn
- Gemini / Google generative AI libraries
- Telegram Bot API
- SQLAlchemy / aiosqlite (PostgreSQL planned)
- Playwright + Chromium for browser agent work

## Quickstart

```bash
cd suri
uv venv
source .venv/bin/activate
uv pip install -r requirements.txt
```

To start the FastAPI app:

```bash
uvicorn app.main:app --reload
```

Then visit `http://127.0.0.1:8000`.

## Project structure

- `app/main.py` - FastAPI application entrypoint
- `app/agents/` - automation and agent implementations
- `app/services/` - AI integration and service abstractions
- `app/config/` - configuration and environment handling
- `app/database/` - persistence and data access
- `app/memory/` - conversation memory and storage logic
- `app/tools/` - utility helpers and automation tools
- `docs/` - design notes and project vision
- `requirements.txt` - Python dependencies

## Current phase 1 tasks

### FastAPI Foundation
- [ ] Setup FastAPI app
- [ ] Add health endpoint
- [ ] Add logging middleware

### Gemini Integration
- [ ] Configure Gemini client
- [ ] Create AI service abstraction
- [ ] Add retry handling

### Telegram Bot
- [ ] Create bot
- [ ] Add webhook/polling
- [ ] Connect to AI service

### Memory System
- [ ] Setup PostgreSQL
- [ ] Create messages table
- [ ] Store conversations

### Browser Agent
- [ ] Setup Playwright
- [ ] Open websites
- [ ] Capture screenshots
- [ ] Extract page text

### Router Agent
- [ ] Command routing
- [ ] Intent classification
- [ ] Tool dispatching

## Notes

- Use `uv` if available for package management, but standard `pip` is also supported.
- The architecture prioritizes incremental progress and low-overhead orchestration.
- Avoid introducing heavy frameworks too early; focus on manual routing, queues, and event-driven design.
