# CareOS-Template

A tool-agnostic, privacy-hardened environment template designed for caregivers managing high-vulnerability patient logistics. This layout is flat, human-readable, and fully compatible with markdown-based knowledge networks (like Obsidian) and autonomous development tools.

## 📂 Layout Map
- `/templates/` — Holds the structural frameworks for parsing telemetry metrics.
- `/docs/` — Grounding baseline instructions and clinical disease protocols.
- `/patient-records/` — Target directory for generating localized logs (Blocked via firewall).

## ⚙️ System Configuration (The Dual-Prompt System)
To maintain both clinical accuracy and operational safety, this template relies on two distinct configuration files:
- `ai-instructions.md` — Defines the **clinical persona**. It instructs the AI on *how* to parse medical data, format logs, and flag emergencies.
- `agents.md` — Defines the **operational guardrails**. It tells AI tools (like Claude Code, Cursor, Windsurf) *how* they are allowed to edit your files (e.g., requiring planning mode, preventing runaway terminal loops).

## 🚀 Deployment Instructions
Open this directory workspace inside your preferred agent tool (Claude Code, Cursor, Windsurf, or Antigravity) and seed the setup prompt:

> "Review `ai-instructions.md` to initialize the workspace context. Generate today's `templates/log-daily.md` file inside a new directory called `patient-records/`."
