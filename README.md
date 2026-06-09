# Muhammad Saad

**Senior Software Engineer** with 5+ years building scalable backend systems, FinTech workflows, and full-stack products.

📍 Lahore, Pakistan · 🌍 Open to remote work globally

[![Email](https://img.shields.io/badge/Email-saad__tayyab@outlook.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:saad_tayyab@outlook.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-saadtayyab-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/saadtayyab)
[![GitHub](https://img.shields.io/badge/GitHub-saad--tayyab-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/saad-tayyab)

---

## Hi there

I'm Muhammad — a backend-focused engineer who enjoys turning complex business rules into reliable, well-tested software. I've spent the last few years in **FinTech and enterprise SaaS**, and I'm currently building **Grammify**, an offline-first learning platform on the side.

I care about clean architecture, strong test coverage, and shipping things that actually hold up in production. I also use **Cursor AI** day to day to move faster while keeping quality high — not as a shortcut around thinking, but as a partner when the specs, boundaries, and verification steps are already clear.

---

## What I'm working on now

### JiBe ERP — Senior Software Engineer
*Remote · Miami, USA · Aug 2023 – Present*

Enterprise **maritime ERP** for global shipping operations. I lead backend work on accounting, payment processing, and financial reporting.

- Shipped **9 production modules** end to end — sales invoices, automated payments, budgets, fixed assets, journal automation, batch payments, inter-bank transfers, tax codes, and management billing — each with **idempotent SQL migrations**, access-rights wiring, and **Azure DevOps** PR/CI gates before release
- Automated **8 complex payment-to-journal workflows** by modeling business rules as **testable, isolated services** instead of one-off UI scripts — cutting manual payment work
- Improved invoice generation latency by **~40%** through **SQL profiling**, targeted indexing, and **batch processing** instead of row-by-row writes on large datasets
- Introduced **event-driven posting** with **RabbitMQ** — async payment settlement and budget consumption decoupled from the request thread, with **optimistic locking** on budget lines to prevent double-spend under concurrency
- Kept **90%+ unit test coverage** (**200+ Jest tests**) on payment and accounting paths — TDD on critical journal logic, peer code review, and regression tests on every shipped feature (**zero production incidents** from my releases)

### Grammify — Personal project
*[github.com/saad-tayyab/grammify](https://github.com/saad-tayyab/grammify)*

**Offline-first English grammar learning** for **CSS / UPSC** competitive exam aspirants — structured curriculum, adaptive practice, error-pattern intelligence, AI tutoring, and exam-mode assessments.

| Layer | Stack |
|-------|--------|
| Mobile | Expo · React Native · SQLite · MMKV |
| API | NestJS · Prisma · PostgreSQL |
| Admin | Next.js App Router |
| Monorepo | Turborepo · Bun · Biome · framework-free engines in `packages/core` |

---

## How I build

This is the approach I use on Grammify — and it's the same discipline I bring to production work at JiBe: **write it down first, build in layers, verify before you call it done.**

### 1. Spec-driven, not vibe-driven

Before code, there's a doc. Grammify is organized around **epic PRDs** (user stories + acceptance criteria), linked **technical specs**, a **definition of done**, and a living **status board**. Every feature has a clear "in scope / out of scope" boundary so work doesn't sprawl across half the product in one PR.

I don't ask AI to "build the whole app." I ship **one epic, one feature, or one backlog step at a time** — each with its own acceptance checklist.

### 2. Types first, UI last

Code flows in a fixed order:

```text
packages/types  →  packages/core  →  apps/api  →  apps/mobile  →  apps/admin
```

Shared domain types and port interfaces come first. Pure business logic (quiz engines, adaptive difficulty, scoring, spaced revision) lives in **`packages/core`** with zero framework imports — no React, no NestJS, no Prisma. Apps are thin adapters: SQLite on mobile, Prisma on the API, dumb screens that delegate to `features/` hooks.

That means the same cognitive logic runs on mobile and server, and I can unit-test the hard parts without spinning up an app.

### 3. Offline-first by design

Learners shouldn't need a signal to study. On mobile, **SQLite is the source of truth** — syllabus, questions, progress, attempts, and review queues all work locally. Sync is a background concern, not a blocker. The UI never waits on the network to render a lesson or submit a practice answer.

### 4. Docs stay in sync with code

When code changes, docs change too — architecture, data model, sync rules, API contracts. Cursor rules and `AGENTS.md` tell both me and AI agents exactly where things belong and what not to touch (e.g. mastery formulas locked behind an ADR until accepted).

Docs aren't decoration. They're how I onboard future me, keep AI context accurate, and make every epic shippable without re-explaining the system from scratch.

### 5. AI-assisted, but verified

I use **Cursor** with structured prompts — implement, verify, backlog step — and treat AI like a fast junior engineer: great at boilerplate and cross-file changes, but only as good as the spec you give it.

Before anything is "done":
- Acceptance criteria checked off in the PRD
- Definition of done satisfied (offline behavior, error/empty states, tests where it matters)
- `bun run check` + tests on touched packages
- Status board and docs updated

Move fast, but don't merge ambiguity.

### 6. Product principles that shape the architecture

Grammify isn't just a quiz app. The product docs encode real learning decisions:

- **Diagnostic-first** — place learners before personalizing
- **Structured before adaptive** — always know where you are in the curriculum
- **Practice with diagnosis** — every wrong answer feeds error-pattern intelligence
- **Exam relevance first** — content maps to CSS/UPSC needs
- **AI as tutor, not replacement** — hints and explanations grounded in official lesson content

Those principles drive what gets built and how — not the other way around.

---

## Background

**Software Engineer · Skill Knight Studios** *(Lahore · May 2021 – Feb 2023)*  
Blockchain gaming and mobile apps — Solana (Rifters Kalinvale), EOS.IO NFT games (Nefty Ballers), Unity WebGL, auth microservices, AWS/GCP deployments.

**Machine Learning Engineer · Freelance** *(Nov 2019 – Feb 2021)*  
Predictive analytics, real-time medical imaging APIs (PyTorch), and streaming data pipelines with Kafka.

**Education:** B.S. Computer Science — FAST NUCES, Lahore *(2016 – 2020)*

---

## Tech I work with

**Backend:** TypeScript · JavaScript · Node.js · Express · NestJS · REST · Microservices · Event-driven architecture · RabbitMQ

**Frontend:** React · Angular · Next.js · React Native / Expo

**Databases:** SQL Server · PostgreSQL · MySQL · MongoDB · TypeORM · Prisma

**Cloud & DevOps:** AWS · GCP · Azure DevOps · Docker · CI/CD

**Quality:** Jest · TDD · Code reviews · mentoring junior engineers

**Also:** Python · PyTorch · scikit-learn · C++17 · EOS.IO · Solana · Unity · Cursor AI

---

## Other projects on GitHub

| Repo | About |
|------|--------|
| [home-server](https://github.com/saad-tayyab/home-server) | Self-hosted Docker stack for media, files, and downloads |
| [document-reconstruction-engine](https://github.com/saad-tayyab/document-reconstruction-engine) | Python tooling for document and journal-entry reconstruction |
| [fin](https://github.com/saad-tayyab/fin) | Personal finance app (TypeScript) |
| [Learning](https://github.com/saad-tayyab/Learning) | Notes and notebooks from ongoing learning |

Earlier work includes blockchain games on EOS.IO, real-time speech recognition, HR analytics with Kafka, and pneumonia detection from chest X-rays.

---

## Let's connect

I'm open to **senior backend roles**, **solution architecture**, and collaborations in **FinTech, SaaS, and edtech**.

Happy to chat about backend systems, event-driven design, spec-driven development, or what I'm building with Grammify.

- 📧 [saad_tayyab@outlook.com](mailto:saad_tayyab@outlook.com)
- 💼 [linkedin.com/in/saadtayyab](https://linkedin.com/in/saadtayyab)
- 💻 [github.com/saad-tayyab](https://github.com/saad-tayyab)

---

<p align="left">
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" />
  <img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white" />
  <img src="https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white" />
  <img src="https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB" />
  <img src="https://img.shields.io/badge/SQL_Server-CC2927?style=flat-square&logo=microsoft-sql-server&logoColor=white" />
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" />
  <img src="https://img.shields.io/badge/RabbitMQ-FF6600?style=flat-square&logo=rabbitmq&logoColor=white" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" />
  <img src="https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazon-aws&logoColor=white" />
</p>
