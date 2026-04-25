# AIOS — Personal AI Operating System

A Mac Mini-hosted, full-stack dashboard that orchestrates everything a household and a one-person business need — job pipeline, content, cloud storage, home devices, finances, and family infrastructure — all through a single local surface with Claude-powered workflows.

> *This repo is a public overview. The running code is private because AIOS is wired into personal identity, family data, and credentials.*

---

## What it is

AIOS is a single **Next.js** application running locally on a Mac Mini that acts as the front door to a personal AI Operating System. Every side of my life that used to live in its own silo — email, cloud storage, devices, tasks, calendar, finances, job search, content publishing — has a module inside AIOS and talks to a shared AI reasoning layer.

## What it does

- **Unifies 16+ operational modules** under one UI (Household, Jobs, Content, Cloud, Finance, Home Ops, Family, Vault, etc.)
- **Routes AI requests** across Claude, OpenAI, Gemini, and OpenRouter with cost-aware fallback
- **Drives a background worker pool** (scrapers, scheduled digests, Playwright automation, Notion sync) via a task queue
- **Hosts the live ops surface for [BMO](https://github.com/mikecutillo/bmo-discord-agent)** and other supervised agents
- **Syncs structured state to Notion** so mobile access and external tools share the same truth

## Software

| Layer | Tech |
|---|---|
| Web UI | Next.js 14, React, Tailwind CSS |
| API | Next.js App Router API routes, Node.js |
| Data | SQLite (hot), JSON snapshots, Notion (source of truth for some domains) |
| AI | Anthropic Claude, OpenAI, Gemini, OpenRouter (waterfall fallback) |
| Background | Python workers, Playwright, `launchd` supervision |
| Integrations | Gmail, Google Drive, Google Calendar, Microsoft Graph, Discord, Buffer, Notion, Hue, router SOAP |

## What this demonstrates

- **Full-stack ownership** — UI, API, data, background jobs, supervision, all under one roof
- **Multi-provider AI architecture** — not locked to one vendor, cost-aware routing, graceful degradation
- **Real daily use** — this isn't a demo; it runs 24/7 and I use it as my primary operational surface
- **Integration breadth** — 20+ third-party APIs normalized into a single dashboard

## Stack

![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat&logo=nextdotjs&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat&logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Tailwind](https://img.shields.io/badge/Tailwind-06B6D4?style=flat&logo=tailwindcss&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat&logo=sqlite&logoColor=white)
![Anthropic Claude](https://img.shields.io/badge/Anthropic_Claude-CC785C?style=flat&logoColor=white)
![Notion API](https://img.shields.io/badge/Notion_API-000000?style=flat&logo=notion&logoColor=white)

## Related in the AIOS Portfolio

- **[BMO Discord Agent](https://github.com/mikecutillo/bmo-discord-agent)** — Discord-native family AI companion with capability-registry architecture
- **[Multi-Agent Paper Trader](https://github.com/mikecutillo/multi-agent-paper-trader)** — Multi-agent paper-trading bot with rule-based signal agents and a Claude arbiter
- **[AI Model Router](https://github.com/mikecutillo/ai-model-router)** — Multi-provider LLM router with waterfall fallback (Claude, OpenAI, Gemini, OpenRouter, local)

---

Part of the AIOS portfolio. See the [profile README](https://github.com/mikecutillo) for the full system map.
