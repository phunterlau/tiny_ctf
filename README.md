# picoCTF Agent Workspace

This project exists purely for educational practice: it helps researchers and learners study how AI-guided agents can approach CTF problems end to end.

This repository contains a reusable workspace for practicing picoCTF-style challenges with Codex acting as a ReAct agent. The core prompt lives in `AGENTS.md`, guiding the agent through common CTF disciplines—currently Reverse Engineering and Cryptography—to surface flags efficiently.

## How It Works
- `AGENTS.md` describes the mission mindset, toolbelt, and workflow habits that Codex follows while triaging challenges.
- During a session, the agent builds an iterative ReAct plan, proposes Linux command sequences or Python scripts, and focuses on uncovering flags.
- The flow supports user interrupts and feedback loops so you can steer the investigation in real time.

For other CLIs, copy `AGENTS.md` to `CLAUDE.md` or `GEMINI.md` (or any agent-specific filename) and load it as the system prompt.

## Getting Started
1. Create and activate a Python virtual environment.
2. Install the helper tooling with `pip install -r requirements.txt`.
3. Follow the instructions in `AGENTS.md` to drive Codex (or the alternative agent file) as you work through challenges.

## Real Challenge Flow
- Visit picoCTF, pick a challenge, and download its payloads into a local directory such as `./315/`.
- Tell Codex, “solve ./315/ with problem statement and hints as …” (fill in the prompt details), then let the agent spin up its triage and tooling plan.
- Grab a coffee while the agent iterates, enumerates, and hunts for the flag.

With the environment ready, drop challenge artifacts into their numbered directories, let the agent enumerate, iterate, and document findings, and expect a final `walkthrough.md` capturing key findings, tools used, and lessons learned—supporting transparent, educational insight into the AI-guided process.
