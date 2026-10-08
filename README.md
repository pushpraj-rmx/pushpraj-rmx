<div align="center">

# Pushpraj Dwivedi

### Backend &amp; DevOps Engineer

**Systems that scale. Pipelines that ship.**

I build scalable, reliable systems — messaging infrastructure, multi-tenant
platforms, and the pipelines that ship them.

[![Portfolio](https://img.shields.io/badge/Portfolio-pushpraj--rmx.github.io-0D1117?style=for-the-badge&logo=githubpages&logoColor=white)](https://pushpraj-rmx.github.io/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/pushpraj-rmx)
[![Email](https://img.shields.io/badge/Email-Say_hello-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:pushprajdwivedi001@gmail.com)

</div>

---

## 🛰 MsgBuddy — customer messaging platform

A production multi-channel messaging platform — **WhatsApp, Telegram, email and
SMS** — built and shipped end to end. Support and sales teams handle every
customer conversation and marketing campaign from one shared inbox, on the web,
desktop or phone.

Workspaces, contacts, a shared inbox, templates, campaigns, automation, a voice
agent and subscription commerce sit on **one multi-tenant API**, delivered
through five clients and documented in a full product handbook. It also ships as
a single-tenant build for enterprise customers.

```mermaid
flowchart TD
    subgraph clients["Six surfaces"]
        W["Web app<br/><i>Next.js</i>"]
        D["Desktop<br/><i>Electron</i>"]
        M["Mobile<br/><i>Expo</i>"]
        S["Storefront<br/><i>white-label</i>"]
        H["Handbook<br/><i>Nextra · MDX</i>"]
    end

    API["Multi-tenant API<br/><b>NestJS 11 · Prisma 7</b>"]

    W --> API
    D --> API
    M --> API
    S --> API
    H -.documents.-> API

    API --> PG[("PostgreSQL")]
    API --> Q["BullMQ + Redis<br/><i>queue-backed delivery</i>"]
    Q --> CH["WhatsApp Cloud API<br/>Telegram · Email · SMS"]
```

| Surface | What it is | Built with |
| :-- | :-- | :-- |
| **API** | Multi-tenant core — JWT access tokens with rotating refresh, encrypted fields, queue-backed delivery, published OpenAPI spec | NestJS 11, Prisma 7, BullMQ, Swagger |
| **Web app** | The primary client. Short-lived access tokens refresh silently on `401` against HttpOnly rotating refresh cookies | Next.js, TypeScript, Axios |
| **Desktop** | macOS and Windows shell — persistent session, in-window OAuth, deep links, tray-resident realtime, auto-update | Electron, electron-updater |
| **Mobile** | React Native client sharing the same API surface as web and desktop | React Native, Expo |
| **Storefront** | White-label per-merchant subscription storefront. Tenant branding resolves server-side into CSS variables — no flash, pages stay indexable | Next.js, Server Components, WhatsApp OTP |
| **Handbook** | Customer-facing product manual — 17 chapters of plain-language guides, worked examples and 60+ diagrams | Nextra, MDX, Mermaid |

<div align="center">

[**msgbuddy.com**](https://msgbuddy.com) · [**Web app**](https://app.msgbuddy.com) · [**Handbook**](https://docs.msgbuddy.com) · [**API docs**](https://api.msgbuddy.com/v2/docs)

</div>

---

## 🧱 Other work

<details open>
<summary><b>Synapse</b> — WhatsApp Business messaging microservice</summary>

<br/>

Connects a company's existing systems to WhatsApp so it can send and receive
business messages reliably, at volume. A standalone service wrapping the Meta
Graph API — template-based outbound messaging, inbound webhook verification,
structured logging, rate limiting and request validation behind a typed
interface.

`TypeScript` `Express` `Meta Graph API` `Winston`

</details>

<details>
<summary><b>The Panipat Handloom</b> — Django → TypeScript platform migration</summary>

<br/>

Moved a handloom retailer's ageing online store onto a modern stack — without
losing a product, an order or its search ranking. Rebuilt a legacy Django
storefront as a pnpm monorepo: a NestJS API with OpenAPI, a Next.js 15
storefront and a React-Admin console, plus ETL scripts that carried the original
data across intact.

`NestJS` `Next.js 15` `React-Admin` `Prisma` `Neon Postgres`

</details>

<details>
<summary><b>Bhartiya Aviation Services</b> — recruitment &amp; examination platform</summary>

<br/>

Runs aviation recruitment end to end — applications, online exams, scheduling
and paperwork — for candidates and staff alike. Marketing site, candidate portal
and admin panel over a single backend, with a dedicated worker tier handling
email, PDF, CSV and calendar jobs.

`NestJS` `Prisma` `Next.js` `BullMQ` `Zod` `Docker`

</details>

<details>
<summary><b>Vision360</b> — optical commerce &amp; franchise management</summary>

<br/>

Lets an optical chain run stock, sales and franchise stores across many
locations from a single system. A Turborepo monorepo for multi-store retail,
sharing typed contracts between the API and web app so a React Native client can
reuse them later.

`Turborepo` `NestJS` `Next.js 15` `Prisma`

</details>

<details>
<summary><b>Plan &amp; Book Trip</b> — travel booking &amp; package management</summary>

<br/>

Sells and manages travel packages online, payments included, with an admin
console for the operator. Public booking site, admin console and payment
checkout, split into two independently deployed applications over a modular
monolith API.

`NestJS` `Prisma` `Redis` `BullMQ` `Razorpay` `Next.js 16`

</details>

<details>
<summary><b>SearchArchitect</b> — architect listing &amp; hiring marketplace</summary>

<br/>

Helps clients find and hire architects, with structured briefs that carry budget
and timeline from the first message. Architects publish and manage portfolios;
clients search and hire them through structured project requests.

`TypeScript` `NestJS` `PostgreSQL` `React`

</details>

<details>
<summary><b>NestJS Production Template</b> — the starter behind the above</summary>

<br/>

A batteries-included NestJS starter for real SaaS workloads — ESM, strict
TypeScript, Zod-validated environment config, Prisma, Redis, queues and auth
wired up from the start.

`NestJS` `ESM` `Zod` `Prisma` `Redis`

</details>

---

## 🧰 Stack

| | |
| :-- | :-- |
| **Backend** | ![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white) ![Node.js](https://img.shields.io/badge/Node.js-5FA04E?style=flat-square&logo=nodedotjs&logoColor=white) ![Express](https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white) ![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=flat-square&logo=prisma&logoColor=white) ![BullMQ](https://img.shields.io/badge/BullMQ-DC382D?style=flat-square&logo=redis&logoColor=white) |
| **Frontend** | ![React](https://img.shields.io/badge/React-087EA4?style=flat-square&logo=react&logoColor=white) ![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white) ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white) ![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white) ![Tailwind CSS](https://img.shields.io/badge/Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white) |
| **Data** | ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white) ![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white) ![Redis](https://img.shields.io/badge/Redis-FF4438?style=flat-square&logo=redis&logoColor=white) ![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white) |
| **DevOps** | ![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black) ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white) ![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white) ![PM2](https://img.shields.io/badge/PM2-2B037A?style=flat-square&logo=pm2&logoColor=white) ![Turborepo](https://img.shields.io/badge/Turborepo-EF4444?style=flat-square&logo=turborepo&logoColor=white) |

---

## 🤝 What I take on

- **Platform build-out** — design and ship a multi-tenant product end to end: API, web, mobile and desktop clients, auth, background jobs, payments and documentation.
- **Legacy migration** — move an ageing PHP, Django or Laravel system onto a modern TypeScript stack, carrying the existing data across intact.
- **Messaging &amp; WhatsApp integration** — WhatsApp Business and Cloud API work: template messaging, inbound webhooks, bulk delivery, rate limiting and retry handling.
- **DevOps &amp; delivery** — dockerised environments, CI/CD pipelines, VPS deployment and process management, so shipping stops being an event.

<div align="center">
<br/>

**Open to remote or hybrid backend / platform roles.**

🌐 [pushpraj-rmx.github.io](https://pushpraj-rmx.github.io/) &nbsp;·&nbsp; ✉️ [pushprajdwivedi001@gmail.com](mailto:pushprajdwivedi001@gmail.com) &nbsp;·&nbsp; 💼 [LinkedIn](https://linkedin.com/in/pushpraj-rmx)

</div>
