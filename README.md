<div align="center">

# Mohammed Waliuddin

[![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=21&duration=3200&pause=900&color=2B34C9&center=true&vCenter=true&width=680&lines=AI+engineer+%E2%80%94+I+ship+systems+people+can+use+today;Agentic+LLM+apps%2C+voice+agents%2C+media+pipelines;Claude+Code+and+Cursor+type.+I+own+the+design.;Birmingham%2C+UK+%E2%86%92+ready+to+relocate+to+Dubai)](https://github.com/M9Bazooka)

**From empty repo to deployed** — architecture, tests, hosting, DNS and, on one product, the hardware.

<a href="https://m9bazooka.github.io"><img src="https://img.shields.io/badge/Portfolio-m9bazooka.github.io-2B34C9?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Portfolio"></a>
<a href="mailto:mohd.wali.uddin.2003@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
<a href="https://www.linkedin.com/in/mohammed-waliuddin/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>

**Live right now** &nbsp;
<a href="https://tapworth.co.uk"><img src="https://img.shields.io/badge/●_tapworth.co.uk-0A8558?style=flat-square" alt="tapworth.co.uk"></a>
<a href="https://eatlo.in"><img src="https://img.shields.io/badge/●_eatlo.in-0A8558?style=flat-square" alt="eatlo.in"></a>
<a href="https://ik-designs.in"><img src="https://img.shields.io/badge/●_ik--designs.in-0A8558?style=flat-square" alt="ik-designs.in"></a>

</div>

---

## Not a screenshot — a real run

<div align="center">

<img src="assets/eatlo-three-screens.gif" alt="One Eatlo order moving across the diner's phone, the kitchen display and the owner dashboard in real time" width="760">

**One order, three screens, no refresh.** The diner's tracker, the kitchen display and the owner's revenue all move together over Socket.io. Captured from a real local run on 17 September 2026 — subtotal ₹800, CGST ₹20, SGST ₹20, ₹840 landing on the dashboard.

<sub>Full capture, event traces and the four bugs it exposed → <a href="https://github.com/M9Bazooka/eatlo-showcase">eatlo-showcase</a></sub>

</div>

---

## Read the code

> Most of my work is commercial and private. This one is public in full.

### [comfy-thumbs](https://github.com/M9Bazooka/comfy-thumbs) — where the product's own pixels always survive

<a href="https://github.com/M9Bazooka/comfy-thumbs"><img src="assets/card-comfy.png" width="46%" align="right" alt="comfy-thumbs"></a>

<div align="center">
<img src="https://raw.githubusercontent.com/M9Bazooka/comfy-thumbs/main/examples/outputs/charger-pinterest.jpg" alt="Generated Pinterest pin of a charger" height="215">
<img src="https://raw.githubusercontent.com/M9Bazooka/comfy-thumbs/main/examples/outputs/camera-square.jpg" alt="Generated square post of a camera" height="215">
<img src="https://raw.githubusercontent.com/M9Bazooka/comfy-thumbs/main/examples/outputs/headphones-vertical.jpg" alt="Generated vertical frame of headphones" height="215">
</div>

Every label, lens marking and grille line above is the **source photo's own pixels**. The lamps, windows and desks are generated.

A model asked to redraw a charger gets the ports wrong and invents a button. For affiliate content — where the picture is a claim about what someone will receive — that isn't a quality problem, it's a false advertisement. So the model never sees the product: it generates only the scene, and the original pixels are composited back at output resolution. Then the client checks every opaque product pixel against the source and **refuses to save the image if one differs by more than 1/255**. Across every render made while building it, the maximum difference was **0**.

<div align="center">

| ⏱ Warm render | 🎮 Peak VRAM | 🧪 Tests | ⚙️ CI |
|:---:|:---:|:---:|:---:|
| **7–8 s** / image | **4.33 GB** on an RTX 4060 | **101** cases | Ubuntu + Windows |

</div>

`TypeScript` · `ComfyUI` · `sharp` · `Zod` · `vitest` — with a mock ComfyUI replaying recorded real traffic, so the integrity check runs for real in CI without a GPU.

---

## Built and running

<div align="center">

<a href="https://github.com/M9Bazooka/tapworth-showcase"><img src="assets/card-tapworth.png" width="46%" alt="Tapworth"></a>
<a href="https://github.com/M9Bazooka/affiliate-content-studio-showcase"><img src="assets/card-studio.png" width="46%" alt="Affiliate Content Studio"></a>
<a href="https://github.com/M9Bazooka/ai-os-showcase"><img src="assets/card-aios.png" width="46%" alt="AI OS"></a>
<a href="https://github.com/M9Bazooka/eatlo-showcase"><img src="assets/card-eatlo.png" width="46%" alt="Eatlo"></a>

</div>

<details>
<summary><b>🧾 Tapworth</b> — an NFC terminal between a shop's till and its printer &nbsp;<code>built · tapworth.co.uk</code></summary>

<br>

A low-cost terminal sits inline on the receipt-printer cable, forwards every byte to the printer first, and parses the ESC/POS stream on the way past. Open banking sees "£47 at Tesco"; Tapworth sees the 23 items inside. One capture feeds three products: merchant intelligence, a receipt wallet with an AI agent, and a consent-gated identity score.

- **Grounding is enforced after generation.** No figure reaches the user without a tool result behind it; unsupported output is discarded, not flagged.
- **Guardrails run in code before any model call**, tested in CI. The user's tap creates agent memory, and sending anything is never automated at any autonomy level. About **$0.021** per question.
- **The till never depends on us.** A normally-closed relay means an unpowered or crashed terminal is a direct POS-to-printer wire. Firmware TLS is pinned to the root certificate, not the 90-day leaf.
- **Arabic RTL and dark mode from day one**, with automated EN/AR string-parity checks and a measured contrast auditor.
- **575 backend tests**, Docker, CI, field-level AES-256-GCM encryption, k-anonymity of 5 on merchant analytics.

`Python` `FastAPI` `PostgreSQL` `Redis` `ESP32-S3` `Railway` `Cloudflare`

**[Read the architecture →](https://github.com/M9Bazooka/tapworth-showcase)**

</details>

<details>
<summary><b>🎬 Affiliate Content Studio</b> — product in, posted video out &nbsp;<code>built · 297 tests</code></summary>

<br>

<img src="assets/studio-copy-checks.webp" align="right" width="330" alt="Copy variants measured against platform limits">

Turns an Amazon product into ready-to-post Pinterest and Instagram videos with copy, then tracks what went out.

- **Claude decides, the backend executes.** Claude Code runs headless, writes one validated result file and exits. A clean exit code isn't success; a valid file is.
- **Spend is checked before it happens** — the estimate goes on screen for approval before any render.
- **Compliance is code.** Platform rules live in one module feeding the prompt, the validator and the on-screen counters. Disclosures are added by the backend, never left to a prompt.
- **It outgrew n8n**, so I rebuilt it as an app with a job queue, a worker and live log streaming.

In the captured run the render was **refused** — the Higgsfield account is on the free plan — so the job retried once and failed cleanly with **zero credits spent**. That is the pipeline working, not failing.

`Next.js 15` `Prisma` `Claude Code` `Higgsfield` `FFmpeg` `Zod`

**[Read the write-up →](https://github.com/M9Bazooka/affiliate-content-studio-showcase)**

</details>

<details>
<summary><b>🤖 AI OS</b> — 20 agents, and an approval queue nothing bypasses &nbsp;<code>built</code></summary>

<br>

<img src="assets/aios-approval-queue.webp" align="right" width="330" alt="An outreach draft stopped in the approval queue">

A brief goes in; a spec agent, a task-breakdown agent, research and outreach agents work one job queue behind a LangGraph orchestrator, with status streaming to a dashboard over WebSockets.

- **Sending is not a feature.** The app has no send capability at all — the outreach agent writes a draft, it lands with `status=draft` and `sent_at=None`, and the button a human presses only marks a row as sent. An agent cannot email anyone by design, not by configuration.
- **Local first, escalate deliberately.** Qwen 3 8B through Ollama for ordinary work, the Claude API for hard jobs, routed per agent.
- **20 agents · 126 API routes · 2 LangGraph pipelines · 243 source files.**
- The captured run cost **$0.118** over 320 seconds — and exposed that the pipeline never records its approval pause. That failed check is published in the trace rather than edited out.

`LangGraph` `FastAPI` `Next.js 14` `Ollama` `Redis` `Docker`

**[Read the write-up →](https://github.com/M9Bazooka/ai-os-showcase)**

</details>

<details>
<summary><b>🍽 Eatlo</b> — NFC table ordering, live in Hyderabad &nbsp;<code>live · eatlo.in</code></summary>

<br>

Every table gets an NFC and QR card. Diners tap or scan, then order and track their food in the browser with no app.

- **Four interfaces on one backend** — customer, kitchen display, owner dashboard, operator console — across **120 API endpoints** and **25 tables**.
- **A new restaurant goes live in 1.59 s** with the provisioning CLI, 95 ms of it server time.
- **AI menu import** reads a photo into structured items in 13 s, then waits for the owner to review before saving.
- **Built for Indian rules:** veg/non-veg marks, CGST and SGST split on every bill, a scheduled discount engine, staff roles. I designed and sourced the physical table cards too.

`React` `Node` `Express` `PostgreSQL` `Socket.io` `Railway`

**[Read the write-up →](https://github.com/M9Bazooka/eatlo-showcase)**

</details>

<details>
<summary><b>📇 recruitment-intel</b> — lead scraping and candidate matching for a UK agency &nbsp;<code>built · client work</code></summary>

<br>

Job-posting lead generation, CV ingestion, hybrid embedding-based candidate matching and human-approved outreach, running as a daily pipeline that prints a morning digest.

- Every external service sits behind a **swappable adapter with a fake implementation**, so the whole system runs and tests with no third-party calls at all.
- **GDPR-first** by design, not by policy note.
- Local embeddings (`BAAI/bge-small-en-v1.5`) or a hosted provider, switched by config.

`Python` `FastAPI` `PostgreSQL` `Alembic` `Docker` `embeddings`

</details>

<details>
<summary><b>⚔️ Hunter System</b> &nbsp;·&nbsp; <b>🏆 Pookie Cup Bot</b> &nbsp;·&nbsp; <b>🛋 IK Designs</b> &nbsp;·&nbsp; <b>📱 Tap2DineIn</b></summary>

<br>

- **[Hunter System](https://github.com/M9Bazooka/hunter-system)** — a Solo Leveling-inspired training PWA, offline-capable and local-first, with one XP/rank engine serving both a gym and a calisthenics mode. **121 engine tests.** `TypeScript` `Vite` `PWA`
- **[Pookie Cup Bot](https://github.com/M9Bazooka/pookie-cup-bot)** — a Discord tournament bot for a League community: swiss and double-elimination brackets, a live tier-based draft lottery, captain trades, casting and stats, plus a Claude-powered assistant. `discord.js v14` `Claude` `drizzle` `SQLite`
- **[IK Designs](https://ik-designs.in)** — a commerce platform for a Hyderabad furniture studio: a six-step order builder, public order tracking, a secured admin area with print-ready PDF quotes. It replaced orders taken over WhatsApp. `Next.js 14` `Prisma` — [write-up](https://github.com/M9Bazooka/ik-designs-showcase)
- **Tap2DineIn** — a QR ordering platform built on contract for a UK operator; backend in a ~20-hour sprint, then the customer app. `Express` `Socket.io` `Stripe` — [write-up](https://github.com/M9Bazooka/tap2dineinn-showcase)

</details>

<details>
<summary><b>🎙 AI automations</b> — a voice agent that answers the phone, and two content pipelines</summary>

<br>

- **Prawn**, an AI voice receptionist for a seafood restaurant: Twilio → n8n → an LLM agent with seven tools → ElevenLabs. It answers menu and allergen questions **only from the menu tool**, never from memory, so it cannot invent a dish or a price. Recognises returning callers before the greeting plays and texts a confirmation after every booking.
- **An end-to-end YouTube pipeline**: one trigger researches a topic, writes a script, generates voiceover, music, images and AI video, and assembles a 1080p film. A master workflow drives eight sub-workflows, each testable alone.
- **A Pinterest/Instagram content factory** with affiliate compliance enforced in code.

**[Read all three →](https://github.com/M9Bazooka/ai-automations-showcase)**

</details>

---

## How I build

<table>
<tr>
<td width="33%" valign="top">

### 🧠 The agents type
### I own the design

Claude Code and Cursor write most of the code. I own the architecture, the written contracts they work from, and the tests that decide when something is done.

</td>
<td width="33%" valign="top">

### 🚫 Model output
### is untrusted

Validated, repaired or discarded before it reaches a user. Tapworth deletes any figure it can't back with a tool result; comfy-thumbs refuses to save an image whose product pixels drifted.

</td>
<td width="33%" valign="top">

### 🔒 Rules that matter
### live in code

Guardrails, legal disclosures and spending limits are enforced by code and covered by tests, not requested politely in a prompt.

</td>
</tr>
</table>

---

## Toolkit

<div align="center">

**AI & agents**

![Claude](https://img.shields.io/badge/Claude_Code-191919?style=flat-square&logo=anthropic&logoColor=white)
![Cursor](https://img.shields.io/badge/Cursor-000000?style=flat-square)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=flat-square&logo=openai&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![MCP](https://img.shields.io/badge/MCP-2C2C54?style=flat-square)
![LiteLLM](https://img.shields.io/badge/LiteLLM-4B32C3?style=flat-square)
![HuggingFace](https://img.shields.io/badge/Hugging_Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![Ollama](https://img.shields.io/badge/Ollama-000000?style=flat-square&logo=ollama&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)

**Generative media**

![ComfyUI](https://img.shields.io/badge/ComfyUI-1A1A2E?style=flat-square)
![Higgsfield](https://img.shields.io/badge/Higgsfield-7C3AED?style=flat-square)
![fal.ai](https://img.shields.io/badge/fal.ai-FF4081?style=flat-square)
![ElevenLabs](https://img.shields.io/badge/ElevenLabs-000000?style=flat-square&logo=elevenlabs&logoColor=white)
![FFmpeg](https://img.shields.io/badge/FFmpeg-007808?style=flat-square&logo=ffmpeg&logoColor=white)
![sharp](https://img.shields.io/badge/sharp-99CC00?style=flat-square)

**Backend & data**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=flat-square&logo=prisma&logoColor=white)
![Socket.io](https://img.shields.io/badge/Socket.io-010101?style=flat-square&logo=socketdotio&logoColor=white)

**Frontend & infra**

![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Tailwind](https://img.shields.io/badge/Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=flat-square&logo=cloudflare&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white)
![Railway](https://img.shields.io/badge/Railway-0B0D0E?style=flat-square&logo=railway&logoColor=white)

</div>

---

## Currently building

**🏨 Night Audit** — a Roblox horror game whose rulebook regenerates every shift, so it can't be looked up online. Claude Code drives Roblox Studio and Blender over MCP from a written project contract. I started with no Luau experience.

**🛡 MSc dissertation**, Aston University — a pre-registered study on memory-guided adaptive red teaming of LLMs, with a length-matched **sham-memory control** to separate retrieval gains from simply having examples in context. 502 tests, and a pilot bug fixed as a formal pre-registration amendment rather than a quiet patch.

---

<div align="center">

<img src="assets/langs.png" width="800" alt="Language distribution across every repository: JavaScript 48%, Python 32.6%, TypeScript 11.4%, HTML 6.5%, CSS 0.6%, C++ firmware 0.4%">

### Background

**MSc Artificial Intelligence** — Aston University, 2025–2026<br>
**BCA, AI specialisation** — KL University, GPA 9.14/10<br>
**AWS Certified AI Practitioner** · **IBM AI Developer** · **Automation Anywhere RPA Advanced**<br>
Founder of **Verris**, an AI studio<br>
English (professional) · Urdu (native) · Arabic (basic conversational)

<br>

**Open to Senior AI / full-stack roles in Dubai.**

<a href="mailto:mohd.wali.uddin.2003@gmail.com"><img src="https://img.shields.io/badge/Get_in_touch-2B34C9?style=for-the-badge&logo=maildotru&logoColor=white" alt="Get in touch"></a>

</div>
