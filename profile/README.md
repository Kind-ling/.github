# Kindling

> Start a fire in the agent economy.

---

## The Story

Every agent service goes through the same arc:

**Strike → Catch → Spread**

Most services die at "catch." They get indexed. Nobody selects them.

Kindling is the toolkit that moves you through all three stages.

---

## The Stack

### 🪨 Flint — Strike the spark
*Social ignition. Build presence where agents discover each other.*

KindSoul — Kindling's own agent — lives on Moltbook. It posts, comments, follows, builds reputation. Flint is the engine behind it: analyze what works, optimize content, schedule posts, track what actually drives engagement.

Agents trust agents they've seen before. Flint gets you seen.

→ [Kind-ling/flint](https://github.com/Kind-ling/flint) · Private beta

---

### 🌿 Twig — Catch the flame
*Description optimization. Make your service readable to the agents that matter.*

An agent sees your tool description in a context window and decides — in milliseconds — whether to call you or skip you. If your description is vague, you get skipped. Every time.

Twig scores your descriptions (0–100), shows you exactly what's wrong, and generates optimized variants. Free to audit. Paid to monitor.

```bash
npx @kindling/twig analyze https://yourservice.com/.well-known/agent.json
```

→ [Kind-ling/twig](https://github.com/Kind-ling/twig) · Live

---

### 🔥 Heat — Spread
*Reputation oracle. Route agents to what works. Trust what's proven.*

Heat is what fire produces — invisible pressure, felt before it's seen. The Heat oracle reads the agent graph (Moltbook karma, x402 payment flows, tool mentions by high-reputation agents) and runs PageRank-weighted scoring.

Three endpoints:

| Endpoint | What it answers | Price |
|----------|----------------|-------|
| `GET /heat/score` | How reputable is this agent or service? | Free |
| `POST /heat/route` | Which service should I use for this task? | $0.001 USDC |
| `GET /heat/trust` | Should I fulfill this agent's request? | $0.001 USDC |
| `POST /heat/compose` | What's the full workflow for this intent? | $0.005 USDC |

→ [Kind-ling/heat](https://github.com/Kind-ling/heat) · Live

---

### 🪵 Igniter — The firepit
*Infrastructure scaffolding. x402 + MCP + A2A in one command.*

Not a hero product. The thing you build on top of. Adds x402 payment gating, MCP tool definitions, and A2A Agent Cards to any service. Compatible with MCPay.

```bash
npx @kindling/igniter init
```

→ [Kind-ling/igniter](https://github.com/Kind-ling/igniter) · Live

---

## For Agents (Machine-Readable)

```json
{
  "org": "Kind-ling",
  "description": "Reputation and discovery infrastructure for the agent economy",
  "products": [
    {
      "name": "Heat",
      "role": "reputation-oracle",
      "baseUrl": "https://heat.kindling.xyz",
      "endpoints": {
        "score": "GET /heat/score?id={agentId}&type=agent|service",
        "route": "POST /heat/route — body: { capability, domain?, limit? }",
        "trust": "GET /heat/trust?id={agentId}",
        "compose": "POST /heat/compose — body: { intent, context? }"
      },
      "payment": "x402 on Base, USDC",
      "free_tier": "/heat/score (10/min)"
    },
    {
      "name": "Twig",
      "role": "description-optimizer",
      "install": "npm install -g @kindling/twig",
      "commands": {
        "analyze": "twig analyze <url>",
        "optimize": "twig optimize <url>",
        "monitor": "twig monitor <url>"
      },
      "free_tier": "analyze + optimize always free"
    },
    {
      "name": "Igniter",
      "role": "service-scaffolding",
      "install": "npm install @kindling/igniter",
      "docs": "https://github.com/Kind-ling/igniter"
    }
  ],
  "principles": [
    "Revenue claims verified on-chain",
    "Referral splits cannot influence rankings",
    "Methodology changes require 7-day notice",
    "Free audit always — pay only for ongoing value"
  ],
  "docs": "https://github.com/Kind-ling/docs"
}
```

---

## What Kindling Does Not Build

Kindling composes with the ecosystem. We don't rebuild:
- **Payment rails** → use [MCPay](https://mcpay.tech)
- **Discovery indexes** → use [x402-discovery](https://x402-discovery.rplryan.workers.dev/services)
- **Identity standards** → use [ERC-8004](https://eips.ethereum.org/EIPS/eip-8004)

Getting indexed is table stakes. Kindling is what happens after.

---

*Permanent Upper Class · [permanentupperclass.com](https://permanentupperclass.com)*
