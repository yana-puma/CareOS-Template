# CareOS: AI Agent Operational Best Practices

Because AI assistants (like Claude Code, Cursor, Windsurf, or Antigravity) can actively edit your files and execute terminal scripts, you must guide them with strict operational constraints. Use these guidelines to preserve your vault's sanity and protect your token quota budget.

## 🛟 Rule 1: Always Use "Planning Mode" First
Before you let an agent write a script or modify multiple care templates, explicitly tell it:
> "Put yourself into Planning Mode. Propose a step-by-step implementation plan for what you want to change, and wait for my explicit confirmation before modifying any files."
This cuts out autonomous mistakes and saves your token budget.

## 📥 Rule 2: Enforce the Staging Inbox Protocol
Never let an AI agent write text directly into your clean, historical reference notes. It might break your custom properties, tags, or internal links. 
- Instruct the agent to write all new summaries, extracted doctor metrics, or log entries into a dedicated file named `patient-records/_Log_Inbox.md`.
- You act as the human editor. Review the text in the inbox file first, then manually copy or link it into your permanent folders.

## 🛑 Rule 3: Stop Runaway Self-Healing Loops
If a local automation script errors out, agents love to repeatedly execute back-to-back terminal commands to try to fix it on autopilot. This can obliterate your daily high-priority model quota in minutes.
- **The Safeguard:** Ensure your environment's "Terminal Auto-Execution" setting is changed from *Always Proceed* to *Require Review*. 
- If the AI hits a bug, it will gracefully freeze execution and wait for you to click an "Approve" button.