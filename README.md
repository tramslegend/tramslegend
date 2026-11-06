<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:1b2a4a,100:7AA2F7&height=200&section=header&text=Full-stack%20Engineer&fontSize=58&fontColor=ffffff&fontAlignY=35&desc=Next.js%20%E2%80%A2%20Real-time%20%E2%80%A2%20Web3%20%E2%80%A2%20Commerce&descAlignY=58&descSize=18" width="100%" />

<a href="https://github.com/tramslegend">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=22&duration=3000&pause=900&color=7AA2F7&center=true&vCenter=true&width=650&lines=Full-stack+TypeScript+Developer;Real-time+Multiplayer+Game+Systems;On-chain+Games+on+Solana;E-commerce+Platforms+with+Payments+%26+Auth;Next.js+App+Router+at+Production+Scale" alt="Typing SVG" />
</a>

<br/>

![Next.js](https://img.shields.io/badge/Next.js-App_Router-7AA2F7?style=for-the-badge&labelColor=0d1117)
![TypeScript](https://img.shields.io/badge/TypeScript-End_to_End-3178C6?style=for-the-badge&labelColor=0d1117)
![Real-time](https://img.shields.io/badge/Real--time-WebSockets-16c79a?style=for-the-badge&labelColor=0d1117)
![Web3](https://img.shields.io/badge/Solana-On--chain-9D7CD8?style=for-the-badge&labelColor=0d1117)

</div>

---

## `>` whoami

```ts
const dev: FullStackEngineer = {
  role:       "Full-stack TypeScript Developer",
  focus:      ["Next.js App Router", "Real-time systems", "Web3 / Solana"],
  frontend:   ["React", "TypeScript", "Tailwind CSS", "shadcn/ui"],
  backend:    ["Node.js", "PostgreSQL", "MongoDB", "Redis", "Zod"],
  realtime:   ["WebSockets", "Pusher", "live rounds & leaderboards"],
  web3:       ["Solana web3.js", "wallet integration", "on-chain settlement"],
  currently:  "real-time multiplayer games with wallets & live state",
  philosophy: "Ship production systems, not demos.",
};
```

I build fast, production-ready web apps — from the database schema all the way to the pixel.
**Real-time multiplayer games** on Solana, and **full e-commerce platforms** with payments, auth,
email and admin tooling. Not prototypes — systems that handle real users, real money, and real traffic.

---

## `>` what I build

<table>
<tr>
<td width="33%" valign="top">

### 🎮 Real-time Games

Live multiplayer rounds<br/>
WebSocket state sync<br/>
Wallet integration (Solana)<br/>
Live leaderboards<br/>
Round history & replay<br/>
Provably-fair outcomes<br/>
Low-latency broadcast

</td>
<td width="33%" valign="top">

### 🛒 E-commerce

Product catalog & search<br/>
Stripe checkout & webhooks<br/>
Auth & sessions<br/>
Transactional email<br/>
Image / file uploads<br/>
Admin & order tooling<br/>
Inventory management

</td>
<td width="33%" valign="top">

### 🔌 Full-stack & Infra

Next.js App Router<br/>
API routes & server actions<br/>
PostgreSQL / Mongo / Redis<br/>
Caching & rate limiting<br/>
Docker & Vercel deploys<br/>
Type-safe end to end (Zod)<br/>
Testing with Vitest

</td>
</tr>
</table>

---

## `>` the stack

<div align="center">

**Frontend**

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![Tailwind](https://img.shields.io/badge/Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![shadcn/ui](https://img.shields.io/badge/shadcn/ui-000000?style=flat-square&logo=shadcnui&logoColor=white)

**Backend / Real-time**

![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white)
![Socket.IO](https://img.shields.io/badge/WebSocket-010101?style=flat-square&logo=socketdotio&logoColor=white)
![Pusher](https://img.shields.io/badge/Pusher-300D4F?style=flat-square&logo=pusher&logoColor=white)
![Zod](https://img.shields.io/badge/Zod-3E67B1?style=flat-square&logo=zod&logoColor=white)

**Data &amp; Infra**

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white)

**Payments / Web3**

![Stripe](https://img.shields.io/badge/Stripe-635BFF?style=flat-square&logo=stripe&logoColor=white)
![Solana](https://img.shields.io/badge/Solana-9945FF?style=flat-square&logo=solana&logoColor=white)
![Better Auth](https://img.shields.io/badge/Better_Auth-000000?style=flat-square&logo=auth0&logoColor=white)
![Resend](https://img.shields.io/badge/Resend-000000?style=flat-square&logo=resend&logoColor=white)

</div>

---

## `>` real-time game round

How a live multiplayer round flows — bet, live state, cash-out, settle:

```mermaid
sequenceDiagram
    autonumber
    participant P as Player
    participant C as Game Client
    participant S as Game Server
    participant W as Wallet / Chain

    P->>C: connect(wallet)
    C->>S: join round (WebSocket)
    S-->>C: round state + countdown

    P->>C: place bet (1.0)
    C->>S: POST /round/bet
    S->>W: debit (txId) — idempotent
    W-->>S: ok, balance

    loop live tick
        S-->>C: broadcast multiplier (x1.00 → x1.87 ...)
    end

    P->>C: CASH OUT @ x1.87
    C->>S: POST /round/cashout
    S->>W: credit win (txId)
    W-->>S: settled
    S-->>C: result + updated leaderboard

    Note over S,W: crash mid-round → rollback(txId), replayable from event log
```

---

## `>` provably-fair outcome

```ts
import { createHmac, createHash } from "node:crypto";

/**
 * Deterministic round outcome from a committed server seed.
 * Players verify after the round: sha256(serverSeed) === publishedHash
 */
export function roundOutcome(
  serverSeed: string,
  clientSeed: string,
  nonce: number,
): number {
  const digest = createHmac("sha256", serverSeed)
    .update(`${clientSeed}:${nonce}`)
    .digest();

  // unbiased sampling — never a naive `% n` (modulo bias skews fairness)
  const n = digest.readUInt32BE(0) / 0xffffffff;
  return Math.max(1, Math.floor((1 / (1 - n)) * 100) / 100); // crash multiplier
}

export const commit = (serverSeed: string) =>
  createHash("sha256").update(serverSeed).digest("hex");
```

<div align="center">

**`commit` → `play` → `reveal` → `verify`** — every round is auditable.

</div>

---

## `>` featured work

| Project | What it is | Stack |
|---|---|---|
| **RUG-GAME** | Real-time crash-style game on Solana — live rounds, wallet integration, leaderboard | Next.js · Solana · Pusher · Redis · Postgres |
| **Electronics-shop** | Full e-commerce: catalog, Stripe checkout, auth, email, image uploads | Next.js · Stripe · Better Auth · MongoDB |
| **CCTV-SHOP** | Security-equipment storefront on the same commerce platform | Next.js · Stripe · MongoDB · Resend |
| **[Stop-watch](https://github.com/tramslegend/Stop-watch)** | Minimal stopwatch app | Next.js · Tailwind |

<!-- Swap in your real project links / live demos for each row. -->

---

## `>` platform capabilities

<details>
<summary><b>🎮 Real-time Engine</b></summary>

- Authoritative server state with WebSocket broadcast
- Live multiplier / round ticks at low latency
- Reconnect & state resync on drop
- Round history, replay and audit log
- Redis-backed leaderboards (sorted sets)

</details>

<details>
<summary><b>💳 Payments &amp; Commerce</b></summary>

- Stripe checkout, webhooks and refunds
- Idempotent order & payment handling
- Cart, inventory and catalog management
- Transactional email (Resend) for receipts & auth
- Admin dashboard for orders and products

</details>

<details>
<summary><b>🔐 Auth &amp; Security</b></summary>

- Session & credential auth (Better Auth)
- Role-based access for admin tooling
- Input validation end-to-end with Zod
- Rate limiting and request validation
- Secure file/image uploads (Vercel Blob)

</details>

<details>
<summary><b>📊 Data &amp; Tooling</b></summary>

- PostgreSQL, MongoDB and Redis depending on the workload
- Type-safe data access and schemas
- Docker for local parity, Vercel for deploys
- Vitest test coverage on core logic

</details>

---

## `>` engineering principles

```
1. Type-safe end to end — if it compiles, it's closer to correct.
2. Money and game state move through a state machine, never an if-statement.
3. Every write is idempotent — the network will betray you.
4. Real-time means authoritative server, dumb client.
5. Validate at the boundary (Zod), trust nothing from the wire.
6. Ship production systems, not demos.
```

---

## `>` stats

<div align="center">

<img height="165" src="https://github-readme-stats.vercel.app/api?username=tramslegend&show_icons=true&hide_border=true&theme=tokyonight&count_private=true&include_all_commits=true&icon_color=7AA2F7&title_color=7AA2F7" />
<img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=tramslegend&layout=compact&hide_border=true&theme=tokyonight&langs_count=8&title_color=7AA2F7" />

<img src="https://github-readme-streak-stats.herokuapp.com/?user=tramslegend&hide_border=true&theme=tokyonight&fire=7AA2F7&ring=7AA2F7&currStreakLabel=7AA2F7" />

<img src="https://github-profile-trophy.vercel.app/?username=tramslegend&theme=nord&no-frame=true&no-bg=true&column=7&margin-w=8" />

</div>

---

## `>` let's build

<div align="center">

Open to **freelance** and **full-time** work — real-time apps, Next.js products, or e-commerce builds.

<a href="https://github.com/tramslegend">
  <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" />
</a>
<!-- Replace the placeholder hrefs below with your real links, then uncomment:
<a href="mailto:you@example.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" /></a>
<a href="https://t.me/your-handle"><img src="https://img.shields.io/badge/Telegram-26A5E4?style=for-the-badge&logo=telegram&logoColor=white" /></a>
<a href="https://linkedin.com/in/your-handle"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" /></a>
-->

<br/><br/>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:7AA2F7,50:1b2a4a,100:0d1117&height=120&section=footer" width="100%" />

</div>
