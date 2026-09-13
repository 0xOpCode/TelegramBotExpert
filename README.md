<div align="center">

  # 🤖 TelegramBotExpert
  ### Claude-Architect-Prime: Autonomous Telegram Bot & Mini App Architecture

  [![Claude Code](https://img.shields.io/badge/Powered%20By-Claude%20Code-D97706.svg?style=flat-square&logo=anthropic&logoColor=white)](https://github.com/anthropics/claude-code)
  [![Telegram API](https://img.shields.io/badge/Telegram-Bot%20%26%20Mini%20Apps-26A5E4.svg?style=flat-square&logo=telegram&logoColor=white)](https://core.telegram.org/bots)
  [![Architecture](https://img.shields.io/badge/Architecture-Sub--Agent%20Orchestration-8A2BE2.svg?style=flat-square)](#-architecture-overview)
  [![License](https://img.shields.io/badge/License-MIT-green.svg?style=flat-square)](LICENSE)
  [![Maintained](https://img.shields.io/badge/Maintained%20by-0xOpCode-orange.svg?style=flat-square)](https://github.com/0xOpCode)

  <p align="center">
    <b>An enterprise-grade, language-agnostic agentic framework designed to build, scale, and maintain high-concurrency Telegram Bots and Telegram Mini Apps (TMAs).</b>
  </p>

  <p align="center">
    <a href="#-specialized-sub-agents">Sub-Agents</a> •
    <a href="#-advanced-bot-skills">Skills</a> •
    <a href="#-getting-started">Getting Started</a> •
    <a href="#-architecture-overview">Architecture</a> •
    <a href="#-workflow-commands">Commands</a>
  </p>

</div>

---

## 📌 Overview

**TelegramBotExpert** acts as an autonomous Chief Architect, Lead UX Engineer, and Security Auditor inside [Claude Code](https://github.com/anthropics/claude-code). Rather than relying on generic LLM prompts, it provides specialized domain sub-agents, memory manifests, and state machine builders tuned specifically for the Telegram Bot API lifecycle.

---

## 🤖 Specialized Sub-Agents

| Agent | Responsibility | Core Deliverables |
| :--- | :--- | :--- |
| `tg-architect` | **System & Data Architecture** | FSM conversation models, DB schemas (PostgreSQL / Redis), Webhook scaling vs Long Polling strategies. |
| `tg-ux-engineer` | **Conversational UI & Mini Apps** | Inline keyboard pagination, deep-linking routing, message templating, and Telegram Web App (TMA) viewports. |
| `tg-sec-auditor` | **Security & Compliance** | Webhook secret validation, HMAC signature verification, user rate-limiting, and RBAC admin protections. |

---

## ⚡ Advanced Bot Skills

On-demand prompt injection modules designed to generate production patterns:

- 🔄 **`fsm-builder`**: Scaffolds resilient multi-step conversation flows with input fallbacks.
- 🗄️ **`create-db-schema`**: Generates high-efficiency relational and document storage for Telegram sessions.
- 🌐 **`setup-webhook`**: Configures production NGINX / FastAPI / Express reverse-proxy webhook endpoints with SSL.
- 🌍 **`i18n-builder`**: Modular multi-language string dictionaries and locale detection.
- 📱 **`mini-app-builder`**: Fullstack Telegram Mini App (TMA) scaffolds integrating Telegram WebApp JS SDK.
- 💳 **`payment-gateway-setup`**: Telegram native Stars, Stripe, and Crypto invoice integrations.

---

## 🚀 Getting Started

### Prerequisites
1. Install and authenticate [Claude Code](https://github.com/anthropics/claude-code).
2. Works with any stack: **Python** (`aiogram`, `python-telegram-bot`), **Node.js** (`grammY`, `telegraf`), **Go** (`telebot`), **Rust** (`teloxide`).

### Installation
Clone into your bot project's workspace:

```bash
git clone https://github.com/0xOpCode/TelegramBotExpert.git .claude-expert
cp -r .claude-expert/.claude .
cp .claude-expert/CLAUDE.md .
rm -rf .claude-expert
```

### 1. Initialize for Your Tech Stack
Launch Claude Code CLI in your project directory:

```bash
claude
```

Run the stack initialization command:
```text
/init-bot python/aiogram3
# or: /init-bot nodejs/grammy
# or: /init-bot go/telebot
```

### 2. Scaffold a Conversational Flow
```text
/add-flow "User onboarding flow with email validation, referral codes, and inline keyboard confirmation"
```

### 3. Session Handoff & Memory Persistence
Preserve tokens and agent context across long engineering sessions:
- Save session memory: `/save-state`
- Resume from previous milestone: `/resume`

---

## 📂 Architecture Overview

```text
.claude/
├── settings.json              # Autonomous permissions and configuration
├── agents/                    # Domain-specialized sub-agents
│   ├── tg-architect.md        # System design & DB schemas
│   ├── tg-ux-engineer.md      # Inline keyboards & Mini App UI
│   └── tg-sec-auditor.md      # Cryptographic verification & security
├── skills/                    # Specialized injection skills
│   ├── tg-api-navigator/      # Endpoint and routing utilities
│   ├── fsm-builder/           # Conversation state management
│   ├── create-db-schema/      # Optimized database modeling
│   ├── setup-webhook/         # Webhook infrastructure
│   ├── i18n-builder/          # Multilingual dictionary pipelines
│   ├── mini-app-builder/      # Telegram Mini Apps (TMA)
│   └── payment-gateway-setup/ # Telegram Payments & Stars
├── commands/                  # Orchestration slash commands
│   ├── init-bot.md
│   ├── add-flow.md
│   ├── save-state.md
│   └── resume.md
├── hooks/
│   └── hooks.json             # Pre/Post session state management
└── memory/
    ├── bot_manifest.md        # Living architecture spec
    ├── progress.md            # Sprint milestones
    └── master_protocol.md     # Engineering rules of engagement
```

---

## 📄 License

Distributed under the **MIT License**.

---

## 👨‍💻 Maintainer

Engineered by **[0xOpCode](https://github.com/0xOpCode)**.