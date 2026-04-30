# JARVIS - Intelligent Local AI Agent

A secure, privacy-first AI agent framework with voice control, web automation, and intelligent planning capabilities.

## Features

- **Secure Architecture**: Backend server gateway with authentication tokens
- **Voice Control**: Speech recognition and synthesis for hands-free operation
- **Intelligent Brain**: Planning, intent inference, and tool governance
- **Web Automation**: Screen capture, web scraping, and system control
- **Privacy First**: Groq API key stored server-side only (never exposed to frontend)
- **Localhost-Only**: Runs on 127.0.0.1 with restricted CORS for maximum security

## Quick Start

1. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

2. **Configure Environment**
   ```bash
   cp .env.template .env
   # Edit .env and add your Groq API key
   ```

3. **Start JARVIS**
   - Terminal 1: `python jarvis_engine.py` (backend engine on :5050)
   - Terminal 2: `python jarvis_server.py` (gateway server on :5000)
   - Then open `http://localhost:5000` in your browser

## Architecture

- **jarvis_engine.py**: Local execution engine (system control, vision, scripting)
- **jarvis_server.py**: Secure gateway server (auth, Groq proxy, config management)
- **jarvis-v2.html**: Frontend UI with agentic brain (planning, intent, tool governance)

## Security

- Token-based authentication on all sensitive endpoints
- Groq API key kept server-side only
- Localhost-only binding
- CORS restricted to localhost origins
- Command filtering and URL validation on all operations

## License

MIT
