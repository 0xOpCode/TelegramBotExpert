# 🤖 TelegramBotExpert (Claude-Architect-Prime)

**TelegramBotExpert** is an advanced, language-agnostic, agentic AI architecture designed to build, scale, and maintain Telegram Bots and Mini Apps. It acts as an autonomous Chief Architect, UX Engineer, and Security Auditor, specifically tailored for the complexities of the Telegram Bot API.

It utilizes Anthropic's [Claude Code](https://github.com/anthropics/claude-code) native primitives (`.claude/`) to scaffold a centralized, scalable, memory-persistent, and hook-driven framework.

## ✨ Features

- **Language & Framework Agnostic**: Initialize the expert for *any* stack (Python/aiogram, Node/Telegraf, Go/telebot, Rust/teloxide, etc.).
- **Agent Orchestration**: Specialized sub-agents automatically handle different domains of bot development:
  - `tg-architect`: System design, DB schema modeling, FSM (state machine) planning, and Webhook vs. Polling strategies.
  - `tg-ux-engineer`: Crafting Inline Keyboards, conversational text, Inline Queries, and Telegram Mini Apps.
  - `tg-sec-auditor`: Input sanitization, rate limiting, role-based access control, and securing webhook endpoints.
- **Advanced Bot Skills**: On-demand prompt injection modules for:
  - Finite State Machine (`fsm-builder`)
  - Database Schemas (`create-db-schema`)
  - Webhook Architecture (`setup-webhook`)
  - Internationalization (`i18n-builder`)
  - Web Apps / Mini Apps (`mini-app-builder`)
  - Payment Gateways (`payment-gateway-setup`)
- **Memory & Session Handoff**: Dedicated commands (`/save-state`, `/resume`) and files (`progress.md`, `bot_manifest.md`) to maintain context across sessions and prevent token bloat.

## 🚀 Getting Started

### Prerequisites

1. You must have [Claude Code](https://github.com/anthropics/claude-code) installed and authenticated.
2. Initialize your underlying bot project (e.g., `npm init`, `poetry new`, `go mod init`) in the same directory.

### Installation

Clone this repository or copy the `.claude/` directory and `CLAUDE.md` into your existing bot project's root:

```bash
git clone https://github.com/yourusername/TelegramBotExpert.git my-bot-project
cd my-bot-project
```

### 1. Initialize the Expert

Bind the expert to your specific tech stack. Run the Claude Code CLI:

```bash
claude
```

Then, use the custom `/init-bot` slash command, specifying your language and framework:

```text
/init-bot nodejs/telegraf
```
*(Or `/init-bot python/aiogram3`, `/init-bot go/telebot`, etc.)*

This will automatically configure all agents, skills, and memory manifests to specialize in your chosen ecosystem.

### 2. Scaffold a Flow

Want to build a multi-step conversation? Just ask the orchestrator:

```text
/add-flow "User registration wizard that asks for name and email with validation, using an Inline Keyboard"
```
The `tg-architect` will design the state machine, the `tg-ux-engineer` will write the UI/prompts, and the code will be written to your project.

### 3. Build a Mini App

Need a Telegram Web App? Use the specialized skill:

```text
Use the mini-app-builder skill to create a storefront Mini App integrated with the bot.
```

### 4. Save Your State

When you're done for the day or your context window is getting full, save your progress:

```text
/save-state
```
This writes a clean handoff to `.claude/memory/temp_context.md`. You can safely run `/clear` or exit.

When you return, start Claude Code and run:
```text
/resume
```

## 📂 Architecture Overview

```text
.claude/
├── settings.json              # Permissions and model config
├── agents/                    # Declarative sub-agents (auto-invoked)
│   ├── tg-architect.md
│   ├── tg-ux-engineer.md
│   └── tg-sec-auditor.md
├── skills/                    # On-demand prompt injection modules
│   ├── tg-api-navigator/      # Codebase routing
│   ├── fsm-builder/           # Conversation state management
│   ├── create-db-schema/      # DB architecture
│   ├── setup-webhook/         # Webhook endpoints
│   ├── i18n-builder/          # Multi-language support
│   ├── mini-app-builder/      # Telegram Web Apps
│   └── payment-gateway-setup/ # Telegram Payments & Crypto
├── commands/                  # Custom slash commands
│   ├── init-bot.md
│   ├── add-flow.md
│   ├── save-state.md
│   └── resume.md
├── hooks/
│   └── hooks.json             # Pre/Post tool automation (SessionStart/Stop)
├── memory/
│   ├── bot_manifest.md        # The living architecture document
│   ├── progress.md            # Milestones
│   ├── temp_context.md        # Session handoff state
│   └── master_protocol.md     # Core rules for Telegram bots
└── CLAUDE.md                  # Lightweight entry point
```

## 🤝 Contributing

Contributions are welcome! If you have a specific Telegram Bot pattern, architecture, or skill you'd like to add, please open a PR.

## 📄 License

MIT License