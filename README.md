<div align="center">

<img src="https://i.ibb.co/8D6xfjXn/shihab-cover.png" width="100%" alt="Sheikh Shihab Hossain — Full-Stack & LLM Engineer"/>

<br/>

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=23&pause=1400&color=2CA697&center=true&vCenter=true&width=760&lines=Full-Stack+Engineer+%40+Sharetasking+Inc.;I+build+LLM+systems+that+can+be+measured.;Voice+%2B+SMS+agents%2C+workflow+engines%2C+multi-tenant+SaaS)](https://shihab-portfolio.vercel.app/)

<br/>

<a href="https://shihab-portfolio.vercel.app/"><img src="https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=vercel&logoColor=white" alt="Portfolio"/></a>
&nbsp;
<a href="https://www.linkedin.com/in/sheikh-shihab-hossain/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
&nbsp;
<a href="mailto:shihabhossainii20@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"/></a>
&nbsp;
<a href="https://gitroll.io/profile/utRX49Aq4JUcZF7ZE9TTjsp95f0S2"><img src="https://img.shields.io/badge/GitRoll-8A2BE2?style=for-the-badge&logo=git&logoColor=white" alt="GitRoll"/></a>

</div>

---

I'm a full-stack engineer at **Sharetasking Inc.**, building **SiloCRM** with a team of five. Most of my recent work is LLM application engineering: a real-time voice agent on ElevenLabs ConvAI, AI-generated SMS on Twilio, RAG with per-tenant knowledge-base sync — and a visual workflow automation engine I designed and built end-to-end, solo.

I care about the part most LLM work skips: proving the thing actually works. That's why I wrote [EvalLab](https://github.com/iamshihab2020/evallab).

**Khulna, Bangladesh (UTC+6)** · remote with US teams · open to senior full-stack roles

---

## The workflow engine, running its own example

The engine walks a trigger graph **breadth-first, one depth at a time**, and writes a log line per node. Every run is replayable in a read-only viewer. This is the shape of a real workflow a user builds on the canvas:

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

React Flow canvas + Zustand on the front, a custom Fastify execution engine behind it. **33 trigger types**, **20+ actions** across the CRM lifecycle.

---

<details>
<summary><b>What I'm shipping right now</b></summary>

<br/>

**SiloPilot** — a per-tenant, multi-channel AI agent for lead qualification, appointment booking, data collection and call routing. Each agent is bound to a tenant-owned Twilio number. I built:

- the **ElevenLabs ConvAI voice integration** — real-time WebSocket, document store / RAG, agent provisioning
- the **Twilio SMS layer** with AI-generated replies
- **webhook ingest** for transcription, audio and conversation events
- **RAG pipelines** with per-tenant knowledge-base sync
- **tool-use** for call transfer and data collection
- the **AI agents management UI**

**Workflow Automation Engine** — owned end-to-end, solo. Visual no-code builder, custom execution engine, breadth-first graph traversal, per-node logs, replayable run viewer.

> Both are company products behind a private repo, not side projects. The public repos below are my own work.

</details>

<details>
<summary><b>Selected work</b></summary>

<br/>

| Project | What it is | |
| --- | --- | --- |
| **EvalLab** | LLM evaluation harness — LLM-as-judge scoring across four dimensions, failure clustering, judge calibration with Cohen's κ and a 5×5 confusion matrix. Python/FastAPI + Next.js. | [repo](https://github.com/iamshihab2020/evallab) · [live](https://evallab-pearl.vercel.app/) |
| **Zaxvio CRM** | Multi-tenant field-service SaaS for HVAC contractors. Scheduling, quoting, invoicing, customer history. Built solo, end-to-end. | [repo](https://github.com/iamshihab2020/zaxvio-crm) · [live](https://zaxvio-crm-web.vercel.app) |
| **SiloCRM** | Multi-tenant AI-powered CRM. SiloPilot and the workflow engine live here. | [live](https://silocrm.com) |
| **TabDeck** | A Chrome new-tab page. Open source. | [repo](https://github.com/iamshihab2020/tabdeck) |
| **Counterfoil** | SaaS platform — frontend contribution at Ternary Solutions. | [live](https://counterfoil.app/) |

</details>

<details>
<summary><b>The stack, by layer</b></summary>

<br/>

**LLM** — Prompt engineering · Agent design · RAG · Tool-use / function-calling · Streaming inference · LLM-as-judge evaluation · Prompt versioning

![ElevenLabs](https://img.shields.io/badge/ElevenLabs-000000?style=flat-square&logoColor=white)
![Twilio](https://img.shields.io/badge/Twilio-F22F46?style=flat-square&logo=twilio&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=flat-square&logo=openai&logoColor=white)
![Anthropic](https://img.shields.io/badge/Anthropic-D97757?style=flat-square&logo=anthropic&logoColor=white)
![Groq](https://img.shields.io/badge/Groq-F55036?style=flat-square&logoColor=white)

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
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Django](https://img.shields.io/badge/Django-092E20?style=flat-square&logo=django&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=flat-square&logo=prisma&logoColor=white)
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-D71F00?style=flat-square&logo=sqlalchemy&logoColor=white)

**Data & infra**

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Neon](https://img.shields.io/badge/Neon-00E599?style=flat-square&logo=neon&logoColor=black)
![Supabase](https://img.shields.io/badge/Supabase-3FCF8E?style=flat-square&logo=supabase&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white)
![Turborepo](https://img.shields.io/badge/Turborepo-EF4444?style=flat-square&logo=turborepo&logoColor=white)

Multi-tenant isolation is enforced at the database with **PostgreSQL row-level security**, not in application code.

**Practice**

![Claude](https://img.shields.io/badge/Claude_Code-D97757?style=flat-square&logo=anthropic&logoColor=white)
![Cursor](https://img.shields.io/badge/Cursor-000000?style=flat-square&logoColor=white)
![Vitest](https://img.shields.io/badge/Vitest-6E9F18?style=flat-square&logo=vitest&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white)
![Linear](https://img.shields.io/badge/Linear-5E6AD2?style=flat-square&logo=linear&logoColor=white)

</details>

<details>
<summary><b>How I work</b></summary>

<br/>

- **REST APIs get designed before they get implemented.** The contract is the artifact; the handler is a detail.
- **Tenant isolation belongs in the database.** Row-level security means a missed `WHERE` clause is a failed query, not a data leak.
- **Evals before vibes.** If an LLM feature ships without a way to measure regression, it ships without a way to know it broke. That opinion is why EvalLab exists.
- **Daily Claude Code and Cursor user** — directing agents, curating context, and reviewing what they produce across the monorepo.

</details>

---

## Activity

<div align="center">

<img src="https://streak-stats.demolab.com/?user=iamshihab2020&theme=github-dark-blue&hide_border=true&background=0D1117&ring=2CA697&fire=2CA697&currStreakLabel=2CA697" width="60%" alt="GitHub streak"/>

<br/><br/>

<a href="https://gitroll.io/profile/utRX49Aq4JUcZF7ZE9TTjsp95f0S2" target="_blank">
  <img src="https://gitroll.io/api/badges/profiles/v1/utRX49Aq4JUcZF7ZE9TTjsp95f0S2?theme=tokyoNight" alt="GitRoll profile"/>
</a>

</div>

---

## Let's talk

I'm open to senior full-stack roles, particularly LLM application work. Multi-tenant SaaS, agent plumbing, workflow tooling — anything where the engineering has a real job to do.

Outside of code it's history, storytelling, and the occasional YouTube rabbit hole. Happy to swap notes on either.

<div align="center">
<br/>

[![Email](https://img.shields.io/badge/Email_me-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:shihabhossainii20@gmail.com)
&nbsp;
[![LinkedIn](https://img.shields.io/badge/Connect_on_LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/sheikh-shihab-hossain/)

</div>
