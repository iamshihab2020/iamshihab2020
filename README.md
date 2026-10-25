<div align="center">

<img src="assets/hero.svg" width="100%" alt="Sheikh Shihab Hossain, software developer: AI SaaS, LLM systems and automation"/>

<br/>

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&pause=1400&color=2CA697&center=true&vCenter=true&width=900&lines=I+build+LLM+systems+that+can+be+measured.;Voice+and+SMS+agents%2C+workflow+engines%2C+multi-tenant+SaaS.;Open+source+on+the+side%3A+TabbyDeck%2C+DropMate%2C+TabDeck.)](https://shihab-portfolio.vercel.app/)

<a href="https://shihab-portfolio.vercel.app/"><img src="https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=vercel&logoColor=white" alt="Portfolio"/></a>
&nbsp;
<a href="mailto:sheikhshihabhossain2020@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"/></a>
&nbsp;
<a href="https://gitroll.io/profile/utRX49Aq4JUcZF7ZE9TTjsp95f0S2"><img src="https://img.shields.io/badge/GitRoll-8A2BE2?style=for-the-badge&logo=git&logoColor=white" alt="GitRoll"/></a>

</div>

---

I'm a software developer building **SiloCRM** and **SiloCSM** for **JWeis Marketing**, and before that for Sharetasking Inc. Most of my recent work is LLM application engineering: a real-time voice agent on ElevenLabs ConvAI, AI-written SMS on Twilio, RAG with per-tenant knowledge-base sync, MCP tools that expose CRM data to agents, and a visual workflow automation engine.

I care about the part most LLM work skips: proving the thing actually works. That's why I built [EvalLab](https://github.com/iamshihab2020/evallab).

**Open to senior full-stack and LLM application roles**, remote with US teams.

---

## What I'm shipping at work

**SiloPilot**, a per-tenant AI agent for calls, SMS and email. It qualifies leads, books appointments, collects data and routes calls, each agent on a tenant-owned Twilio number. My part:

- the **ElevenLabs ConvAI voice integration**: real-time WebSocket, document store and RAG, agent provisioning
- the **Twilio layer**: calling, conference calls and AI-written SMS replies
- **webhook ingest** for transcripts, audio and conversation events
- **MCP integrations** and tool use for call transfer and data collection
- the **AI agents management UI**

**The workflow automation engine.** A no-code canvas (React Flow and Zustand) on a custom Fastify execution engine: **33 triggers, 20+ actions**, conditional branches. It walks the graph **breadth-first, one depth at a time**, and logs every node, so each run can be replayed. The header above is that idea, animated. A real workflow looks like this:

```mermaid
flowchart LR
    T([New lead]) --> A[Tag inbound]
    A --> W[Wait 5 min]
    W --> Q{Replied?}
    Q -- no --> S[Send SMS]
    Q -- yes --> C[Create task]
    S --> L[(Per-node<br/>execution log)]
    C --> L
```

> Both live in a private company repo. Everything below is my own public work.

---

## Selected work

| Project | What it is | Links |
| --- | --- | --- |
| **EvalLab** | LLM evaluation platform. LLM-as-judge scoring on accuracy, completeness, tone and safety; run-to-run regression checks; failure clustering; judge calibration against humans with Cohen's κ. Next.js, FastAPI, PostgreSQL. | [repo](https://github.com/iamshihab2020/evallab) · [live](https://evallab-pearl.vercel.app/) |
| **Zaxvio CRM** | Multi-tenant field-service SaaS for small HVAC teams: scheduling, invoicing, customer history. Turborepo with Next.js, Fastify, Supabase and Drizzle. Built solo. | [repo](https://github.com/iamshihab2020/zaxvio-crm) · [live](https://zaxvio-crm-web.vercel.app) |
| **Bangla sentiment fine-tuning** | How much labelled data a QLoRA-tuned 1–2B model needs to match BanglaBERT, on a 6 GB laptop GPU. Reproduced the published baseline and found 7.2% train/test leakage in SentNoB. | [repo](https://github.com/iamshihab2020/bangla-sentiment-finetuning) |
| **TabbyDeck** | Turns a phone or tablet into a Stream Deck for Windows. Node host, Preact deck and editor, 399 tests. Open source. | [repo](https://github.com/iamshihab2020/TabbyDeck) · [site](https://iamshihab2020.github.io/TabbyDeck/) |
| **DropMate** | Chat and send files to people at home over your own Wi-Fi. Windows and Android, no cloud, no account. Flutter. | [repo](https://github.com/iamshihab2020/DropMate) |
| **TabDeck** | A feature-packed new-tab page for Chrome. My most-starred repo. | [repo](https://github.com/iamshihab2020/tabdeck) |

---

## Research

**Autism Spectrum Disorder Identification from Facial Images Using Fine-Tuned Pre-trained Deep Learning Models and Explainable AI Techniques**<br/>
Hossain, S. S., et al. (2025). *Semarak International Journal of Applied Psychology*, 5(1), 29–53. First author.<br/>
Compared 12 fine-tuned CNNs; DenseNet121 reached 90.33% accuracy and 90.00% F1. LIME and Grad-CAM show which facial regions drive each prediction.

---

## Stack

<p align="center">
  <img src="https://skillicons.dev/icons?i=ts,react,nextjs,tailwind,nodejs,python,fastapi,django,postgres,redis,supabase,docker,vercel&perline=13" alt="TypeScript, React, Next.js, Tailwind, Node.js, Python, FastAPI, Django, PostgreSQL, Redis, Supabase, Docker, Vercel"/>
</p>

<details>
<summary><b>The full stack, by layer</b></summary>

<br/>

**LLM**: prompt and context engineering · agents and tool calling · MCP · RAG · structured outputs · LLM-as-judge evaluation · QLoRA fine-tuning

![ElevenLabs](https://img.shields.io/badge/ElevenLabs-000000?style=flat-square&logoColor=white)
![Twilio](https://img.shields.io/badge/Twilio-F22F46?style=flat-square&logo=twilio&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=flat-square&logo=openai&logoColor=white)
![Anthropic](https://img.shields.io/badge/Anthropic-191919?style=flat-square&logo=anthropic&logoColor=white)
![Groq](https://img.shields.io/badge/Groq-F55036?style=flat-square&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Hugging_Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)

**Interface**

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=next.js&logoColor=white)
![Tailwind](https://img.shields.io/badge/Tailwind-38B2AC?style=flat-square&logo=tailwind-css&logoColor=white)
![shadcn/ui](https://img.shields.io/badge/shadcn%2Fui-000000?style=flat-square&logo=shadcnui&logoColor=white)
![React Flow](https://img.shields.io/badge/React_Flow-FF0072?style=flat-square&logoColor=white)
![Zustand](https://img.shields.io/badge/Zustand-433E38?style=flat-square&logoColor=white)
![Framer Motion](https://img.shields.io/badge/Framer_Motion-0055FF?style=flat-square&logo=framer&logoColor=white)

**Service**

![Fastify](https://img.shields.io/badge/Fastify-000000?style=flat-square&logo=fastify&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white)
![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Django](https://img.shields.io/badge/Django-092E20?style=flat-square&logo=django&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=flat-square&logo=prisma&logoColor=white)
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-D71F00?style=flat-square&logo=sqlalchemy&logoColor=white)

**Data and infra**

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Neon](https://img.shields.io/badge/Neon-00E599?style=flat-square&logo=neon&logoColor=black)
![Supabase](https://img.shields.io/badge/Supabase-3FCF8E?style=flat-square&logo=supabase&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white)
![Turborepo](https://img.shields.io/badge/Turborepo-EF4444?style=flat-square&logo=turborepo&logoColor=white)

**Practice**

![Claude Code](https://img.shields.io/badge/Claude_Code-191919?style=flat-square&logo=anthropic&logoColor=white)
![Cursor](https://img.shields.io/badge/Cursor-000000?style=flat-square&logoColor=white)
![Vitest](https://img.shields.io/badge/Vitest-6E9F18?style=flat-square&logo=vitest&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white)
![Linear](https://img.shields.io/badge/Linear-5E6AD2?style=flat-square&logo=linear&logoColor=white)

</details>

<details>
<summary><b>How I work</b></summary>

<br/>

- **Design the API before writing it.** The contract is what matters; the handler is a detail.
- **Tenant isolation belongs in the database.** With PostgreSQL row-level security, a missing `WHERE` clause fails the query instead of leaking data.
- **Measure before trusting.** An LLM feature without a regression check has no way to tell you it broke. That's why EvalLab exists.
- **I use Claude Code and Cursor every day**: directing agents, curating context, and reviewing what they write.

</details>

---

## Activity

<div align="center">

<img src="https://streak-stats.demolab.com/?user=iamshihab2020&theme=github-dark-blue&hide_border=true&background=0D1117&ring=2CA697&fire=2CA697&currStreakLabel=2CA697" width="60%" alt="GitHub streak"/>

<br/><br/>

<a href="https://gitroll.io/profile/utRX49Aq4JUcZF7ZE9TTjsp95f0S2" target="_blank"><img src="https://gitroll.io/api/badges/profiles/v1/utRX49Aq4JUcZF7ZE9TTjsp95f0S2?theme=dark" alt="GitRoll Profile Badge"/></a>

</div>

---

## Let's talk

I'm looking for senior full-stack roles, especially LLM application work: multi-tenant SaaS, agent plumbing, workflow tooling, anywhere the engineering has a real job to do.

Outside code, it's history, storytelling and the occasional YouTube rabbit hole. Happy to swap notes on either.

<div align="center">
<br/>

[![Email](https://img.shields.io/badge/Email_me-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:sheikhshihabhossain2020@gmail.com)
&nbsp;
[![Portfolio](https://img.shields.io/badge/See_my_portfolio-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://shihab-portfolio.vercel.app/)

</div>
