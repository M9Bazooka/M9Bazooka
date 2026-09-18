<img src="assets/banner.png" alt="Mohammed Waliuddin — AI engineer and full-stack developer" width="100%">

<div align="center">

[![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=17&duration=3400&pause=1000&color=959CFF&center=true&vCenter=true&width=700&lines=Production+AI+systems%2C+shipped+end+to+end;Agentic+LLM+apps+%C2%B7+voice+agents+%C2%B7+media+pipelines;Full-stack+products+with+real+users+behind+them;Open+to+roles%2C+contract+work+and+collaborations)](https://m9bazooka.github.io)

<a href="https://m9bazooka.github.io"><img src="https://img.shields.io/badge/Portfolio-m9bazooka.github.io-2B34C9?style=for-the-badge&logo=googlechrome&logoColor=white"></a>
<a href="mailto:mohd.wali.uddin.2003@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white"></a>
<a href="https://www.linkedin.com/in/mohammed-waliuddin/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"></a>

</div>

I build AI systems that people actually use, and the products around them. That usually means the whole thing: the architecture, the model work, the front end, the tests, the deployment, the DNS — and on one product, the circuit board. Some of it is mine, some of it belongs to clients, and one is open source.

I work fast with Claude Code and Cursor, which is the point of the engineering rules further down: speed is only worth anything if the result holds up.

<br>

## What I do

<table>
<tr>
<td width="33%" valign="top">

### AI systems & agents

LLM apps that call tools over real data, multi-agent pipelines, voice agents, and the grounding and guardrail work that makes them safe to put in front of a customer.

</td>
<td width="33%" valign="top">

### Full-stack products

Multi-tenant SaaS, real-time systems, commerce platforms and dashboards — from schema to deployment, including the boring parts that decide whether it survives.

</td>
<td width="33%" valign="top">

### Automation & pipelines

Scrapers, data pipelines, generative-media production and API integrations, in n8n where that fits and in code when it stops fitting.

</td>
</tr>
</table>

<br>

## Selected work

Each card opens a write-up with the architecture, the decisions and — where I captured one — a recording of the system actually running.

<div align="center">

<a href="https://github.com/M9Bazooka/tapworth-showcase"><img src="assets/c-tapworth.png" width="48%"></a>
<a href="https://github.com/M9Bazooka/eatlo-showcase"><img src="assets/c-eatlo.png" width="48%"></a>
<a href="https://github.com/M9Bazooka/affiliate-content-studio-showcase"><img src="assets/c-studio.png" width="48%"></a>
<a href="https://github.com/M9Bazooka/ai-os-showcase"><img src="assets/c-aios.png" width="48%"></a>
<a href="https://github.com/M9Bazooka/comfy-thumbs"><img src="assets/c-comfy.png" width="48%"></a>
<img src="assets/c-recruit.png" width="48%">

</div>

<br>

## Also built

| | What it is | |
|---|---|---|
| **IK Designs** | A commerce platform for a Hyderabad furniture studio: a six-step order builder, public order tracking by reference number, a secured admin area with print-ready quotes. It replaced orders taken over WhatsApp. | [site](https://ik-designs.in) · [write-up](https://github.com/M9Bazooka/ik-designs-showcase) |
| **AI automations** | A voice agent that answers a restaurant's phone and books real tables, an end-to-end YouTube production pipeline, and a Pinterest/Instagram content factory with compliance enforced in code. | [write-up](https://github.com/M9Bazooka/ai-automations-showcase) |
| **Tap2DineIn** | A QR ordering platform built on contract for a UK operator — table sessions, price-snapshotted orders, a real-time kitchen flow and Stripe payments. | [write-up](https://github.com/M9Bazooka/tap2dineinn-showcase) |
| **Hunter System** | A Solo Leveling-inspired training PWA: offline-capable, local-first, one XP and rank engine serving two training modes. 121 engine tests. | [repo](https://github.com/M9Bazooka/hunter-system) |
| **Pookie Cup Bot** | A Discord tournament bot for a League community: swiss and double-elimination brackets, a live tier-based draft lottery, captain trades and casting, with a Claude-powered assistant. | [repo](https://github.com/M9Bazooka/pookie-cup-bot) |

<br>

## How I build

> **The agents type. I own the design.**
> Claude Code and Cursor write most of the code. I own the architecture, the written contracts they work from, and the tests that decide when something is done.

> **Model output is untrusted.**
> It gets validated, repaired or discarded before it reaches a user. Tapworth's agent deletes any figure it cannot back with a tool result. comfy-thumbs refuses to save an image whose product pixels drifted from the source photo.

> **Rules that matter live in code.**
> Guardrails, legal disclosures and spending limits are enforced by code and covered by tests, not requested politely in a prompt. AI OS has no send capability at all — an agent there cannot email anyone by design, not by configuration.

> **Publish what broke.**
> When I record a system running, the failures stay in. Capturing real runs this year surfaced a modifier missing from a bill total, a socket event with no listener, and a pipeline that never recorded its own approval pause. They are all in the write-ups.

<br>

## Stack

<div align="center">

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white)

![Claude](https://img.shields.io/badge/Claude_Code-191919?style=flat-square&logo=anthropic&logoColor=white)
![Cursor](https://img.shields.io/badge/Cursor-000000?style=flat-square)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=flat-square&logo=openai&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![MCP](https://img.shields.io/badge/MCP-2C2C54?style=flat-square)
![LiteLLM](https://img.shields.io/badge/LiteLLM-4B32C3?style=flat-square)
![Hugging Face](https://img.shields.io/badge/Hugging_Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![Ollama](https://img.shields.io/badge/Ollama-000000?style=flat-square&logo=ollama&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)

![ComfyUI](https://img.shields.io/badge/ComfyUI-1A1A2E?style=flat-square)
![ElevenLabs](https://img.shields.io/badge/ElevenLabs-000000?style=flat-square&logo=elevenlabs&logoColor=white)
![fal.ai](https://img.shields.io/badge/fal.ai-FF4081?style=flat-square)
![FFmpeg](https://img.shields.io/badge/FFmpeg-007808?style=flat-square&logo=ffmpeg&logoColor=white)
![n8n](https://img.shields.io/badge/n8n-EA4B71?style=flat-square&logo=n8n&logoColor=white)
![Twilio](https://img.shields.io/badge/Twilio-F22F46?style=flat-square&logo=twilio&logoColor=white)

![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=flat-square&logo=prisma&logoColor=white)
![Socket.io](https://img.shields.io/badge/Socket.io-010101?style=flat-square&logo=socketdotio&logoColor=white)

![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonaws&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=flat-square&logo=cloudflare&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white)
![Railway](https://img.shields.io/badge/Railway-0B0D0E?style=flat-square&logo=railway&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3FCF8E?style=flat-square&logo=supabase&logoColor=white)

<br>

<img src="assets/langs.png" width="820" alt="Language distribution across every repository: JavaScript 48%, Python 32.6%, TypeScript 11.4%, HTML 6.5%, CSS 0.6%, C++ firmware 0.4%">

</div>

<br>

## Currently building

**Night Audit** — a Roblox horror game whose rulebook regenerates every shift, so the answers can't be looked up online. Claude Code drives Roblox Studio and Blender over MCP from a written project contract. I started with no Luau experience.

**MSc dissertation**, Aston University — a pre-registered study on memory-guided adaptive red teaming of LLMs, with a length-matched sham-memory control to separate retrieval gains from simply having examples in context. 502 tests, and a pilot bug filed as a formal pre-registration amendment rather than quietly patched.

<br>

## Background

**MSc Artificial Intelligence** — Aston University, 2025–2026<br>
**BCA, AI specialisation** — KL University, GPA 9.14/10<br>
**AWS Certified AI Practitioner** · **IBM AI Developer** · **Automation Anywhere RPA Advanced**<br>
Founder of **Verris**, an AI studio building agents, automations and web platforms for businesses<br>
English (professional) · Urdu (native) · Arabic (basic conversational)

<br>

## Get in touch

Based in Birmingham, UK. Open to engineering roles, contract work and collaborations — remote or relocating.

If you have something you want built, or you want to talk through how one of these systems works, email is the fastest way to reach me and I'm happy to screen-share any of it.

<div align="center">
<br>
<a href="mailto:mohd.wali.uddin.2003@gmail.com"><img src="https://img.shields.io/badge/mohd.wali.uddin.2003@gmail.com-2B34C9?style=for-the-badge&logo=maildotru&logoColor=white"></a>
<a href="https://www.linkedin.com/in/mohammed-waliuddin/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"></a>
<a href="https://m9bazooka.github.io"><img src="https://img.shields.io/badge/Portfolio-111337?style=for-the-badge&logo=googlechrome&logoColor=white"></a>
</div>
