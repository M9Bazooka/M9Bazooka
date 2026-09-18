# Mohammed Waliuddin

**AI engineer.** I ship agentic LLM apps, voice agents, generative-media pipelines and full-stack products, from empty repo to deployed. I build with Claude Code and Cursor, and I own everything around the code: architecture, tests, hosting, DNS and, on one product, the hardware.

Birmingham, UK, and ready to relocate to Dubai. English (professional), Urdu (native), Arabic (basic conversational).

**Live now:** [tapworth.co.uk](https://tapworth.co.uk) · [eatlo.in](https://eatlo.in) · [ik-designs.in](https://ik-designs.in)

---

## Read the code

Most of my work is commercial and private, so this one is public in full.

### [comfy-thumbs](https://github.com/M9Bazooka/comfy-thumbs)

Product thumbnails from a ComfyUI workflow, **where the product's own pixels always survive.**

A model asked to redraw a charger gets the ports wrong and invents a button. For affiliate content — where the picture is a claim about what someone will receive — that isn't a quality problem, it's a false advertisement. So the model is never shown the product: it generates only the scene, and the original pixels are composited back at output resolution. The client then verifies every opaque product pixel against the source and **refuses to save the image if a single one differs by more than 1/255.** Across every render made while building it, the maximum difference was 0.

Measured on an RTX 4060 (8 GB): about 7–8 s per image warm, 4.33 GB peak VRAM on the core graph. 101 test cases, a mock ComfyUI replaying recorded real traffic so the integrity check runs for real in CI, and golden tests pinning every workflow node. CI on Ubuntu and Windows.

`TypeScript · ComfyUI · sharp · Zod · vitest`

---

## Built and running

| Project | What it is | Stack |
|---|---|---|
| **[Tapworth](https://tapworth.co.uk)** | An NFC terminal between a shop's till and its receipt printer, reading every line item as it prints. Feeds a merchant dashboard, a receipt wallet with a grounded AI agent, and a consent-gated identity score. I built the firmware too. | Python · FastAPI · PostgreSQL · Redis · ESP32-S3 |
| **[Eatlo](https://eatlo.in)** | NFC and QR table ordering for Indian restaurants: four interfaces on one backend, a real-time kitchen display, AI menu import, CGST/SGST on every bill. Live with its first restaurants. | Node · Express · PostgreSQL · Socket.io |
| **[IK Designs](https://ik-designs.in)** | Commerce platform for a Hyderabad furniture studio: a six-step order builder, public order tracking, PDF quotes. Replaced orders taken over WhatsApp. | Next.js 14 · TypeScript · Prisma |
| **Affiliate Content Studio** | An Amazon product in, Pinterest and Instagram video plus copy out. Claude Code runs headless as the planner and the backend does the executing. 297 tests. | Next.js 15 · Claude Code · Higgsfield · FFmpeg |
| **recruitment-intel** | Lead generation from job postings, CV ingestion, hybrid embedding-based candidate matching and human-approved outreach, for a UK agency. Every external service sits behind a swappable adapter with a fake, and it is GDPR-first. | Python · FastAPI · PostgreSQL · Docker · embeddings |
| **AI OS** | My own multi-agent system: 20 agents behind a LangGraph orchestrator, 126 API routes, and an approval queue that outreach never bypasses. | LangGraph · FastAPI · Next.js · Ollama |
| **[Hunter System](https://github.com/M9Bazooka/hunter-system)** | A Solo Leveling-inspired training PWA, offline-capable and local-first, with one progression engine serving two training modes. 121 tests. | TypeScript · Vite · PWA |
| **[Pookie Cup Bot](https://github.com/M9Bazooka/pookie-cup-bot)** | A Discord tournament bot running swiss and double-elimination brackets, a live draft lottery and a Claude-powered assistant, for a League community. | discord.js v14 · Claude · drizzle · SQLite |

## Write-ups

Source is private for the commercial work, so these repos carry the architecture and the engineering decisions instead.

- **[ai-automations-showcase](https://github.com/M9Bazooka/ai-automations-showcase)** — a restaurant voice agent that books tables over a real phone call, an end-to-end YouTube production pipeline, and a Pinterest/Instagram content factory
- **[eatlo-showcase](https://github.com/M9Bazooka/eatlo-showcase)** · **[ik-designs-showcase](https://github.com/M9Bazooka/ik-designs-showcase)** · **[tap2dineinn-showcase](https://github.com/M9Bazooka/tap2dineinn-showcase)**

## Currently building

- **Night Audit** — a Roblox horror game whose rulebook regenerates every shift, built with Claude Code driving Roblox Studio and Blender over MCP. I started with no Luau experience.
- **MSc dissertation** at Aston University: a pre-registered study on memory-guided adaptive red teaming of LLMs, with a sham-memory control to separate retrieval gains from in-context ones. 502 tests.

## How I build

- **The agents type. I own the design.** Claude Code and Cursor write most of the code; I own the architecture, the written contracts they work from, and the tests that decide when something is done.
- **Model output is untrusted.** It gets validated, repaired or discarded before it reaches a user or a live system. Tapworth's agent deletes any figure it cannot back with a tool result; comfy-thumbs refuses to save an image whose product pixels drifted.
- **Rules that matter live in code.** Guardrails, disclosures and spending limits are enforced and tested, not requested in a prompt.

## Toolkit

**AI** Claude Code · Cursor · Anthropic & OpenAI APIs · LangGraph · LangChain · MCP · LiteLLM · Hugging Face · Ollama · PyTorch

**Media** ComfyUI · Higgsfield · fal.ai · ElevenLabs · FFmpeg · sharp

**Backend** Python · FastAPI · Node · Express · PostgreSQL · Prisma · SQLAlchemy · Redis · Socket.io

**Frontend** React · Next.js · TypeScript · Tailwind · PWAs · Arabic RTL

**Infra** Docker · GitHub Actions · AWS · Railway · Vercel · Cloudflare · Supabase

## Background

MSc Artificial Intelligence, Aston University (2025-2026) · BCA with AI specialisation, KL University (GPA 9.14/10) · AWS Certified AI Practitioner · IBM AI Developer · Automation Anywhere RPA Advanced · Founder of **Verris**, an AI studio

## Contact

[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:mohd.wali.uddin.2003@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/mohammed-waliuddin/)
